# Low-Level Programming University

## What is it?

This page is for beginner who want to be low-level programmer.

I'm inspired by [google-interview-university](https://github.com/jwasham/google-interview-university). I'd like to share my experience and show a kind of roadmap to be low-level programmer because I found that the low-level programmer is getting rare. And many students and beginners asked me how I could be low-level programmer and Linux kernel engineer.

I've working as low-level programmer for 10 years.
* 80x86 Assembly programming
* Hardware device with Atmel chip and firmware
* C language system programming for Unix
* Device driver in Linux
* Linux kernel: page allocation
* Linux kernel: block device driver and md module

## What Is the Low-Level?

I think the low-level programming is programming something that is very close to the machine, rather than the user. The user can be people who use the computer and programmer who use the product of low-level programmer.
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language)

Yes, system programming is very close concept to the low-level programming. But this page includes the hardware design and firmware development that is not included in system programming.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Finally this page includes topics from the hardware components to Linux kernel. That is the huge range of layers. One page document can never cover the detail of all layers. The aim of this page is beging the starting point of the low-level programming.

## Languages

### Assembly

* [8086 assembly programming with emu8086(translation in progress)](https://github.com/gurugio/book_assembly_8086)
 * basic concepts of CPU and computer architecture
 * basic concepts of C programming language
* [64bit assembly programming(translation in progress)](https://github.com/gurugio/book_assembly_64bit)
 * basic concepts of modern CPU and computer architecture
 * basic concepts of disassembling and debugging of C code

### C language

There is no short-cut. Just read the entire book and solve all exercises.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
 * For new standard of C
 
## Applications

### Hardware && Firmware

If you want to be Embedded system engieer, it'd better start from simple hardware kit.
It's not good idea to start with the latest ARM chipset.

* [Arduino Start Kit](https://www.arduino.cc/)
 * There are various series of Arduino but "Arduino Start Kit" has the most simple processor(Atmega328P) and guide book
 * Atmega328P has 8bit core that is the good to start "Digital circuit design" and "Firware development".
 * Just follow the guide book!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
 * If you're very beginner 8086 is also very good guide for processor architecture and 80x86 assembly
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
 * Best guide for protected mode and paging machanism of 80x86 processor
 * Web version: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

Now you would be good to start ARM chipset.
* https://www.raspberrypi.org/
* https://beagleboard.org/

Raspberry Pi board has Cortex-A53 Processor that supports 64bit instruction set.
So you can experience the latest processor architecture with rPi.
Yes, you can buy it...but...what are you going to do with it?
In fact you have already the latest processor and the latest hardware devices.
Your laptop! Your desktop! You already have all to start!

So I recommend one project for you.
* [Making your own kernel](http://wiki.osdev.org/Getting_Started)

You don't need to buy anything.
The qemu emulator can emulate the latest ARM processors and Intel processors.
So everything is already on your hand.
There are so many toy projects you can consult.
Just install qemu emulator and make tiny kernel that just boot and turn on paging and print some messages.

I've made [a toy kernel](https://github.com/gurugio/caos) that supports 64bit long mode, paging and very simple context switching. Making a toy kernel is good way to understand modern computer architecture and hardware control.

### Linux kernel and device driver

You don't need to make a complete operating system.
Join the Linux community and participate in development.

#### Read carefully

* Books: Read followings in order
 * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
   * Make all examples for yourself
 * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
   * Understand the design of Linux Kernel
 * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
   * Read this book and the kernel source v2.6 at the same time
   * Never start with the latest version, v2.6 is enough!
   * Use qemu and gdb to run the kernel source line by line
     * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
     * https://gurugio.kldp.net/wiki/wiki.php/howto_debug_kernel
   * Use busybox to make the simplest filesystem that takes only 1-second to boot
     * https://gurugio.kldp.net/wiki/wiki.php/qemu_kernel
* [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * This is like an awesome private teacher who guide you what to do.
  * If you don't know what to do, just start this.
* [Block layer and device driver(translation in progress)](https://github.com/gurugio/book_linuxkernel_blockdrv)
  * start from a simple block device driver example (Ramdisk) with multi-queue mode
  * go forward to block layer
* [md driver of Linux kernel(in progress)](https://github.com/gurugio/book_linuxkernel_md)
  * how mdadm tool works and how it calls md driver
  * how md driver works

#### References

Check when you need something

* [Free-electrons homepage](http://free-electrons.com/docs/)
 * many slide files introducing good topics, specially ARM-linux
