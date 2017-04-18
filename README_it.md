* [Universit&agrave; della programmazione a basso livello](#Low-Level-Programming-University)
  * [Che cos'&egrave;](#What-is-it)
  * [Che cos'&egrave; il basso livello'](#What-Is-the-Low-Level)
  *  [Teoria](#Theory)
  *  [Linguaggi](#Languages)
    * [Assembly](#Assembly)
    * [Linguaggio C](#C-language)
  * [Applicazioni](#Applications)
    * [Hardware e Firmware](#Hardware-Firmware)
    * [Il kernel Linux e i driver di dispositivo](#Linux-kernel-and-device-driver)
      * [Leggi con attenzione](#Read-carefully)
      * [Riferimenti](#References)
  * [Futuro della programmazione a basso livello](#Future-of-low-level-programming)
* [Traduzioni](#Translation)

# <a name="Low-Level-Programming-University"></a>Universit&agrave; della programmazione a basso livello

## <a name="What-is-it"></a>Che cos'&egrave;?

Questa pagina &egrave; per i principianti che vogliono essere programmatori a basso livello.

L'inspirazione proviene dalla pagina [google-interview-university](https://github.com/jwasham/google-interview-university). Vorrei condividere la mia esperienza e mostrare un piano per diventare un programmatore a basso livello perch&egrave; mi sono reso conto che queste skill non sono cos&igrave; diffuse come una volta. Inoltre, molti studenti e principianti mi chiedono come possono diventare dei programmatori a basso livello e ingegneri del kernel di Linux.

Questa pagina non potr&agrave; mai includere ogni link/libro/corso a riguardo.
Ad esempio, questa pagina introduce Arduino ma non sono presenti informazioni dettagliate riguardo ad esso e alla programmazione embedded. Il resto spetta a te. Hai letto la parola chiave "Arduino" dalla quale puoi partire; perci&ograve; il tuo prossimo passo sar&agrave; probabilmente ricercarla su Google, comprare il kit e **sperimentare** per te stesso, non collezionare libri gratuiti e link. Ricorda che questa pagina &egrave; solo un piano.

Per tua informazione, ho oltre 10 anni di esperienza come programmatore a basso livello:
* Programmazione assembly 80x86
* Driver per hardware con chip e firmware Atmel chip
* Programmazione di sistema in linguaggio C per Unix
* Driver di dispositivo per Linux
* Kernel linux: allocazione di pagina
* Kernel linux: dispostivi a blocchi e modulo md

## <a name="What-Is-the-Low-Level"></a>Che cos'&egrave; il basso livello?

Identifico come programmazione a basso livello, quella programmazione che &egrave; molto vicina alla macchina, usando un linguaggio a basso come C o Assembly. Ci&ograve; &egrave; in contrasto la programmazione ad alto livello, tipica delle applicazioni denominate user-space, che utilizzano linguaggi ad alto livello (es. Python, Java).
* [Wikipedia: Linguaggio di programmazione a basso livello](https://it.wikipedia.org/wiki/Linguaggio_di_programmazione_a_basso_livello)

***TO DO***

Yes, systems programming is a very close concept to low-level programming. This page includes the hardware design and firmware development that is not included in system programming.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Finally, this page includes topics ranging from hardware components to the Linux kernel. That is a huge range of layers. A one page document can never cover the details of all the layers, so the aim of this document is to serve as a starting point for low-level programming.

##  <a name="Theory"></a>Theory

There are two background theories to low-level programming:
* Computer Architecture
* Operating Systems

You can find many good classes on online universities, for instance, Coursera.org and edx.org.
Theory is theory. I don't think you should get A+ in the class, just understand the big picture in the class.
You'll get better and better with experience.

##  <a name="Languages"></a>Languages

### <a name="Assembly"></a>Assembly

* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
  * basic concepts of CPU and computer architecture
  * basic concepts of C programming language
* [64bit assembly programming(translation in progress)](https://github.com/gurugio/book_assembly_64bit)
  * basic concepts of modern CPU and computer architecture
  * basic concepts of disassembling and debugging of C code
  * _need help for translation_
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * Complete reference on ARM programming
* Computer Organization and Design
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * Academic books that explain how every component of a computer work from the ground up.
  * Explains in details the different concepts that make up computer architecture.
  * They are not for targeted to becoming proficient in a specific assembly language.
  * The MIPS and ARM edition cover the same topics but by dissecting a different architecture.
  * Both editions contain examples in the x86 world

### <a name="C-language"></a>C language

There is no short-cut. Just read the entire book and solve all the exercises.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * For new standard of C
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * raw implementation of synchronization with C
  * Essential for large scale C programming (especially for kernel programming)
* [C programming challenge?](https://github.com/gurugio/lowlevelprogramming-university/blob/master/c-language-challenge.md)
  * plan for service like [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Just an idea at the moment..
  * If you can make all tiny projects in that page, you would be good to start big projects.
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * Reference on optimization using C and a bit of x86 assembly
  * Starts from the 8088 up to today
  * Special focus on low-level graphics optimization

## <a name="Applications"></a>Applications

### <a name="Hardware-Firmware"></a>Hardware && Firmware

If you want to be an embedded systems engineer, it would be best to start from a simple hardware kit, rather than starting with the latest ARM chipset.

* [Arduino Start Kit](https://www.arduino.cc/)
  * There are various series of Arduino but "Arduino Start Kit" has the most simple processor(Atmega328P) and guide book
  * Atmega328P has 8bit core that is the good to start "Digital circuit design" and "Firware development".
  * You don't need to know how to draw schematics and layout, and assemble the chips.
  * But you need to know how to read schematics and understand how the chips are connected.
  * Firmware developers should be able to read the schematics and figure out how to send data to the target device.
  * Follow the guide book!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * If you're a beginner to x86 architecture, 8086 is also very good guide for processor architecture and 80x86 assembly
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Best guide for protected mode and paging machanism of 80x86 processor
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

I've made [a toy kernel](https://github.com/gurugio/caos) that supports 64bit long mode, paging and very simple context switching. Making a toy kernel is good way to understand modern computer architecture and hardware control.

In fact, you have already the latest processor and the latest hardware devices.
Your laptop! Your desktop! You already have all to start!
You don't need to buy anything.
The qemu emulator can emulate the latest ARM processors and Intel processors.
So everything you need is already on hand.
There are so many toy kernel and documents you can refer to.
Just install qemu emulator and make a tiny kernel that just boots and turns on paging, and prints some messages.

Other toy kernels:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Linux kernel and device driver

You don't need to make a complete operating system.
Join the Linux community and participate in development.

#### <a name="Read-carefully"></a>Read carefully

* Books: Read followings in order
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * The basic concepts of Unix are applied into all operating system.
    * This book is very good to get the concepts of operating system.
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
  * _need help for translation_
* [md driver of Linux kernel(in progress)](https://github.com/gurugio/book_linuxkernel_md)
  * how mdadm tool works and how it calls md driver
  * how md driver works
  * _need help for translation_

#### <a name="References"></a>References

Check when you need something

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * many slide files introducing good topics, specially ARM-linux
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * guide to start kernel programming

## <a name="Future-of-low-level-programming"></a>Future of low-level programming

I do not know the future, but I keep my eye on RUST.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

If I could have one week free and alone, I would learn RUST.
That is because RUST is the latest language with which I can develop Linux device driver.

IoT is new trend, so it's worth to check what OSs are for IoT.
ARM, Samsung and some companies has their own realtime OS but sadly many of them are close source.
But Linux Foundation also has a solution: Zephyr
* https://www.zephyrproject.org/

Typical cloud server has so many layers, for instance, host OS, kvm driver, qemu process, guest OS and service application. So container has been developed to provide light virtualization. In near future, a new concept of OS, so-called library OS or Unikernel, would be replace the typical stack of SW for virtualization.
* http://unikernel.org/

# <a name="Translation"></a>Translation

Please send me the pull request if you'd like to translate this page. I'll list it here.
