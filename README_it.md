* [Universit&agrave; della programmazione a basso livello](#Low-Level-Programming-University)
  * [Che cos'&egrave;](#What-is-it)
  * [Che cos'&egrave; il basso livello](#What-Is-the-Low-Level)
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

S&igrave; la programmazione di sistemi &egrave; volto vicina al concetto della programmazione a basso livello. Questa pagina include il design di hardware e lo sviluppo di firmware che non &egrave; incluso nella programmazione di sistema.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Per l'ultimo, questa pagina include argomenti che spaziano dalle componenti hardware al kernel Linux. Ci&ograve; &egrave; un enorme collezioni di strati. Un documento di una singola pagina non potr&agrave; mai coprire i dettagli di tutti gli strati, perci&ograve; lo scopo di questo documento &egrave; di servire come punto iniziale per la programmazione a basso livello.

##  <a name="Theory"></a>Teoria

Ci sono due teorie di fondo applicate alla programmazione di basso livello:
* Architettura di computer
* Sistemi operativi

Penso che il miglior sistema per imparare la teoria &egrave; seguendo un corso. Leggere libri non &egrave; male ma prende molto tempo e fatica. Puoi trovare buoni corsi nelle universt&agrave; online, per esempio, Coursera.org e edx.org. La teoria &egrave; teoria. Non penso tu possa prendere un 10 con lode in classe, giusto capendo l&igrave; il quadro generale. Migliorerai in continuazione con l'esperienza.

Ti introduco vari libri che ho letto. Sono libri di testo che sono utilizzati solitamente nelle universit&agrave;. Se non ci sono classi con quei libri, &egrave; consigliato spendere un po' di tempo su di essi.

* Architettura di computer
  - Computer Architecture, Fifth Edition: A Quantitative Approach
  - Computer Systems: A Programmer's Perspective
  - Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* Sistemi operativi
   - The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
   - The Design of the UNIX Operating System
   - Operating Systems: Internals and Design Principles by William Stallings
C'&egrave; una lista finita di buoni libri. Non voglio dire che dovresti leggere molti libri. Leggine giusto uno molto attentamente. Una volta che impari una teoria, implementa un codice di prova per esso. Implementare una cosa &egrave; meglio che conoscere centinaia di teorie.

##  <a name="Languages"></a>Linguaggi

### <a name="Assembly"></a>Assembly

* [assembly 8086 con emu8086](https://github.com/gurugio/book_assembly_8086)
  * concetti base della CPU e dell'architettura dei computer
  * concetti base del linguaggio di programmazione C of C programming language
* [programmazione assembly a 64bit (traduzione inglese in corso)](https://github.com/gurugio/book_assembly_64bit)
  * concetti base di una CPU moderna e dell'architettura di computer
  * concetti base di reverse engineering e di debug di codice C
  * _necessito aiuto per la traduzione_
* [Manuale di riferimento per l'architettura ARM](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * Completa guida dell'architettura ARM
* Design ed organizzazione di un computer
  * [Edizione MIPS](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [Edizione ARM](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * Libri accademici che spiegano come ogni componente di un computer lavora in dettaglio
  * Spiegano in dettaglio i vari concetti di un'architettura che costituisce un computer
  * Non sono orientati a diventare fluido in un linguaggio assembly specifico
  * L'edizione MIPs e ARM copre gli stessi argomenti ma analizzando una differente architettura
  * Entrambi le edizioni contengono esempi per il mondo x86

### <a name="C-language"></a>Linguaggio C

Non ci sono scorciatorie. Leggi l'intero libro e risolvi tutti gli esercizi.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [C moderno](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * Per il nuovo standard C
* [La programmazione parallela &egrave; difficile, e, se lo &egrave, cosa puoi farci?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * implementazione cruda della sincronizzazione con C
  * Essenziale per la programmazione C a larga scala (specialmente per la programmazione di kernel)
* [Sfida di programmazione C?](https://github.com/gurugio/lowlevelprogramming-university/blob/master/c-language-challenge_it.md)
  * Piano per un servizio come il "[The Eudyptula Challenge]"(http://eudyptula-challenge.org/)
  * Semplicemente un idea al momento..
  * Se puoi creare tutti i progetti piccoli di quella pagina, potresti iniziare con grandi progetti
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * Guida all'ottimizzazione utilizzando C e un po' di assembly x86
  * Comincia dal 8088 fino ad oggi
  * Focus speciale sull'ottimizzazione della grafica a basso livello

## <a name="Applications"></a>Applicazioni

### <a name="Hardware-Firmware"></a>Hardware e firmware

Se vuoi essere un ingegnere dei sistemi embedded, sarebbe meglio iniziare con un kit hardware semplice, come ad esempio partire con l'ultimo chipset ARM.

* [Arduino Start Kit](https://www.arduino.cc/)
  * Ci sono varie serie ma il "Arduino Start Kit" ha il processore pi&ugrave; semplice(Atmega328P) e un libro che ti guida
  * Atmega328P ha un core a 8bit che un buon punto di inizio per la "progettazione di circuiti" and lo "sviluppo firmware".
  * Non hai bisogno di sapere come disegnare schemi e strutture, e di assemblare i chip
  * Ma hai bisogno di sapere come leggere gli schemi e capire come i chip sono connessi
  * Sviluppatori firmware dovrebbero essere in grado di legge gli schemi e capire come inviare i dati ai dispositivi interessati.
  * Segui la guida!
* [manuale 8086](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * Se sei un principiante sull'architettura x86, anche il 8086 &egrave, una buona guida per l'architettura dei processori e l'assembly 80x86
* [manuale 80386](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Miglior guida per la modalit&agrave; protetta e i meccanismi di paginazione del processore 80x86
  * Versione web: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

A qeusto punto, dovrebbe essere una buona idea partire con l'ultimo processore x86 o ARM.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Per esempio, la scheda Raspeberry Pi ha un processore Cortex-A53 che supporta un set di istruzioni a 64-bit.
Questo ti permette di far esperienza su un processore moderno con rPi.
S&igrave; puoi comparlo...ma...come hai intenzione di utilizzarlo?
Se non ha un obiettivo di progetto, probabilmente lascerai la scheda in un cassetto e te ne dimenticherai come ogni altro gadget che hai comprato in precedenza.

Perci&ograve; ti raccomando un progetto.
* [Crea il tuo kernel](http://wiki.osdev.org/Getting_Started)
  * Spunti interessanti: https://www.reddit.com/r/osdev/

Ho creato [un kernel giocattolo](https://github.com/gurugio/caos) che supporta la modalità long 64-bit, paginazione e un cambio di contesto molto essenziale. Creare un kernel giocattolo &egrave; un buon sistema per capire l'architettura moderna e il controllo dell'hardware.

Ovviamente, tu hai gi&agrave; l'ultimo processore e gli ultimi dispositivi hardware.
Il tuo portatile! Il tuo desktop! Hai tutto ci&ograve; per poter iniziare.
Non hai bisogno di compare nulla.
L'emulatore qemu pu&ograve, emulare gli ultimi porocessori ARM e Intel.
Perci&ograve; ogni cosa necessiti e&grave; gi&agrave; sottomano.
Ci sono molti kernel giocattolo e documenti a cui puoi far riferimento.
Installa qemu e crea il tuo piccolo kernel che semplicemente si avvia, avvia la paginazione e stampa alcuni messaggi.

Altri kernel giocattolo:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Kernel linux kernel e driver di dispositivo

Non hai bisogno di creare un sistema operativo completo.
Unisciti alla comunit&agrave; Linux e partecipa nello sviluppo.

#### <a name="Read-carefully"></a>Leggi attentamente

* Libri: leggi i seguenti in ordine
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * I concetti base di Unix sono applicati su tutti i sistemi operativi.
    * Questo libro &egrave; ottimo per i concetti sui sistemi operativi.
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Fai una prova su tutti gli esempi
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Capire la struttura del kernel Linux
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Leggi questi libro e fai rifermento ai sorgenti kernel 2.6 in contemporanea
    * Mai iniziare con l'ultima versione, la 2.6 &egrave; pi&ugrave; che sufficiente!
    * Usa qemu e gdb per eseguire i sorgenti del kernel linea per linea
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://gurugio.kldp.net/wiki/wiki.php/howto_debug_kernel
    * Usa busybox per creare un file system molto semplice che impiega un secondo per avviarsi 
      * https://gurugio.kldp.net/wiki/wiki.php/qemu_kernel
* [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * &Egrave; come un insegnate privato bravissimo che ti guida su cosa fare.
  * Se non sai cosa fare, parti da qui.
* [Block layer and device driver(translation in progress)](https://github.com/gurugio/book_linuxkernel_blockdrv)
  * inizia da un semplice dispositivo a blocchi di esempio (Ramdisk) con code multiple
  * prosegui fino al dispositivo di blocco
  * _necessit&agrave; di aiuto per la traduzione_
* [md driver of Linux kernel(in progress)](https://github.com/gurugio/book_linuxkernel_md)
  * come funziona lo strumento mdam e come chiava il driver md
  * come funziona il driver md
  * _necessit&agrave; di aiuto per la traduzione_

#### <a name="References"></a>Riferimenti

Controlla qui se necessiti di qualcosa

* [Homepage di Free-electrons](http://free-electrons.com/docs/)
  * molte diapositive che introducono concetti interessanti, specialmente ARM-Linux
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * guida per iniziare la programmazione kernel
  
## <a name="Future-of-low-level-programming"></a>Futuro della programmazione a basso livello

Non conosco il futuro, ma sto tenendo osservato RUST.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Se avessi una settimana libera e sono da solo, vorrei imparare RUST.
Questo perch&egrave; RUST &egrave, il linguaggio pi&ugrave; recente con il quale posso sviluppare un driver di dispositivo Linux.

IoT &egrave; un trend nuovo, perci&ograve; vale controllare quali sistemi operativi sono per l'IoT.
ARM, Samsung e alcune aziende hanno il loro sistema operativo realtime ma tristemente molti di essi sono a sorgenti chiusi.
Ma la Fondazione Linux ha una soluzione: Zephyr
* https://www.zephyrproject.org/

Il server cloud tipico ha cos&igrave; tanti strati, per esempio, il sistema operativo host, driver kvm, processo qemu, sistema operativo guet e applicazioni di servizio. Perci&ograve; i container sono sviluppati per fornire una virtualizzazione leggera. In un prossimo futuro, un nuovo concetto di OS, chiamato sistema operativo libreria o Unikernel, rimpiazzer&agrave; il tipico stack software per la virtualizzazione.
* http://unikernel.org/

# <a name="Translation"></a>Traduzioni
Inviami una pull request se desideri che questa pagina venga tradotto. La elencher&ograve; qui.
