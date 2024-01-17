# Universidade de Programação em Baixo Nível

Nota 1: Por favor, não copie o conteúdo desta página para o seu blog. Você pode compartilhar esta página, mas, por favor, compartilhe com o link original. Essa é a forma que nós elogiamos os autores de bons documentos e projetos de código aberto.

Nota 2: Por favor, note que programação de baixo nível não está em alta e atualmente não há muitas companhias contratando desenvolvedores de baixo nível. Está ficando mais difícil para encontrar trabalho. Se você ainda não começou a sua carreira profissional, eu recomendaria considerar outros campos cuidadosamente.

Nota 3: Se você quiser ir direto ao ponto, vá para [Como começar?](#como-começar).

## Sumário

* [O que é esse repositório?](#o-que-é-esse-repositório)
* [O que é programação de baixo nível?](#o-que-é-programação-de-baixo-nível)
* [Teoria](#teoria)
* [Linguagens](#linguagens)
    * [Assembly](#assembly)
    * [C](#c)
    * [Rust](#rust)
* [Carreiras](#carreiras)
    * [Hardware e Firmware](#hardware-e-firmware)
    * [Kernel Linux e Drivers de Dispositivos](#kernel-linux-e-drivers-de-dispositivos)
        * [Referências](#referências)
    * [Outras carreiras](#outras-carreiras)
* [Futuro da programação em baixo nível](#futuro-da-programação-em-baixo-nível)
* [Como começar?](#como-começar)
* [Traduções](#traduções)
* [Quem sou eu?](#quem-sou-eu)

## O que é esse repositório?

Eu me inspirei na [google-interview-university](https://github.com/jwasham/coding-interview-university). Eu gostaria de compartilhar minha experiência e um roteiro de como se tornar um programador de baixo nível, pois acredito que essas habilidades não são tão comuns quanto antigamente. Além disso, muitos iniciantes e estudantes me perguntam como poderiam se tornar desenvolvedores de baixo nível e engenheiros do kernel Linux.

Esta página não inclui todos os links, livros ou cursos. Por exemplo, esta página introduz Arduino, mas não tem informações detalhados sobre Arduino e sistemas embarcados. Você deve se aprofundar por si mesmo. Você tem a palavra-chave "Arduino" para começar, então seu próximo passo é pesquisar sobre Arduino, comprar um kit e fazer alguma coisa você mesmo, e não colecionar links e livros. Por favor, lembre que esta página é apenas um roteiro para iniciantes.

Programação de baixo nível é uma parte de Ciências da Computação, de tal forma que, é certamente muito melhor ter esse conhecimento primeiro.

* [Path to a free self-taught education in Computer Science!](https://github.com/ossu/computer-science)

*Nota do tradutor*: os links que estiverem em inglês é devido o conteúdo estar em inglês. Em alguns casos, por exemplo livros, foi colocado o nome da versão em português, caso haja. Alguns poucos links que estão em inglês podem ter a refência escrita em português por motivos de maior de clareza.

## O que é programação de baixo nível?

Eu classifico programação de baixo nível como uma programação que é muito próxima da máquina. Usa-se uma linguagem de programação de mais baixo nível, como C ou assembly, diferentemente de linguagens de programação de alto nível, típicas de aplicações do espaço de usuário, como Python ou Java.

* [Linguagem de Programação de Baixo Nível - Wikipedia](https://pt.wikipedia.org/wiki/Linguagem_de_programa%C3%A7%C3%A3o#Quanto_ao_grau_de_abstra%C3%A7%C3%A3o)

Sim, o conceito de programação de sistemas é bem próximo do de programação de baixo nível. Esse roteiro inclui o desenvolvimento de hardware e firmware que não estão inclusos no desenvolvimento de sistemas.

* [Systems Programming - Wikipedia](https://en.wikipedia.org/wiki/System_programming)

Finalmente, esse roteiro inclui tópicos indo de componentes de hardware até o kernel Linux. Isso é uma variedade enorme de camadas. Um documento de uma página nunca conseguiria cobrir detalhadamente todas elas, então o foco deste é servir de ponto inicial para programação de baixo nível.

## Teoria

Existem dois conhecimentos teóricos para se programar em baixo nível:

* Arquitetura de Computadores
* Sistemas Operacionais

Acredito que a melhor maneira de aprender teoria é fazendo um curso. Ler livros não é ruim, mas consome muito tempo e esforço. Você pode achar várias aulas em universidades online, por exemplo [Coursera](https://www.coursera.org) e [edX](https://www.edx.org/).

Teoria é teoria. Eu não acho que você necessite de um 10 em uma matéria, apenas entenda seu conteúdo geral; você evoluirá com experiência.

Irei apresentar vários livros que li. Eles são comumente usados como livros-texto em universidades. Se não existe uma matéria com esses livros na sua universidade, vale a pena gastar um pouco de tempo os lendo.

* Arquitetura de Computadores
    * Organização e Projeto de Computadores, 5ª edição. HENNESSY, John. 2021.
    * Arquitetura de Computadores: Uma Abordagem Quantitativa, 6ª edição. HENNESSY, John. 2019.
    * Computer Systems: A Programmer's Perspective, 3rd Revised Edition. BRYANT, Randal; O'HALLARON, David. 2015.
* Sistemas Operacionais
    * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design. GOODHEART, Berny; COX, James. 1994.
    * The Design of the UNIX Operating System. BACH, Maurice. 1986.
    * Operating Systems: Internals and Design Principles, 9th Edition. STALLINGS, William. 2017.
    * *Adicionado pelo tradutor*: [Operating Systems: Three Easy Pieces](https://pages.cs.wisc.edu/~remzi/OSTEP/). ARPACI-DUSSEAU, Remzi H.; ARPACI-DUSSEAU, Andrea C.
        * E-book online e gratuito sendo atualizado constantemente. Se encontra na versão 1.10 no momento do lançamento desta tradução.
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
      * Eu montei o meu kit na universidade e foi uma das mais valiosas atividades que fiz. Tente fazer seu próprio kit, sendo melhor que o hardware seja mais velho e simples, porque deve lhe dar mais trabalho.
      * Pesquise "kit 8086": você deve achar alguns sites em que pode comprar uma esquema de hardware, partes e manuais.

Existe uma lista infinita de bons livros, e eu não quero dizer que você deve ler todos; leia um com cuidado: fazendo marcações, anotações e pesquisas. Sempre que aprender uma teoria, implemente um código simulando isso. **Implementar algo é melhor do que saber 100 teorias**.

## Linguagens

### Assembly

Escolha um entre x86 e ARM, não precisa saber as duas. Não importa tanto saber assembly a princípio, o essencial é entender o funcionamento interno de uma CPU e um computador, logo não há necessidade de praticar com assembly das CPU mais recentes. Apenas escolha entre 8086 ou Cortex-M.

* [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * Conceitos básicos de arquitetura de processadores e computadores
    * Conceitos básicos de C
* [64 bit assembly programming (translation in progress)](https://github.com/gurugio/book_assembly_64bit)
    * Conceitos básicos de arquitetura de CPUs e computadores modernos.
    * Conceitos básicos de disassembling e debugging em C
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

### C

Aqui não existe atalho: leia o livro todo e resolva todos os exercícios.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language, 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* Modern C: Jens Gustedt. Modern C. Manning, 2019, 9781617295812. ffhal-02383654f
    * Nova convenção/novo padrão de C
* [Is Parallel Programming Hard? And If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
    * Implementação real de paralelismo em C
    * Essencial para programas C de larga escala (especialmente kernels)
* [Projects in C](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
    * Se você leu um ou dois livros sobre C, então você DEVE programar algo
    * Escolha qualquer coisa que lhe agrade
    * Primeiro faça o seu e depois compare com o código de outra pessoa
    * É muito impotante comparar seu código, pois você só melhora suas habilidades quando você vê o código de alguém e aprende métodos melhores
    * **Livros são mortos enquanto que códigos são vivos**
* [Projects in C and other languages](https://github.com/danistefanovic/build-your-own-x)
    * Mais projetos interessantes
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
    * Referência em otimização usando C e assembly x86
    * Começa do 8088 até hoje em dia
    * Foco especial em otimização de gráficos em baixo nível
* [Frameworks and plugins in C](https://github.com/gurugio/book_cprogramming)
    * Como desenvolver frameworks e plugins em C para programas de larga escala
    * Dicas bem básicas sobre como ler o kernel Linux

Se quiser ser um especialista em C, visite [LeetCode](https://leetcode.com/). Boa sorte!

### Rust

Tenho convicção que a próxima linguagem para programação de sistemas vai ser [Rust](https://www.rust-lang.org/). Farei uma lista do que fiz para aprender esta linguagem.

[Linus Torvalds: Rust will go into Linux 6.1 ](https://www.zdnet.com/article/linus-torvalds-rust-will-go-into-linux-6-1/)

*Adicionado pelo tradutor*: [Torvalds Speaks: Rust's Impact on the Linux Kernel](https://www.youtube.com/watch?v=YyRVOGxRKLg)

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
    * Vários exercícios de nível fácil são voltados para o aspecto funcional da linguagem, usando métodos como: `map`, `filter` e `any`
* [Easy rust](https://dhghomon.github.io/easy_rust/)
    * Um livro escrito em um inglês simples e com [material adicional no YouTube](https://www.youtube.com/playlist?list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk)
* [Let's Get Rusty](https://www.youtube.com/c/LetsGetRusty)
    * Há muitos youtubers fazendo cursos de Rust, mas esse foi o meu preferido
    * Ele também tem upado vídeos sobre as últimas notícias envolvendo Rust, então acredito que valha sua inscrição
* *Adicionado pelo tradutor*: Rust for Rustaceans: Idiomatic Programming for Experienced Developers. GJENGSET, Jon. 2021.
    * Livro de um ex-mantenedor da insfraestrutura em Rust da [AWS](https://aws.amazon.com/pt/what-is-aws/?nc1=f_cc)
    * Atualmente fazendo uma pesquisa relacionada a um banco de dados escrito em Rust
    * Comumente faz [lives no YouTube](https://www.youtube.com/c/JonGjengset) cobrindo tópicos como detalhes de implementação da biblioteca padrão do Rust, contribuindo para projetos de código aberto ou desenvolvendo algum projeto próprio
    * Este livro é um complemento para quando você já conhecer um pouco melhor a sintaxe e como programas são escritos em Rust; ele NÃO é um livro para iniciantes na linguagem
* [Rust for Linux](https://github.com/Rust-for-Linux)
    * Veja os exemplos e dê uma olhada em como Rust entrou no kernel Linux

## Carreiras

### Hardware e Firmware

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

Por exemplo, a placa Raspberry Pi tem um processador Cortex-A53 que suporta um conjunto de instruções de 64 bits, permitindo que você experiencie arquitetura moderna de processadores.

Certo, você pode comprá-la, mas o que você vai fazer com isso? Se você não tem um projeto em mente, você tenderá a deixá-la na estante e esquecer da sua existência, como você provavelmente deve ter feito com outros equipamentos que você deve ter comprado.

Então eu recomendarei um projeto a você:

* [Fazer seu próprio kernel](http://wiki.osdev.org/Getting_Started)
    * Boas referências: [r/osdev](https://www.reddit.com/r/osdev/)
* [Aprendendo desenvolvimento de sistemas operacionais usando Linux e Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
    * > This repository contains a step-by-step guide that teaches how to create a simple operating system (OS) kernel from scratch. [...] Each lesson is designed in such a way that it first explains how some kernel feature is implemented in the RPi OS, and then it tries to demonstrate how the same functionality works in the Linux kernel.

Eu fiz um [kernel de brinquedo](https://github.com/gurugio/caos) que suporta modo 64 bits, paginação e uma troca de contexto bem simples. Fazer um kernel para brincar é um bom caminho para entender arquitetura de computadores modernos e controle de hardware.

Na verdade, você já tem os processadores e hardware atuais: seu notebook ou seu computador! Você já tem tudo que você precisa para começar, não precisa comprar nada.

O emulador [QEMU](https://www.qemu.org/) pode emular os processadores ARM e Intel atuais, então tudo que você precisa já está disponível.

Existem vários kernels de brinquedo e documentos que você pode se basear. Apenas instale o emulador QEMU e faça um pequeno kernel que apenas da boot, liga paginação e imprime algumas mensagens.

Outros kernels de brinquedo:

* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### Kernel Linux e Drivers de Dispositivos

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
        * Nunca comece com a versão mais recente, a 2.6 é suficiente!
        * Use QEMU e [GDB](https://www.sourceware.org/gdb/) para rodar o código linha por linha
            * [Como debuggar o kernel Linux com GDB e QEMU](http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu)
            * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
        * Use busybox para fazer o sistema de arquivos mais simples possível, levando apenas um segundo para bootar
            * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Outros recursos gratuitos que recomendo
    * [Linux Device Driver Labs](https://linux-kernel-labs.github.io/)
        * Guia prático e com excelentes exercícios fazendo drivers com APIs essenciais do kernel
        * Acredito que este documento introduz quase toda API essencial
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
        * *Infelizmente este desafio não aceita mais requisições porque não tem mais desafios*, mas você pode encontrar as questões do desafio as pesquisando
        * O mantenedor falou que está planejando um novo formato
        * Isto é como um professor incrível que lhe guia pelo que fazer
        * Se você não sabe o que fazer, apenas comece
    * [Aprendendo desenvolvimento de sistemas operacionais usando Linux e Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
        * Este projeto não está completo ainda
        * Eu penso que fazer um kernel similar ao do Linux é a melhor maneira de o entender
    * [Block layer and device driver](https://github.com/gurugio/book_linuxkernel_blockdrv)
        * Comece com um simples exemplo de driver de bloco (Ramdisk) com modo multi-fila
        * Prossiga com a camada de blocos
    * [Driver md do kernel Linux (Coreano)](https://github.com/gurugio/book_linuxkernel_md)
        * Como ferramentas mdadm funcionam e como chamam o driver md
        * Como o driver md funciona
    * [Código fonte do kernel Linux com vários comentários](http://www.oldlinux.org/)
        * Vários comentários para o Linux v0.12
        * Seria bom começar com um antigo e simples SO
        * Versão Unix: [Lions' Commentary on UNIX 6th Edition, with Source Code](https://en.wikipedia.org/wiki/Lions%27_Commentary_on_UNIX_6th_Edition,_with_Source_Code)

#### Referências

Cheque quando estiver precisando de algo

* [Bootlin Docs](https://bootlin.com/docs/)
    * Vários slides intruduzinho bons tópicos, especialmente ARM-Linux
* [You can be a kernel hacker! (blog post)](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
    * Guia para começar programação de kernel

### Outras carreiras

Sim, você pode não ser interessando em Linux ou firmware. Nesse caso, você pode procurar outras carreiras:

* Programação de sistemas e drivers em Windows
* Segurança
* Engenharia reversa

Eu não tenho conhecimento algum sobre estas. Por favor, mande-me qualquer informação para iniciantes.

**Kernels e drivers não são tudo de programação de baixo nível.**

Mais uma importante carreira de programação de baixo nível é o armazenamento definido por software (*software-defined storage*) ou sistemas de arquivos distribuidos. Descrições detalhadas sobre isto estão além do escopo desse documento, mas existe cursos excelentes em que você pode fazer um simples sistema de arquivos distribuidos.

* Curso: https://pdos.csail.mit.edu/archive/6.824-2012/
* Fonte: https://github.com/srned/yfs

## Futuro da programação em baixo nível

Eu não sei o futuro, mas estou de olho no Rust.

* [Rust and the Future of Systems Programming](https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/)

Se eu tivesse uma semana livre, eu aprenderia Rust, pois é a linguagem mais nova que consigo desenvolver drivers no Linux.

* https://github.com/tsgates/rust.ko

IoT (*Internet of Things* - Internet das  Coisas) é o que anda em alta, então vale a pena olhar o que são SOs para IoT. Algumas empresas possuem seus próprios RTOSes (*Real-Time Operating System* - Sistema Operacional de Tempo Real), como ARM e Samsung, mas muitos deles são de código fechado; a Linux Foundation tem sua própria solução:

* https://www.zephyrproject.org/

Servidores em nuvem tipicamente possuem várias camadas, por exemplo SO hospedeiro, driver KVM, processo QEMU, SO hóspede e serviço da aplicação. Um contêiner foi desenvolvido para prover virtualização leve. Em um futuro próximo, um novo conceito de SO, assim chamado de *Library OS* ou *Unikernel*, substituiria as ferramentas típicas de software e hardware para virtualização.

* http://unikernel.org/

Big data e computação em nuvem está requerindo armazenamentos cada vez maiores. Alguns discos ligados diretamente à máquina do servidor não satifaz as requisições de capacidade, estabilidade e performance. Dessa forma, estão acontecendo pesquisas para a produção de sistemas de grande armazenamento, com várias máquinas para armazenar os dados conectadas por uma rede de alta velocidade. Antes era focada um armazenamento único de grande volume, porém atualmente estão provendo vários volumes dedicados para as várias máquinas virtuais.

* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

## Como começar?

Eu recebi um email perguntando como começar. Existe muita informação sobre livros, cursos e projetos nesta página, mas foi erro meu esquecer de escrever como começar. Infelizmente não existe um *Caminho Real* ([Porto Real](https://gameofthrones.fandom.com/pt-br/wiki/Porto_Real)).

Irei apenas escrever o que eu fiz em ordem. Se você já tiver feito algo, pule. NOVAMENTE, isso é apenas um exemplo que você pode fazer em ordem, em caso de você não saber como começar ou o que fazer.

* Lendo livros sobre sistemas operacionais: pelo menos "The Design of the UNIX Operating System" por Maurice J. Bach (já citado anteriormente).
* Aprenda assembly e C
    * [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
        * É suficiente você entender o conceito de programação em assembly, não há necessidade de fazer algo prático
    * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
        * Dê seu melhor para resolver CADA UM do exercícios
    * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Faça algo prático com C
    * [Projects in C](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
        * Encontre um ou dois projetos interessantes e faça você mesmo
    * [LeetCode](https://leetcode.com/)
        * Se você não achar nenhum projeto interessante, também é bom focar em estrutura de dados e algoritmos
* Faça um projeto de hardware
    * Raspberry Pi ou Arduino não importa, você precisa experimentar controlar o hardware diretamente com APENAS C!
    * Eu recomendo comprar um kit ATmega128 e fazer um firmware ligar/desligar LEDs, detectar o input de um switch e mostrar uma mensagem de texto no LCD
    * Um programa de controle de motor também é um projeto muito bom (um *line tracer*, por exemplo)
    * NÃO USE bibliotecas: você deveria fazer tudo você mesmo (com exceção do software de colocar o programa na placa)
* Básicos do Kernel Linux
    * Programação de baixo nível é bem próxima de sistemas operacionais, então você deve saber o interior de um sistema operacional
    * Comece por drivers
        * Leia [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
        * [Linux device driver labs](https://linux-kernel-labs.github.io/)
        * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
    * Leia [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) para entender os detalhes internos do kernel Linux
* Vá para o ambiente profissional
    * Se você quer se tornar um desenvolvedor profissional do kernel Linux
        * Precisa ler [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
        * E então fazer seu kernel de brinquedo
            * [Aprender desenvolvimento de sistemas operacionais usando Linux e Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
            * [Fazendo seu próprio kernel](http://wiki.osdev.org/Getting_Started)
        * Escreva o link do repositório do seu kernel no seu currículo (não esqueça de escrever mensagens descritivas nos commits)
        * Veja issues em https://lwn.net/, pegue alguma e a resolva
            * Vá para "Recent Kernel Pacthes" em https://lwn.net/Kernel/ ou pelo link direto https://lwn.net/Kernel/Pacthes
            * Encontre um patch para você e tente entender o código fonte. Claro que vai ser difícil, mas tente. Você entenderá mais e mais sempre que tentar
            * Builde o kernel e teste na sua máquina: teste de performance, de estabilidade com [LTP](https://linux-test-project.github.io/) ou análise estática de código dentro do kernel
            * Reporte qualquer problema que encontrar: warnings ou erros de compilação, redução de performance, kernel entrando em pânico ou qualquer outro
            * Se funciona bem, reporte com a descrição da sua máquina e o dono do patch vai escrever "Reviewed-by" (revisado por) e seu nome
            * Parabéns pelo seu nome no log do git do kernel
    * Ou encontre outros tópicos
        * Existem vários outros campos em que engenheiros de baixo nível podem trabalhar: segurança, compiladores, firmware, robótica, setor automotivo e muito mais

# Traduções

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

# Quem sou eu?

Eu me inspirei na [google-interview-university](https://github.com/jwasham/coding-interview-university). Eu gostaria de compartilhar minha experiência e um roteiro de como se tornar um programador de baixo nível, pois acredito que essas habilidades não são tão comuns quanto antigamente. Além disso, muitos iniciantes e estudantes me perguntam como poderiam se tornar desenvolvedores de baixo nível e engenheiros do kernel Linux.

Tenho mais de 10 anos de experiência como programador de baixo nível, incluindo:

* Programação em assembly 80x86
* Hardware com chip ATmel e firmware
* Programação de sistemas Unix com C
* Drivers em Linux
* Kernel Linux: page allocation
* Kernel Linux: block driver e módulo md

