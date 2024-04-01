AVIS1: Veuillez ne pas copier le contenu de cette page sur votre blog. Vous pouvez partager cette page mais veuillez partager avec le lien d'origine. C'est ainsi que nous citons les auteurs de bons documents et de projets open source.

AVIS2: Veuillez noter que la programmation de bas niveau est hors de propos et qu'actuellement, il n'y a pas beaucoup d'entreprises qui embauchent des développeurs de bas niveau. Il devient de plus en plus difficile pour moi de trouver un emploi.
Si vous n'avez pas encore commencé une carrière professionnelle, je vous recommande de bien réfléchir avant de choisir ce domaine.

AVIS3: Si vous voulez un démarrage rapide, allez à "Comment démarrer ?".

* [Université de programmation de bas niveau](#Université-de-programmation-de-bas-niveau)
  * [Qu'est-ce que c'est ?](#Qu'est-ce-que-c'est-?)
  * [Qu'est-ce que le bas niveau ?](#Qu'est-ce-que-le-bas-niveau-?)
  *  [Théorie](#Théorie)
  *  [Langages](#Langages)
     * [Assemblage](#Assemblage)
     * [Langage C](#Langage-C)
     * [Langage Rust](#Langage-Rust)
  * [Applications](#Applications)
    * [Matériel et micrologiciel](#Matériel-et-micrologiciel)
    * [Linux noyau et pilote de périphérique](#Linux-noyau-et-pilote-de-périphérique)
      * [Références](#References)
    * [Autres applications](#Autres-applications)
  * [L'avenir de la programmation de bas niveau](#L'avenir-de-la-programmation-de-bas-niveau)
  * [Comment démarrer ?](#Comment-démarrer-?)
* [Traduction](#Traduction)
* [Qui suis-je ?](#qui-suis-je-?)

# Université de programmation de bas niveau

## <a name="Qu'est-ce-que-c'est-?"></a>Qu'est-ce que c'est ?

Je suis inspiré par [google-interview-university](https://github.com/jwasham/coding-interview-university). J'aimerais partager mon expérience et montrer une feuille de route pour devenir ingénieur en systèmes embarqués car j'ai constaté que ces compétences ne sont plus aussi courantes qu'avant. De plus, de nombreux étudiants et débutants me demandent comment ils pourraient devenir développeurs en systèmes embarqués et ingénieurs du noyau Linux.

Cette page ne peut pas inclure tous les liens/livres/cours. Par exemple, cette page présente Arduino mais il n'y a pas d'informations détaillées sur Arduino et les systèmes embarqués. Vous devriez aller plus loin par vous-même. Vous avez le mot-clé "Arduino" avec lequel vous pouvez commencer. Donc, votre prochaine étape est probablement de googler "Arduino", d'acheter un kit et de faire quelque chose par vous-même, pas de collecter des liens ou des livres gratuits. N'oubliez pas que cette page n'est qu'une feuille de route pour les débutants.

La programmation de bas niveau fait partie de l'informatique.
Absolument, il serait beaucoup mieux d'obtenir d'abord une éducation en informatique. 
* `EN` [Chemin vers une éducation autodidacte gratuite en informatique !](https://github.com/ossu/computer-science)


## <a name="Qu'est-ce-que-le-bas-niveau-?"></a>Qu'est-ce que le bas niveau ?

 Je classe la programmation de bas niveau comme une programmation très proche de la machine, en utilisant un langage de programmation de bas niveau comme C ou l'assembleur. Cela contraste avec la programmation de haut niveau, typique des applications utilisateur, utilisant des langages de haut niveau (par exemple Python, Java).
* `FR` [Wikipedia: Langage de programmation de bas niveau](https://fr.wikipedia.org/wiki/Langage_de_programmation_de_bas_niveau)

Oui, la programmation système est un concept très proche de la programmation de bas niveau. Cette page inclut la conception matérielle et le développement de micrologiciels qui ne sont pas inclus dans la programmation système.
* `EN` [Wikipédia: Programmation système](https://en.wikipedia.org/wiki/System_programming)

Enfin, cette page couvre des sujets allant des composants matériels au noyau Linux. C'est une énorme gamme de couches. Un document d'une page ne peut jamais couvrir les détails de toutes les couches, donc l'objectif de ce document est de servir de point de départ pour la programmation de bas niveau.

##  <a name="Théorie"></a>Théorie

Il y a deux théories de fond pour la programmation de bas niveau:
* Architecture des ordinateurs
* Systèmes d'exploitation

Je pense que le meilleur moyen d'apprendre la théorie est de suivre un cours. Lire des livres n'est pas mal mais prend trop de temps et d'efforts. Vous pouvez trouver de nombreuses bonnes classes sur les universités en ligne, par exemple Coursera.org et edx.org.
La théorie est la théorie. Je ne pense pas que vous ayez besoin d'obtenir un A+ en classe, comprenez juste les grandes lignes.
Vous vous améliorerez de mieux en mieux avec l'expérience.

Je vous présenter plusieurs livres que j'ai lus. Ils sont couramment utilisés comme manuels dans les universités. S'il n'y a pas de classe avec ces livres dans votre université, il vaut la peine d'y consacrer un peu de temps.
* Livres sur l'Architecture d'ordinateurs
  * `FR` Architecture des ordinateurs, cinquième édition: une approche quantitative
  * `EN` Computer Systems: A Programmer's Perspective
  * `EN` Computer Organization and Design, Fourth Edition: The Hardware/Software Interface
* Systèmes d'exploitation 
  * `EN` The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * `FR` La conception du système d'exploitation UNIX par Maurice Bach
  * `EN` Operating Systems: Internals and Design Principles by William Stallings
* Cours recommandés
  * `EN` [CS401: Operating Systems par saylor.org](https://learn.saylor.org/course/view.php?id=94)
* Compétences générales en programmation
   * `EN` [Structure et interprétation des programmes informatiques](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs)
      * C'est de la façon d'être un bon programmeur logiciel. Vous avez besoin non seulement de théorie mais aussi de techniques car la programmation est une sorte d'artisanat.
      * Si vous apprenez Lisp/Scheme, vous devriez être capable d'apprendre rapidement n'importe quel autre langage.
      * `EN` [J'ai résolu environ 80 % des exercices. Cela vaut la peine d'essayer chaque exercice unique.](https://github.com/gurugio/sicp_exercise)
* Conception de matériel
   * Construisez votre propre kit de microprocesseur 8086
      * Si vous ne construisez pas votre carte matériel, vous ne comprenez pas ce qu'est un périphérique mémoire mappé physiquement.
      * Les AP modernes incluent tellement d'IPs. Donc, vous n'avez pas la chance de comprendre comment le noyau CPU et les périphériques sont connectés.
      * Lorsque vous construisez votre propre kit 8086, vous avez la chance de localiser chaque périphérique sur la mémoire physique. Et vous pouvez définir comment les principaux composants de matériel (BUS, IRQ, horloge, alimentation, etc.) fonctionnent avec vos propres yeux.
      * J'ai construit le kit 8086 dans mon université. C'était l'un des cours les plus précieux que j'ai jamais suivis. Essayez de construire votre propre kit de matériel. Ce serait mieux si le matériel est plus ancien et plus simple car vous devriez faire plus par vous-même.
      * Google "kit 8086". Vous pourriez trouver certains sites Web où vous pouvez acheter un schéma matériel, des pièces et des manuels.

Il y a une liste infinie de bons livres. Je ne veux pas dire que vous devriez lire de nombreux livres. Il suffit de lire un livre avec soin. Chaque fois que vous apprenez une théorie, implémentez le code de simulation de celui-ci. **La mise en œuvre d'une chose vaut mieux que de connaître une centaine de théories.**

##  <a name="Langages"></a>Langages

### <a name="Assemblage"></a>Assemblage

Choisissez entre de l'architecture x86 ou ARM. Pas besoin de connaître les deux. Peu importe de connaître le langage d'assemblage. L'essentiel est de comprendre les internes d'un processeur et d'un ordinateur. Vous n'avez donc pas besoin de pratiquer l'assemblage du dernier CPU. Sélectionnez 8086 ou Corex-M.

* `EN` [8086 Programmation d'assemblage avec EMU8086](https://github.com/gurugio/book_assembly_8086)
    * Concepts de base de la processeur et de l'architecture informatique
    * Concepts de base du langage de programmation C
* `EN` [64bit Assembly Programming (traduction en cours)](https://github.com/gurugio/book_assembly_64bit)
    * Concepts de base du processeur moderne et de l'architecture informatique
    * Concepts de base de désastre et de débogage du code C
    * _Il y a de besoin d'aide à traduire._
* `EN` [Assemblage d'apprentissage pour Linux-x64](https://github.com/0xax/asm)
    * Programmation d'assemblage 64 bits pure avec NASM et assemblage en ligne avec GCC
* `EN` [ARM Architecture Reference Manual, 2e édition](https://www.amazon.com/ARM-Architecture-Reference-Manual-2nd/dp/0201737191)
    * Référence complète sur la programmation des bras
* Organisation et conception informatiques
    * `EN` [Édition MIPS](https://www.amazon.ca/computer-organisation-design-mips-interface/dp/0124077269/)
    * `EN` [Édition ARM](https://www.amazon.ca/computer-organisation-design-arm-interface/dp/0128017333/)
    * `EN` [Édition RISC-V](https://www.amazon.com/computer-organisation-design-derish-vchitecture/dp/0128122757)
    * Livres universitaires qui expliquent comment chaque composant d'un ordinateur fonctionne à partir de zéro.
    * Explique en détail les différents concepts qui composent l'architecture informatique.
    * Ils ne sont pas destinés aux lecteurs qui souhaitent devenir compétents dans un langage d'assemblage spécifique.
    * L'édition MIPS et ARM couvre les mêmes sujets mais en disséquant une architecture différente.
    * Les deux éditions contiennent des exemples dans le monde x86

### <a name="Langage-C"></a>Langage-C

Il n'y a pas de raccourci. Il suffit de lire tout le livre et de résoudre tous les exercices.

* `EN` [C Programming: A Modern Approach, 2e édition](https://www.amazon.com/c-programming-modern-approach-2nd/dp/0393979504)
* `EN` [The C Programming Language, 2e édition](https://www.amazon.com/programming-anguage-brian-w-kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=utf8&psc=1&refrid=60r1d2chba8dhyt6jnmn)
* Modern C: Jens Gustedt. Manning, 2019, 9781617295812. FFHAL-02383654F
   * Pour une nouvelle norme de C
* `EN` [La programmation parallèle est-elle difficile et, si oui, que pouvez-vous faire à ce sujet?](Https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
   * Implémentation âpre de la synchronisation avec C
   * Essentiel pour la programmation C à grande échelle (en particulier pour la programmation du noyau)
* `EN` [C Tutoriels basés sur le projet?](Https://www.reddit.com/r/c_programming/comments/872rlt/c_project_based_tutorials/)
   * Si vous finissez de lire un ou deux livres de programmation C, il faut s'appliquez à quelque chose.
   * Choisissez ce que vous voulez.
   * Faites d'abord vous-même, puis comparez avec le code source de quelqu'un d'autre. Il est très important de comparer votre source et d'autres. Vous ne pouvez améliorer vos compétences que lorsque vous lisez le code source des autres et apprendre de meilleures méthodes. Les livres sont inflexible et le code source est en direct.
* `EN` [C et autres projets basés sur les langues](https://github.com/danistefanovic/build-your-own-x)
   * Trouvez des projets plus intéressants
* `EN` [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
   * Référence sur l'optimisation en utilisant C et un peu d'assemblage x86
   * Commence du 8088 à aujourd'hui
   * Focus spécial sur l'optimisation des graphiques de bas niveau
* `EN` [Framework and Plugin Design in C](https://github.com/gurugio/book_cprogramming)
   * Comment développer le framework et le plugin en C pour les logiciels à grande échelle
   * Conseils de programmation très basiques pour la lecture de le code source du noyau Linux

Si vous souhaitez être expert de la programmation C, visitez  `EN` https://leetcode.com/. Bonne chance!

### <a name="Langage-Rust"></a>Rust

Je suis sûr que le prochain langage pour la programmation des systèmes serait Rust.
Je ferai une liste ce que j'ai fait pour apprendre Rust.

`EN` [Linus Torvalds a déclaré "Sauf quelque chose d'étrange, il arrivera en 6.1."](Https://www.zdnet.com/article/linus-torvalds-rust-will-go-into-linux-6-1/)

* `FR` [The Rust Programming Language](https://jimskapt.github.io/rust-book-fr/)
   * Introduction excellente, mais il manque d'exemples et d'exercices.
* `EN` [Rust par l'exemple](https://doc.rust-lang.org/rust-by-example/)
   * En lisant "The Rust Programming Language", vous pouvez trouver des exemples et des exercices ici.
   * Mais il n'y a pas beaucoup d'exercices que vous pouvez faire quelque chose pour vous-même. Seuls quelques exemples comprennent des exercices «à faire» et ils sont très simples.
* `EN` [Programming Rust, 2e édition](https://www.oreilly.com/library/view/Programming-Rust-2nd/9781492052586/)
   * Introduction plus profonde, mais toujours manque d'exemples et d'exercices.
* `EN` [Des Exercices](https://exercism.org/tracks/rust)
   * De bons exercices pour pratiquer les caractéristiques indivisuelles de Rust.
   * Je ne suis pas sûr que les mentors travaillent activement, mais ce serait suffisant pour comparer votre solution avec les autres.
     * Après avoir soumis votre solution, vous pouvez voir les solutions des autres avec l'onglet "Solutions communautaires" (depuis l'exercice v3).
     * De nombreux exercices de niveau facile sont destinés aux fonctionnalités utilitaires telles que la carte / filtre / tout et etc.
* `EN` [Rust Easy](https://dhghomon.github.io/easy_rust/)
   * Un livre écrit en anglais simple.
   * Leçons YouTube fourni: https://www.youtube.com/playlist?list=plfllocyhvgsrwlktahg0e-2qxcf-ozbkkk
* `EN` [Let's Get Rusty](https://www.youtube.com/c/letsgetrusty)
   * Il y a beaucoup de YouTubers à télécharger le cours de Rust, mais j'ai le plus apprécié ce cours.
   * Il a téléchargé les dernières nouvelles pour Rust. Il vaut la peine de s'abonner.
* `EN` [Rust en Linux](https://github.com/rust-for-linux)
   * Voir l'exemple de sources et vérifier comment Rust va entrer dans le noyau Linux

##  <a name="Applications"></a>Applications

### <a name="Matériel-et-micrologiciel"></a>Matériel & Micrologiciel

Si vous voulez être ingénieur en systèmes embarqués, il serait préférable de commencer par un simple kit matériel, plutôt que de commencer avec le dernier jeu de puces ARM.

* `EN` [Kit de démarrage Arduino](https://www.arduino.cc/)
  * Il existe de nombreuses séries d'Arduinos mais le "Kit de démarrage Arduino" a le processeur le plus simple (Atmega328P) et le livre de guide
  * L'Atmega328P a un cœur 8 bits qui est un bon endroit pour commencer la conception de circuits numériques et le développement de microprogrammes.
  * Vous n'avez pas besoin de savoir comment dessiner des schémas et des plans et assembler les puces. 
  * Mais vous devez savoir comment lire les schémas et comprendre comment les puces sont connectées.
  * Les développeurs de micrologiciels doivent être capables de lire les schémas et de comprendre comment envoyer des données au périphérique cible.
  * Suivez le guide !
* `EN` [Manuel 8086](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * Si vous débutez dans l'architecture x86, le 8086 est également un très bon guide pour l'architecture du processeur et l'assemblage 80x86.
* `EN` [Manuel 80386](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Meilleur guide pour le mode protégé et le mécanisme de pagination du processeur 80x86
  * Version Web:  `EN` https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

À ce stade, vous devriez être en mesure de commencer le dernier processeur ARM ou x86.
*  `EN` https://www.raspberrypi.org/
*  `EN` https://beagleboard.org/
*  `EN` https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Par exemple, la carte Raspberry Pi (rPi) possède un processeur Cortex-A53 qui prend en charge un jeu d'instructions 64 bits.
Cela vous permet de découvrir une architecture de processeur moderne avec rPi.
Oui, vous pouvez l'acheter... mais... qu'allez-vous en faire ?
Si vous n'avez pas de projet cible, vous seriez susceptible de jeter le matériel dans un tiroir et de l'oublier comme les autres gadgets que vous avez peut-être achetés auparavant.

Donc, je vous recommande un projet pour vous.
* [Faire votre propre noyau](http://wiki.osdev.org/getting_started)
   * Bonnes références: https://www.reddit.com/r/osdev/
* [Développement du système d'exploitation d'apprentissage à l'aide du noyau Linux et de Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
   * (Description du projet) Ce référentiel contient un guide étape par étape qui enseigne comment créer un simple noyau de système d'exploitation (OS) à partir de zéro ... (skip) ... chaque leçon est conçue de telle manière que Il explique d'abord comment certaines fonctionnalités du noyau sont implémentées dans le rPi OS, puis il essaie de démontrer comment la même fonctionnalité fonctionne dans le noyau Linux.

J'ai fait [un petit noyau](https://github.com/gurugio/caos) qui prend en charge le mode long 64 bits, la pagination et la commutation de contexte très simple. Faire un petit noyau est un bon moyen de comprendre l'architecture informatique moderne et le contrôle du matériel.

En fait, vous avez déjà le dernier processeur et les derniers appareils matériels.
Ton ordinateur portable! Votre bureau! Vous avez déjà tout ce dont vous avez besoin pour commencer!
Vous n'avez rien à acheter.
L'émulateur Qemu peut imiter les derniers processeurs ARM et processeurs Intel.
Donc, tout ce dont vous avez besoin est déjà à portée de main.
Il existe de nombreux grains de jouets et documents auxquels vous pouvez vous référer.
Installez simplement l'émulateur Qemu et faites un minuscule noyau qui bottise, allume la pagination et imprime certains messages.

Des autres petites noyau:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01

### <a name="Linux-noyau-et-pilote-de-périphérique"></a>Linux noyau et pilote de périphérique

Vous n'avez pas besoin de faire un système d'exploitation complet. Rejoignez la communauté Linux et participez au développement.

Quelques ressources pour le développement de pilotes de périphériques et de noyaux Linux, du débutant à l'avancé.
* Livres: Lisez ce qui suit dans l'ordre
  * `EN` [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * Les concepts de base d'Unix sont appliqués à tous les systèmes d'exploitation.
    * Ce livre est un très bon resource pour apprendre les concepts de base des systèmes d'exploitation.
  * `EN` [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Faites tous les exemples par vous-même
  * `EN` [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Comprendre la conception du noyau Linux
  * `EN` [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Lisez ce livre et le code source du noyau v2.6 en même temps
    * Ne commencez jamais par la dernière version, v2.6 est suffisant !
    * Utilisez qemu et gdb pour exécuter le code source du noyau ligne par ligne
      * `EN` http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu
      * `EN` https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * Utilisez busybox pour créer le système de fichiers le plus simple qui ne prend qu'une seconde pour démarrer
      * `EN` https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Autres ressources: ressources gratuites que je recommande 
  * `EN` [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * Guide pratique et excellents exercices de création de pilotes de périphériques Linux avec les API de noyau essentielles
    * Je pense que ce document présente presque toutes les API de noyau essentielles.
  * `EN` [Le défi Eudyptula](http://eudyptula-challenge.org/)
    * _Malheureusement, ce défi n'accepte plus de nouveaux challengers car il n'y a plus de défi._ Le mainteneur a dit qu'il prévoyait un nouveau format. J'espère qu'il reviendra dès que possible.
      * Mais vous pouvez trouver les questions du défi avec Google. Certaines personnes ont déjà téléchargé ce qu'elles ont fait. Trouvez les questions et essayez de les résoudre par vous-même, puis comparez votre solution avec celles des autres.
    * C'est comme un excellent professeur privé qui vous guide sur ce qu'il faut faire.
    * Si vous ne savez pas quoi faire, commencez simplement par cela.
  *  `EN` [Apprendre le développement de systèmes d'exploitation à l'aide du noyau Linux et du Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
     * Ce projet n'est pas encore terminé.
     * Je pense toujours que créer un noyau similaire au noyau Linux est le meilleur moyen de comprendre le noyau Linux.
  * `EN` [Couche de bloc et pilote de périphérique](https://github.com/gurugio/book_linuxkernel_blockdrv)
    * commencez par un exemple simple de pilote de périphérique de bloc (ramdisk) avec le mode multi-files d'attente
    * allez de l'avant vers la couche de bloc
    * J'ai terminé la traduction en anglais. Envoyez-moi vos commentaires.
  * `KO` [Pilote md du noyau Linux (coréen)](https://github.com/gurugio/book_linuxkernel_md)
    * comment l'outil mdadm fonctionne et comment il appelle le pilote md
    * comment fonctionne le pilote md
  * `EN` [Un code source de noyau Linux lourdement commémoré](http://www.oldlinux.org/)
    * Commentaires profonds pour l'ancien Linux v0.12.
    * Il serait bon de commencer par un OS ancien et simple.
    * Version Unix: `EN` [Commentaire de Lions sur UNIX 6e édition, avec code source](https://en.wikipedia.org/wiki/Lions%27_Commentary_on_UNIX_6th_Edition,_with_Source_Code)

#### <a name="Références"></a>Références

Vérifiez lorsque vous avez besoin de quelque chose

* `EN` [Page d'accueil bootlin](https://bootlin.com/docs/)
  * de nombreux fichiers de diapositives présentant de bons sujets, spécialement ARM-linux
* `EN` [Publication de Julia Evans: Vous pouvez être un hacker de noyau !](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * guide pour commencer la programmation de noyau

### <a name="Autres-applications"></a>Autres applications

Oui, vous n'êtes peut-être pas intéressé par Linux ou le micrologiciel. Si tel est le cas, vous pouvez trouver d'autres applications:
* Programmation de systèmes Windows et pilotes de périphériques
* Sécurité
* Rétro-ingénierie

Je n'ai aucune connaissance sur ces applications. Veuillez m'envoyer toute information pour les débutants.

**Les noyaux et les pilotes ne sont pas toute la programmation de bas niveau.** Une autre application importante de la programmation de bas niveau est le stockage défini par logiciel ou le système de fichiers distribué. La description détaillée de ceux-ci dépasse le cadre de ce document, mais il existe un excellent cours où vous pouvez essayer un simple système de fichiers distribué.
* Cours: `EN` https://pdos.csail.mit.edu/archive/6.824-2012/
* Source de référence: `EN` https://github.com/srned/yfs

## <a name="L'avenir-de-la-programmation-de-bas-niveau"></a>L'avenir de la programmation de bas niveau

Je ne connais pas l'avenir, mais je tiens Rust en compte.
* `EN` https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Si je pouvais avoir une semaine de libre et seul, j'apprendrais Rust.
C'est parce que Rust est le dernier langage avec lequel je peux développer des pilotes de périphériques Linux.
* `EN` https://github.com/tsgates/rust.ko

L'IdO est une nouvelle tendance, il vaut donc la peine de vérifier quels sont les systèmes d'exploitation pour l'IdO.
ARM, Samsung et certaines entreprises ont leur propre système d'exploitation en temps réel mais malheureusement beaucoup d'entre eux sont à code propriétaire (source fermé).
Mais la Fondation Linux a également une solution: Zephyr
* `EN` https://www.zephyrproject.org/

Les serveurs cloud typiques ont de nombreuses couches ; par exemple, le système d'exploitation hôte, le pilote kvm, le processus qemu, le système d'exploitation guest et l'application de service. Un conteneur a été développé pour fournir une virtualisation légère. Dans un avenir proche, un nouveau concept de système d'exploitation, un soi-disant système d'exploitation de bibliothèque ou Unikernel, remplacerait la pile logicielle typique pour la virtualisation.
* `EN` http://unikernel.org/

Le Big Data et le cloud computing nécessitent un stockage de plus en plus important. Certains disques connectés directement aux machines serveurs ne peuvent pas satisfaire la capacité, la stabilité et les performances requises. Par conséquent, des recherches ont été menées pour créer d'énormes systèmes de stockage avec de nombreuses machines de stockage connectées par un réseau haut débit. L'objectif était de créer un énorme volume de stockage. Mais actuellement, ils fournissent de nombreux volumes dédiés à de nombreuses machines virtuelles. 
* `EN` https://en.wikipedia.org/wiki/Software-defined_storage
* `EN` https://en.wikipedia.org/wiki/Clustered_file_system
* `EN` https://en.wikipedia.org/wiki/Ceph_(software)

## <a name="Comment-démarrer-?"></a>Comment démarrer ?

J'ai reçu un e-mail me demandant comment démarrer. Il y a pleine d'informations sur les livres, les cours et les projets dans cette page. C'est mon erreur d'avoir oublié d'écrire comment démarrer. Malheureusement, il n'y a pas de route royale vers `EN` [King's Landing](https://gameofthrones.fandom.com/wiki/King%27s_Landing). Je vais simplement écrire ce que j'ai fait dans l'ordre. Si vous avez déjà fait quelque chose, veuillez le ignorer. Tiens en compte, c'est juste un exemple que vous pouvez suivre dans l'ordre, au cas où vous ne sauriez pas comment démarrer ou quoi faire.

* Lire les livres de théorie des systèmes d'exploitation: au moins "The Design of the UNIX Operating System" par Maurice J. Bach
* Apprendre l'assemblage et C
  * `EN` [Programmation en assembleur 8086 avec emu8086](https://github.com/gurugio/book_assembly_8086)
    * Il suffit de comprendre le concept de la programmation en assembleur. Vous n'avez pas besoin de faire quelque chose de pratique.
  * `EN` [The C Programming Language, 2e édition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
    * FAITES DE VOTRE MIEUX pour résoudre chaque exercice !
  * `EN` [C Programming: A Modern Approach, 2e édition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Faites quelque chose de pratique avec C
  * `EN` [Tutoriels de projet basés sur C ?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): trouvez un ou deux projets intéressants et faites votre propre projet.
  * `EN` [leetcode.com](https://leetcode.com/): Si vous ne trouvez pas de projet intéressant, il serait également bon de vous concentrer sur la structure de données et les algorithmes.
* Faire un projet matériel
  * Choisissez Raspberrypi ou Arduino, peu importe lequel. Vous avez besoin d'expérience pour contrôler un matériel directement avec seulement C. UNIQUEMENT C !
  * Je vous recommande d'acheter un kit Atmega128 et de créer un micrologiciel pour allumer/éteindre des LED, détecter l'entrée d'un commutateur et afficher un message sur l'écran LCD texte. Le programme de contrôle de moteur est également un très bon projet: par exemple, le traceur de ligne.
  * N'UTILISEZ AUCUNE bibliothèque. Vous devez tout faire par vous-même, sauf le téléchargeur de programme.  
* Notions de base du noyau Linux
  * La programmation de bas niveau est très proche du système d'exploitation. Vous devez connaître l'intérieur du système d'exploitation.
  * Commencez avec les pilotes
    * Lisez `EN` [Pilotes de périphériques Linux](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * `EN` [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * `EN` [Le défi Eudyptula](http://eudyptula-challenge.org/)
  * Lisez `EN` [Linux Kernel Driver Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) pour comprendre l'interne du noyau Linux.
* Aller dans le domaine professionnel
  * Si vous souhaitez devenir développeur professionnel de noyaux Linux
    * doit lire `EN` [Comprendre le noyau Linux](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+noyau)
      * Essayez ensuite de créer un noyau petit
      * `EN` [Apprendre le développement de systèmes d'exploitation à l'aide du noyau Linux et du Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
      * `EN` [Créer votre propre noyau](http://wiki.osdev.org/Getting_Started) 
      * Écrivez le lien github vers votre noyau sur votre CV (n'oubliez pas d'écrire la description détaillée dans le message de validation)
    * Consultez les derniers problèmes sur `EN` https://lwn.net/ et rejoignez-le.
      * Consultez les "Correctifs de noyau récents" à `EN` "https://lwn.net/Kernel/" ou le lien direct `EN` https://lwn.net/Kernel/Patches
      * Trouvez un correctif qui vous intéresse. Essayez de comprendre le code source. Bien sûr, ce sera vraiment difficile, mais essayez. Vous vous rapprocherez de plus en plus à chaque fois que vous essayerez.
      * Générez le noyau et testez-le sur votre système. Par exemple, test de performances, test de stabilité avec LTP (`EN` https://linux-test-project.github.io/) ou outils d'analyse de code statique à l'intérieur du noyau.
      * Signalez tout problème si vous en trouvez: avertissements/erreurs de compilation, dégradation des performances, panique du noyau/oops ou tout autre problème
      * Si cela fonctionne bien, rapportez-le avec les spécifications de votre système. Le propriétaire du correctif écrira une balise "Reviewed-by" avec votre nom.
      * Trouvez votre nom dans le journal git du noyau
  * Ou trouvez d'autres sujets
    * Il existe de nombreuses spécialités où l'ingénieur de bas niveau peut travailler: sécurité, compilateur, micrologiciel, robot / voiture, etc.

# <a name="Traduction"></a>Traduction

Veuillez m'envoyer une pull request si vous souhaitez traduire cette page. Je la répertorierai ici.

# <a name="qui-suis-je"></a>Qui suis-je ?

Je suis inspiré par [google-interview-university](https://github.com/jwasham/google-interview-university). J'aimerais partager mon expérience et montrer une feuille de route pour devenir ingénieur(e) en systèmes embarqués car j'ai constaté que ces compétences ne sont plus aussi courantes qu'avant. De plus, de nombreux étudiants et débutants me demandent comment ils pourraient devenir programmeurs de bas niveau et ingénieurs de noyaux Linux.

Pour votre information, j'ai plus de 10 ans d'expérience en tant que ingénieur en systèmes embarqués:
* Programmation en assembleur 80x86
* Périphérique matériel avec puce Atmel et micrologiciel 
* Programmation système en langage C pour Unix
* Pilote de périphérique dans Linux
* Noyau Linux: allocation de pages
* Noyau Linux: pilote de périphérique de bloc et module md
