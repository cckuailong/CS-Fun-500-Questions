# Linux /dev/shm的作用

## 简介

/dev/shm/是linux下一个非常有用的目录，因为这个目录不在硬盘上，而是在内存里。因此在linux下，就不需要大费周折去建ramdisk，直接使用/dev/shm/就可达到很好的优化效果。 /dev /shm/需要注意的一个是容量问题，在linux下，它默认最大为内存的一半大小，使用df -h命令可以看到。但它并不会真正的占用这块内存，如果/dev/shm/下没有任何文件，它占用的内存实际上就是0字节；如果它最大为1G，里头放有 100M文件，那剩余的900M仍然可为其它应用程序所使用，但它所占用的100M内存，是绝不会被系统回收重新划分的，否则谁还敢往里头存文件呢？

默认系统就会加载/dev/shm ，它就是所谓的tmpfs，有人说是ramdisk（虚拟磁盘），但不一样。象虚拟磁盘一样，tmpfs 可以使用您的 RAM，但它也可以使用您的交换分区来存储。而且传统的虚拟磁盘是个块设备，并需要一个 mkfs 之类的命令才能真正地使用它，tmpfs 是一个文件系统，而不是块设备；您只是安装它，它就可以使用了。

tmpfs有以下优势：

- 动态文件系统的大小
- 闪电般的速度。因为典型的 tmpfs 文件系统会完全驻留在 RAM 中，读写几乎可以是瞬间的。
- tmpfs 数据在重新启动之后不会保留，因为虚拟内存本质上就是易失的。所以有必要做一些脚本做诸如加载，绑定的操作。

## 修改/dev/shm大小

默认的最大一半内存大小在某些场合可能不够用，并且默认的inode数量很低一般都要调高些，这时可以用mount命令来管理它。

```
mount -o size=1500M -o nr_inodes=1000000 -o noatime,nodiratime -o remount /dev/shm
```

在2G的机器上，将最大容量调到1.5G，并且inode数量调到1000000，这意味着大致可存入最多一百万个小文件。

如果需要永久修改/dev/shm的值，需要修改/etc/fstab

```
tmpfs /dev/shm tmpfs defaults,size=1.5G 0 0
mount -o remount /dev/shm
```

## 使用

首先在/dev/shm建个tmp文件夹，然后与实际/tmp绑定

```
mkdir /dev/shm/tmp
chmod 1777 /dev/shm/tmp
mount –bind /dev/shm/tmp /tmp
```

在使用mount –bind olderdir newerdir命令来挂载一个目录到另一个目录后，newerdir的权限和所有者等所有信息会发生变化。挂载后的目录继承了被挂载目录的所有属性，除了名称。Oracle 11g的amm内存管理模式就是使用/dev/shm，所以有时候修改MEMORY_TARGET或者MEMORY_MAX_TARGET会出现ORA-00845的错误
