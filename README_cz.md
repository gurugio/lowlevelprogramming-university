# PROSBA O POMOC!
Prosím informujte mě (ticketem nebo pomocí pull) jestli víte o nějakých dobrých odkazech na :
* **Programování Hardwaru firmwaru**
* **Qemu/KVM hypervisor**
* **Síťový zásobník jádra**

----
* [Univerzita nízkoúrovňového programování](#Low-Level-Programming-University)
  * [Co to je?](#What-is-it)
  * [Co to je nízkoúrovňové](#What-Is-the-Low-Level)
  *  [Teorie](#Theory)
  *  [Jazyky](#Languages)
     * [Assembly](#Assembly)
     * [Jazyk C](#C-language)
  * [Aplikace](#Applications)
    * [Hardware && Firmware](#Hardware-Firmware)
    * [Linuxové jádro a ovladač zařízení](#Linux-kernel-and-device-driver)
      * [Pečlivě prostudujte](#Follow-carefully)
      * [Odkazy](#References)
    * [Jiné aplikace](#Other-applications)
  * [Budoucnost nízkoúrovňového programování](#Future-of-low-level-programming)
* [Překlad](#Translation)
* [Kdo jsem?](#who-am-i)

# Univerzita nízkoúrovňového programování

## <a name="What-is-it"></a>Co to je?

Jsem inspirován [google-interview-university](https://github.com/jwasham/coding-interview-university). Rád bych se podělil o zkušenosti a ukázal cestu, jak se stát nízkoúrovňovým programátorem, protože jsem zjistil, že tyto dovednosti nejsou tak běžné jako byly kdysi. Navíc se mě mnoho studentů a začátečníků ptá, jak by se mohli stát nízkoúrovňovým programátorem a inženýrem Linuxového jádra.

Tato stránka nemůže obsahovat všechny odkazy/knihy/kurzy. Například tato stránka představuje Arduino, ale nejsou zde detailní informace o Arduinu a vestavěných systémech. Dál už musíte sami. Máte heslo "Arduino" se kterým můžete začít. Takže vaším dalším krokem bude pravděpodobně progooglování Arduina, a nakoupení sady a udělání něčeho samostatně a ne sbírání odkazů a knih co jsou zadarmo. Prosím mějte napaměti, že tato stránka je pouze plánek pro začátečníky.

## <a name="What-Is-the-Low-Level"></a>Co to je nízkoúrovňové?

Za nízkoúrovňové programování považuji takové programování, které má velmi blízko ke stroji, používání nízkoúrovňových jazyků jako C a assembly. Toto je v kontrastu s vysokoúrovňovým programováním, typickým pro aplikace uživatelského prostoru, používajícím vysokoúrovňové jazyky (např. Python, Java).
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language)

Ano, programování systémů má velmi blízko ke konceptu nízkoúrovňového programování. Tato stránka zahrnuje navrhování hardwaru a nasazování firmwaru, které systémové programování neobsahuje.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Takže tato stránka zahrnuje témata spadající mezi hardwarové komponenty a Linuxové jádro. To je velký rozsah různých rovin. Dokument o jedné straně nemůže nikdy pokrýt detaily každé z nich, a tak se tento dokument zaměřuje na to stát se odrazovým můstkem pro nízkoúrovňové programování.

##  <a name="Theory"></a>Teorie

Základní teorie pro nízkoúrovňové programování jsou dvě:
* Stavba (architektura) počítače
* Operační systémy

Myslím, že nejlepší cestou jak se naučit teorii je zúčastnit se kurzu. Čtení knih není špatné, ale zabere příliš mnoho času a úsilí. Můžete najít spoustu dobrých kurzů na online univerzitách, například na Coursea.org a edx.org.
Teorie je teorie. Nemyslím, že musíte obdržet nejlepší známku, jde o to udělat si obrázek.
Stále se budete zlepšovat zkušenostmi.

Nechte mě představit vám pár knih, které jsem přečetl. Běžně se používají jako skripta na univerzitách. Pokud nebude kurz s těmito knihami na vaší univerzitě, stojí za to přečíst si je.

* Počítačová architektura
  * Computer Architecture, Fifth Edition: A Quantitative Approach
  * Computer Systems: A Programmer's Perspective
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* Operační systémy
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System
  * Operating Systems: Internals and Design Principles by William Stallings
* Doporučené kurzy
   * [CS401: Operating Systems from saylor.org](https://learn.saylor.org/mod/page/view.php?id=921)

Existuje nepřeberné množství dobrých knih. Nechci tím říci, že by jste měli přečíst hodně knih. Hlavně přečtěte jednu důkaldně. Kdykoli se naučíte teorii, simultánně implementujte její kód. **Implementování jedné věci je lepší než znát jedno sto teorií.**

##  <a name="Languages"></a>Jazyky

### <a name="Assembly"></a>Assembly

Vyberte si jeden mezi x86 a ARM. Nemusíte znát oba. Nezáleží na tom znát assembly jazyk. Hlavní věcí je porozumění vnitřním procesů CPU a počítače. Takže nemusíte cvičit assemly posledních CPU. Vyberte si 8086 nebo Cortex-M.

* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
  * základní koncepty CPU a počítačové architektury
  * základní koncepty programovacího jazyka C
* [64bit assembly programming(na překladu ještě pracuji)](https://github.com/gurugio/book_assembly_64bit)
  * základní koncepty moderní CPU a počítačové architektury
  * základní koncepty převodu ze strojového kódu a opravování kódu v jazyce C
  * _potřebuji pomoci s překladem_
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * Kompletní reference o ARM programování
* Organizace počítače a design
  * [MIPS edice](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM edice](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * [RISC-V edice](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757)
  * Akademické knihy, které vysvětlují jak jednotlivé komponenty počítače pracují od základů.
  * Detailně vysvětlují rozdílné koncepty, které tvoří stavbu počítače.
  * nejsou určeny čtenářům, kteří se chtějí stát zdatnými v určitém assembly jazyku.
  * MIPS a ARM edice pokrývají ta samá témata, ale rozpitvávají rozdílné architektury.
  * Obě edice obsahují příklady ve světě x86.

### <a name="C-language"></a>Jazyk C

Tady neexistuje zkratka. Jen přečtěte jednu celou knihu a vyřešte všechny příklady.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * Pro nový standard C
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * hrubá implementace a synchronizace s C
  * Základy pro rozsáhlé C programování (zvláště pro programování jádra) 
* [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * Poté, co přečtete jednu či dvě knihy o programování v C, ihned MUSÍTE něco dělat.
  * Vyberte si, co chcete.
  * Nejdříve něco vytvořte a potom porovnejte s kódem někoho jiného. To je velmi důležité porovnávání vašeho zdrojového kódu s ostatními. Můžete zdokonalit vaše dovednosti pouze čtením cizího zdrojového kódu a učením se lepším metodám. Knihy jsou mrtvé, ale zdrojový kód živý.
* [Projekty založené na C a dalších jazycích](https://github.com/danistefanovic/build-your-own-x)
  * najděte si více zajímavých projektů
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * Reference na optimalizaci za použití C a části x86 assembly
  * Začíná 8088 a pokračuje až do současnoti
  * Speiálně se zaměřuje na nízkoúrovňovou grafickou optimalizaci

Chcete-li být expertem na programování v C, navštivte https://leetcode.com/. Hodně štěstí!

## <a name="Applications"></a>Aplikace

### <a name="Hardware-Firmware"></a>Hardware && Firmware

Jestli chcete být inženýrem vázaných systémů, nejlépe bude začít jednoduchou soupravou hardwaru, než začít s nejnovějším ARM chipsetem.

* [Arduino Start Kit](https://www.arduino.cc/)
  * K dispozici je mnoho sérií Arduina, ale "Arduino Start Kit" má nejjednodušší procesor(Atmega328P) a knihu návodů.
  * Atmega328P má osmi bitové jádro, což je dobré místo, kde začít s navrhováním digitálních obvodů a vývojem firmwaru.
  * Nepotřebujete vědět jak kreslit schémata a plánky a sestavit čip.
  * Musíte ale vědět, jak číst schémata a porozumět zapojení čipů.
  * Vývojáři firmwaru by měli být schopni číst schémata a zjistit, jak poslat data do cílového zařízení.
  * Postupujte podle knihy návodů!
* [8086 manuál](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * Pokud jste nováčkem co se týká x86 architektury, 8086 je také velmi dobrý návod co do stavby procesoru a 80x86 assembly
* [80386 manuál](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Nejlepší návod pro chráněný mód a stránkovací mechanismus procesorů 80x86
  * Webovská verze: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

V tomto bodě by jste měli být dost dobří na to začít s nejnovějšími ARM nebo x86 procesory.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Například Raspberry Pi deska má Cortex-A53 procesor, který podporuje 64-bitové sady instrukcí.
To vám dovoluje si vyzkoušet moderní procesorovou architekturu s rPi.
Ano, můžete si ti koupit... ale... co s tím budete dělat?
Pokud nemáte žádný cílový projekt, můžete klidně desku hodit do šuplíku a zapomenout na ni jako na další věcičky, co jste nakoupili předtím.

Takže vám doporučuji jeden projekt.
* [Vytvoření vlastního jádra](http://wiki.osdev.org/Getting_Started)
  * Dobré podklady: https://www.reddit.com/r/osdev/
* [Naučení se vyvíjet operační systém za použití Linuxového jádra a Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
  * (popis projektu) Toto úložiště obsahuje návod, který vás krok za krokem naučí, jak vytvořit jednoduché jádro operačního systému (OS) z ničeho... Každá lekce je navržena tak, že nejdříve vysvětlí, jak je jádrová vlastnost implementována do RPi OS, a potom se snaží předvést, jak ta samá funkce pracuje v Linuxovém jádře.

Vytvořil jsem [jádro na hraní](https://github.com/gurugio/caos) které podporuje 64-bitově délkový mód, stránkující a ve velmi jednoduchém kontextu přepínající. Udělání jádra na hraní je dobrá cesta k porozumění moderní počítačové architektuře a kontroly nad hardwarem.

V podstatě poslední procesor a poslední hardwarové prostředky už máte. Svůj laptop! Svůj desktop! Máte všechno, co potřebujete k tomu začít!
Nemusíte nic kupovat.
Qemu emulátor může napodobit poslední ARM procesory a procesory Intel.
Takže všechno, co potřebujete, už máte v rukou.
Je mnoho jader na hraní a dokumentací z kterých můžete těžit.
Stačí si nainstalovat qemu emulátor a vyrobit drobné jádro, které bootuje, začne stránkovat a tiskne zprávy.

Další jádra na hraní:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Linuxové jádro a ovladač zařízení

Nepotřebujete vytvořit kompletní operační systém.
Připojete se ke komunitě a podílejte se na vývoji.

#### <a name="Follow-carefully"></a>Důsledně nastudujte

* Knihy: Přečtěte v následujícím pořadí
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * Základní koncepty Unixu jsou aplikovány do všech operačních systémů.
    * Tato kniha je dobrým místem, kde se naučit základní postupy operačních systémů.
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Sami vyřešte všechny příklady
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Porozumějte designu Linuxového jádra
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Přečtěte tuto knihu a zdrojový kód jádra v2.6 zároveň
    * Nikdy nezačínejte s nejnovější verzí, v2.6 je dostačující!
    * Použijte qemu a gdb ke spouštění zdrojového kódu jádra řádek po řádku
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * Použijte busybox k vytvoření toho nejjednoduššího systému souborů, jehož bootování zabere pouze jednu sekundu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Jiné zdroje: Ze zdrojů, co jsou zadarmo doporučuji
  * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * Praktický průvodce a vynikající příklady vytváření Linuxových ovladačů zařízení se základními jádrovými aplikacemi
    * Myslím, že tento dokument představuje téměř všechny podstatné jádrové aplikace.
  * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
    * _Bohužel, tento úkol nepřijímá další účastníky, protože se tu už žádná výzva nevyskytuje._ Správce řekl, že plánuje nový formát. Doufám, že to bude co nejdříve.
      * Můžete ale nalézt podněty k výzvám přes Google. Někteří už nahráli, co vytvořili. Najděte úkoly a snažte se je sami vyřešit a porovnejte svoje řešení s ostatními.
    * To je jako zatraceně dobrý soukromý učitel, který vás vede k tomu, co by se mělo dělat.
    * Jesliže nevíte, co dělat, prostě začněte tímto.
  * [Blokovací vrstva a ovladač zařízení](https://github.com/gurugio/book_linuxkernel_blockdrv)
    * začněte jednoduchým příkladem blokovacího ovladačem zařízení (Ramdisk) s multi-frontovým módem
    * jděte dál až ke blokovací vrstvě
    * Dokončil jsem překlad do angličtiny. Dejte mi prosím zpětnou vazbu.
  * [md ovladač Linuxového jádra (korejsky)](https://github.com/gurugio/book_linuxkernel_md)
    * jak mdadm nástroj funguje a jak volá md ovladač
    * jak md ovladač funguje
  *  [Učení se vývoji operačního systému za použití Linuxového jádra a Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
     * Tento projekt ještě není dokončen.
     * Vždy si myslím, že vytvoření jádra podobného tomu Linuxovému je nejlepší cestou k porozumění jádra Linuxu.

#### <a name="References"></a>Dokumentace

Projděte, když něco potřebujete

* [Domovská stránka volné elektroniky](http://free-electrons.com/docs/)
  * mnoho souborů s prezentacemi představujícími dobrá témata, hlavně ARM-linux
* [Blogy Julie Evansové: Můžeš být jádrový hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * návod, jak začít s programováním jádra

### <a name="Other-applications"></a>Jiné aplikace

Ano, nemusí vás zajímat Linux nebo firmware. Pokud tomu tak je, můžete nalézt jiná uplatnění:
* Programování systému Windows & ovladače zařízení
* Zabezpečení
* Reverzní inženýrství

Nemám žádné znalosti o těchto uplatněních. Prosím pošlete mi nějaké informace pro začátečníky.

**Nízkoúrovňové programování nejsou jenom jádra a ovladače.** Je ještě jedno důležité uplatnění nízkoúrovňového programování a to je softwarově ovládané úložiště nebo poskytovaný systém souborů. Jejich detailní popis již spadá mimo rámec tohoto dokumentu, ale existuje jeden vynikající kurz, kde si můžete jednoduchý poskytovaný systém souborů vyzkoušet.
* Kurz: https://pdos.csail.mit.edu/archive/6.824-2012/
* zdrojový kód dokumentace: https://github.com/srned/yfs

## <a name="Future-of-low-level-programming"></a>Budoucnost nízkoúrovňového programování

Neznám budoucnost, ale sleduji RUST.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Kdybych měl týden volna, učil bych se RUST.
A to proto, že RUST je nejnovější jazyk se kterým mohu vyvíjet Linuxové ovladače zařízení.
* https://github.com/tsgates/rust.ko

IoT (internet věcí) je nový trend, takže by stálo za to podívat se, jaký operační systém se pro IoT používá.
ARM, Samsung a některé další společnosti mají svůj vlastní real-time operační systém, ale bohužel mnoho z nich má uzavřený zdrojový kód.
Ale Linux Foundation má také řešení: Zephyr
* https://www.zephyrproject.org/

Typické serevery cloudů mají mnoho vrstev; například, hostitelský operační systém, kvm ovladač, qemu proces, hostující operační systém a servisní aplikace. K nenáročné virtualizaci byl vyvinut kontejner. V blízké budoucnosti by měl nový koncept OS, takzvaný OS knihoven nebo Unikernel, nahradit typické zásobníky softwaru pro virtualizaci.
* http://unikernel.org/

Velká data a používání cloudů vyžaduje stále větší a větší úložiště. Disky přímo přiložené k serverům nemohou uspokojit požadovanou kapacitu, stabilitu a výkon. Proto byl učiněn výzkum k vytvoření obrovských úložných systémů s mnoha úložnými zařízeními propojených vysokorychlostní sítí. Původně to bylo zaměřené na sestavení jednoho velkého úložného souboru. Ale v současné době se provozuje větší počet souborů pro mnoho virtuálních přístrojů.
* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

# <a name="Translation"></a>Překlad

Prosím pošlete mi pull request, pokud chcete přeložit tuto stránku. Uvedu jej zde.

* [čínština](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [portugalština (Brazílie)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_pt.md)
* [italština](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)

# <a name="who-am-i"></a>Kdo jsem?

Jsem inspirován [google-interview-university](https://github.com/jwasham/google-interview-university). Rád bych se podělil o zkušenosti a ukázal návod jak se stát nízkoúrovňovým programátorem, protože jsem zjistil, že tyto dovednosti nejsou tak běžné jako kdysi byly. Navíc se mě mnoho studentů a začátečníků ptá, jak by se mohli stát nízkoúrovňovým programátorem a inženýrem Linuxového jádra.

Pro vaši informaci, mám přes deset let zkušeností coby nízkoúrovňový programátor:
* 80x86 Assembly programování
* Hardwarová zařízení s čipem Atmel a firmware
* Systémové programování v jazyku C pro Unix
* Ovladače zařízení v Linuxu
* Linuxové jádro: stránková alokace
* Linuxové jádro: blokovací ovladač zařízení a md modul
