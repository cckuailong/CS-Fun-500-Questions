# Ftp, NFS和Samba的故事

## 解释

在早期网络世界当中，档案数据在不同主机之间的传输大多是使用 FTP 这个好用的服务器软件来进行传送。
不过，使用FTP 传输档案却有个小小的问题，那就您无法直接修改主机上面的档案数据！
也就是说您想要更改Linux 主机上的某个档案时，必需要由 Server 端将该档案下载到 Client端后才能修改，
也因此该档案在 Server 与 Client 端都会存在。这个时候，万一如果有一天您修改了某个档案，却忘记将数据上传回主机，
那么等过了一阵子之后，如何知道那个档案才是最新的？

既然有这样的问题，可不可以在 Client 端的机器上面直接取用Server 上面的档案，如果可以在 Client 端直接进行 Server 端档案的存取，
那么在Client 端就不需要存在该档案数据，也就是说，只要有 Server 上面的档案资料存在就可以！
有没有这样的档案系统( File System )？很高兴的是， NetworkFile System, NFS 就是这样的档案系统之一！
我只要在 Client 端将 Server所提供分享的目录挂载进来，那么在 Client 的机器上面就可以直接取用 Server上的档案数据，
而且，该数据就像 Client 端上面的partition 一般！而除了可以让 Unix Like 的机器互相分享档案的NFS 服务器之外，
在微软 ( Microsoft ) 上面也有类似的档案系统，那就是 CommonInternet File System, CIFS 这个咚咚啦！
CIFS 最简单的想法就是目前常见的『网上邻居』。Windows 系统的计算机可以透过桌面上『网上邻居』来分享别人所提供的档案数据。
不过，NFS仅能让 Unix 机器沟通， CIFS 只能让 Windows 机器沟通。
伤脑筋，那么有没有让Windows 与 Unix-Like 这两个不同的平台相互分享档案数据的档案系统？

1991 年一个名叫Andrew Tridgwell 的大学生就有这样的困扰，他手上有三部机器，
分别是跑DOS 的个人计算机、DEC公司的 Digital Unix 系统以及 Sun 的 Unix 系统。在当时，DEC 公司有发展出一套称为 PATHWORKS 的软件，
这套软件可以用来分享 DEC 的Unix 与个人计算机的 DOS 这两个操作系统的档案数据，可惜让 Tridgwell 觉得较困扰的是，
Sun的 Unix 无法藉由这个软件来达到数据分享的目的。这个时候 Tridgwell 就想说：

『咦！既然这两部系统可以相互沟通，没道理Sun 就必需这么苦命吧？可不可以将这两部系统的运作原理找出来，然后让 Sun这部机器也能够分享档案数据呢？』，

为了解决这样的的问题，这老兄就自行写了个program 去侦测当 DOS 与 DEC 的 Unix 系统在进行数据分享传送时所使用到的通讯协议信息，
然后将这些重要的信息撷取下来，并且基于上述所找到的通讯协议而开发出ServerMessage Block (SMB) 这个档案系统，
而就是这套SMB软件能够让 Unix 与 DOS 互相的分享数据！

注：再次的给他强调一次，在Unix Like 上面可以分享档案数据的 file system 是 NFS，
那么在 Windows 上面使用的『网络邻居』所使用的档案系统则称为Common Internet File System, CIFS

因此 Tridgwell就去申请了 SMBServer ( Server Message Block 的简写 ) 这个名字来做为他撰写的这个软件的商标，
可惜的是，因为SMB 是没有意义的文字，因此没有办法达成注册。既然如此的话，那么能不能在字典里面找到相关的字词可以做为商标来注册呢？
翻了老半天，呵呵！这个SAMBA刚好含有 SMB ，又是热情有劲的拉丁舞蹈的名称，不如就用这个名字来做为商标好了。

如此，这成为我们今天所使用的SAMBA 的名称由来。
