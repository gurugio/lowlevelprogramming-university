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

## Applications

### Hardware device

### Hardware circuit design

### Firmware

### Linux kernel and device driver

* [Block layer and device driver(translation in progress)](https://github.com/gurugio/book_linuxkernel_blockdrv)
 * start from a simple block device driver example (Ramdisk)
 * make multi-queue mode of ramdisk
 * go forward to block layer
 
* [md driver of Linux kernel(in progress)](https://github.com/gurugio/book_linuxkernel_md)
 * how mdadm tool works and how it calls md driver
 * how md driver works
