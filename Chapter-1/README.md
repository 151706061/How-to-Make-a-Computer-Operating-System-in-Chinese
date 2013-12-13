## 第1章: 如何制作一个操作系统

### 什么是x86架构?

> x86表示基于英特尔8086 CPU的后向兼容的指令集架构

x86架构自1981年IBM PC引人后, 即成为最常用的指令集架构. 大量的软件, 包括操作系统, 如DOS, Windows, Linux, BSD, Solaris和Mac OS X, 都工作在基于x86的硬件上.

在这个课程中, 我们会为x86-32而不是x86-64架构设计操作系统. 由于有后向兼容, 这个操作系统可以与新PC相兼容(不过如果你想真机测试, 要小心点).

### 我们的操作系统

目标是使用C++构建一个基于UNIX, 非常简单的操作系统, 而不只是一个"概念验证". 这个操作系统可以启动, 运行一个userland shell, 可以扩展.

它是x86架构的32位操作系统, 可以兼容IBM PC.

**详述**

* C++编程
* x86, 32位架构
* 通过Grub启动
* 用于驱动的模块化系统
* Unix风格
* 多任务
* Userland下的可执行ELF
* 模块 (可在userland下通过/dev/...进行访问) :
    * IDE磁盘
    * DOS分区
    * 时钟
    * EXT2 (只读)
    * Boch VBE
* Userland :
    * Posix规范的API
    * LibC
    * "可以"运行shell或其他一些可执行程序, 如Lua, ...

<table><tr><td>&larr; 上一篇</td><td><a href="../Chapter-2/README.md" >下一篇 &rarr;</a></td></tr></table>
