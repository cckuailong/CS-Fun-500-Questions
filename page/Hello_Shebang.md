# Hello "#!"

## 前言

使用类Unix系统的同学可能都对 "#!" 这个符号并不陌生，但是你真的了解它吗？

![shebang](../image/Hello_Shebang_1.jpg)

这个符号的名称，叫做 "Shebang" 或者 "Sha-bang"。长期以来，Shebang都没有正式的中文名称。
Linux中国翻译组的GOLinux将其翻译为“释伴”，即“解释伴随行”的简称，同时又是Shebang的音译。
本文将简单介绍一下Shebang这个符号。

## 词源与历史

Shebang的名字来自于SHArp 和 bang，或 haSH bang的缩写，指代 Shebang 中 "#!" 两个符号的典型 Unix名称。
Unix 术语中，"#" 通常称为 sharp，hash 或 mesh；而 ! 则常常称为 bang。
也有看法认为，shebang 名字中的 she 来自于默认shell Bourne shell 的名称。

在2010年版的 Advanced bash scripting guide（revision 6.2）中，Shebang 被称为 “sha-bang”，
同时提到”也写作 she-bang 或 sh-bang”，但该文件中没有提到 “shebang” 这一形式。

## 用法

Shebang通常出现在类Unix系统的脚本中第一行，作为前两个字符。在Shebang之后，可以有一个或数个空白字符，
后接解释器的绝对路径，用于指明执行这个脚本文件的解释器。
在直接调用脚本时，系统的程序载入器会分析 Shebang 后的内容，将这些内容作为解释器指令，并调用该指令，
将载有 Shebang 的文件路径作为该解释器的参数，执行脚本，从而使得脚本文件的调用方式与普通的可执行文件类似。
例如，以指令 #!/bin/sh 开头的文件，在执行时会实际调用 /bin/sh 程序
（通常是 Bourne shell 或兼容的 shell，例如 bash、dash 等）来执行。

由于 # 符号在许多脚本语言中都是注释标识符，Shebang 的内容会被这些脚本解释器自动忽略。
在 # 字符不是注释标识符的语言中，例如 Scheme，解释器也可能忽略以 "#!" 开头的首行内容，
以提供与 Shebang 的兼容性。

### Shebang的一些具体用法罗列如下

- 如果脚本文件中没有 "#!" 这一行，那么执行时会默认采用当前Shell去解释这个脚本(即：$SHELL环境变量）。
- 如果 "#!" 之后的解释程序是一个可执行文件，那么执行这个脚本时，
它就会把文件名及其参数一起作为参数传给那个解释程序去执行。
- 如果 "#!" 指定的解释程序没有可执行权限，则会报错“bad interpreter: Permission denied”。
如果 "#!" 指定的解释程序不是一个可执行文件，那么指定的解释程序会被忽略，转而交给当前的SHELL去执行这个脚本。
- 如果 "#!" 指定的解释程序不存在，那么会报错“bad interpreter: No such file or directory”。
注意："#!" 之后的解释程序，需要写其绝对路径（如：#!/bin/bash），它是不会自动到$PATH中寻找解释器的。
- 当然，如果你使用类似于”bash test.sh”这样的命令来执行脚本，那么 "#!" 这一行将会被忽略掉，
解释器当然是用命令行中显式指定的bash。
- 脚本文件必须拥有可执行权限。

### 其他例子

Shebang的好处在于，允许脚本和数据文件充当系统命令，无需在调用时由用户指定解释器，
从而对用户和其它程序隐藏其实现细节。下面我们一起来看几个典型的例子：

```
#!/bin/sh：             使用 sh，即 Bourne shell 或其它兼容 shell 执行脚本
#!/bin/csh：            使用 csh，即 C shell 执行
#!/usr/bin/perl -w：    使用带警告的 Perl 执行
#!/usr/bin/python -O：  使用具有代码优化的 Python 执行
#!/usr/bin/php：        使用 PHP 的命令行解释器执行
```

Shebang 行也可以包含需要传递到解释器的特定选项（如上述的 Perl 和 Python 例子）。

### 注意

- 之前我们提到过，解释器指令本身会被解释器认为是单纯的注释而跳过。
然而，并不是每一种解释器都会自动忽略Shebang行，例如对于下面的脚本，

```
#!/bin/cat
Hello world!
```

cat 会把文件中的两行都输出到标准输出中。

- 使用 #!/usr/bin/env 脚本解释器名称 是一种常见的在不同平台上都能正确找到解释器的办法。
因为env一般固定在/usr/bin目录下，而其余解释器的安装位置就相对不那么固定。
但是，用env时你应该注意这么一个事实：传递给解释器的argv和你想象得并不一样。下面这个就是不对的：

```
#!/usr/bin/env perl -w
```

shell会提示：/usr/bin/env: perl -w: No such file or directory。错误的根源就在于 perl -w 被当成了整体传递给env。

## 总结

最后，我们来总结一下Shebang的几点要求

- "#!" 必须连接在一起
- "#!" 一句必须在文件的最开始，第一行
- "#" 开头的语句一般情况下会被当成注释而忽略，所以Shebang 对文件的内容是没有影响的
- "#!" 开头的一行会设置解释器运行环境
