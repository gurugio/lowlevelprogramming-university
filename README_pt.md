# Universidade de Programação em Baixo Nível

Nota 1: Por favor, não copie o conteúdo dessa página para o seu blog. Você pode compartilhar essa página, mas, por favor, compartilhe com o link original. Essa é a forma que nós elogiamos os autores de bons documentos e projetos open source.

Nota 2: Por favor, note que programação de baixo nível está fora de moda e atualente não há muitas companhias contratando desenvolvedores de baixo nível. Está ficando mais difícil para eu encontrar um trabalho.
Se você ainda não começou a sua carreira profissional, eu recomendaria considerar outros campos cuidadosamente.

Nota 3: Se você quer ir direto ao ponto, vá para [Como começar?](#How-to-start).

## Sumário

* [O que é esse repositório?](#What-is-it)
* [O que é programação de baixo nível?](#What-Is-the-Low-Level)
* [Teoria](#Theory)
* [Linguagens](#Languages)
    * [Assembly](#Assembly)
    * [C](#C-language)
    * [Rust](#Rust-language)
* [Carreiras](#Applications)
    * [Hardware e Firmware](#Hardware-Firmware)
    * [Kernel Linux e Driver de Dispositivo](#Linux-kernel-and-device-driver)
        * [Referências](#References)
    * [Outras carreiras](#Other-applications)
* [Futuro da programação em baixo nível](#Future-of-low-level-programming)
* [Como começar?](#How-to-start)
* [Traduções](#Translation)
* [Quem eu sou?](#who-am-i)

## <a name="What-is-it"></a>O que é esse repositório?

Eu me inspirei na [google-interview-university](https://github.com/jwasham/coding-interview-university). Eu gostaria de compartilhar minha experiência e um roteiro de como se tornar um programador de baixo nível porque acredito que essas habilidades não são tão comuns quanto antigamente. Além disso, muitos iniciantes e estudantes me perguntam como poderiam se tornar desenvolvedores de baixo nível e engenheiros do kernel Linux.

Essa página não inclui todos os links, livros ou cursos. Por exemplo, essa página introduz Arduino, mas não tem informações detalhados sobre Arduino de sistemas embarcados. Você deve se aprofundar por si mesmo. Você tem a palavra-chave "Arduino" para começar, então seu próximo passo é provalmente pesquisar sobre Arduino, comprar um kit e fazer alguma coisa você mesmo, e não colecionar links e livros. Por favor, lembre que essa página é apenas um roteiro para iniciantes.

Programação de baixo nível é uma parte de Ciências da Computação, de tal forma que, é certamente muito melhor ter esse conhecimento primeiro.

* [Caminho para uma educação autodidata gratuita em Ciências da Computação!](https://github.com/ossu/computer-science)

## <a name="What-Is-the-Low-Level"></a>O que é programação de baixo nível?

Eu classifico programação de baixo nível como uma programação que é muito próxima da máquina. Usa-se uma linguagem de programação de mais baixo nível, como C ou assembly, diferentimente de linguagens de programação de alto nível, típicas de aplicações do espaço de usuário, como Python ou Java.

* [Linguagem de Programação de Baixo Nível - Wikipedia](https://pt.wikipedia.org/wiki/Linguagem_de_programa%C3%A7%C3%A3o#Quanto_ao_grau_de_abstra%C3%A7%C3%A3o)

Sim, o conceito de programação de sistemas é bem próximo do de programação de baixo nível. Esse roteiro inclui o desenvolvimento de hardware e firmware que não estão inclusos no desenvolvimento de sistemas.

* [Systems Programming - Wikipedia](https://en.wikipedia.org/wiki/System_programming)

Finalmente, esse roteiro inclui tópicos indo de componentes de hardware até o kernel Linux. Isso é uma variedade enorme de camadas. Um documento de uma página nunca conseguiria cobrir detalhadamente todas elas, então o foco deste é servir de ponto inicial para programação de baixo nível.

## <a name="Theory"></a>Teoria

Existem dois conhecimentos teóricos para se programar em baixo nível:

* Arquitetura de Computadores
* Sistemas Operacinais

Acredito que a melhor maneira de aprender teoria é fazendo um curso. Ler livros não é ruim, mas consome muito tempo e esforço. Você pode achar várias aulas em univerisades online, por exemplo: [Coursera](https://www.coursera.org) e [edX](https://www.edx.org/).

Teoria é teoria. Eu não acho que você necessite de uma 10 em uma matéria, apenas entenda seu conteúdo geral; você evoluirá com experiência.

Irei apresentar vários livros que li. Eles são comumente usados como livros-texto em universidades. Se não existe uma matéria com esses livros na sua universidade, vale a pena gastar um pouco de tempo os lendo.

* Arquitetura de Computadores
    * Organização e Projeto de Computadores, 5ª edição. HENNESSY, John. 2021.
    * Arquitetura de Computadores: Uma Abordagem Quantitativa, 6ª edição. HENNESSY, John. 2019.
    * Computer Systems: A Programmer's Perspective, 3rd Edition. BRYANT, Randal; O'HALLARON, David. 2015.
* Sistemas Operacionais
    * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design. GOODHEART, Berny; COX, James. 1994.
    * The Design of the UNIX Operating System. BACH, Maurice. 1986.
    * Operating Systems: Internals and Design Principles, 9th Edition. STALLINGS, William. 2017.
    * *Adicionado pelo tradutor*: [Operating Systems: Three Easy Pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/). ARPACI-DUSSEAU, Remzi H.; ARPACI-DUSSEAU, Andrea C.. E-book online e gratuito sendo mantido atualizado constantemente. Se encontra na versão 1.10 no momento do lançamento desta tradução.
* Cursos Recomendados
    * [CS401: Operating Systems from saylor.org](https://learn.saylor.org/course/view.php?id=94)
* Habilidades Gerais de Programação
    * [Structure and Interpretation of Computer Programs](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs)
      * É sobre como se tornar um bom desenvolvedor de softwares. Você precisa de não somente teoria, mas também técnica, pois programação é como um trabalho artesanal.
      * Se você aprender [Lisp](https://en.wikipedia.org/wiki/Lisp_(programming_language))/[Scheme](https://en.wikipedia.org/wiki/Scheme_(programming_language)), você deve ser capaz de aprender qualquer outra linguagem rapidamente.
      * [Eu resolvi 80% dos exercícios e vale a pena tentar cada um deles.](https://github.com/gurugio/sicp_exercise)
* Design de Hardware
   * Faça seu próprio kit do microprocessador [8086](https://en.wikipedia.org/wiki/Intel_8086).
      * Se você não fizer seu próprio hardware, você não entenderá o que é um dispositivo físico de memória mapeada.
      * Pontos de acesso modernos incluem muitos IPs, então você não tem a chance de entender como a CPU e os periféricos estão conectados.
      * Fazendo seu próprio kit 8086, você tem uma oportunidade de colocar cada dispositivo periférico na memória física e definir como os componentes de hardware principais (barramentos, interrupções do sistema, clock, alimentação, etc.) funcionam com seus próprios olhos.
      * Eu montei o meu kit na universidade. Foi uma das mais valiosas atividades que eu fiz. Tente fazer seu próprio kit, sendo melhor que o hardware seja mais velho e simples, porque deve lhe dar mais trabalho.
      * Pesquise "kit 8086", você deve achar alguns sites em que pode comprar uma esquema de hardware, partes e manuais.

Existe uma lista infinita de bons livros, e eu não quero dizer que você deve ler todos; leia um com cuidado: fazendo marcações, anotações e pesquisas. Sempre que aprender uma teoria, implemente um código simulando isso. **Implementar algo é melhor do que saber 100 teorias**.

## <a name="Languages"></a>Linguagens

### <a name="Assembly"></a>Assembly

Escolha uma entre x86 e ARM, não precisa saber as duas. Não importa tanto saber assembly a princípio, o essencial é entender o funcionamento interno de uma CPU e um computador, logo não há necessidade de praticar com assembly das CPU mais recentes. Apenas escolha entre 8086 ou Cortex-M.

* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * Conceitos básicos de arquitetura de processadores e computadores
    * Conceitos básicos de C
TODO: check owner's response
* [64 bit assembly programming(tradução em andamento)](https://github.com/gurugio/book_assembly_64bit)
    * Conceitos básicos de arquitetura de CPUs e computadores modernos.
    * Conceitos básicos de disassembling e debugging em C
    * *Preciso de ajuda na tradução*
* [Learning assembly for Linux x64](https://github.com/0xAX/asm)
    * Programação em puro assembly 64 bits com NASM e inline assembly com GCC
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
    * Referência completa em programação ARM
* Organização e Arquitetura de Computadores
    * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
    * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
    * [RISC-V Edition](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757)
    * Estes são livros acadêmicos que explicam como cada componente do computador funciona desde o começo
    * Explicam em detalhe os diferentes conceitos que compõem a arquitetura de computadores
    * O público-alvo não são leitores que desejam desejam proficiência em assembly
    * A versão MIPS e ARM cobrem os mesmos tópicos, mas dissecando as diferentes arquiteturas
    * Ambas edições contêm exemplos no universo x86

### <a name="C-language"></a>C

Aqui não existe atalho: leia o livro todo e resolva todos os exercícios.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language, 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* Modern C: Jens Gustedt. Modern C. Manning, 2019, 9781617295812. ffhal-02383654f
    * Nova convenção/novo padrão de C
* [Is Parallel Programming Hard? And If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
    * Implementação real de sincronização em C
    * Essencial para programas C de larga escala (especialmente kernels)
* [Projetos em C](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
    * Se você leu um ou dois livros sobre C, então você DEVE programar algo
    * Escolha qualquer coisa que lhe agrade
    * Primeiro faça o seu e depois compare com o código de outra pessoa
    * É muito impotante comparar seu código, pois você só melhora suas habilidades quando você vê o código de alguém e aprende métodos melhores
    * **livros são mortos e códigos são vivos**
* [Projetos em C e em outras linguagens](https://github.com/danistefanovic/build-your-own-x)
    * Mais projetos interessantes
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
    * Referência em otimização usando C e assembly x86
    * Começa do 8088 até hoje em dia
    * Foco especial em otimização de gráficos em baixo nível
* [Frameworks e plugins em C](https://github.com/gurugio/book_cprogramming)
    * Como desenvolver frameworks e plugins em C para programas de larga escala
    * Dicas bem básicas sobre como ler o kernel Linux

Se quiser ser um especialista em C, visite [LeetCode](https://leetcode.com/). Boa sorte!

### <a name="Rust-language"></a>Rust

Tenho convicção que a próxima linguagem para programação de sistemas vai ser [Rust](https://www.rust-lang.org/). Farei uma lista do que fiz para aprender esta linguagem.

[Linus Torvalds sobre entrada do Rust na versão 6.1 do Linux.](https://www.zdnet.com/article/linus-torvalds-rust-will-go-into-linux-6-1/)
*Adicionado pelo tradutor*: [Linus Torvals sobre o impacto do Rust no kernel.](https://www.youtube.com/watch?v=YyRVOGxRKLg)

* [The Rust Programming Language](https://doc.rust-lang.org/book/)
    * Livro online e gratuito da própria Rust Foundation
    * Boa introdução, mas falta exemplos e exercícios
* [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
    * Enquanto lê o livro anterior, você pode encontrar exemplos aqui
    * Não há muitos exercícios, mas você pode fazer alguma coisa você mesmo
* *Adicionado pelo tradutor*: [Rustlings](https://rustlings.cool/)
    * Repositório da própria Rust Foundation contendo alguns exercícios e com indicação de acerto ou erro
* [Programming Rust, 2nd](https://www.oreilly.com/library/view/programming-rust-2nd/9781492052586/)
    * Introdução mais aprofundada, porém ainda com falta de exercícios
* [Exercism](https://exercism.org/tracks/rust)
    * Bons exercícios para praticar características individuais da linguagem
    * Não tenho certeza se os Mentors estão trabalhando ativamente, mas comparar sua solução com a de outros deve ser o suficiente
    * Depois de submeter sua solução, você pode ver a solução de outros na aba "Community Solutions"
    * Vários exercícios de nível fácil são voltados para o aspecto funcional da linguagem, usando métodos como: `map`, `filter` e `fold`
* [Easy rust](https://dhghomon.github.io/easy_rust/)
    * Um livro escrito em um inglês simples e com [material adicional no YouTube](https://www.youtube.com/playlist?list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk)
* [Let's Get Rusty](https://www.youtube.com/c/LetsGetRusty)
    * Há muitos youtubers fazendo cursos de Rust, mas esse foi o meu preferido
    * Ele também tem upado vídeos sobre as últimas notícias envolvendo Rust, então acredito que valha sua inscrição
* *Adicionado pelo tradutor*: Rust for Rustaceans: Idiomatic Programming for Experienced Developers. GJENGSET, Jon. 2021.
    * Livro de um ex-mantenedor da insfraestrutura em Rust da [AWS](https://aws.amazon.com/pt/)
    * Atualmente fazendo uma pesquisa relacionada a um banco de dados escrito em Rust
    * Comumente faz [lives no YouTube](https://www.youtube.com/c/JonGjengset) cobrindo tópicos como detalhes de implementação da biblioteca padrão do Rust, contribuindo para projetos de código aberto ou desenvolvendo algum projeto próprio
    * Este livro é um complemento para quando você já conhecer um pouco melhor a sintaxe e como programas são escritos em Rust; ele NÃO é um livro para iniciantes na linguagem
* [Rust for Linux](https://github.com/Rust-for-Linux)
    * Veja os exemplos e dê uma olhada em como Rust entrou no kernel Linux

## <a name="Applications"></a>Carreiras

### <a name="Hardware-Firmware"></a>Hardware e Firmware

Se você quer se tornar um engenheiro de sistemas embarcados, seria melhor começar um simples kit de hardware, ao invés de começar com o chipset ARM mais recente.

* [Arduino Start Kit](https://www.arduino.cc/)
    * Existem várias séries de Arduinos, mas o "Arduino Start Kit" tem o processador mais simples (ATmega328P) e um livro guia
    * ATmega328P tem uma arquitetura de 8 bits, o que é um bom lugar para começar em design de circuitos digitais e desenvolvimento de firmware
    * Você não precisa saber como desenhar esquemas, leiautes e montar os chips
    * Mas você precisa saber ler esquemas e entender como os chips estão conectados
    * Desenvolvedores de firmware devem ser capazes de ler esquemas e compreender como mandar dados para outro dispositivo
    * Siga o guia do livro
* [Manual do 8086](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
    * Se você é um iniciante em arquitetura x86, 8086 é, também, um ótimo de guia para arquitetura de processadores e assembly x86
* [Manual do 80386](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
    * Melhor guia para modo protegido (*protected mode*) e mecanismo de paginação (*paging mechanism*) de processadores 80x86
    * [Web version](https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm)

Nesse ponto, você deve ser capaz de começar a ver arquitetura ARM ou x86 atual.

* [Raspberry Pi](https://www.raspberrypi.com/) - ARM
* [BleagleBoard](https://beagleboard.org/) - ARM
* [Certificação Arduino](https://www.arduino.cc/en/ArduinoCertified/IntelEdison)

Por exemplo, a placa Raspberry Pi tem um processador Cortex-A53 que suporte um conjunto de instruções de 64 bits, permitindo que você experiencie arquitetura de processadores moderna.

Certo, você pode comprá-la, mas o que você vai fazer com isso? Se você não tem um projeto em mente, você tenderá a deixá-la na estante e esquecer da sua existência, como você provavelmente deve ter feito com outros equipamentos que você deve ter comprado.

Então eu recomendarei um projeto a você:

* [Fazer seu próprio kernel](http://wiki.osdev.org/Getting_Started)
    * Boas referências: [r/osdev](https://www.reddit.com/r/osdev/)
* [Aprendendo desenvolvimento de sistemas operacionais usando Linux e Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
    * > This repository contains a step-by-step guide that teaches how to create a simple operating system (OS) kernel from scratch...(skip)...Each lesson is designed in such a way that it first explains how some kernel feature is implemented in the RPi OS, and then it tries to demonstrate how the same functionality works in the Linux kernel.

Eu fiz um [kernel de brinquedo](https://github.com/gurugio/caos) que suporta modo 64 bits, paginação e uma troca de contexto bem simples. Fazer um kernel para brincar é um bom caminho para entender arquitetura de computadores modernos e controle de hardware.

Na verdade, você já tem os processadores e hardware atuais: seu notebook ou seu computador! Você já tem tudo que você precisa para começar, você não precisa comprar nada.

O emulador [QEMU](https://www.qemu.org/) pode emular os processadores ARM e Intel atuais, então tudo que você precisa, já está disponível.

Existem vários kernels de brinquedo e documentos que você pode se basear. Apenas instale o emulador QEMU e faça um pequeno kernel que apenas da boot, liga paginação e printa algumas mensagens.

Outros kernels de brinquedo:

* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Kernel Linux e Drivers de Dispositivos

Você não precisa montar um sistema operacional completo, entre na comunidade Linux e participe do desenvolvimento.

Alguns recursos para o desenvolvimento do Linux e de drivers, de iniciante a avançado:

* Livros (leia-os na seguinte ordem)
    * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
        * Os conceitos básicos de Unix são aplicados em todos os sistemas operacionais
        * Esse livro é um bom lugar para aprender os conceitos fundamentais de sistemas operacionais
    * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
        * Faça todos os exemplos
    * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
        * Entenda o design do kernel Linux
    * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
        * Leia este livro e o código fonte do kernel na versão 2.6 ao mesmo tempo
        * Nunca começa com a versão mais recente, a 2.6 é suficiente!
        * Use QEMU e [GDB](https://www.sourceware.org/gdb/) para rodar o código linha por linha
            * [Como debuggar o kernel Linux com GDB e QEMU](http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu)
            * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
        * Use busybox para fazer o sistema de arquivos mais simples que leva apenas um segundo para bootar
            * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Outros recursos [gratuitos que recomendo]
    * [Linux Device Driver Labs](https://linux-kernel-labs.github.io/)
        * Guia prático e com excelentes exercícios fazendo drivers com APIs essenciais do kernel
        * Acredito que este documento introduz quase toda API essencial
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
        * *Infelizmente este desafio não aceito mais requisições porque não tem mais desafios*, mas você pode encontrar as questões do desafio pesquisando
        * O mantenedor falou que está planejando um novo formato
        * Isto é como um professor incrível que lhe guia pelo que fazer
        * Se você não sabe o que fazer, apenas comece
    * [Aprendendo desenvolvimento de sistemas operacionais usando Linux e Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
        * Este projeto não está completo ainda
        * Eu penso que fazer um kernel similar ao do Linux é a melhor maneira de o entender
    * [Camada de bloco e drivers](https://github.com/gurugio/book_linuxkernel_blockdrv)
        * Comece com um simples exemplo de driver de bloco (Ramdisk) com modo multi-fila
        * Prossiga com a camada de blocos
    * [Driver md do kernel Linux (Coreano)](https://github.com/gurugio/book_linuxkernel_md)
        * Como ferramentas mdadm funcionam e como chamam o driver md
        * Como o driver md funciona
    * [Código fonte do kernel Linux com vários comentários](http://www.oldlinux.org/)
        * Vários comentários para o Linux v0.12
        * Seria bom começar com um antigo e simples SO
        * Versão Unix: [Lions' Commentary on UNIX 6th Edition, with Source Code](https://en.wikipedia.org/wiki/Lions%27_Commentary_on_UNIX_6th_Edition,_with_Source_Code)

#### <a name="References"></a>Referências

Cheque quando estiver precisando de algo

* [Bootlin Docs](https://bootlin.com/docs/)
    * Vários slides intruduzinho bons tópicos, especialmente ARM-Linux
* [Você pode ser um hacker de kernels! (blog post)](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
    * Guia para começar programação de kernel

### <a name="Other-applications"></a>Outras carreiras

Sim, você pode não ser interessando em Linux ou firmware. Nesse caso, você pode procurar outras carreiras:

* Programação de sistemas e drivers em Windows
* Segurança
* Engenharia reversa

Eu não tenho conhecimento algum sobre estas. Por favor, mande-me qualquer informação para iniciantes.

**Kernels e drivers não são tudo de programação de baixo nível.**

Mais uma importante carreira de programação de baixo nível é o armazenamento definido por software (*software-defined storage*) ou sistemas de arquivos distribuidos. Descrições detalhadas sobre isto está além do escopo desse documento, mas existe cursos excelentes em que você pode fazer um simples sistema de arquivos distribuidos.

* Curso: https://pdos.csail.mit.edu/archive/6.824-2012/
* Fonte: https://github.com/srned/yfs

## <a name="Future-of-low-level-programming"></a>Future of low-level programming

I do not know the future, but I keep my eye on Rust.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

If I could have one week free and alone, I would learn Rust.
That is because Rust is the latest language with which I can develop Linux device drivers.
* https://github.com/tsgates/rust.ko

IoT is new trend, so it's worth to check what OSs are for IoT.
ARM, Samsung and some companies has their own realtime OS but sadly many of them are closed source.
But Linux Foundation also has a solution: Zephyr
* https://www.zephyrproject.org/

Typical cloud servers have many layers; for instance, host OS, kvm driver, qemu process, guest OS and service application. A container has been developed to provide light virtualization. In the near future, a new concept of OS, a so-called library OS or Unikernel, would replace the typical stack of SW for virtualization.
* http://unikernel.org/

Big data and cloud computing require bigger and bigger storage. Some disks directly attached to server machines cannot satisfy the required capacity, stability and performance. Therefore there has been research to make huge storage systems with many storage machines connected by a high speed network. It used to be focused on making one huge storage volume. But currently they are providing many volumes dedicated for many virtual machines.
* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

## <a name="How-to-start"></a>How to start?

I received an email asking how to start. There are many information about books, courses and projects in this page. It is my mistake to forget to write how to start. Unfortunately, there is no King's Road to [King's Landing](https://gameofthrones.fandom.com/wiki/King%27s_Landing). I will just write what I did in order. If you have already done something, please skip it. AGAIN, this is just an example that you could do in order, just in case if you do not know how to start or what to do.

* Reading OS theory books: at least "The Design of the UNIX Operating System by Maurice J. Bach"
* Learn assembly and C
  * [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * It is enough if you understand the concept of assembly programming. You do not need to do something practical.
  * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
    * DO YOUR BEST TO solve every single exercise!
  * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Do something practical with C
  * [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): Find one or two interesting projects and make your own project.
  * [leetcode.com](https://leetcode.com/): If you cannot find an interesting project, it would be also good to focus on data structure and algorithm.
* Do a hardware project
  * Raspberrypi or Arduino does not matter. You need experience to control a hardware directly with only C. ONLY C!
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
  * If you want to be a professional Linux Kernel Developer
    * must read [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
      * Then try to make a toy kernel
      * [Learn operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
      * [Making your own kernel](http://wiki.osdev.org/Getting_Started)
      * Write the github link to your kernel on your resume (Don't forget to write the detailed description in commit message)
    * Check the latest issues at https://lwn.net/ and join it.
      * Check "Recent kernel patches" at "https://lwn.net/Kernel/" or direct link https://lwn.net/Kernel/Patches
      * Find an interesting patch to you. Try to understand the source code. Of course it would be really difficult but try. You will be closer and closer whenever you try.
      * Build kernel and test it on your system. For example, performance test, stability test with LTP(https://linux-test-project.github.io/) or static code analysis tools inside of kernel.
      * Report any problem if you find any: compile warnings/errors, performance drop, kernel panic/oops or any problem
      * If it works well, report that with the spec of your system. The patch owner would write a "Reviewed-by" tag with your name.
      * Find your name in kernel git log
  * Or find other topics
    * There are many fields where the low-level engineer can work: security, Compiler, Firmware, robot/car and so on

# <a name="Translation"></a>Traduções

Por favor, faça uma PR se deseja traduzir esta página, irei lista-la aqui.

* [Chinese (Traditional)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tw.md)
* [Chinese (Simplified)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [English](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README.md)
* [Italian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)
* [Czech](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cz.md)
* [Russian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_ru.md)
* [Turkish](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_tr.md)
* [Persian](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_fa.md)
* [Spanish](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_es.md)

# <a name="who-am-i"></a>Who am I?

I'm inspired by [google-interview-university](https://github.com/jwasham/google-interview-university). I'd like to share my experience and show a roadmap to becoming a low-level programmer because I have found that these skills are not as common as they once were. In addition, many students and beginners ask me how they could become low-level programmers and Linux kernel engineers.

FYI, I have over 10 years of experience as a low-level programmer:
* 80x86 Assembly programming
* Hardware device with Atmel chip and firmware
* C language system programming for Unix
* Device driver in Linux
* Linux kernel: page allocation
* Linux kernel: block device driver and md module

