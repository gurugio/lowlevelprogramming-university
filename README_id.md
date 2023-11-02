CATATAN1: Mohon untuk tidak menyalin konten pada halaman ini untuk blog anda. Anda bisa membagikan halaman ini tapi mohon untuk menyertakan link asli. Itu adalah cara kita untuk mengapresiasi penulis dari proyek-proyek dokumentasi dan open source yang baik.

CATATAN2: Mohon untuk dicatat bahwa pemrograman tingkat rendah sudah ketinggalan zaman dan saat ini tidak banyak perusahaan yang mempekerjakan pengembang bahasa tingkat rendah. Dari hari ke hari semakin sulit untuk saya mencari pekerjaan di bidang ini. Jika anda masih belum memulai karir profesional, saya ingin menyarankan Anda mempertimbangkan bidang lain dengan hati-hati.

CATATAN3: Jika anda ingin langsung mulai, silahkan ke bagian "How to start?".

* [Low-Level Programming University](#Low-Level-Programming-University)
  * [Apa itu?](#What-is-it)
  * [Apa yang dimaksud dengan Low-Level?](#What-Is-the-Low-Level)
  *  [Teori](#Theory)
  *  [Bahasa](#Languages)
     * [Assembly](#Assembly)
     * [Bahasa C](#C-language)
     * [Bahasa Rust](#Rust-language)
  * [Pengaplikasian](#Applications)
    * [Perangkat Keras && Firmware](#Hardware-Firmware)
    * [Linux kernel and device driver](#Linux-kernel-and-device-driver)
      * [Referensi](#References)
    * [Pengaplikasian lain](#Other-applications)
  * [Masa depan pemrograman tingkat rendah](#Future-of-low-level-programming)
  * [Cara memulai?](#How-to-start)
* [Terjemahan](#Translation)
* [Tentang Saya?](#who-am-i)

# Low-Level Programming University

## <a name="What-is-it"></a>Apa itu?

Saya terinspirasi oleh [google-interview-university](https://github.com/jwasham/coding-interview-university). Saya ingin membagikan pengalaman dan menunjukkan roadmap untuk menjadi programmer low-level karena saya menemukan bahwa keterampilan ini tidak lagi umum seperti dulu. Selain itu,  banyak pelajar dan pemula bertanya kepada saya bagaimana mereka bisa menjadi programmer low-level dan Linux kernel engineers.

Halaman ini tidak bisa menyertakan setiap tautan/buku/course. Contohnya, halaman ini memperkenalkan Arduino walaupun tidak ada informasi mendetil tentang Arduino dan sistem tertanam. Anda harus mengeksplorasinya sendiri.Anda sudah memiliki kata kunci "Arduino" sehingga anda bisa langsung memulai untuk mengeksplorasinya. Jadi untuk langkah selanjutnya adalah mungkin bisa mulai dengan "googling" tentang Arduino, membeli satu set alatnya, dan membuat sesuatu untuk diri anda sendiri, bukan mengumpulkan tautan-tautan dan buku-buku gratis. Mohon untuk diingat bahwa halaman ini hanyalah sebuah roadmap untuk pemula.

Pemrograman Low-level adalah bagian dari ilmu komputer.
Tentu saja akan lebih baik untuk memperoleh edukasi di ilmu komputer terlebih dahulu.
* [Jalan menuju pendidikan otodidak gratis di bidang Ilmu Komputer!](https://github.com/ossu/computer-science)


## <a name="What-Is-the-Low-Level"></a>Apa yang dimaksud dengan Low-Level?

Saya mengelompokkan pemrograman low-level sebagai pemrogaman yang sangat dekat ke mesin, menggunakan sebuah bahasa tingkat yang lebih rendah seperti C atau Assembly. Ini berlawanan dengan bahasa pemrograman yang lebih tinggi, seperti aplikasi pengguna pada umumnya, menggunakan bahasa tingkat tinggi (contoh: Python, Java).
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language)

Ya, pemrograman sistem adalah sebuah konsep yang sangat dekat dengan pemrograman low-level. Halaman ini berisi tentang perancangan perangkat keras dan pengembangan firmware yang tidak termasuk dalam pemrograman sistem.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Terakhir, halaman ini mencakup topik mulai dari komponen perangkat keras hingga kernel Linux. Itu adalah cakupan lapisan yang sangat banyak. Satu halaman dokumen tidak akan pernah cukup untuk mencakup detil-detil dari semua lapisan, jadi tujuan dari dokumen ini adalah sebagai titik mula untuk pemrograman low-level.

##  <a name="Theory"></a>Teori

Ada dua latar belakang teori pada pemrograman low-level:
* Arsitektur Komputer
* Sistem Operasi

Menurut saya cara terbaik untuk belajar teori adalah dengan mengikuti course. Membaca buku bukan hal yang jelek juga, tetapi terlalu memakan banyak waktu dan tenaga. Anda bisa menemukan banyak kelas-kelas bagus pada kuliah online, contohnya, Coursera.org dan edx.org. Teori hanyalah teori. Saya tidak berpikir anda perlu dapat nilai A+ di kelas, cukup mengerti secara garis besar saja. Anda akan semakin baik seiring dengan pengalaman.

Izinkan saya untuk memperkenalkan buku-buku yang pernah saya baca. Secara umum digunakan sebagai buku teks di universitas-unversitas. Jika tidak ada buku-buku tersebut di universitas anda, dianjurkan untuk meluangkan waktu anda untuk membacanya.
* Arsitektur Komputer
  * Computer Architecture, Fifth Edition: A Quantitative Approach
  * Computer Systems: A Programmer's Perspective
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* Sistem Operasi
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System
  * Operating Systems: Internals and Design Principles by William Stallings
* Course yang Direkomendasikan
   * [CS401: Operating Systems from saylor.org](https://learn.saylor.org/course/view.php?id=94)
* Keterampilan Pemrograman Umum
   * [Structure and Interpretation of Computer Programs](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs)
      * Berisi tentang bagaimana cara menjadi pemrograman perangkat lunak yang baik. Anda bukan hanya butuh teori tapi juga teknik karena pemrograman adalah hal semacam kerajinan tangan (craftworks).
      * Jika anda mempelajari Lisp/Scheme, anda seharusnya sudah bisa belajar bahasa lain dengan cepat. 
      * [Saya telah menyelesaikan sekitar 80% latihan. Dianjurkan untuk mencoba setiap latihan yang ada](https://github.com/gurugio/sicp_exercise)
* Perancangan Perangkat Keras
   * Membangun 8086 Microprocessor Kit Anda Sendiri
      * Jika anda tidak membangun papan HW (Hardware) anda sendiri, anda tidak memahami apa itu perangkat yang dipetakan memori fisik.
      * AP modern memuat banyak sekali IP. Jadi anda tidak memiliki kesempatan untuk memahami bagaimana inti CPU dan perangkat periferal dihubungkan.
      * Saat anda membangun 8086 kit anda sendiri,  anda memiliki kesempatan untuk menempatkan tiap perangkat-perangkat periferal pada memori fisik. Dan anda sekarang bisa atur bagaimana komponen HW utama (BUS, IRQ, Clock, Power, dan lain-lain) bekerja dengan mata Anda sendiri.
      * Saya membangun 8086 kit di universitas. Itu adalah salah satu course yang paling berharga yang pernah saya ambil. Cobalah untuk membangun HW kit anda sendiri. Akan lebih baik jika perangkat kerasnya lebih tua dan lebih simple karena anda harus melakukan hal lebih extra untuk anda sendiri.
      * Coba ketik di Google "8086 kit". Anda seharusnya akan bisa menemuan beberapa situs web dimana anda bisa membeli sebuah skema HW, parts, dah panduannya.
      
Ada banyak daftar buku-buku yang bagus. Saya tidak menyebutkan anda harus baca banyak buku. Cukup baca satu buku dengan teliti. Kapanpun anda belajar sebuah teori, implementasikan kode simulasinya. **Mengimplementasikan satu hal lebih baik daripada mengetahui seratus teori**

##  <a name="Languages"></a>Bahasa

### <a name="Assembly"></a>Assembly

Pilih satu antara x86 atau ARM. Tidak perlu untuk tau keduanya. Tidak mengetahui bahasa assembly juga tidak masalah. Hal yang mendasar adalah memahami bagian internal dari sebuah CPU dan komputer. Jadi anda tidak perlu mempraktikkan assembly dari CPU terbaru. Pilih 8086 atau Corex-M.

* [8086 pemrograman assembly dengan emu8068](https://github.com/gurugio/book_assembly_8086)
  * konsep-konsep dasar CPU dan arsitektur komputer
  * konsep-konsep dasar bahasa pemrograman C
* [pemrograman assembly 64bit (terjemahan sedang dalam pengerjaan)](https://github.com/gurugio/book_assembly_64bit)
  * konsep-konsep dasar CPU modern dan arsitektur komputer
  * konsep-konsep dasar pembongkaran dan debugging kode C
  * _perlu bantuan untuk penterjemahan_
* [Belajar assembly untuk linux-x64](https://github.com/0xAX/asm)
  * pemrograman assembly 64-bit murni dengan NASM dan inline assembly dengan GCC
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * Referensi lengkap pada pemrograman ARM
* Organisasi dan Perancangan Komputer
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * [RISC-V Edition](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757)
  * Buku-buku akademis yang menjelaskan bagaimana tiap komponen dari sebuah komputer bekerja dari awal.
  * Penjelasan detil perbedaan konsep-konsep yang membentuk arsitektur komputer.
  * Buku tersebut tidak menargetkan ke para pembaca yang mengharapkan untuk mahir di bahasa assembly yang spesifik.
  * Edisi MIPS dan ARM mencakup topik-topik yang sama tapi membedah arsitektur yang berbeda.
  * Kedua edisi tersebut mengandung contoh-contoh di dunia x86.

### <a name="C-language"></a>Bahasa C
  
Tidak ada jalan pintas. Baca saja seluruh isi buku dan selesaikan semua latihan.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* Modern C: Jens Gustedt. Modern C. Manning, 2019, 9781617295812. ffhal-02383654f
  * Untuk standar C yang baru
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * implementasi mentah sinkronisasi dengan C
  * Sangat diperlukan untuk pemrograman C skala besar (terutama untuk pemrograman kernel)
* [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * Jika anda selesai membaca satu atau dua buku pemrograman C, kamu HARUS membuat sesuatu.
  * Pilih yang manapun yang anda sukai.
  * Pertama, buatlah kode anda sendiri lalu bandingkan dengan kode orang lain. Itu sangan penting untuk membandingkan sumber anda dengan yang lain. Anda bisa bisa meningkatkan skill hanya ketika anda membaca sumber lain dan belajar metode-metode yang lebih baik. Books are dead and source is live.
* [C and other languages based projects](https://github.com/danistefanovic/build-your-own-x)
  * temukan proyek-proyek menarik lainnya
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * Referensi optimisasi menggunakan C dan sedikit x86 assembly
  * Mulai dari 8088 hingga saat ini
  * Berfokus khusus pada optimisasi grafik tingkat rendah
* [Framework and plugin design in C](https://github.com/gurugio/book_cprogramming)
  * Cara mengembangkan framework dan plugin di C pada perangkat lunak skala besar
  * Tips-tips pemrograman yang sangat mendasar untuk membaca sumber kernel Linux

Jika anda ingin menjadi ahli pemrograman C, kunjungi https://leetcode.com/. Semoga beruntung!

### <a name="Rust-language"></a>Bahasa Rust

Saya meyakini bahwa bahasa pemrograman selanjutnya untuk pemrograman sistem adalah Rust.
Saya akan membuat daftar apa yang saya lakukan untuk belajar Rust.

[Linus Torvalds mengatakan Kecuali terjadi sesuatu yang aneh, [Rust] akan membuatnya menjadi 6.1."](https://www.zdnet.com/article/linus-torvalds-rust-will-go-into-linux-6-1/)

* [The Rust Programming Language](https://doc.rust-lang.org/book/)
  * Pengenalan yang bagus, namun kurang akan contoh dan latihan-latihan.
* [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
  * Ketika membaca "The Rust Programming Language", anda bisa menemukan contoh dan latihan-latihan di sini.
  * Namun tidak banyak latihan yang bisa Anda lakukan sendiri. Hanya beberapa contoh termasuk latihan "lakukan ini" dan latihan tersebut sangat mudah.
* [Programming Rust, 2nd](https://www.oreilly.com/library/view/programming-rust-2nd/9781492052586/)
  * Pengenalan yang lebih dalam, namun masih kurang akan contoh dan latihan-latihan.
* [Exercism](https://exercism.org/tracks/rust)
  * Latihan-latihan yang bagus untuk melatih fitur individu dari RUST.
  * Saya tidak yakin para mentor bekerja secara aktif namun itu seharusnya cukup untuk membandingkan solusi anda dengan solusi lain.
    * Setelah mengirimkan solusi anda, anda bisa melihat solusi orang lain dengan tab "Community solutions" (sejak Exercism V3).
    * Banyak latihan-latihan dengan level mudah adalah untuk fitur fungsional seperti map/filter/any dan lain-lain. 
* [Easy rust](https://dhghomon.github.io/easy_rust/)
  * Sebuah buku yang ditulis dengan bahasa inggris yang mudah.
  * Bahan ajar youtubed yang tersedia: https://www.youtube.com/playlist?list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk
* [Let's get rusty](https://www.youtube.com/c/LetsGetRusty)
  * Banyak Youtuber mengunggah kursus Rust namun saya paling menikmati kursus ini.
  * Dia telah mengunggah berita terbaru untuk Rust. Layak untuk disubscribe.
* [Rust for Linux](https://github.com/Rust-for-Linux)
  * Lihat sumber-sumber contoh dan cek bagaimana Rust akan masuk ke kernel Linux

## <a name="Applications"></a>Pengaplikasian

### <a name="Hardware-Firmware"></a>Hardware && Firmware

Jika anda ingin menjadi embedded system engineer, akan lebih baik untuk mulai dari sebuah hardware kit yang sederhana, daripada memulai dengan chipset ARM terbaru.

* [Arduino Start Kit](https://www.arduino.cc/)
  * Ada banyak seri dari Arduino namun "Arduino Start Kit" yang punya prosesor(Atmega328P) dan buku panduan yang paling sederhana.
  * Atmega328P memiliki 8-bit inti yang mana membuatnya jadi permulaan yang bagus untuk perancangan sirkuit digital dan pengembangan firmware.
  * Anda tidak perlu tahu cara menggambar skema dan tata letak serta merakit chip. 
  * Namun anda perlu tahu cara membaca skema dan memahami bagaimana chip saling terhubung.
  * Pengembang firmware seharusnya tahu cara membaca skema dan mencari tahu cara mengirim data ke perangkat target.
  * Ikuti buku panduan!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * Jika anda pemula pada arsitektur x86, 8086 juga panduan yang sangat bagus untuk arsitektur prosesor dan assembly 80x86
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Panduan terbaik untuk mode terproteksi dan mekanisme paging prosesor 80x86
  * Versi web: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

  Pada titik ini, anda sebaiknya mulai dengan prosesor ARM dan x86 terbaru.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Sebagai contoh, board Raspberry Pi memiliki prosesor Cortex-A53 yang mendukung set instruksi 64-bit.
Ini mengizinkan anda untuk merasakan arsitektur prosesor modern dengan rPi.
Ya, anda bisa membelinya... namun... apa yang akan anda lakukan dengan itu?
Jika anda tidak punya target proyek, anda kemungkinan besar akan membuang boardnya ke dalam laci dan melupakannya seperti gadget lain yang mungkin pernah anda beli sebelumnya.

Jadi, saya merekomendasikan satu proyek untuk anda.
* [Making your own kernel](http://wiki.osdev.org/Getting_Started)
  * Referensi bagus: https://www.reddit.com/r/osdev/
* [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
  * (deskripsi dari proyek) Repositori ini mengandung panduan langkah demi langkah yang mengajari cara membuat sebuah kernel sistem operasi (OS) sederhana dari awal...(skip)...Setiap pelajaran dirancang sedemikian rupa sehingga pertama-tama menjelaskan bagaimana beberapa fitur kernel diimplementasikan di OS RPi, dan kemudian mencoba mendemonstrasikan cara kerja fungsi yang sama di kernel Linux.


Saya telah membuat [kernel mainan](https://github.com/gurugio/caos) yang mendukung 64-bit long mode, paging dan context switching yang sangat sederhana. Membuat kernel mainan adalah cara yang bagus untuk memahami arsitektur komputer dan kontrol perangkat keras.

Faktanya, Anda sudah memiliki prosesor terbaru dan perangkat keras terbaru.
Laptop anda! Desktop anda! Anda telah memiliki semua yang anda perlukan untuk memulai!
Anda tidak perlu membeli apapun.
Emulator qemu dapat mengemulasi prosesor ARM dan prosesor Intel terbaru.
Jadi segala yang anda perlukan sudah ada di tangan.
Ada banyak kernel mainan dan dokumen yang dapat anda jadikan rujukan.
Install saja emulator qemu dan buatlah sebuah kernel kecil yang hanya booting, mengaktifkan paging, dan print beberapa pesan.

Kernel mainan lainnya: 
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Kernel Linux dan driver perangkat

Anda tidak perlu untuk membuat sebuah sistem operasi yang lengkap.
Bergabung ke komunitas Linux dan berpartisipasi di dalam pengembangan.

Beberapa sumber untuk pengembangan kernel Linux dan driver perangkat dari tingkat pemula ke tingkat lanjut.
* Buku-buku: Bacalah dalam urutan berikut
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * Konsep-konsep dasar dari Unix yang diaplikasikan ke dalam semua sistem operasi.
    * Buku ini adalah tempat yang sangat bagus untuk belajar konsep-konsep ini dari sistem operasi.
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Kerjakan semua contoh-contoh untuk diri anda sendiri
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Pahami perancangan kernel Linux
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Baca buku ini dan sumber kernel v2.6 sekaligus
    * Jangan pernah memulai dengan versi terbaru, v2.6 sudah cukup!
    * Gunakan qemu dan gdb untuk menjalankan sumber kernel baris demi baris
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md 
    * Gunakan busybox untuk membuat filesystem paling sederhana yang hanya butuh satu detik untuk booting
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Sumber-sumber lain: Sumber gratis yang saya rekomendasikan
  * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * Panduan praktis dan latihan luar biasa membuat driver perangkat Linux dengan API kernel penting
    * Menurut saya dokumen ini memperkenalkan hampir semua API kernel esensial.
  * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
    * _Sayangnya, challenge ini tidak menerima peserta challange baru karena tidak ada challange lagi._ Pengelola mengatakan dia sedang merencanakan format baru. Saya harap ini kembali secepatnya.
      * Namun anda bisa mencari pertanyaan-pertanyaan challange dengan Google. Beberapa orang telah mengunggah apa yang mereka telah lakukan. Cari pertanyaan-pertanyaan dan cobalah untuk menyelesaikannya sendiri, dan bandingkan solusi anda dengan orang lain.
    * Ini seperti guru privat luar biasa yang memandu Anda tentang apa yang harus dilakukan.
    * Jika Anda tidak tahu harus berbuat apa, mulailah saja.
  * [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
    * Proyek ini masih belum selesai.
    * Saya selalu berpikir membuat sebuah kernel yang mirip dengan kernel Linux adalah cara terbaik untuk memahami kernel Linux. 
  * [Block layer and device driver](https://github.com/gurugio/book_linuxkernel_blockdrv)
    * mulai dari contoh driver perangkat blok sederhana (Ramdisk) dengan mode multi-queue
    * maju ke lapisan blok
    * Saya menyelesaikan penerjemahan ke bahasa inggris. Silakan kirimkan tanggapan Anda kepada saya.
  * [md driver of Linux kernel(Korean)](https://github.com/gurugio/book_linuxkernel_md)
    * bagaimana tool mdadm bekerja dan cara dia memanggil driver md
    * bagaimana driver md bekerja
  * [A Heavily Commemted Linux Kernel Source Code](http://www.oldlinux.org/)
    * Komentar berat untuk Linux kuno v0.12.
    * Sebaiknya memulai dengan OS yang lama dan sederhana.
    * versi Unix: [Lions' Commentary on UNIX 6th Edition, with Source Code](https://en.wikipedia.org/wiki/Lions%27_Commentary_on_UNIX_6th_Edition,_with_Source_Code)

#### <a name="References"></a>Referensi

Periksa ketika anda memerlukan sesuatu

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * banyak file slide yang memperkenalkan topik-topik bagus, khususnya ARM-linux
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * panduan untuk memulai pemrograman kernel

### <a name="Other-applications"></a>Penerapan lain

Ya, anda mungkin tidak tertarik pada Linux atau firmware. Jika begitu, anda bisa menemukan penerapan lain:
* Pemrograman sistem Windows & driver-driver perangkat
* Security
* Reverse engineering

Saya tidak memiliki pengetahuan apapun tentang penerapan-penerapan tersebut. Silahkan kirimkan saya informasi apapun untuk pemula.

**Kernel dan driver tidak semuanya merupakan pemrograman tingkat rendah.** Satu lagi aplikasi penting dari pemrograman tingkat rendah adalah software-defined storage atau filesystem terdistribusi. Deskripsi detailnya diluar cakupan dari dokumen ini namun ada course bagus dimana anda bisa mencoba sebuah filesystem terdistribusi sederhana.
* Course: https://pdos.csail.mit.edu/archive/6.824-2012/
* sumber referensi: https://github.com/srned/yfs

## <a name="Future-of-low-level-programming"></a>Masa depan pemrograman tingkat rendah

Saya tidak tahu masa depan, namun saya terus memperhatikans Rust.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Jika saya bisa punya satu minggu bebas dan sendiri, saya akan belajar Rust.
Itu dikarenakan Rust ada adalah bahasa terbaru yang dapat saya gunakan untuk mengembangkan driver perangkat Linux.
* https://github.com/tsgates/rust.ko

IoT adalah tren baru, jadi ada baikny cek OS apa untuk IoT.
ARM, Samsung dan beberapa perusahaan memiliki realtime OS mereka masing-masing namun sayangnya banyak dari mereka adalah closed source.
Tetapu Linux Foundation juga memiliki sebuah solusi: Zephyr
* https://www.zephyrproject.org/

Server cloud pada mumnya memiliki banyak lapisan-lapisan; contohnya, OS host, driver kvm, proses qemu, OS guest dan service application. Sebuah container telah dikembangkan untuk menyediakan virtualisasi ringan. Dalam waktu dekat, konsep OS baru, yang disebut OS library atau Unikernel, akan menggantikan tumpukan SW untuk virtualisasi.
* http://unikernel.org/

Big data dan komputasi cloud membutuhkan penyimpanan yang semakin besar. Beberapa disk secara langsung ditanamkan di mesin server tidak memenuhi kebutuhan kapasitas, stabilitas dan performa. Oleh karena itu telah dilakukan penelitian untuk membuat sistem penyimpanan berukuran besar dengan banyak mesin penyimpanan yang dihubungkan oleh jaringan berkecepatan tinggi. Dulunya difokuskan untuk membuat satu volume penyimpanan yang besar. Namun saat ini mereka menyediakan banyak volume yang didedikasikan untuk banyak mesin virtual.
* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

## <a name="How-to-start"></a>Bagaimana cara untuk memulai?

Saya menerima sebuah email yang menanyakan cara untuk memulai. Ada banyak informasi tentang buku, course dan proyek di halama ini. Itu adalah kesalahan saya yang lupa untuk menulis bagaimana untuk memulai. Sayangnya, there is no King's Road to [King's Landing](https://gameofthrones.fandom.com/wiki/King%27s_Landing). Saya hanya akan menulis apa yang saya lakukan secara berurutan. Jika anda telah melakukan sesuatu, silahkan lewati saja. LAGI, ini hanya sebuah contoh yang anda bisa lakukan secara berurutan, untuk berjaga-jaga jika Anda tidak tahu bagaimana memulainya atau apa yang harus dilakukan.

* Membaca buku-buku teori OS: setidaknya "The Design of the UNIX Operating System by Maurice J. Bach"
* Belajar assembly dan C
  * [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * Itu cukup jika anda mengerti konsep dari pemrograman assembly. Anda tidak perlu untuk melakukan sesuatu yang praktikal.
  * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
    * LAKUKAN YANG TERBAIK untuk menyelesaikan semua latihan!
  *  [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Lakukan sesuatu yang praktikal dengan C
  * [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): Cari satu atau dua proyek menarik dan buat proyek anda sendiri.
  * [leetcode.com](https://leetcode.com/): Jika anda tidak bisa menemukan sebuah proyek yang menarik, sebaiknya juga fokus pada struktur data dan algoritma.
* Lakukan proyek hardware
  * RaspberryPi atau Arduino tidak masalah. Anda memerlukan pengalaman untuk mengontrol hardware secara langsung dengan C. HANYA C!
  * Saya merekomendasikan untuk membeli sebuah kit Atmega128 dan buat sebuah firmware untuk mnghidupkan/mematikan LED, mendeteksi input switch dan menampilkan pesan pada LCD teks. Program kontrol motor juga proyek yang sangat bagus: contohnya, line tracer (pelacak garis).
  * JANGAN menggunakan library apapun. Anda harus membuat semuanya sendiri, kecuali pengunduh program.
* Dasar dari kernel Linux
  * Pemrogaman tingkat rendah sangat dekat dengan sistem operasi. Anda harus tahu bagian dalam dari OS.
  * Mulailah dengan driver
    * Baca [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Baca [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) untuk memahami internal kernel Linux.
* Terjun ke bidang profesional
  * Jika anda mau menjadi seorang Developer Kernel Linxu profesional
    * harus baca [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
      * Lalu cobalah buat sebuah kernel mainan
      * [Learn operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
      * [Making your own kernel](http://wiki.osdev.org/Getting_Started)
      * Tulis tautan github kernel anda pada resume (Jangan lupa untuk menulis deskripsi detail dalam commit message)
    * Cek issue terbaru di https://lwn.net/ dan bergabunglah.
      * Cek "Recent kernel patches" pada "https://lwn.net/Kernel/" atau tautan langsung https://lwn.net/Kernel/Patches
      * Temukan patch yang menarik untuk anda. Cobalah untuk memahami kode sumber. Tentu saja akan sangat sulit namun cobalah. Anda akan semakin dekat setiap kali anda mencobanya.
      * Bangun kernel dan tes di sistem anda. Contohnya, tes performa, tes stabilitas dengan LTP(https://linux-test-project.github.io/) atau tool static code analysis di dalam kernel.
      * Laporkan masalah apapun jika anda menemukan: compile warnings/errors, performance drop, kernel panic/oops atau masalah apapun
      * Jika bekerja dengan baik, laporkan itu dengan spesifikasi sistem anda, Pemilik patch akan menulis sebuah tag "Direview oleh" dengan nama anda.
      * Temukan nama anda pada git log kernel.
  * Atau temukan topik lainnya
    * Ada banyak bidang di mana low-level engineer bisa bekerja: security, Compiler, Firmware, robot/mobil dan sebagainya

# <a name="Translation"></a>Terjemahan

Silahkan kirimkan saya pull request jika anda ingin menerjemahkan halaman ini. Saya akan mencantumkannya di sini.

* [Chinese(Traditional)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tw.md)
* [Chinese(Simplified)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [Portuguese (Brazilian)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_pt.md)
* [Italian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)
* [Czech](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cz.md)
* [Russian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_ru.md)
* [Turkish](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tr.md)
* [Persian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_fa.md)
* [Spanish](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_es.md)
* [Indonesian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_id.md)

# <a name="who-am-i"></a>Siapa saya?

Saya terinspirasi oleh [google-interview-university](https://github.com/jwasham/google-interview-university). Saya ingin membagikan pengalaman saya dan menunjukkan roadmap untuk menjadi pemrogram low-level karena saya menemukan bahwa keterampilan ini tidak seumum dulu. Selain itu, banyak pelajar dan pemula menanyakan kepada saya bagaimana mereka bisa menjadi pemrogram tingkat rendah dan engineer kernel Linux.

FYI, saya memiliki pengalaman lebih dari 10 tahun sebagai seorang pemrogram low-level:
* Pemrograman Assembly 80x86
* Perangkat hardware dengan chip Atmel dan firmware
* Pemrograman sistem Bahasa C untuk Unix
* Driver perangkat di linux
* Kernel Linux: page allocation
* Kernel Linux: driver block device dan modul md