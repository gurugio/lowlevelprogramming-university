* [Low-Level Programming University](#Low-Level-Programming-University)
  * [What is it?](#What-is-it)
  * [What Is the Low Level](#What-Is-the-Low-Level)
  *  [Theory](#Theory)
  *  [Languages](#Languages)
     * [Assembly](#Assembly)
     * [C language](#C-language)
  * [Applications](#Applications)
    * [Hardware && Firmware](#Hardware-Firmware)
    * [Linux kernel and device driver](#Linux-kernel-and-device-driver)
      * [Follow carefully](#Follow-carefully)
      * [References](#References)
    * [Other applications](#Other-applications)
  * [Future of low-level programming](#Future-of-low-level-programming)
  * [How to start?](#How-to-start)
* [Translation](#Translation)
* [Who am I?](#who-am-i)

# Low-Level Programming University

## <a name="What-is-it"></a>What is it?

I'm inspired by [google-interview-university](https://github.com/jwasham/coding-interview-university). I'd like to share my experience and show a roadmap to becoming a low-level programmer because I have found that these skills are not as common as they once were. In addition, many students and beginners ask me how they could become low-level programmers and Linux kernel engineers.

This page cannot include every link/book/course. For example, this page introduces Arduino but there is not detailed information about Arduino and embedded systems. You should go further yourself. You have the keyword "Arduino" with which you can start. So your next step is probably googling Arduino, buying a kit, and doing something for yourself, not collecting links or free books. Please remember this page is just a roadmap for beginners.

## <a name="What-Is-the-Low-Level"></a>What Is the Low-Level?

I classify low-level programming as programming that is very close to the machine, using a lower level programming language like C or assembly. This is in contrast to higher-level programming, typical of user-space applications, using high level languages (e.g. Python, Java).
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language)

Yes, systems programming is a very close concept to low-level programming. This page includes the hardware design and firmware development that is not included in systems programming.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Finally, this page includes topics ranging from hardware components to the Linux kernel. That is a huge range of layers. A one page document can never cover the details of all the layers, so the aim of this document is to serve as a starting point for low-level programming.

##  <a name="Theory"></a>Theory

There are two background theories to low-level programming:
* Computer Architecture
* Operating Systems

I think the best way to learn theory is by taking a course. Reading books is not bad but takes too much time and effort. You can find many good classes on online universities, for instance, Coursera.org and edx.org.
Theory is theory. I don't think you need to get an A+ in the class, just understand the big picture.
You'll get better and better with experience.

Let me introduce several books that I've read. They are commonly used as textbooks in universities. If there is no class with these books in your university, it's worth spending some time reading them.
* Computer Architecture
  * Computer Architecture, Fifth Edition: A Quantitative Approach
  * Computer Systems: A Programmer's Perspective
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* Operating Systems
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System
  * Operating Systems: Internals and Design Principles by William Stallings
* Recommended Courses
   * [CS401: Operating Systems from saylor.org](https://learn.saylor.org/mod/page/view.php?id=921)

There is an infinite list of good books. I don't want to say that you should read many books. Just read one book carefully. Whenever you learn a theory, implement simulation code of it. **Implementing one thing is better than knowing one hundred theories.**

##  <a name="Languages"></a>Languages

### <a name="Assembly"></a>Assembly

Choose one between x86 or ARM. No need to know both. It doesn't matter to know assembly language. The essential thing is understanding the internals of a CPU and computer. So you don't need to practice the assembly of the latest CPU. Select 8086 or Corex-M.

* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
  * basic concepts of CPU and computer architecture
  * basic concepts of C programming language
* [64bit assembly programming(translation in progress)](https://github.com/gurugio/book_assembly_64bit)
  * basic concepts of modern CPU and computer architecture
  * basic concepts of disassembling and debugging of C code
  * _need help for translation_
* [Learning assembly for linux-x64](https://github.com/0xAX/asm)
  * pure 64-bit assembly programming with NASM and inline assembly with GCC
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * Complete reference on ARM programming
* Computer Organization and Design
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * [RISC-V Edition](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757)
  * Academic books that explain how every component of a computer work from the ground up.
  * Explains in detail the different concepts that make up computer architecture.
  * They are not targeted at readers who wish to become proficient in a specific assembly language.
  * The MIPS and ARM edition cover the same topics but by dissecting a different architecture.
  * Both editions contain examples in the x86 world

### <a name="C-language"></a>C language

There is no shortcut. Just read the entire book and solve all the exercises.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * For new standard of C
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * raw implementation of synchronization with C
  * Essential for large scale C programming (especially for kernel programming)
* [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * If you finish reading one or two C programming books, then you MUST make something.
  * Choose whatever you like.
  * First make on your own and then compare with someone else's source code. It is very important to compare your source and others. You can improve your skill only when you read the other's source and learn better methods. Books are dead and source is live.
* [C and other languages based projects](https://github.com/danistefanovic/build-your-own-x)
  * find more interesting projects
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * Reference on optimization using C and a bit of x86 assembly
  * Starts from the 8088 up to today
  * Special focus on low-level graphics optimization
* [Framework and plugin design in C](https://github.com/gurugio/book_cprogramming)
  * How to develop framework and plugin in C for large scale software
  * Very basic programming tips for Linux kernel source reading

If you want to be expert of C programming, visit https://leetcode.com/. Good luck!

## <a name="Applications"></a>Applications

### <a name="Hardware-Firmware"></a>Hardware && Firmware

If you want to be an embedded systems engineer, it would be best to start from a simple hardware kit, rather than starting with the latest ARM chipset.

* [Arduino Start Kit](https://www.arduino.cc/)
  * There are many series of Arduinos but "Arduino Start Kit" has the most simple processor(Atmega328P) and guide book
  * Atmega328P has an 8-bit core which is a good place to start digital circuit design and firmware development.
  * You don't need to know how to draw schematics and layouts and assemble the chips.
  * But you do need to know how to read schematics and understand how the chips are connected.
  * Firmware developers should be able to read the schematics and figure out how to send data to the target device.
  * Follow the guide book!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * If you're a beginner to x86 architecture, 8086 is also very good guide for processor architecture and 80x86 assembly
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Best guide for protected mode and paging mechanism of 80x86 processor
  * Web version: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

At this point, you should be good to start the latest ARM or x86 processor.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

For example, the Raspberry Pi board has a Cortex-A53 Processor that supports a 64-bit instruction set.
This allows you to experience a modern processor architecture with rPi.
Yes, you can buy it... but... what are you going to do with it?
If you have no target project, you would be likely to throw the board into a drawer and forget it like other gadgets you may have bought before.

So, I recommend one project for you.
* [Making your own kernel](http://wiki.osdev.org/Getting_Started)
  * Good references: https://www.reddit.com/r/osdev/
* [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
  * (description of the project) This repository contains a step-by-step guide that teaches how to create a simple operating system (OS) kernel from scratch...(skip)...Each lesson is designed in such a way that it first explains how some kernel feature is implemented in the RPi OS, and then it tries to demonstrate how the same functionality works in the Linux kernel.

I've made [a toy kernel](https://github.com/gurugio/caos) that supports 64-bit long mode, paging and very simple context switching. Making a toy kernel is good way to understand modern computer architecture and hardware control.

In fact, you have already the latest processor and the latest hardware devices.
Your laptop! Your desktop! You already have all that you need in order to start!
You don't need to buy anything.
The qemu emulator can emulate the latest ARM processors and Intel processors.
So everything you need is already on hand.
There are many toy kernels and documents you can refer to.
Just install qemu emulator and make a tiny kernel that just boots, turns on paging, and prints some messages.

Other toy kernels:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Linux kernel and device driver

You don't need to make a complete operating system.
Join the Linux community and participate in development.

#### <a name="Follow-carefully"></a>Follow carefully

* Books: Read the following in order
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * The basic concepts of Unix are applied into all operating systems.
    * This book is a very good place to learn the core concepts of operating systems.
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Make all examples for yourself
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Understand the design of the Linux Kernel
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Read this book and the kernel source v2.6 at the same time
    * Never start with the latest version, v2.6 is enough!
    * Use qemu and gdb to run the kernel source line by line
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * Use busybox to make the simplest filesystem that takes only one second to boot
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Other resources: Free resources I recommend
  * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * Practical guide and excellent exercises making Linux device drivers with essential kernel APIs
    * I think this document introduces almost all essential kernel APIs.
  * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
    * _Sadly, this challenge does not accept new challengers because there is no challenge anymore._ The maintainer said he/she is planning a new format. I hope it comes back ASAP.
      * But you can find the questions of the challenge with Google. Some people already uploaded what they did. Find the questions and try to solve them on your own, and compare your solution with others.
    * This is like an awesome private teacher who guides you on what to do.
    * If you don't know what to do, just start this.
  *  [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
     * This project is not completed yet.
     * I always think making a kernel similar to the Linux kernel is the best way to understand the Linux kernel.
  * [Block layer and device driver](https://github.com/gurugio/book_linuxkernel_blockdrv)
    * start from a simple block device driver example (Ramdisk) with multi-queue mode
    * go forward to block layer
    * I completed translation into English. Please send me your feedback.
  * [md driver of Linux kernel(Korean)](https://github.com/gurugio/book_linuxkernel_md)
    * how mdadm tool works and how it calls md driver
    * how md driver works

#### <a name="References"></a>References

Check when you need something

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * many slide files introducing good topics, specially ARM-linux
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * guide to start kernel programming

### <a name="Other-applications"></a>Other application

Yes, you might not be interested in Linux or firmware. If so, you can find other applications:
* Windows systems programming & device drivers
* Security
* Reverse engineering

I don't have any knowledge about those applications. Please send me any information for beginners.

**Kernels and drivers are not all of low-level programming.** One more important application of low-level programming is the software-defined storage or distributed filesystem. Detailed descriptions of them is beyond the scope of this document but there is an excellent course where you can try a simple distributed filesystem.
* Course: https://pdos.csail.mit.edu/archive/6.824-2012/
* reference Source: https://github.com/srned/yfs

## <a name="Future-of-low-level-programming"></a>Future of low-level programming

I do not know the future, but I keep my eye on RUST.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

If I could have one week free and alone, I would learn RUST.
That is because RUST is the latest language with which I can develop Linux device drivers.
* https://github.com/tsgates/rust.ko

IoT is new trend, so it's worth to check what OSs are for IoT.
ARM, Samsung and some companies has their own realtime OS but sadly many of them are closed source.
But Linux Foundation also has a solution: Zephyr
* https://www.zephyrproject.org/

Typical cloud servers have many layers; for instance, host OS, kvm driver, qemu process, guest OS and service application. A container has been developed to provide light virtualization. In the near future, a new concept of OS, a so-called library OS or Unikernel, would replace the typical stack of SW for virtualization.
* http://unikernel.org/

Big data and cloud computing require bigger and bigger storage. Some disks directly attached to server machines cannot satisfy the required capacity, stability and performance. Therefore there has been research to make huge storage systems with many storage machines connected by a high speed network. It used to be focused on making one huge storage volume. But currently they are providing many volumes dedicated for many virtual machines.
* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

## <a name="How-to-start"></a>How to start?

I received an email to ask how to start. There are so many information about books, courses and projects in this page. It is my mistake to forget to write how to start. Of course, there is no King's Road to follow. I just write what I did in order. If you have already done something, please skip it. AGAIN, this is an example that you could do in order. If you do not know what to do, please do following IN ORDER.

* Reading OS theory books: at least "The Design of the UNIX Operating System"
* Learn assembly and C
  * [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * It is enough if you understand the concept of assembly programming. You do not need to do something practical.
  * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
    * DO NOT FORGET to solve every single exercises!
  * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Do something with C
  * [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): Find one or two interesting projects and make your own project.
  * [leetcode.com](https://leetcode.com/): If you cannot find an interesting project, it would be also good to focus on data-structure and algorithm.
* Do a hardware project
  * Raspberrypi or Arduino does not matter. You need a experience to control a hardware directly with only C. ONLY C!
* Jump into the Linux kernel
  * Start with drivers
    * Read [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Read [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) to understand the internal of Linux kernel.
* If you want to be Linux Kernel Developer
  * must read [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
  * Then try to make a toy kernel
    * [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
    * [Making your own kernel](http://wiki.osdev.org/Getting_Started)
  * Read kernel sources and document at https://lwn.net/
* Or find another topic.

# <a name="Translation"></a>Translation

Please send me the pull request if you'd like to translate this page. I'll list it here.

* [Chinese](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [Portuguese (Brazilian)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_pt.md)
* [Italian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)
* [Czech](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cz.md)
* [Russian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_ru.md)

# <a name="who-am-i"></a>Who am I?

I'm inspired by [google-interview-university](https://github.com/jwasham/google-interview-university). I'd like to share my experience and show a roadmap to becoming a low-level programmer because I have found that these skills are not as common as they once were. In addition, many students and beginners ask me how they could become low-level programmers and Linux kernel engineers.

FYI, I have over 10 years of experience as a low-level programmer:
* 80x86 Assembly programming
* Hardware device with Atmel chip and firmware
* C language system programming for Unix
* Device driver in Linux
* Linux kernel: page allocation
* Linux kernel: block device driver and md module
