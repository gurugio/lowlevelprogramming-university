* [Low-Level Programming University](#Low-Level-Programming-University)
  * [O que é?](#What-is-it)
  * [O que é "Low-Level?"](#What-Is-the-Low-Level)
  *  [Teoria](#Theory)
  *  [Linguagens](#Languages)
    * [Assembly](#Assembly)
    * [Linguagem C](#C-language)
  * [Aplicações](#Applications)
    * [Hardware && Firmware](#Hardware-Firmware)
    * [Kernel Linux e driver de dispositivos](#Linux-kernel-and-device-driver)
      * [Leia cuidadosamente](#Read-carefully)
      * [Referências](#References)
    * [Outras aplicações](#Other-applications)
  * [Futuro da programação "low-level"](#Future-of-low-level-programming)
  * [Trabalho](#Job)
* [Tradução](#Translation)

# <a name="Low-Level-Programming-University"></a>Low-Level Programming University

## <a name="What-is-it"></a>O que é?

Esta página é para iniciantes que querem ser programadores de baixo nível (low-level).

Eu me inspirei no [google-interview-university](https://github.com/jwasham/google-interview-university). Gostaria de compartilhar minha experiência e mostrar um roteiro para se tornar um programador de baixo nível, pois descobri que essas habilidades não são tão comuns como eram antigamente. Além disso, muitos estudantes e principiantes me perguntam como poderiam se tornar programadores de baixo nível e engenheiros de kernel Linux.

Esta página pode não incluir todos links/livros/cursos. Por exemplo, esta página apresenta o Arduino, mas não há informações detalhadas sobre Arduino e sistemas embarcados. Você deve ir mais longe consigo. Você tem a palavra-chave "Arduino" no qual você pode iniciar. Então, o próximo passo é provavelmente pesquisar no google por Arduino, comprar um kit e ** fazer algo ** para si mesmo. Lembre-se que esta página é apenas um roteiro.

Para mais informações, Eu tenho mais de 10 anos de experiência como programador de baixo nível:
* Programação de assembly 80x86
* Dispositivo de hardware com chip Atmel e firmware
* Programação de sistemas Unix com linguagem C
* driver de dispositivos Linux
* Kernel Linux: paginação
* Kernel Linux: block device driver e módulo md

## <a name="What-Is-the-Low-Level"></a>O que é "Low-Level"?

Classifiquei a programação de baixo nível (low-level programming language) como uma programação muito próxima da máquina, usando uma linguagem de programação de nível inferior como C ou assembly. Isto está em contraste com a programação de alto nível, típica de aplicações de espaço de usuário (user space), usando linguagens de alto nível (por exemplo, Python, Java).
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language)

Sim, a programação de sistemas (system programming) é um conceito muito próximo da programação de baixo nível. Esta página inclui o design de hardware e o desenvolvimento de firmware que não está incluído na programação do sistema.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming)

Finalmente, esta página inclui tópicos que vão desde componentes de hardware até o kernel do Linux. Essa é uma enorme variedade de camadas. Um documento de uma página nunca pode cobrir os detalhes de todas as camadas, de modo que o objetivo deste documento é servir de ponto de partida para a programação de baixo nível.

##  <a name="Theory"></a>Teoria

Existem duas áreas de estudo para programação de baixo nível:
* Arquitetura de Computadores
* Sistemas Operacionais

Você pode encontrar muitos bons cursos online de universidades, como por exemplo, Coursera.org e edx.org.
Teoria é teoria. Eu não acho que você precisa tirar 10 (ou conceito A), você precisa apenas entender boa parte do curso.
Você irá melhorar com tempo de experiência.

Deixe-me apresentar vários livros que eu li. Eles são normalmente usados como livro texto nas universidades. Se estes não forem indicados em suas aulas da universidade, vale a pena gastar algum tempo com eles. Recomendo a leitura em inglês desses livros.

* Arquitetura de Computadores
  * Computer Architecture, Fifth Edition: A Quantitative Approach
  * Computer Systems: A Programmer's Perspective
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* Sistema Operacionais
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System
  * Operating Systems: Internals and Design Principles by William Stallings

Há uma lista infinita de bons livros. Eu não quero dizer que você deve ler muitos livros. Basta ler um livro cuidadosamente. Sempre que você aprender uma teoria, implemente o código de teste. ** Implementar é a melhor maneira de conhecer a fundo a teoria. **

##  <a name="Languages"></a>Linguagens

### <a name="Assembly"></a>Assembly

Escolha entre x86 e ARM. No precisa saber os dois. Isso não importa para aprender linguagem assembly. O essencial é conhecer a arquitetura da CPU e do computador. Então você não precisa aprender o assembly da arquitetura de CPU mais recente que existe. Selecione a arqutetura 8086 ou Corex-M.

* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
  * Conceitos básicos de CPU e arquitetura de computadores
  * Conceitos básicos de linguagem de programação C
* [64bit assembly programming(translation in progress)](https://github.com/gurugio/book_assembly_64bit)
  * Conceitos básicos de uma CPU moderna e arquitetura de computadores
  * Conceitos básicos de disassembling and debugging de código C
  * _need help for translation_
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * Rerencência completa de programação em arquiteturas ARM
* Computer Organization and Design
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * Livros acadêmicos que explicam como cada componente de um computador trabalha.
  * Explica com detalhes os diferentes conteitos que compõem a arquitetura de computadores.
  * Eles não são destinados a se tornar proficiente em uma linguagem assembly específico.
  * A edição MIPS e ARM cobrem os mesmos tópicos, mas aprofundando uma arquitetura diferente.
  * Ambas as edições contêm exemplos no mundo x86.

### <a name="C-language"></a>Linguagem C

Não há atalho. Basta ler os livros e resolver todos os exercícios.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * Para o novo padrão C
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * Implementação de sincronização paralela com C
  * Essencial para programação C em larga escala (especialmente para programação de kernel)
* [C programming challenge?](https://github.com/gurugio/lowlevelprogramming-university/blob/master/c-language-challenge.md)
  * Plano de estudos similar ao [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Apenas uma ideia no momento...
  * Se você conseguir fazer todos os pequenos desafios dessa página, provavelmente você estará apto para começar projetos maiores. 
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * Referencia em otimização usando C e um pouco de assembly x86
  * Começa a partir de 8088 até hoje
  * Foco especial na otimização de gráficos de baixo nível

Se você quer ser um especialista em linguagem C, acesse https://leetcode.com/. Boa sorte!

## <a name="Applications"></a>Aplicações

### <a name="Hardware-Firmware"></a>Hardware && Firmware

Se você quiser ser um engenheiro de sistemas embarcados, seria melhor começar a partir de um kit de hardware simples, ao invés de começar com o mais recente chipset ARM.

* [Arduino Start Kit](https://www.arduino.cc/)
  * Existem várias séries de Arduino, mas o "Arduino Start Kit" tem o processador mais simples (Atmega328P) e guia de livros
  * Atmega328P tem um microcontrolador de 8bits que é o bom para ser usado como base de "design de circuitos digitais" e "desenvolvimento de firmware".
  * Você não precisa saber como desenhar esquemas e layout, e construir os chips.
  * Mas você precisa saber como ler esquemas e entender como os chips estão conectados.
  * Os desenvolvedores de firmware devem ser capazes de ler os esquemas e descobrir como enviar dados para o dispositivo de destino.
  * Firmware developers should be able to read the schematics and figure out how to send data to the target device.
  * Siga o "guide book"!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * Se você é um novato para a arquitetura x86, 8086 também é muito bom para aprender a arquitetura do processador e assembly 80x86
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Melhor guia para modo protegido e mecanismo de paginação do processador 80x86
  * Versão web: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

Este ponto, você deve ser bom para começar com uma versão mais recente de um processador ARM ou x86.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Por exemplo, a placa Raspberry Pi tem um processador Cortex-A53 que suporta um conjunto de instruções de 64 bits.
Isso permite que você experimente uma arquitetura de processador moderna com rPi.
Sim, você pode comprá-lo ... mas ... o que você vai fazer com ele?
Se você não tem nenhum projeto em mente, você provavelmente jogaria a placa em uma gaveta e iria esquecê-la como outros gadgets que você comprou.

Então, eu recomendo um projeto para você
* [Making your own kernel](http://wiki.osdev.org/Getting_Started)
  * Boas referências: https://www.reddit.com/r/osdev/

Eu fiz um ["toy kernel"](https://github.com/gurugio/caos) que suporta 64 bits long mode, paginação e comutação muito simples de contexto. Fazer um "toy kernel" é uma boa maneira de entender arquitetura de computadores moderna e controle de hardware.

Na verdade, você já possui o processador mais recente e os dispositivos de hardware mais recentes.
Seu notebook! Seu PC! Você já tem tudo para começar!
Você não precisa comprar nada mais.
O emulador qemu pode simular a mais recente arquitetura de processadores ARM e Intel.
Então tudo o que você precisa já está à mão.
Existem muitos "toy kernel" e documentos que você pode consultar.
Basta instalar o emulador qemu e criar um pequeno kernel que apenas inicialize e ative a paginação e imprima algumas mensagens.

Other toy kernels:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Kernel Linux e driver de dispositivos

Você não precisa fazer um sistema operacional completo.
Junte-se à comunidade Linux e participe do desenvolvimento.

#### <a name="Read-carefully"></a>Leia cuidadosamente

* Livros: Leia os seguintes em ordem:
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * Os conceitos básicos do Unix são aplicados em qualquer o sistema operacional.
    * Este livro é muito bom para obter os conceitos de sistema operacional.
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Faça todos os exemplos
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Compreenda a arquitetura do kernel do Linux
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Leia este livro e o código fonte do kernel v2.6 ao mesmo tempo
    * Nunca comece com a versão mais recente, v2.6 é suficiente!
    * Use qemu e gdb para executar a fonte do kernel linha por linha
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * Use o busybox para fazer um sistema de arquivos mais simples que leva apenas 1 segundo para inicializar
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Isto é como um excelente professor particular que te orienta no que fazer.
  * Se você não sabe o que fazer, basta iniciar isso.
* [Block layer and device driver(translation in progress)](https://github.com/gurugio/book_linuxkernel_blockdrv)
  * Inicie a partir de um exemplo de block device driver (Ramdisk) com modo multi-queue
  * Avance para block layer
  * _need help for translation_
* [md driver of Linux kernel(in progress)](https://github.com/gurugio/book_linuxkernel_md)
  * Como funciona a ferramenta mdadm e como ela chama o md driver
  * Como o md driver funciona
  * _need help for translation_

#### <a name="References"></a>Referências

Verifique quando precisar de algo

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * Muitos arquivos de slides introduzindo bons tópicos, especialmente ARM-linux
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * Guia para iniciar a programação do kernel

### <a name="Other-applications"></a>Outras aplicações

Sim, talvez você não esteja interessado em desenvolvimento Linux ou firmware. Se não, você pode encontrar outras aplicações:
* Programação do sistema Windows e driver de dispositivo
* Segurança
* Engenharia reversa

Eu não tenho nenhum conhecimento sobre essas aplicações. Por favor, me envie qualquer informação para iniciantes.

## <a name="Future-of-low-level-programming"></a>Futuro da programação "low-level"

Eu não sei o futuro, mas fico atento na linguagem RUST.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Se eu tivesse uma semana livre, sozinho, conseguiria aprenderia RUST.
Isso é porque RUST é a linguagem de programação mais recente com que eu posso desenvolver um driver de dispositivo Linux.

IoT é uma nova tendência, por isso vale a pena verificar quais OSs são para IoT.
ARM, Samsung e algumas empresas tem seu próprio sistema operacional em tempo real, mas infelizmente muitos deles proprietários.
Entretanto, a Linux Foundation também tem uma solução: Zephyr
* https://www.zephyrproject.org/

Um servidor de nuvem tem muitas camadas, como por exemplo, host OS, driver kvm, qemu process, guest OS e service application. Assim, o contêiner foi desenvolvido para fornecer uma virtualização mais leve. Em um futuro próximo, um novo conceito de SO, chamado de library OS ou Unikernel, poderá substituir a típica stack de SW para virtualização.
* http://unikernel.org/

# <a name="Translation"></a>Tradução

Por favor, me envie um pull request se você quiser traduzir esta página. Vou listá-lo no documento em inglês.