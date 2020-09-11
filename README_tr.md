UYARI: Lütfen aşağı seviyeli programlamanın popüler olmadığını ve şu anda aşağı seviyeli kod yazan programcıları işe alan çok fazla şirket olmadığını unutmayın. İş bulmam gittikçe zorlaşıyor.
Henüz profesyonel bir kariyere başlamadıysanız, diğer alanları da dikkatlice değerlendirmenizi tavsiye ederim.


* [Aşağı Seviyeli Programlama Üniversitesi](#Aşağı-Seviyeli-Programlama-Üniversitesi)
  * [Nedir?](#Nedir)
  * [Aşağı Seviye nedir?](#Aşağı-Seviye-nedir)
  *  [Teori](#Teori)
  *  [Diller](#Diller)
     * [Assembly](#Assembly)
     * [C dili](#C-dili)
  * [Çalışma Alanları](#Çalışma-Alanları)
    * [Donanım && Firmware](#Donanım-Firmware)
    * [Linux çekirdeği and aygıt sürücüleri](#Linux-çekirdeği-ve-aygıt-sürücüleri)
      * [Dikkatlice okuyun](#Dikkatlice-okuyun)
      * [Referanslar](#Referanslar)
    * [Diğer Çalışma Alanları](#Diğer-Çalışma-Alanları)
  * [Aşağı Seviyeli Programlamanın Geleceği](#Aşağı-Seviyeli-Programlamanın-Geleceği)
  * [Nasıl Başlanır?](#Nasıl-Başlanır)
* [Çeviriler](#Çeviriler)
* [Ben Kimim?](#Ben-Kimim)

# Aşağı Seviyeli Programlama Üniversitesi

## <a name="Nedir"></a>Nedir?

[google-interview-university](https://github.com/jwasham/coding-interview-university)'den esinlendim. Deneyimlerimi paylaşmak ve aşağı seviyeli kod yazan bir programcı olma yolunda bir yol haritası göstermek istiyorum çünkü bu becerilerin eskisi kadar yaygın olmadığını anladım. Ek olarak, birçok öğrenci ve yeni başlayanlar bana nasıl aşağı seviyeli kod yazan programcılar ve Linux çekirdek kodu yazan bir mühendis olabileceklerini soruyor.

Bu sayfa her bağlantıyı/kitabı/kursu içeremez. Örneğin bu sayfada Arduino tanıtılmaktadır ancak Arduino ve gömülü sistemler hakkında detaylı bilgi bulunmamaktadır. Kendin daha fazlasını araştırmalısın. Başlayabileceğiniz "Arduino" anahtar kelimesine sahipsiniz. Yani bir sonraki adımınız muhtemelen Arduino'yu araştırmak, bir Arduino geliştirme seti(kit) satın almak ve bağlantı veya ücretsiz kitap toplamak değil, kendiniz için bir şeyler yapmaktır. Lütfen bu sayfanın yeni başlayanlar için bir yol haritası olduğunu unutmayın.

Aşağı seviyeli programlama, bilgisayar biliminin bir parçasıdır.
Öncelikle bilgisayar bilimi için eğitim almak kesinlikle çok daha iyi olacaktır.
* [Path to a free self-taught education in Computer Science!](https://github.com/ossu/computer-science)


## <a name="Aşağı-Seviye-nedir"></a>Aşağı Seviye nedir?

Aşağı seviyeli programlamayı, C veya Assembly gibi daha düşük seviyeli bir programlama dili kullanarak makineye çok yakın olan programlama olarak sınıflandırıyorum. Bu, yüksek seviyeli diller (ör.Python, Java) kullanan tipik kullanıcı alanı(userspace ve kernelspace kavramlarına bakınız) uygulamaları olan üst düzey programlamanın tersidir.
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language)

Evet, sistem programlama, aşağı seviyeli programlamaya çok yakın bir kavramdır. Bu sayfa, sistem programlamasına dahil olmayan donanım tasarımını ve ürün yazılımı geliştirmeyi içerir.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Son olarak, bu sayfa donanım bileşenlerinden Linux çekirdeğine kadar değişen konuları içerir. Bu, çok çeşitli katmanlardır. Tek sayfalık bir belge hiçbir zaman tüm katmanların ayrıntılarını kapsamaz, bu nedenle bu belgenin amacı, aşağı seviyeli programlama için bir başlangıç ​​noktası olarak hizmet etmektir.

##  <a name="Teori"></a>Teori

Aşağı seviyeli programlamanın iki temel teorisi vardır:
* Computer Architecture
* Operating Systems

Bence teori öğrenmenin en iyi yolu bir kurs almaktır. Kitap okumak fena değil ama çok zaman ve çaba gerektiriyor. Coursera.org ve edx.org gibi çevrimiçi üniversitelerde birçok iyi kurslar bulabilirsiniz.

Teorik bilgi ile gerçeği yani pratik kodlama becerisini ayırt etmek gerekir. Sınıfta A+ almanız gerektiğini düşünmüyorum, sadece büyük resmi görün.

Tecrübe ile gün geçtikçe daha iyi olacaksınız.

Okuduğum birkaç kitabı tanıtmama izin verin. Genellikle üniversitelerde ders kitabı olarak kullanılırlar. Üniversitenizde bu kitapların olduğu bir sınıf yoksa, onları okumak için biraz zaman ayırmaya değer.
* Computer Architecture
  * Computer Architecture, Fifth Edition: A Quantitative Approach
  * Computer Systems: A Programmer's Perspective
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* Operating Systems
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System
  * Operating Systems: Internals and Design Principles by William Stallings
* Recommended Courses
   * [CS401: Operating Systems from saylor.org](https://learn.saylor.org/course/view.php?id=94)

Sayısız iyi kitap listesi var. Çok kitap okumalısın demek istemiyorum. Sadece bir kitabı dikkatlice okuyun. Ne zaman bir teori öğrenirseniz, onun kodunu uygulayın.
**Implementing one thing is better than knowing one hundred theories.**

##  <a name="Diller"></a>Diller

### <a name="Assembly"></a>Assembly

X86 veya ARM arasından birini seçin. İkisini de bilmenize gerek yok. Assembly dilini bilmek önemli değil. Önemli olan bir CPU ve bilgisayarın komut setini anlamaktır. Böylece en yeni CPU'nun assembly dilini yazmanıza gerek kalmaz. 8086 veya Corex-M'yi seçin.

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

### <a name="C-dili"></a>C dili

Kestirme ve hızlı bir yol bulunmuyor. Sadece kitabın tamamını okuyun ve tüm alıştırmaları çözün. 

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

C programlama uzmanı olmak istiyorsanız, https://leetcode.com/ sitesini ziyaret edin. İyi Şanslar!

## <a name="Çalışma-Alanları"></a>Çalışma Alanları

### <a name="Donanım-Firmware"></a>Donanım && Firmware

Gömülü sistem mühendisi olmak istiyorsanız, en son ARM yonga setiyle başlamak yerine basit bir donanım geliştirme setinden(kitinden) başlamak en iyisi olacaktır.

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

Bu noktada, en son ARM veya x86 işlemciye başlamanız gerekir.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Örneğin, Raspberry Pi kartında 64-bit komut setini destekleyen bir Cortex-A53 İşlemci bulunur.
Bu, rPi ile modern bir işlemci mimarisi deneyimlemenizi sağlar.
Evet, satın alabilirsin ... ama ... onunla ne yapacaksın?
Hedef projeniz yoksa, rPi kartı'nı bir çekmeceye atmanız ve daha önce satın almış olabileceğiniz diğer araçlar gibi unutmanız muhtemeldir.

Bu yüzden size aşağıdaki projeleri öneriyorum.
* [Making your own kernel](http://wiki.osdev.org/Getting_Started)
  * Good references: https://www.reddit.com/r/osdev/
* [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
  * (description of the project) This repository contains a step-by-step guide that teaches how to create a simple operating system (OS) kernel from scratch...(skip)...Each lesson is designed in such a way that it first explains how some kernel feature is implemented in the RPi OS, and then it tries to demonstrate how the same functionality works in the Linux kernel.

[a toy kernel](https://github.com/gurugio/caos) yazdım. 64 bit long modu(long mod olarak kalabilir), sayfalamayı ve çok basit bağlam değiştirmeyi destekleyen deneme amaçlı bir çekirdek(kernel) yapmak, modern bilgisayar mimarisini ve donanım kontrolünü anlamanın iyi bir yoludur.

Aslında, en son işlemciye ve en son donanım cihazlarına zaten sahipsiniz.
Senin diz üstü bilgisayarın! Masaüstünüz! Başlamak için ihtiyacınız olan her şeye zaten sahipsiniz!
Hiçbir şey almanıza gerek yok.
QEMU emülatörü, en yeni ARM işlemcileri ve Intel işlemcileri sanal ortamında çalıştırabilir.
Yani ihtiyacınız olan her şey elinizin altında.
Başvurabileceğiniz birçok oyuncak çekirdeği ve belge var.
Sadece QEMU'yu kurun ve sadece önyükleyen, sayfalamayı açan ve bazı mesajları yazdıran küçük bir çekirdek yapın.

Diğer deneme amaçlı çekirdekler(kernel):
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-çekirdeği-ve-aygıt-sürücüleri"></a>Linux çekirdeği and aygıt sürücüleri

Tam bir işletim sistemi oluşturmanıza gerek yok.
Linux topluluğuna katılın ve geliştirmeye katılın.

#### <a name="Dikkatlice-okuyun"></a>Dikkatlice okuyun

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

#### <a name="Referanslar"></a>Referanslar

Bir şeye ihtiyacınız olduğunda kontrol edin

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * many slide files introducing good topics, specially ARM-linux
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * guide to start kernel programming

### <a name="Diğer-Çalışma-Alanları"></a>Diğer Çalışma Alanları

Evet, Linux veya firmware geliştirmeyle ilgilenmeyebilirsiniz. Öyleyse, başka çalışma alanları bulabilirsiniz:
* Windows systems programming & device drivers
* Security
* Reverse engineering

Bu çalışma alanları hakkında hiçbir bilgim yok. Lütfen yeni başlayanlar için yararlı olabilecek bu dosyanın formatına uygun içerikleri gönderin.

**Kernels and drivers are not all of low-level programming.** Aşağı seviyeli programlamanın bir diğer önemli çalışma alanı, yazılım tanımlı depolama veya dağıtık dosya sistemidir. Bunların ayrıntılı açıklamaları bu belgenin kapsamı dışındadır ancak basit bir dağıtık dosya sistemini deneyebileceğiniz mükemmel bir kurs vardır.
* Course: https://pdos.csail.mit.edu/archive/6.824-2012/
* reference Source: https://github.com/srned/yfs

## <a name="Aşağı-Seviyeli-Programlamanın-Geleceği"></a>Aşağı Seviyeli Programlamanın Geleceği

Geleceği öngöremiyorum ama RUST programlama diline dikkatimi vermeye başladım.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Kendime bir hafta zaman ayırabilseydim, RUST öğrenirdim.
Bunun nedeni, RUST'ın Linux aygıt sürücülerini geliştirebileceğim en son dil olmasıdır.
* https://github.com/tsgates/rust.ko

IoT tercih edilmeye başlanan popüler ve yeni bir akım, bu nedenle IoT teknolojisiyle hangi işletim sistemlerinin uyumlu olduğunu kontrol etmeye değer görüyorum.
ARM, Samsung ve bazı şirketlerin kendi gerçek zamanlı işletim sistemleri var, ancak ne yazık ki çoğu kapalı kaynak(yani kaynak kodu verilmeyen, kaynak kodunu düzenlemeye ve yeniden dağıtmaya izin vermeyen çalışmalar).
Ancak Linux Vakfı'nın da bir çözümü var: Zephyr
* https://www.zephyrproject.org/

Geleneksel bulut sunucularının birçok katmanı vardır; örneğin, ana işletim sistemi, kvm sürücüsü, qemu işlemi, konuk işletim sistemi ve hizmet uygulaması. Hafif sanallaştırma sağlamak için bir konteyner geliştirilmiştir. Yakın gelecekte, kütüphane işletim sistemi veya Unikernel olarak adlandırılan yeni bir işletim sistemi kavramı, sanallaştırma için tipik yazılım yığını yerine geçecektir.
* http://unikernel.org/

Büyük veri ve bulut bilişim, daha büyük ve daha büyük depolama gerektirir. Doğrudan sunucu makinelerine takılan bazı diskler gerekli kapasite, kararlılık ve performansı karşılayamaz. Bu nedenle, yüksek hızlı bir ağ ile birbirine bağlanan birçok depolama makinesiyle büyük depolama sistemleri yapmak için araştırmalar yapılmıştır. Eskiden büyük bir depolama hacmi yapmaya odaklanırdı. Ancak şu anda birçok sanal makine için ayrılmış birçok birim sağlıyorlar.
* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

## <a name="Nasıl-Başlanır"></a>Nasıl Başlanır?

Nasıl başlayacağımı soran bir e-posta aldım. Bu sayfada kitaplar, kurslar ve projeler hakkında birçok bilgi var. Nasıl başlayacağımı yazmayı unutmak benim hatam. Maalesef [Kralın Şehrine](https://gameofthrones.fandom.com/wiki/King%27s_Landing) giden Kral Yolu bulunmuyor. Sadece sırayla ne yaptığımı yazacağım. Zaten bir şey yaptıysanız, lütfen atlayın. Ve YİNE belirtmeliyim ki, bu sadece nasıl başlayacağınızı veya ne yapacağınızı bilmiyorsanız, sırayla yapabileceğiniz bir örnek metindir.

* Reading OS theory books: at least "The Design of the UNIX Operating System by Maurice J. Bach"
* Learn assembly and C
  * [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * It is enough if you understand the concept of assembly programming. You do not need to do something practical.
  * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
    * DO YOUR BEST TO solve every single exercises!
  * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Do something practical with C
  * [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): Find one or two interesting projects and make your own project.
  * [leetcode.com](https://leetcode.com/): If you cannot find an interesting project, it would be also good to focus on data-structure and algorithm.
* Do a hardware project
  * Raspberrypi or Arduino does not matter. You need a experience to control a hardware directly with only C. ONLY C!
  * I recommend to buy a Atmega128 kit and make a firmware to turn on/off LEDs, detect switch input and display message on the text LCD. Motor control program is also a very good project: for instance, the line tracer.
  * DO NOT use any library. You should make everything on your own, except program downloader.
* Basic of the Linux kernel
  * Low-level programming is very close to the operating system. You should know inside of the OS.
  * Start with drivers
    * Read [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Read [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) to understand the internal of Linux kernel.
* Go to the professional field
  * If you want to be professional Linux Kernel Developer
    * must read [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
      * Then try to make a toy kernel
      * [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
      * [Making your own kernel](http://wiki.osdev.org/Getting_Started)
    * Check the latest issues at https://lwn.net/ and join it.
  * Or find another topics

# <a name="Çeviriler"></a>Çeviriler

Bu sayfayı çevirmek istiyorsanız lütfen bana çekme talebini gönderin. Burada listeleyeceğim.
* [Chinese](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [Portuguese (Brazilian)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_pt.md)
* [Italian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)
* [Czech](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cz.md)
* [Russian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_ru.md)
* [Turkish](https://github.com/masscollaborationlabs/lowlevelprogramming-university/blob/master/README_tr.md)

# <a name="Ben-Kimim"></a>Ben-Kimim?

[google-interview-university](https://github.com/jwasham/coding-interview-university)'den esinlendim. Deneyimlerimi paylaşmak ve aşağı seviyeli kod yazan bir programcı olma yolunda bir yol haritası göstermek istiyorum çünkü bu becerilerin eskisi kadar yaygın olmadığını anladım. Ek olarak, birçok öğrenci ve yeni başlayanlar bana nasıl aşağı seviyeli kod yazan programcılar ve Linux çekirdek kodu yazan bir mühendis olabileceklerini soruyor.

Bilmenizi isterim ki aşağı seviyeli kod yazan bir programcı olarak 10 yıldan fazla kod yazma deneyimine sahibim:
* 80x86 Assembly programming
* Hardware device with Atmel chip and firmware
* C language system programming for Unix
* Device driver in Linux
* Linux kernel: page allocation
* Linux kernel: block device driver and md module
