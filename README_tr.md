UYARI1: Lütfen bu sayfanın içeriğini blogunuza kopyalamayın.  Bu sayfayı paylaşabilirsiniz ama lütfen orijinal link ile paylaşın.  İyi belge ve açık kaynak projesinin yazarlarını bu şekilde övüyoruz.

UYARI2: Lütfen düşük seviyeli programlamanın popüler olmadığını ve şu anda düşük seviyeli kod yazan programcıları işe alan çok fazla şirket olmadığını unutmayın. İş bulmam gittikçe zorlaşıyor.
Henüz profesyonel bir kariyere başlamadıysanız, diğer alanları da dikkatlice değerlendirmenizi tavsiye ederim.

UYARI3: Eğer hızlı bir başlangıç istiyorsanız, "Nasıl Başlanır?" bölümüne gidin.

* [Düşük Seviyeli Programlama Üniversitesi](#Düşük-Seviyeli-Programlama-Üniversitesi)
  * [Nedir?](#Nedir)
  * [Düşük Seviye nedir?](#Düşük-Seviye-nedir)
  * [Teori](#Teori)
  * [Diller](#Diller)
     * [Assembly](#Assembly)
     * [C dili](#C-dili)
     * [Rust dili](#rust-dili)
  * [Çalışma Alanları](#Çalışma-Alanları)
    * [Donanım && Firmware](#Donanım-Firmware)
    * [Linux çekirdeği and aygıt sürücüleri](#Linux-çekirdeği-ve-aygıt-sürücüleri)
      * [Referanslar](#Referanslar)
    * [Diğer Çalışma Alanları](#Diğer-Çalışma-Alanları)
  * [Düşük Seviyeli Programlamanın Geleceği](#Düşük-Seviyeli-Programlamanın-Geleceği)
  * [Nasıl Başlanır?](#Nasıl-Başlanır)
* [Çeviriler](#Çeviriler)
* [Ben Kimim?](#Ben-Kimim)

# Düşük Seviyeli Programlama Üniversitesi

## <a name="Nedir"></a>Nedir?

Bu yazıyı [google-interview-university](https://github.com/jwasham/coding-interview-university)'den esinlendim. Deneyimlerimi paylaşmak ve düşük seviyeli kod yazan bir programcı olma yolunda bir yol haritası göstermek istiyorum çünkü bu becerilerin eskisi kadar yaygın olmadığını anladım. Ek olarak, birçok öğrenci ve yeni başlayanlar bana nasıl düşük seviyeli kod yazan programcı ve Linux çekirdek kodu yazan bir mühendis olabileceklerini soruyor.

Bu sayfa her bağlantıyı/kitabı/kursu içeremez. Örneğin bu sayfada Arduino tanıtılmaktadır ancak Arduino ve gömülü sistemler hakkında detaylı bilgi bulunmamaktadır. Kendin daha fazlasını araştırmalısın. Başlayabileceğiniz "Arduino" anahtar kelimesine sahipsiniz. Yani bir sonraki adımınız muhtemelen Arduino'yu araştırmak, bir Arduino geliştirme seti(kit) satın almak ve kendiniz için bir şeyler yapmaktır, bağlantı veya kitap toplamak değil. Lütfen bu sayfanın yeni başlayanlar için bir yol haritası olduğunu unutmayın.

Düşük seviyeli programlama, bilgisayar biliminin bir parçasıdır.
Öncelikle bilgisayar bilimi için eğitim almak kesinlikle çok daha iyi olacaktır.
* [Bilgisayar Bilimleri alanında ücretsiz bir eğitime giden yol!](https://github.com/ossu/computer-science)


## <a name="Düşük-Seviye-nedir"></a>Düşük Seviye nedir?

Düşük seviyeli programlamayı, C veya Assembly gibi daha düşük seviyeli bir programlama dili kullanarak makineye çok yakın olan programlama olarak sınıflandırıyorum. Bu, yüksek seviyeli diller (örn. Python, Java) kullanan tipik kullanıcı alanı(userspace ve kernelspace kavramlarına bakınız) uygulamaları olan üst düzey programlamanın tersidir.
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language)

Evet, sistem programlama, düşük seviyeli programlamaya çok yakın bir kavramdır. Bu sayfa, sistem programlamasına dahil olmayan donanım tasarımını ve ürün yazılımı geliştirmeyi içerir.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Son olarak, bu sayfa donanım bileşenlerinden Linux çekirdeğine kadar değişen konuları içerir. Bu, çok çeşitli katmanlardır. Tek sayfalık bir belge hiçbir zaman tüm katmanların ayrıntılarını kapsamaz, bu nedenle bu belgenin amacı, düşük seviyeli programlama için bir başlangıç ​​noktası olarak hizmet etmektir.

##  <a name="Teori"></a>Teori

Düşük seviyeli programlamanın iki temel teorisi vardır:
* Bilgisayar Mimarisi
* İşletim Sistemleri

Bence teori öğrenmenin en iyi yolu bir kurs almaktır. Kitap okumak fena değil ama çok zaman ve çaba gerektiriyor. Coursera.org ve edx.org gibi çevrimiçi üniversitelerde birçok iyi kurslar bulabilirsiniz. Teorik bilgi ile gerçeği yani pratik kodlama becerisini ayırt etmek gerekir. Sınıfta A+ almanız gerektiğini düşünmüyorum, sadece büyük resmi görün. Tecrübe ile gün geçtikçe daha iyi olacaksınız.

Okuduğum birkaç kitabı tanıtmama izin verin. Genellikle üniversitelerde ders kitabı olarak kullanılırlar. Üniversitenizde bu kitapların olduğu bir sınıf yoksa, onları okumak için biraz zaman ayırmaya değer.

* Bilgisayar Mimarisi
  * Computer Architecture, Fifth Edition: A Quantitative Approach
  * Computer Systems: A Programmer's Perspective
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* İşletim sistemleri
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System
  * Operating Systems: Internals and Design Principles by William Stallings
* Önerilen Kurslar
   * [CS401: Operating Systems from saylor.org](https://learn.saylor.org/course/view.php?id=94)
* Genel Programlama Bilgisi
   * [Structure and Interpretation of Computer Programs](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs)
      * Bu nasıl iyi bir Yazılım Geliştirici olacağınızla alakalı. Sadece teoriğe değil tekniğe de ihtiyacınız var çünkü programlama bir tür el işidir.
      * Eğer Lisp/Scheme öğrenirseniz, diğer programlama dillerini daha kolay öğrenebilirsiniz.
      * [Egzersizlerin yaklaşık %80'ini çözdüm. Çözdüğüm her bir egzersize değdi.](https://github.com/gurugio/sicp_exercise)
* Donanım Tasarımı
   * Kendi 8086 Mikroişlemci kitinizi geliştirin.
      * Eğer kendi donanım kartınızı geliştirmeyecekseniz, fiziksel bellek eşlemeli cihaz(physical memory mapped device)'ın ne olduğunu anlamayacaksınız.
      * Günümüzde işlemcilerin(AP - Application Processors) artık çok fazla akıllı özellikleri(Intellectual Properties) var. Bu yüzden bir işlemcinin çekirdeği ve çevre cihazların(peripheral devices) nasıl bağlı olduklarını bilemeyeceksiniz.
      * Kendi 8086 kitinizi geliştirirken, her bir çevre cihazı fiziksel hafızaya yerleştirme imkanınız var. Ve ana donanım cihazlarının(BUS, IRQ, Clock, Power vb.) nasıl çalışacağını kendi gözlerinizle ayarlayabilirsiniz.
      * Kendi 8086 kitimi üniversitede geliştirmiştim. Aldığım en değerli derslerden biriydi, kendi donanım kitini yap. Eğer donanım eski ve basit olursa daha iyi çünkü ayarlamalar için daha fazla uğraşırsınız.
      * İnternette "8086 kit" diye aratın. Donanım şemasını, parçalarını ve kılavuzlarını belli başlı internet sitelerinden alabilirsiniz.

Sayısız iyi kitap listesi var. Çok kitap okumalısın demek istemiyorum. Sadece bir kitabı dikkatlice okuyun. Ne zaman bir teori öğrenirseniz, onun kodunu uygulayın.
**Bir şeyi uygulamak, yüz teori bilmekten daha iyidir.**

##  <a name="Diller"></a>Diller

### <a name="Assembly"></a>Assembly

X86 veya ARM arasından birini seçin. İkisini de bilmenize gerek yok. Assembly dilini bilmek önemli değil. Önemli olan bir CPU ve bilgisayarın içini(işleyiş) anlamaktır. Böylece en yeni CPU'nun assembly dilini yazmanıza gerek kalmaz. 8086 veya Cortex-M'yi seçin.

* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
  * CPU ve bilgisayar mimarisinin temel kavramları
  * C programlama dilinin temel kavramları
* [64bit assembly programming(translation in progress)](https://github.com/gurugio/book_assembly_64bit)
  * modern CPU ve bilgisayar mimarisinin temel kavramları
  * C kodunun disassemble edilmesi ve hata ayıklaması ile ilgili temel kavramlar
  * _need help for translation_
* [Learning assembly for linux-x64](https://github.com/0xAX/asm)
  * NASM ile saf 64-bit Assembly programlama ve GCC ile inline Assembly
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * ARM programlamada eksiksiz referans
* Bilgisayar Organizasyonu ve Tasarımı
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * [RISC-V Edition](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757)
  * Bir bilgisayarın her bileşeninin sıfırdan nasıl çalıştığını açıklayan akademik kitaplar.
  * Bilgisayar mimarisini oluşturan farklı kavramları ayrıntılı olarak açıklar.
  * Belirli bir Assembly dilinde uzmanlaşmak isteyen okuyucuları hedef almazlar.
  * MIPS ve ARM sürümü aynı konuları kapsar, ancak farklı bir mimariyi inceler.
  * Her iki sürüm de x86 dünyasındaki örnekleri içerir

### <a name="C-dili"></a>C dili

Kestirme ve hızlı bir yol bulunmuyor. Sadece kitabın tamamını okuyun ve tüm alıştırmaları çözün. 

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * Yeni C standardı için
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * C dili ile raw uyarlanması ve senkronizasyonu
  * Büyük ölçekli C programlama için gerekli (özellikle çekirdek programlama için)
* [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * Bir veya iki C programlama kitabını okumayı bitirirseniz, bir şeyler yapmanız GEREKİR.
  * Ne istersen onu seç.
  * Önce kendi başınıza yapın ve ardından başka birinin kaynak koduyla karşılaştırın. Kaynağınızı ve diğerlerini karşılaştırmak çok önemlidir. Becerinizi ancak diğerinin kaynağını okuduğunuzda ve daha iyi yöntemler öğrendiğinizde geliştirebilirsiniz. Kitaplar ölüdür ve kaynak kodlar yaşayan kaynaklardır.
* [C and other languages based projects](https://github.com/danistefanovic/build-your-own-x)
  * daha ilginç projeler bulun
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * C ve biraz da x86 Assembly ile optimizasyon hakkında referans
  * 8088'den bugüne kadar
  * Düşük Seviyeli grafik optimizasyonuna özel odaklanın
* [Framework and plugin design in C](https://github.com/gurugio/book_cprogramming)
  * Büyük ölçekli yazılımlar için C'de çerçeve ve eklenti nasıl geliştirilir
  * Linux çekirdek kaynak okuma için çok temel programlama ipuçları

C programlama uzmanı olmak istiyorsanız, https://leetcode.com/ sitesini ziyaret edin. İyi Şanslar!


### <a name="Rust-dili"></a>Rust dili

Sistem programlama için bir sonraki dilin Rust olacağına eminim.
Rust öğrenirken yaptıklarımı bir liste haline getireceğim.

[Linus Torvalds said "Unless something odd happens, it [Rust] will make it into 6.1."](https://www.zdnet.com/article/linus-torvalds-rust-will-go-into-linux-6-1/)

* [The Rust Programming Language](https://doc.rust-lang.org/book/)
  * Güzel bir giriş, ancak eksik örnek ve alıştırmalar.
* [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
  * "The Rust Programming Language"'i okurken, buradan örnek ve alıştırmalar bulabilirsiniz.
  * Ama kendinizin yapabileceği yeteri kadar alıştırma yok. Sadece bazı örneklerde "kendin-yap" alıştırmaları var ve onlarda çok basit.
* [Programming Rust, 2nd](https://www.oreilly.com/library/view/programming-rust-2nd/9781492052586/)
  * Daha derin bir giriş, ama hala örnek ve alıştırmalardan yoksun.
* [Exercism](https://exercism.org/tracks/rust)
  * RUST'ın kendine has özelliklerini öğrenmek için güzel alıştırmalar.
  * Mentörlerin aktif olarak çalışıp çalışmadığını bilmiyorum ama çözümüzü diğerleriyle karşılaştırmak için yeterli.
    * Çözümünüzü gönderdikten sonra, başkalarının çözümlerini "Community solutions" sekmesinde görebilirsizin (Exercism V3'den sonra geçerli).
    * Map/filter/any ve vb. fonksiyonel özellikler için çok sayıda giriş seviyesinde alıştırma.
* [Easy rust](https://dhghomon.github.io/easy_rust/)
  * Basit bir İngilizce ile yazılmış bir kitap.
  * Youtube kaynakları: https://www.youtube.com/playlist?list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk
* [Let's get rusty](https://www.youtube.com/c/LetsGetRusty)
  * Youtube'da çok fazla Rust eğitimi yayınlayan var ama ben en çok bu eğitimi sevdim.
  * Rust hakkında son gelişmeleri yayınlıyor. Abone olmaya değer.
* [Rust for Linux](https://github.com/Rust-for-Linux)
  * Örnek kaynakları inceleyin ve Rust'ın Linux Çekirdeğine nasıl girdiğini görün.


## <a name="Çalışma-Alanları"></a>Çalışma Alanları

### <a name="Donanım-Firmware"></a>Donanım && Firmware

Gömülü sistem mühendisi olmak istiyorsanız, en son ARM yonga setiyle başlamak yerine basit bir donanım geliştirme setinden(kitinden) başlamak en iyisi olacaktır.

* [Arduino Başlangıç Kiti](https://www.arduino.cc/)
  * Birçok Arduino serisi vardır, ancak "Arduino Başlangıç ​​Kiti" en basit işlemciye (Atmega328P) ve kılavuz kitabına sahiptir.
  * Atmega328P, dijital devre tasarımına ve aygıt yazılımı geliştirmeye başlamak için iyi bir yer olan 8 bitlik bir çekirdeğe sahiptir.
  * Şemaları ve düzenleri nasıl çizeceğinizi ve çipleri nasıl monte edeceğinizi bilmenize gerek yok.
  * Ancak şemaları nasıl okuyacağınızı bilmeniz ve çiplerin nasıl bağlandığını anlamanız gerekir.
  * Firmware geliştiricileri, şemaları okuyabilmeli ve verileri hedef cihaza nasıl göndereceklerini bulabilmelidir.
  * Kılavuzu takip edin!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * X86 mimarisine yeni başlayan biriyseniz, 8086 işlemci mimarisi ve 80x86 derlemesi için de çok iyi bir kılavuzdur.
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * 80x86 işlemcinin korumalı modu ve sayfalama mekanizması için en iyi kılavuz
  * Web sürümü: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

Bu noktada, en son ARM veya x86 işlemciye başlamanız gerekir.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Örneğin, Raspberry Pi kartında 64-bit komut setini destekleyen bir Cortex-A53 İşlemci bulunur.
Bu, RPi ile modern bir işlemci mimarisi deneyimlemenizi sağlar.
Evet, satın alabilirsin ... ama ... onunla ne yapacaksın?
Hedef projeniz yoksa, RPi kartı'nı bir çekmeceye atmanız ve daha önce satın almış olabileceğiniz diğer araçlar gibi unutmanız muhtemeldir.

Bu yüzden size aşağıdaki projeleri öneriyorum.
* [Making your own kernel](http://wiki.osdev.org/Getting_Started)
  * İyi referanslar: https://www.reddit.com/r/osdev/
* [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
  * (projenin açıklaması) Bu depo, basit bir işletim sistemi (OS) çekirdeğinin sıfırdan nasıl oluşturulacağını öğreten adım adım bir kılavuz içerir ... (atla) ... Her ders öyle tasarlandı ki önce bazı çekirdek özelliğinin RPi işletim sisteminde nasıl uygulandığını açıklar ve ardından aynı işlevselliğin Linux çekirdeğinde nasıl çalıştığını göstermeye çalışır.



64 bit long modu, sayfalamayı ve çok basit bağlam değiştirmeyi(context switching) destekleyen [basit bir kernel](https://github.com/gurugio/caos) yazdım. Basit bir çekirdek(kernel) yapmak, modern bilgisayar mimarisini ve donanım kontrolünü anlamak için güzel bir yoludur.

Aslında, en son işlemciye ve en son donanım cihazlarına zaten sahipsiniz.
Dizüstü bilgisayarın! Masaüstü bilgisayarınız! Başlamak için ihtiyacınız olan her şeye zaten sahipsin!
Hiçbir şey almanıza gerek yok.
QEMU emülatörü, en yeni ARM işlemcileri ve Intel işlemcileri sanal ortamında çalıştırabilir.
Yani ihtiyacınız olan her şey elinizin altında.
Başvurabileceğiniz birçok basit çekirdekler ve kılavuzlar var.
Sadece QEMU'yu kurun ve sadece ayağa kalkan(boot), sayfalamayı(paging) açan ve bazı mesajları yazdıran küçük bir çekirdek yapın.

Diğer basit çekirdekler(kernel):
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-çekirdeği-ve-aygıt-sürücüleri"></a>Linux çekirdeği and aygıt sürücüleri

Tam bir işletim sistemi oluşturmanıza gerek yok.
Linux topluluğuna katılın ve geliştirmeye ortak olun.

* Linux Çekirdeği ve Aygıt Sürücüleri(driver) ile ilgili başlangıç ​​seviyesinden ileri seviyeye bazı kaynaklar.
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * UNIX'in temel kavramları tüm işletim sistemlerine uygulanır.
    * Bu kitap, işletim sistemlerinin temel kavramlarını öğrenmek için çok iyi bir yerdir.
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Kendiniz için tüm örnekleri yapın
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Linux Kernel'in tasarımını anlayın
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Bu kitabı ve v2.6 çekirdek kaynağını aynı anda okuyun
    * Asla en son sürümle başlamayın, v2.6 yeterlidir!
    * Çekirdek kaynağını satır satır çalıştırmak için qemu ve gdb'yi kullanın
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * Önyüklemesi yalnızca bir saniye süren en basit dosya sistemini yapmak için busybox kullanın
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Diğer kaynaklar: Önerdiğim kaynaklar
  * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * Linux aygıt sürücülerini temel çekirdek API'leri ile yapan pratik kılavuz ve mükemmel alıştırmalar
    * Bu belgenin neredeyse tüm temel çekirdek API'lerini tanıttığını düşünüyorum.
  * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
    * Ne yazık ki, bu meydan okuma yeni meydan okuyanları kabul etmiyor çünkü artık zorluk yok._ Bakımcı yeni bir format planladığını söyledi. Umarım en kısa zamanda geri gelir.
      * Ancak sorunun sorularını Google ile bulabilirsiniz. Bazı insanlar yaptıklarını zaten yükledi. Soruları bulun ve kendi başınıza çözmeye çalışın ve çözümünüzü diğerleriyle karşılaştırın.
    * Bu, size ne yapmanız gerektiği konusunda rehberlik eden harika bir özel öğretmen gibidir.
    * Ne yapacağınızı bilmiyorsanız, hemen başlayın.
  *  [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
     * Bu proje henüz tamamlanmadı.
     * Her zaman Linux çekirdeğine benzer bir çekirdek yapmanın Linux çekirdeğini anlamanın en iyi yolu olduğunu düşünüyorum.
  * [Block layer and device driver](https://github.com/gurugio/book_linuxkernel_blockdrv) 
    * multi-queue mode ile basit bir blok sürücüsü örneğinden (Ramdisk) başlayın
    * blok katmanına bakın
    * İngilizceye çeviriyi tamamladım. Lütfen bana geri bildiriminizi gönderin.
  * [md driver of Linux kernel(Korean)](https://github.com/gurugio/book_linuxkernel_md)
    * mdadm aracı nasıl çalışır ve md sürücüsünü nasıl çağırır
    * md sürücüsü nasıl çalışır

#### <a name="Referanslar"></a>Referanslar

Bir şeye ihtiyacınız olduğunda kontrol edeceğiniz kaynaklardan:

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * iyi konuları, özellikle ARM-linux'u tanıtan birçok slayt dosyasıdır.
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * çekirdek programlamaya başlama kılavuzudur.

### <a name="Diğer-Çalışma-Alanları"></a>Diğer Çalışma Alanları

Evet, Linux veya firmware geliştirmeyle ilgilenmeyebilirsiniz. Öyleyse, başka çalışma alanları bulabilirsiniz:
* Windows sistem programlama & aygıt sürücüleri(driver)
* Bilgi Güvenliği(Security)
* Tersine Mühendislik

Bu çalışma alanları hakkında hiçbir bilgim yok. Lütfen yeni başlayanlar için yararlı olabilecek bu dosyanın formatına uygun içerikleri gönderin.

**Çekirdekler ve sürücüleri, düşük seviyeli programlamanın tamamı değildir.** Düşük seviyeli programlamanın bir diğer önemli çalışma alanı, yazılım tanımlı depolama veya dağıtık dosya sistemidir. Bunların ayrıntılı açıklamaları bu belgenin kapsamı dışındadır ancak basit bir dağıtık dosya sistemini deneyebileceğiniz mükemmel bir kurs vardır.
* Ders: https://pdos.csail.mit.edu/archive/6.824-2012/
* Referans'ın kaynağı: https://github.com/srned/yfs

## <a name="Düşük-Seviyeli-Programlamanın-Geleceği"></a>Düşük Seviyeli Programlamanın Geleceği

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

* İşletim sistemi teorisi kitapları okumak: en azından "The Design of the UNIX Operating System by Maurice J. Bach" okumalısınız.
* Assembly ve C programlama dillerini öğrenmelisiniz.
  * [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * Assembly programlama dilini okuyup anlayabiliyorsanız yeterlidir. Pratik bir şey yapmanıza gerek yoktur.
  * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
    * Her alıştırmayı çözmek için elinizden gelenin en iyisini yapın!
  * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* C ile pratik bir şeyler yapın
  * [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): Find one or two interesting projects and make your own project.
  * [leetcode.com](https://leetcode.com/): İlginç bir proje bulamazsanız, veri yapısı ve algoritmaya odaklanmak da iyi olacaktır.
* Bir donanım projesi yapın
  * Raspberrypi veya Arduino arasında bir tercih yapmanız önemli değildir. Bir donanımı doğrudan yalnızca C ile kontrol etmek için bir deneyime ihtiyacınız var YALNIZCA C ile!
  * Bir ATmega128 geliştirme seti(kiti) satın almanızı ve LED'leri açmak/kapatmak, anahtar girişini algılamak ve metin LCD'sinde mesaj görüntülemek için bir aygıt yazılımı yapmanızı öneririm. Motor kontrol programı da çok iyi bir projedir: örneğin, çizgi izleyici.
  * Herhangi bir yazılım kütüphanesi KULLANMAYIN. Program indiricisi dışında her şeyi kendi başınıza yapmalısınız.
* Linux Çekirdeğinin Temelleri
  * Düşük seviyeli programlama, işletim sistemine çok yakındır. İşletim sisteminin işleyişini bilmelisiniz.
  * Donanım aygıt sürücüleriyle başlayınız
    * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/) belgelerini okuyunuz.
  * Linux Çekirdeğinin işleyişini anlamak için [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) kitabını okuyunuz.
* Profesyonelleşmek için
  * Profesyonel Linux Çekirdek Geliştiricisi olmak istiyorsanız
    * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel) okumalısınız.
      * Sonra kendinize basit bir çekirdek yazın.
      * [Learn operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
      * [Making your own kernel](http://wiki.osdev.org/Getting_Started)
      * Özgeçmişinizde kendi çekirdeğinizin github linkini koyun (Commit mesajlarına detaylı bilgi yazmayı unutmayın.)
    * https://lwn.net/ sitesindeki son sorunları(issue) inceleyin ve çözüme katılın.
      * "Güncel çekirdek yamaları"'nı "https://lwn.net/Kernel/" veya direkt "https://lwn.net/Kernel/Patches" üzerinden kontrol edin.
      * Kendinize ilginç bir yama bulun. Kaynak kodu anlamaya çalışın. Tabii ki bunu yapmak zor olacak ama deneyin. Her denediğinizde adım adım yaklaşacaksınız.
      * Çekirdek geliştirin ve kendi sisteminizde test edin. TLP(https://linux-test-project.github.io/) ile örneğin performans testi, stabilite testi yapın veya statik kod analizi yapın.
      * Eğer herhangi bir problem bulursanız: derleme uyarıları/hataları, performans düşüsü, kernel panic/oops veya herhangi bir problemi bildirin.
      * Eğer sorunsuz çalışırsa, bunu sistem özelliklerinizle beraber raporlayın. Yama sahibi "Reviewed-by" etiketi ile sizin adınızı yazar.
      * Kendi adınızı çekirdeğin git belgelerinde(log) bulun.
  * Veya başka alanlar bulun
    * Düşük seviye mühendislerin çalışabileceği çok fazla alan var: güvenlik, derleyici(compiler), donanım yazılımı(firmware), robotlar/arabalar diye gidiyor...
    

# <a name="Çeviriler"></a>Çeviriler

Bu sayfayı çevirmek istiyorsanız lütfen düzenleme talebi(pull request) gönderin. Burada listeleyeceğim.
* [Chinese (Traditional)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tw.md)
* [Chinese (Simplified)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [Portuguese (Brazilian)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_pt.md)
* [Italian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)
* [Czech](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cz.md)
* [Russian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_ru.md)
* [Turkish](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tr.md)
* [Persian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_fa.md)
* [Spanish](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_es.md)
* [French](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_fr.md)

# <a name="Ben-Kimim"></a>Ben Kimim?

Bu yazıyı [google-interview-university](https://github.com/jwasham/coding-interview-university)'den esinlendim. Deneyimlerimi paylaşmak ve düşük seviyeli kod yazan bir programcı olma yolunda bir yol haritası göstermek istiyorum çünkü bu becerilerin eskisi kadar yaygın olmadığını anladım. Ek olarak, birçok öğrenci ve yeni başlayanlar bana nasıl düşük seviyeli kod yazan programcılar ve Linux çekirdek kodu yazan bir mühendis olabileceklerini soruyor.

Bilmenizi isterim ki düşük seviyeli kod yazan bir programcı olarak 10 yıldan fazla kod yazma deneyimine sahibim:
* 80x86 platformunda Assembly programlama
* ATmel çipli ve firmware'lı donanım cihazı
* UNIX için C ile sistemi programlama çalışması
* Linux'ta aygıt sürücüsü
* Linux çekirdeği: sayfa ayırma(page allocation)
* Linux çekirdeği: blok aygıt sürücüsü ve md modulü
