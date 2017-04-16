* [Low-Level Programming University](#Low-Level-Programming-University)
  * [这是?](#What-is-it)
  * [什么是底层](#What-Is-the-Low-Level)
  *  [理论](#Theory)
  *  [编程语言](#Languages)
    * [汇编](#Assembly)
    * [C语言](#C-language)
  * [应用层](#Applications)
    * [硬件 && 固件](#Hardware-Firmware)
    * [Linux内核和设备驱动](#Linux-kernel-and-device-driver)
      * [仔细阅读](#Read-carefully)
      * [参考目录](#References)
  * [底层编程的未来趋势](#Future-of-low-level-programming)
* [翻译](#Translation)

# <a name="Low-Level-Programming-University"></a>Low-Level Programming University

## <a name="What-is-it"></a>这是?

这篇文章是为那些准备成为一个底层程序员的人所写。

我是受到了 [google-interview-university](https://github.com/jwasham/google-interview-university) 这篇文章的启发。 作为一个底层程序员，我想分享一下我的经验和成长为一个底层程序员的路线图，因为我发现这些底层需要的技能在不断的发生变化。另外，很多学生和初学者也会经常问我，怎么才能成为一个底层程序员或者是成为一个Linux内核工程师。 

本文不可能包含所有的链接/书籍/课程。例如，本文介绍了Arduino，但是没有详细介绍Arduino和嵌入式系统。读者需要自己深入学习这方面的知识。作为一个开始，你知道了关键词"Arduino"，接下来，你可以用google 搜索Arduino，购买一套开发套件，基于开发套件在上面**自己动手做一些事情**，而不是收集链接或者是免费的书籍。请记住，本文仅仅是一个路线图，是一个指导。

又及，我作为一个底层程序员，在以下方面有超过10年的经验：
* 80x86 汇编编程
* 使用基于Atmel芯片和固件的硬件
* Unix下C语言系统编程
* Linux设备驱动开发
* Linux内核: 内存页分配
* Linux内核: 块设备驱动程序和 md 模块

## <a name="What-Is-the-Low-Level"></a>什么是底层?

我把底层编程归类于非常接近设备的编程，使用比较底层的编程语言，例如C或者汇编。这与上层编程相反，例如用户空间的应用程序，使用上层的编程语言（例如，Python，Java）。
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language)

系统编程是一个非常接近底层编程的概念。本文包含了硬件设计以及固件开发，这部分内部不是系统编程的内容。
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

最后，本文包含的主题从硬件到Linux内核，这跨越了很多的层次。一篇文章无法阐述所有层次的详细内容，所以本文的目的是让你知道怎么开始成为一个底层程序员。

##  <a name="Theory"></a>理论

底层编程有两个背景理论：
* 计算机体系结构
* 操作系统

你可以在在线大学上找到很很好的课程，例如Coursera.org and edx.org。但理论仅是理论，你不需要在这些课程上获得A+，但是你需要了解整个课程的大概原理。随着经验的丰富，你可以做得越来越好。

##  <a name="Languages"></a>编程语言

### <a name="Assembly"></a>汇编

* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
  * CPU和计算机体系结构的基本概念
  * C语言的基本概念
* [64bit assembly programming(正在翻译)](https://github.com/gurugio/book_assembly_64bit)
  * 现代CPU和计算机体系结构的基本概念
  * 分解和调试C语言的基本概念
  * _需要帮忙翻译_
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * ARM编程参考手册
* 计算机组成和设计
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * 学术书籍，解释了计算机的各部分是如何从0开始工作的
  * 详细解释了计算机体系结构中各方面概念
  * 他们的目的不是让你成为特定汇编语言专家
  * MIPS和ARM版本阐述了同样的问题，只不过他们以不同的体系结构为例
  * 两个版本都包含了x86结构下的例子

### <a name="C-language"></a>C 语言

学习C语言没有捷径，你需要读完整本书，并解决书上的练习题。

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * C语言新标准
* [并行编程困难吗，如果是的，你能做点什么?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * 用C语言实现同步
  * 大型C程序设计必备 (特别是Linux内核编程)
* [C语言编程的挑战?](https://github.com/gurugio/lowlevelprogramming-university/blob/master/c-language-challenge.md)
  * 开始为[The Eudyptula Challenge](http://eudyptula-challenge.org/) 制作计划
  * 当前只有一个想法
  * 如果你完成了本文的所有小项目，那么你已经可以开始做大的项目了
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * 使用C语言和x86汇编进行优化的参考书籍
  * 从8088系统到现在的系统
  * 特别注重底层的图形优化

## <a name="Applications"></a>应用程序

### <a name="Hardware-Firmware"></a>硬件 && 固件

如果你想做一个嵌入式系统工程师，那最好从一个简单的硬件套件开始，而不是从最新的ARM芯片开始。

* [Arduino Start Kit](https://www.arduino.cc/)
  * Arduino有一系列的套件，但是 "Arduino Start Kit"有最简单的处理器(Atmega328P)以及参考手册。
  * Atmega328P有一个8位的核心，这对于“数字电路设计”和“固件开发” 是个好的开头
  * 你不必要了解怎么画原理图，怎么laytou，怎么组装芯片
  * 但是你需要知道怎么去读原理图，并理解各芯片之间是怎么连接的
  * 固件工程师应该具备阅读原理图并知道怎么给目标设备发送数据的能力
  * 跟随参考手册的指导
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * 如果你刚开始了解x86架构，8086手册对于理解处理器架构和80x86汇编语言也是非常好的指导
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * 对于80x86处理器的保护模式和分页机制是最好的指导
  * 网络版本: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

到这个点上，你可以开始了解最新的ARM和x86处理器。
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

例如，树莓派开发板有一个支持64位指令的Cortex-A53处理器，这可以让你了解现代处理器架构。是的，你可以买一个开发板，但是，你买来做什么呢？如果你没有目标项目，你很可能将它扔到抽屉里，然后忘在脑后。

所以，我向你推荐一个项目：
* [制作自己的内核](http://wiki.osdev.org/Getting_Started)
  * 参考资料: https://www.reddit.com/r/osdev/

我自己制作了[a toy kernel](https://github.com/gurugio/caos)，该内核支持64位长模式，分页以及很简单的上下文切换。制作一个简单的内核对于理解现代计算机体系结构和硬件控制是一种很好途径。

事实上，你已经有了最新的处理器和最新的硬件设备。这就是你的笔记本电脑，你的台式电脑，你已经具备所有的条件了。你不需要购买任何东西。qemu仿真器可以仿真最新的ARM和Intel处理器，所以你需要的资料都已经具备了。有很多简单内核和文档供你参考。你要做的就是安装qemu仿真器，开发一个简单内核，能够启动，开启分页功能并打印一些信息。

其他的简单内核:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Linux内核和设备驱动

你没有必要开发一个完整的操作系统，可以加入Linux社区并参与内核开发。

#### <a name="Read-carefully"></a>仔细阅读

* 书籍: 按照如下顺序阅读
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * Unix系统的基本概念适用于所有的操作系统
    * 这本书对于理解操作系统概念非常好
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * 亲自做所有的例子
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * 理解Linux内核设计原理
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * 读这本书的同时也要读v2.6的内核源码
    * 不要读最新的源码，2.6版本足够了!
    * 使用quemu和gdb来一行一行的运行内核代码
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://gurugio.kldp.net/wiki/wiki.php/howto_debug_kernel
    * 使用busybox来制作最简单的文件系统，使得系统能在1秒内启动
      * https://gurugio.kldp.net/wiki/wiki.php/qemu_kernel
* [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * 这就像一个令人敬畏的私人老师指导你该做什么
  * 如果你不知道做什么，那就从这里开始
* [Block layer and device driver(正在翻译)](https://github.com/gurugio/book_linuxkernel_blockdrv)
  * 从一个简单的具备多队列模式的块设备驱动程序（Ramdisk）开始
  * 深入到块设备层
  * _需要帮忙翻译_
* [md driver of Linux kernel(正在进行)](https://github.com/gurugio/book_linuxkernel_md)
  * mdadm工具工作流程以及调用md驱动程序的过程
  * md驱动程序是怎么工作的
  * _需要帮忙翻译_

#### <a name="References"></a>参考

当你需要帮助时参考下面资料

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * 很多文件介绍的内容都很好，尤其是ARM-linux方面的
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * 指导如何开始内核编程

## <a name="Future-of-low-level-programming"></a>底层编程的未来趋势

我不知道未来会怎么样，但是我会关注RUST。
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

如果我有一周的空闲时间，我会学习RUST。这是因为RUST是可以开发Linux设备驱动程序的最新的一种语言。

IoT是新的趋势，所以值得我们去研究一下IoT所使用的操作系统。ARM，Samsung以及一些公司有他们自己的实时操作系统，但是糟糕的是这些系统都是闭源的。但是Linux基金会有一个解决方案：Zephyr
* https://www.zephyrproject.org/

典型的云服务器有很多层，例如主机OS，kvm驱动，qemu进程，客机OS以及应用服务程序。因此容器被开发出来以提供轻量虚拟化。在不久的将来，一种新型的OS，被称为library OS或者是Unikernel的OS，可能会取代当前的用作虚拟化的软件栈。
* http://unikernel.org/

# <a name="Translation"></a>Translation

如果你要翻译本文，请提交一个PR，我会在这里列出来。
