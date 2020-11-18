RNOTICE:  
Please notice that low-level programming is out of trend and currently  
there are not many companies hiring low-level developer.  
It is getting harder for me to find a job.  
If you does not start professional career yet,  
I would like to recommend you consider other fields carefully.

__提醒__：  
請注意，底層程式開發已不是主要趨勢，現今有許多公司已不再聘請底層程式開發者，  
作者本身也越來越難找到相關的工作。  
如果你並非全職專業技能者，我會建議你仔細考慮其他領域。

* [底層程式開發的世界](#Low-Level-Programming-University)
  * [這篇文章在講什麼?](#What-is-it)
  * [什麼是底層](#What-Is-the-Low-Level)
  * [理論](#Theory)
  * [程式語言](#Languages)
     * [組合語言](#Assembly)
     * [C 語言](#C-language)
  * [應用程式](#Applications)
    * [硬體 && 韌體](#Hardware-Firmware)
    * [Linux 核心與設備驅動程式](#Linux-kernel-and-device-driver)
      * [參考](#References)
    * [其他的應用領域](#Other-applications)
  * [關於底層程式開發的前景](#Future-of-low-level-programming)
  * [如何開始?](#How-to-start)
* [翻譯版本](#Translation)
* [我是誰?](#who-am-i)

# 底層程式開發的世界

## <a name="What-is-it"></a>這篇文章在講什麼?

我是被一篇文章所啟發 [google-interview-university](https://github.com/jwasham/coding-interview-university)。  
我想要來分享我自己的經驗並且展示如何成為一個底層程式開發者，
因為我發現這些技能並不像以前一樣那麼的常見。  
此外，也有越來越多的學生及初學者開始問我，
如何成為一個底層開發者及 Linux 核心工程師。  

這篇文章並不會包含所有相關的 連結/書籍/課程。    
例如，這篇文章包含了 Arduino，但並不會有關於 Arduino 及嵌入式系統的細節資訊，
你得到了 Arduino 這個關鍵字，接下來所要做的就是走出自己的一條路。    
這條路可能是從 googling Arduino 開始，買一些器材、設備，為你的學習做出實際的行動，
而非收集一堆資訊卻不去閱讀。    
請記得，這只是一個給初學者的學習指南而已。

底層程式開發是電腦科學的一部分。    
當然，如果能先學習有關電腦科學的相關教育知識會是更好的。    

* [免費的自學電腦科學途徑!](https://github.com/ossu/computer-science)


## <a name="What-Is-the-Low-Level"></a>什麼是底層?

什麼是底層？什麼是高階層？    
我區分的方式是，你是否使用了 C 或組合語言去撰寫了與機器相關的程式。    
這相對於其他高階層的程式開發有很大的區別，    
因為高階層的程式語言開發，通常不需要注意機器、硬體，
使用者空間 (user-space) 的應用程式，通常會使用高階層程式語言 (例如： Python, Java) 

* [維基百科: 底層程式語言](https://en.wikipedia.org/wiki/Low-level_programming_language)


你可能猜到了一些，系統程式開發是一種非常靠近底層程式開發的型態。    
但是系統程式開發通常不會包含硬體設計及韌體開發，而這篇文章會包含這些額外的內容    

* [維基百科: 系統程式開發](https://en.wikipedia.org/wiki/System_programming)


最後，這篇文章會從硬體的元件，講到 Linux 核心。    
這跨越了非常多的領域，一篇文章不太可能包含所有的細節，
所以請把這篇文章當成一個進入底層程式開發的起始點。    


##  <a name="Theory"></a>理論

底層程式開發有兩種主要的背景知識

* 電腦組織架構
* 作業系統


我認為學習理論最好的方式是跟著一個課程學習，
自己讀書並不是不好，只是會耗費你大量的時間與努力，    
你應該可以在網路上找到各個大學的線上課程，例如像 Coursera.org 和 edx.org。    
理論就是理論，我不認為你一定要在課堂上拿到 A+，只需要在腦中有一個粗略的背景知識。    
你會隨著經驗增加而越來越厲害。    


讓我介紹幾本我讀過的書。    
這些書通常是大學中的教科書。    
就算你的大學中沒有任何的課程是使用這些書，它們還是很值得你花時間去閱讀    

* 電腦組織與架構
  * Computer Architecture, Fifth Edition: A Quantitative Approach
  * Computer Systems: A Programmer's Perspective
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* 作業系統
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System
  * Operating Systems: Internals and Design Principles by William Stallings
* 建議的課程
   * [CS401: 作業系統 from saylor.org](https://learn.saylor.org/course/view.php?id=94)


世界上有無窮無盡的好書等著你。    
我不想說你應該每一本都去念，只要選個一、兩本，仔細的去讀、去學，    
不論你學到了什麼理論，把程式碼實做出來
**實做無價，把東西做出來，知識才真的屬於你**

##  <a name="Languages"></a>程式語言

### <a name="Assembly"></a>組合語言

選擇 X86 或 ARM 其中一種。不需要兩種都知道。    
至於選那一種也不是很重要，因為學習組合語言的重點是，你必須要知道 CPU 與電腦的運作方式，    
所以不需要練習最新 CPU 的組合語言，嘗試選一種 8086 或 Corex-M


* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
  * CPU 與電腦架構的基本知識
  * C 語言開發的基本知識
* [64bit assembly programming(translation in progress)](https://github.com/gurugio/book_assembly_64bit)
  * 現代 CPU 與電腦架構的基本知識
  * C 語言之反組譯、偵錯的基本知識
  * _need help for translation（原作者需要有人幫忙翻譯這本書）_
* [Learning assembly for linux-x64](https://github.com/0xAX/asm)
  * 使用 GCC 之 64-bit 基本語法組合語言與 NASM 之程式開發
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * ARM 程式開發之完整參考
* 電腦組織與設計
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * [RISC-V Edition](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757)
  * 學校的書會解釋電腦的每一個元件是如何運作的
  * 解釋有關於電腦組織架構的相關細節與之間的差別
  * 這些書籍也沒有期望它們的讀者會想要成為組合語言的專家
  * MIPS 與 ARM 的部份會包含同樣的主題在不同的架構上
  * 同樣的版本都會有 x86 的例子

### <a name="C-language"></a>C 語言

關於 C 語言，沒有捷徑。
必須閱讀全部的書籍並且實做所有的練習。

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * 關於 C 語言的新標準
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * 用 C 語言實做同步化
  * 用 C 語言實做大型程式的必須知識 (通常是與核心程式開發相關))
* [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * 如果你讀完了一、兩本 C 語言的書，那你應該要實做一些東西
  * 選一個你喜歡的
  * 嘗試先實做你自己的程式，接著再去對照別人的程式碼，如此就可以學習到哪裡寫的好，哪裡寫的不好，閱讀其他人的程式碼，永遠都可以學到一些東西
* [C and other languages based projects](https://github.com/danistefanovic/build-your-own-x)
  * 找一些有趣的專案做做看
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * 增進 C 語言與 x86 組合語言效能的參考
  * 今天，從 8088 開始
  * 專注底層圖形之效能增進
* [Framework and plugin design in C](https://github.com/gurugio/book_cprogramming)
  * 如何用 C 語言在大型軟體中開發框架與套件
  * 如何閱讀 Linux 核心程式碼之基本程式開發的提示

如果你想成為 C 語言的專家, 請到     

https://leetcode.com/.     

Good luck!

## <a name="Applications"></a>應用程式

### <a name="Hardware-Firmware"></a>硬體 && 韌體

如果你想成為一個嵌入式系統的工程師，
比起學習最新的 ARM 晶片，最好還是從一個簡單的硬體套件開始，

* [Arduino Start Kit](https://www.arduino.cc/)
  * 市面上有很多種 Arduinos 系列， 但 "Arduino Start Kit"有最簡單的處理器  (Atmega328P) 和說明書。
  * Atmega328P 有一個 8-bit 核心，是一個很好做數位電路設計和韌體開發的起點
  * 你不需要知道如何去畫電路圖、不需要知道如何布局、更不需要知道如何封裝晶片。
  * 但你需要知道如何去讀電路圖，也必須知道晶片應該如何連接。
  * 韌體開發者需要知道如何閱讀電路圖及設備之間如何傳遞訊息。
  * 跟著指南書走!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * 如果你是 x86 架構的初學者，8086 也是非常好的學習領域，關於處理器架構和 80x86 組合語言。
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * 80x86 處理器的保護模式及 paging 機制。
  * 網頁版本: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm


在這個部份，你必須要有一定程度的技術能力來開始接下來的部份，最新的 ARM 或 x86 處理器

* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

舉例，樹莓派的開發板上有 Cortex-A53 的處理器，該處理器支援 64 bit 的指令集

新的樹莓派可以讓你體驗先進的處理器架構，你可以買新的沒錯，    
但如果你沒有任何的想法，不知道買來要幹麻，你很可能很快就會把板子忘在抽屜裡面了，    
就像你之前買的那些設備一樣，對吧，你懂的。    

所以，我有個好建議。    

* [寫一個你自己的核心](http://wiki.osdev.org/Getting_Started)
* 很棒的參考: https://www.reddit.com/r/osdev/
* [用樹莓派來學習如何做 Linux 作業系統與核心開發](https://github.com/s-matyukevich/raspberry-pi-os)
* （嘗試描述這個專案）(description of the project) 這個程式庫有說明書，教你如何一步一步的從無到有，建立一個簡單的作業系統核心，每一個課程都是專門為了初學者設計過的，告訴你每一個核心的功能，如何實做在樹莓派作業系統中，並嘗試以此示範在 Linux 核心中同樣的功能是如何運作的

我做了一個 [小型核心程式](https://github.com/gurugio/caos) 
它支援 64-bit 長指令模式，paging，簡單的 context switching，    
用 __小型核心程式__ 來示範，讓人可以比較簡單的了解現代的電腦架構與硬體控制

事實上，你早就有最新的處理器及硬體設備，就是你的筆記型電腦，你隨時可以開始。    
你可以不用再買其他東西，qemu 模擬器可以模擬最新的 ARM 處理器跟 Intel 處理器    

你需要的，你都有，    
你可以參考很多東西，隨便找都有一堆小型核心程式跟文件，    
安裝 qemu 模擬器，編譯出一個小核心，    
啟動核心之後，啟動 paging，印幾行訊息出來看看。    


還有一些你可以參考的小型核心程式 :

* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Linux 核心與設備驅動程式

要做一整個完整的作業系統是非常困難的，其實你不需要自己做，    
加入 Linux 社群，參與開發就好

初階到進階之 Linux 核心與設備驅動程式開發的相關資源

* 書籍: 照著順序讀以下的書
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * Unix 作業系統被應用到其他所有作業系統的基本觀念
    * 這本書是可以學到作業系統的重要觀念
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * 自己嘗試實做出所有的練習
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * 了解 Linux 核心設計
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * 請讀這本書，並同時閱讀 Linux 核心原始碼 v2.6
    * 不需要讀最新的 Linux 核心，v2.6 就已經足夠!
    * 使用 qemu 及 gdb 去一行一行的把核心程式碼跑起來
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * 用 busybox 去做一個最簡單的檔案系統，只需要一秒就可以啟動的檔案系統
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* 其他資源: 我推薦的，不用錢的資源
  * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * Linux 設備驅動程式與常備核心 APIs 之實做指南與經典範例
    * 我認為這份文件介紹了幾乎全部的必要之核心 APIs
  * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
    * _可惜，這個挑戰已經不再接受新的挑戰者申請了，因為已經不再有挑戰的關卡_ 這個服務的維護者說過，他/她已經在準備一個新的服務，我希望可以趕快看到
      * 雖然原本的服務已經不在了，但是有些人上傳了之前的相關題目，可以用 google 找找看，並且嘗試自己解題，再看看你做的與別人做的差別在那
    * 這就像是家教老師，告訴你應該怎麼做
    * 如果你不知道要做什麼，那改作這個
  *  [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
     * 這個專案還沒完成
     * 我一直認為做一個跟 Linux 核心很像的核心，就是學習 Linux 核心最好的方式
  * [Block layer and device driver](https://github.com/gurugio/book_linuxkernel_blockdrv)
    * 用多重佇列模式，來開始學做簡單的區塊設備驅動程式 (Ramdisk)
    * 進入到區塊層
    * 原作者已經將原文翻譯成英文，看過後，有想法可以回饋給原作者
  * [md driver of Linux kernel(Korean)](https://github.com/gurugio/book_linuxkernel_md)
    * mdadm 工作如何運作及如何調用 md 驅動程式
    * md 驅動程式如何運作

#### <a name="References"></a>參考

如果你遇到一些困難，試著找看看有沒有你需要的資料

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * 有很多的投影片，介紹很多主題，特別是關於 ARM-linux
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * 如何開始核心程式開發指南

### <a name="Other-applications"></a>其他的應用程式

或許你對於 Linux 跟韌體並不真的那麼有興趣。
那你還可以考慮試試其他的應用領域：

* Windows 系統程式開發 & 設備驅動程式
* 資訊安全
* 逆向工程

原作者本身並沒有關於這些領域的相關知識，
如果有人懂這方面的知識，原作者期待可以收到相關的入門資料。


**核心以及驅動程式並不是底層程式開發的全部** 
有一個很重要的底層應用程式，稱為『軟體定義儲存裝置』或『分散式檔案系統』。    
關於此領域的知識細節已經超出了這個文件所要介紹的範圍，    
但如果你有興趣，可以參考這個課程，可以了解簡單的分散式檔案系統。

* 課程: https://pdos.csail.mit.edu/archive/6.824-2012/
* 參考來源: https://github.com/srned/yfs

## <a name="Future-of-low-level-programming"></a>底層程式開發的未來

其實我並不知道未來會是怎樣，但是我持續在注意 RUST 這個程式語言。

* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

如果我有一些獨處的時間，我會試著學 RUST。    
因為 RUST 是嶄新的程式語言，也可以拿來開發 Linux 設備驅動程式。

* https://github.com/tsgates/rust.ko

物連網是目前的新趨勢，所以很值得去了解物連網與其相關的作業系統。    
ARM、三星，還有一些其他的公司有發展它們自己的即時作業系統，
可惜的是大部分都為閉源程式（相對於開源程式）。    
但別氣餒，Linux 基金會也有自己的開源解決方案：Zephyr

* https://www.zephyrproject.org/

一個典型的雲端伺服器會有好幾層的技術堆疊，    
例如：會有主層作業系統、客層作業系統、KVM 驅動程式、qemu 的行程、應用程式服務。

有一種應用程式稱為容器，容器已經可以提供輕量型的虛擬化。    
在不久的將來，會有新的作業系統概念，也就是所謂的 library OS 或稱 Unikernel，    
有可能會取代目前典型的軟體虛擬化技術。

* http://unikernel.org/

大數據及雲端計算需要非常非常多的儲存空間。    
有時候，在伺服器內的硬碟容量、穩定性及效能，已經不能負荷其服務所需。    
因此目前有人在研究，嘗試開發出一個巨型儲存系統，這個系統是用許多分散式的儲存設備，配合高速網路互相連接，所搭建起來的。
上述的技術主要是用來搭建一個巨大的儲存空間。    
而目前這樣的技術主要是用來做虛擬機器的使用空間。    

* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

## <a name="How-to-start"></a>如何開始?

我收到了許多的信件來問我說，你說的東西很棒，但是該怎麼開始？    
其實你們所需要的東西都已經在這篇文章裡面了，不管是書籍、課程、還是專案。    
我想我忘了告訴大家該怎麼開始做這一切，
但其實關於這個問題…，就如同詢問，該如何從河岸的一岸到另外一岸？    
該如何到達彼岸，並沒有正確的答案

[King's Landing](https://gameofthrones.fandom.com/wiki/King%27s_Landing)

我所能做的就是把我曾經做過得寫出來。    
如果你也曾經學過這些，就跳過去學下一個，
我必須再次聲明，這只是個讓你參考如何開始的範例。    

* 閱讀作業系統理論書籍: 最少要看一下 "The Design of the UNIX Operating System by Maurice J. Bach"
* 學組合語言與 C 語言
  * [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * 如果你已經了解組合語言的概念，這樣就夠了。
  * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
    * 試著自己去解出書中所有的題目
  * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* C 語言專案的實做
  * [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): 找一兩個有興趣的專案做做看，然後試著做你自己的專案。
  * [leetcode.com](https://leetcode.com/): 如果你真的找不到有興趣的專案，那就到 leetcode 練習練習你的資料結構跟演算法，這樣也是 OK 的。
* 做一些硬體相關的專案
  * 用樹莓派或者是 Arduino 都可以，你需要的是用 C 語言控制硬體的經驗，記住，只有 C 語言!
  * 我建議買一個 Atmega128 套件，然後編譯一個韌體去試著開關 LEDs, 在文字 LCD 上觀察觀察輸入與顯示的狀況。用程式來控制馬達也是一個很好的專案，例如: 尋軌機器人。 
  * 試著不要去用任何程式庫，你應該試著自己做出輪子，這樣才能學到從無到有的知識。
* Linux 核心的基礎
  * 底層程式開發是非常靠近作業系統的，你應該知道作業系統裡面是怎運作的。
  * 如何起手設備驅動程式
    * 請閱讀 [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * 請閱讀 [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) 試著去了解 Linux 核心的運作。
* 成為專業人士、擁有專業的知識
  * 如果你想成為專業的 Linux 核心開發者
    * 一定要讀 [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
      * 試著自己做出並編譯一個具體而微的核心
      * [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
      * [Making your own kernel](http://wiki.osdev.org/Getting_Started)
    * 注意最新的內容消息 https://lwn.net/ 並加入這個社群.
  * 試著找其他你有興趣的議題

# <a name="Translation"></a>翻譯版本

如果你翻譯了這份文章，請發個 pull request 給我，    
我會將你翻譯的部份放在下方的列表中

* [Chinese (Simpllified)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [Chinese (Traditional))](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tw.md)
* [Portuguese (Brazilian)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_pt.md)
* [Italian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)
* [Czech](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cz.md)
* [Russian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_ru.md)
* [Turkish](https://github.com/masscollaborationlabs/lowlevelprogramming-university/blob/master/README_tr.md)

# <a name="who-am-i"></a>原作者?


我因為閱讀了 [google-interview-university](https://github.com/jwasham/google-interview-university) 這篇文章而被啟發。    
我想要分享我的知識、經驗，並且告訴世人要如何成為一個底層程式語言開發者，
因為我發現這些知識，已經不像以前那麼常見。    
此外，許多初學者及學生一直再問我，他們應該如何做才能成為底層程式開發者。    


如果你想了解我？
我是一位擁有 10 年底層程式開發經驗的程式設計師：

* 80x86 組合語言程式開發
* Atmel 晶片、硬體、韌體開發經驗
* Unix 系統 C 語言開發經驗
* Linux 驅動程式開發經驗
* Linux 核心: page allocation
* Linux 核心: 區塊設備、模組之驅動程式