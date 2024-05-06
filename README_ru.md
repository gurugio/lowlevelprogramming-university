* [Университет Низкоуровневого Программирования](#Low-Level-Programming-University)
  * [Что это такое?](#What-is-it)
  * [Что значит "низкоуровневый"?](#What-Is-the-Low-Level)
  *  [Теория](#Theory)
  *  [Языки](#Languages)
     * [Ассемблер](#Assembly)
     * [Язык C](#C-language)
     * [Язык Rust](#Rust-language)
  * [Приложения](#Applications)
    * [Железо && Прошивки](#Hardware-Firmware)
    * [Ядро Linux и драйвера устройств](#Linux-kernel-and-device-driver)
      * [Следуй осторожно](#Follow-carefully)
      * [Ссылки](#References)
    * [Прочие приложения](#Other-applications)
  * [Будущее низкоуровневого программирования](#Future-of-low-level-programming)
  * [Как начать?](#How-to-start)
* [Перевод](#Translation)
* [Кто я такой?](#who-am-i)

# Университет Низкоуровневого Программирования

## <a name="What-is-it"></a>Что это такое?

Вдохновляясь [google-interview-university](https://github.com/jwasham/coding-interview-university), мне бы хотелось поделиться опытом и показать путь к становлению программистом низкого уровня, потому что соответствующие навыки перестали быть столь обыденными, каковыми были раньше. К тому же, многие учащиеся и просто новички часто меня сами спрашивают, как стать низкоуровневым программистом и разработчиком ядра Linux в частности.

Очевидно, что на одной странице нельзя указать каждую ссылку/книгу/курс. То есть, хоть эта страница и представляет читателю Arduino, на ней нет более детальной информации о ней и встраиваемых системах. Идти дальше необходимо самому. Имея ключевое слово "Arduino", можно воспользоваться поисковыми сервисами, купить кит и начать делать с ним что-нибудь самому, а не просто собирать ссылки и бесплатные книги. Прошу помнить, что вся эта страница является лишь путеводителем для новичков.

Прим. [переводчика](https://github.com/LabunskyA):
не для всех ссылок и книг существует русский аналог или перевод. Тех, что нашел, должно быть достаточно для начала пути, но, в любом случае, английский язык является необходимым навыком для успешного развития своих навыков в данной сфере. Поэтому к оригинальным совета добавлю от себя: **учи английский**.

## <a name="What-Is-the-Low-Level"></a>Что значит "низкоуровневый"?

Я определяю низкоуровневое программирование как очень близкое к устройству, используя низкоуровневые языки программирования, такие как C или ассемблер, на контрасте с высокоуровневым программированием, типичного для приложений в user-space, использующим языки высокого уровня (такие как Python, Java).
* [Wikipedia: Low-level programming language](https://en.wikipedia.org/wiki/Low-level_programming_language), [на русском](https://ru.wikipedia.org/wiki/Низкоуровневый_язык_программирования)

Да, системное программирование является очень близким по смыслу концептом к низкоуровневому программированию. Но эта страница также включает проектирование аппаратных средств и разработку прошивок, которые не входят в понятие системного программирования.
* [Wikipedia: System programming](https://en.wikipedia.org/wiki/System_programming), [на русском](https://ru.wikipedia.org/wiki/Системное_программное_обеспечение)

Наконец, эта страница включает темы от аппаратных компонентов до ядра Linux. Между ними невероятно большое число слоев. Документ на одну страницу никогда не сможет покрыть детали каждого из них, поэтому его целью является лишь дать точку входа в мир низкоуровневого программирования. 

##  <a name="Theory"></a>Теория

Низкоуровневое программирование базируется на двух теориях:
* Архитектура Компьютеров
* Операционные Системы

Мне кажется, лучший способ выучить теорию - пройти соответствующий курс. Чтение книг само по себе не плохо, но отнимает слишком много времени и сил. При желании, можно найти много хороших курсов в онлайн университетах, в частности, на coursera.org и edx.org.
Но теория - это лишь теория. Не думаю, что необходимо закончить курс на отлично, чтобы понять общую суть.
Ты будешь становиться лучше и лучше с ростом опыта.

Позволь мне представить несколько книг, которые я читал. Они широко используются в качестве учебников в университетах. Если их нет или не было у читателя в университете, то стоит потратить немного времени на ознакомление. 
* Архитектура Компьютеров
  * Computer Architecture, Fifth Edition: A Quantitative Approach 
  * [Компьютерная Архитектура. Количественный подход. Издание 5-е](http://www.technosphera.ru/files/book_pdf/0/book_348_882.pdf)
  * Computer Systems: A Programmer's Perspective 
  * [Компьютерные системы: архитектура и программирование](https://www.ozon.ru/context/detail/id/2355879/) 
  * Computer Organization and Design, Fourth Edition: The Hardware/Software Interface 
  * [Архитектура компьютера и проектирование компьютерных систем](https://www.labirint.ru/books/317754/)
* Операционные системы
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System 
  * [Архитектура операционной системы Unix](http://lib.ru/BACH/)
  * Operating Systems: Internals and Design Principles by William Stallings 
  * [Операционные системы](https://www.ozon.ru/context/detail/id/1150703/)
* Рекомендуемые курсы
   * [CS401: Operating Systems](https://learn.saylor.org/mod/page/view.php?id=921)

Список хороших книг бесконечен. Не хочу сказать, что нужно перемолоть множество книг: достаточно и одной, но прочитанной внимательно. Когда бы ты не учил теорию, попробуй свои силы в ее реализации. **Одна практическая реализация лучше, нежели знание сотни теорий**

##  <a name="Languages"></a>Языки

### <a name="Assembly"></a>Ассемблер

Выбери один, х68 или ARM. Нужды знать оба нет смысла. Не имеет смысла даже знать сам язык по себе. Суть состоит в понимании внутренности процессора и компьютера в целом. То есть, нет нужды практиковаться в ассемблере самой последней модели. Выбери 8086 или Cortex-M.

* [Программирование на ассемблере 8086 с помощью emu8086](https://github.com/gurugio/book_assembly_8086)
  * базовые концепты процессора и архитектуры компьютера
  * базовые концепты языка программирования C
* [Программирование на 64-битном ассемблере (перевод на англ. в процессе)](https://github.com/gurugio/book_assembly_64bit)
  * базовые концепты современного процессора и архитектуры компьютера
  * базовые концепты дезассемблирования и отладки кода на C
  * _нужна помощь в переводе на английский_
* [ARM Architecture Reference Manual, 2nd Edition](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-9780201737196)
  * Полная справка по программированию на ARM
* [Паттерсон, Хеннесси: Архитектура компьютера и проектирование компьютерных систем](https://www.labirint.ru/books/317754/)
  * [MIPS Edition](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [ARM Edition](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * [RISC-V Edition](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757)
  * Академические книги, объясняющие работу каждого компонента компьютера с самых основ.
  * Объясняют в деталях разные концепты, составляющие архитектуру компьютера.
  * Они не нацелены на читателец, которые хотят стать специалистами в каждом отдельном языке ассемблера.
  * Издания для MIPS и ARM покрывают одни и те же темы, различающиеся архитектурами.
  * Оба издания содержат примеры из мира x86

### <a name="C-language"></a>Язык C

Тут коротких путей нет. Просто читай всю книгу и решай все упражнения.

* [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN) 
* [Брайан У. Керниган, Деннис М. Ритчи, Язык программирования C, 2-е издание](https://www.ozon.ru/context/detail/id/2480925/)
* [Modern C](http://icube-icps.unistra.fr/img_auth.php/d/db/ModernC.pdf)
  * Для нового стандарта C
* [Is Parallel Programming Hard, And, If So, What Can You Do About It?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * базовая реализация синхронизации в C
  * Необходим для крупномасштабного программирования на C (особенно, для программирования на уровне ядра)
* [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * Если ты закончил читать одну или две книги по C, то ты ДОЛЖЕН начать делать что-нибудь.
  * Выбери что угодно по нраву.
  * Сначала, сделай что-нибудь свое, после чего сравни с чужим исходным кодом. Очень важно проводить подобные сравнения. Улучшить свои навыки можно только при чтении чужого кода, обучаясь использованию лучших методов. Книги мертвы, код же живет.
* [Проекты на C и других языках](https://github.com/danistefanovic/build-your-own-x)
  * Найди больше интересных проектов
* [Michael Abrash’s Graphics Programming Black Book, Special Edition](http://www.jagregory.com/abrash-black-book/)
  * Справочник по оптимизации с использованием C и капли ассемблера x86
  * Начиная с 8088 до сегодняшнего дня
  * Особый фокус на низкоуровневых оптимизациях графики
* [Framework and plugin design in C (Korean)](https://github.com/gurugio/book_cprogramming)
  * Как разработать фреймворк и плагин на C для крупномасштабного ПО
  * Планируется перевод на английский

Если хочешь стать экспертном в программировании на C, посети https://leetcode.com/. Удачи!

### <a name="Rust-language"></a>Язык Rust

Я уверен, что следующий язык для системного программирования будет Rust. 
Я предоставлю лист того что я делал чтобы выучить Rust.

[Линус Торвальдс сказал - "Если резко обстоятельства не изменятся, то он [Rust] появится в 6.1."](https://www.zdnet.com/article/linus-torvalds-rust-will-go-into-linux-6-1/)

* [The Rust Programming Language](https://doc.rust-lang.org/book/)
  * Хорошо для знакомства с языком, но имеет мало примеров и упражнений.
* [Rust by Example](https://doc.rust-lang.org/rust-by-example/)
  * Пока читаешь "The Rust Programming Language", можешь находить примеры и упражнения здесь.
  * Но здесь не так много упражнений которые ты можешь сделать для себя. Только некоторые примеры включают в себя "сделай это" упражнения, и они очень простые.
* [Programming Rust, 2nd](https://www.oreilly.com/library/view/programming-rust-2nd/9781492052586/)
  * Глубокое ознакомление с языком, но также имеет мало примеров и упражнений.
* [Exercism](https://exercism.org/tracks/rust)
  * Хорошие упражнения для практики индивидуальных особенностей Rust.
  * Я не уверен что Менторы активно работают, но этого будет достаточно чтобы сравнивать свои решения с другими.
  * После отправки своего решения, ты можешь видеть решения других во вкладке "Community solutions" (с поры Exercism V3).
  * Много легких упражнений нацелено на функциональные особенности, такие как map/filter/any и т.д.
* [Легкий Rust](https://dhghomon.github.io/easy_rust/)
  * Книга написанная на несложном английском.
  * Ютуб материалы: https://www.youtube.com/playlist?list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk
* [Let's get rusty](https://www.youtube.com/c/LetsGetRusty)
  * Много ютуберов делают курсы по Rust, но этот понравился мне больше всего.
  * Он выставляет последний новости по Rust. Заслуживает подписки.
* [Rust для Linux](https://github.com/Rust-for-Linux)
  * Смотри примеры источников как Rust попал в ядро Linux

## <a name="Applications"></a>Приложения

### <a name="Hardware-Firmware"></a>Железо && Прошивки

Если хочешь стать системным инженером встраиваемых систем, то лучше начать с простых kit'ов для разработки, нежели с последнего чипсета ARM.

* [Arduino Start Kit](https://www.arduino.cc/)
  * Существует множество серий Arduino, но "Arduino Start Kit" имеет наиболее простой процессор (Atmega328P) и книгу-гайд.
  * Atmega328P имеет 8-битное ядро, с которого хорошо начинать в сфере проектирования цифровых схем и разработки прошивок.
  * Тебе не требуется знать, как создавать схематики и макеты, а так же собирать чипы.
  * Но нужно знать, как читать схематики и понимать, как чипы соединены между собой.
  * Разработчик прошивок должен уметь читать схематики и понимать, как передать данные на целевое устройство.
  * Следуй гайду!
* [8086 manual](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * Если ты не знаком с архитектурой x86, то 8086 также является хорошим гайдом архитектуры процессора и ассембрела 80x86
* [80386 manual](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * Лучший гайд защищенног режима и механизма подкачки страниц процессора 80x86
  * Веб-версия: https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm

К этому моменту, можно приступать к последним процессорам архитектур ARM и x86.
* https://www.raspberrypi.org/
* https://beagleboard.org/
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Для примера, плата Raspberry Pi имеет процессор Cortex-A53, поддерживающий 64-битный набор инструкций.
Это позволяет получить опыт в работе с современной процессорной архитектуры с помощью rPi.
Да, его можно купить... но... что ты собираешься с ним делать?
Если нет целевого проекта, скорее всего ты просто положишь плату в дальний ящик и забудешь о ней как и обо всех других, купленных до этого.

Поэтому, я рекомендую следующий проект.
* [Создание своего собственного ядра](http://wiki.osdev.org/Getting_Started)
  * Хорошие ссылки: https://www.reddit.com/r/osdev/
* [Учимся разработке операционных систем используя Linux и Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
  * (Описание проекта) Этот репозиторий содержит пошаговый гайд, учащий создавать простое ядро операционной системы с нуля...(пропуск)...Каждый урок создан таким образом, что сначала объясняет, как некоторые фичи ядра реализованы в RPI OS, и лишь потом пытается продемонстрировать работу подобного функционала в ядре Linux.

Я сделал [игрушечное ядро](https://github.com/gurugio/caos), поддерживающее 64-битный "длинный" режим, подкачку страниц и очень простое переключение контекста. создания ядра является хорошим способом понять архитектуру современного компьютера и управление "железом".

Вообще говоря, у тебя уже есть доступ к последнему процессору и последним аппаратным устройствам.
Твой ноутбук! Твой ПК! Ты уже имеешь все необходимое для старта!
Не нужно ничего покупать.
QEMU может эмулировать последние процессоры ARM и x86.
То есть, все необходимое на руках.
Существует множество игрушечных ядер и документации для справки.
Просто установи QEMU эмулятор и создай микро-ядро, которое способно загрузиться, включить подкачку и вывести текстовые сообщения. 

Другие игрушечные ядра:
* https://littleosbook.github.io/
* https://tuhdo.github.io/os01/

### <a name="Linux-kernel-and-device-driver"></a>Ядро Linux и драйвера устройств

Не нужно создавать свою полноценную операционную систему.
Присоединйяся к сообществу Linux и участвуй в разработке.

#### <a name="Follow-carefully"></a>Следуй аккуратно

* Книги (читать в следующем порядке):
  * [The Design of the Unix Operating System](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
  * [Морис Дж. Бах, Архитектура операционной системы Unix](http://lib.ru/BACH/)
    * Базовые концепты Unix применимы ко всем операционным системам.
    * Эта книга хороша для изучения ключевых концептов ОС.
  * [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel) 
  * [Дж. Корбет, Linux. Драйверы устройств](http://padabum.net/d.php?id=137122)
    * Сделай все примеры самостоятельно
  * [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) 
  * [Роберт Лав, Разработка ядра Linux](https://www.ozon.ru/context/detail/id/2918313/)
    * Пойми устройство ядра Linux
  * [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel) 
  * [Д. Бовет, Ядро Linux](https://www.ozon.ru/context/detail/id/3589107/)
    * Читай эту книгу и исходный код ядра Linux v2.6 одновременно
    * Никогда не начинай с последней версии, v2.6 будет достаточно!
    * Используй qemu и gdb для отслеживания работы кода строчка за строчкой
      * http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdЧТо за проводаb-and-qemu
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * Использый busybox для создания простейшей файловой системы, которая будет грузиться за одну секунду
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Остальные ресурсы, которые я рекомендую:
  * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * Гид по практике и отличные упражнения по созданию драйверов устройств для Linux с необходимыми API.
    * Думаю, этот документ представляет читателю практически все необходимые API ядра.
  * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
    * _К сожалению, это соревнование больше не принимает новых участников._ Мейнтейнер сказал, что планирует переход на новый формат. Надеюсь на его возвращение в скором времени.
      * Но ты можешь найти вопросы по этому соревнованию с помощью Гугла. Некоторые люди уже выложили результат своей работы. Найди вопросы и попытайся решить их самостоятельно, после чего сравни свое решение с чужими.
    * Это как иметь потрясающего частного учителя, который направляет тебя и говорит, что нужно делать.
    * Если ты не знаешь, чем заняться, просто начни с этого.
  *  [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
     * Этот проект еще не завершен.
     * Я всегда думал, что сделать ядро, похожее на Linux, является лучшим способом понять его самого.
  * [Block layer and device driver](https://github.com/gurugio/book_linuxkernel_blockdrv)
    * начни с драйвера простого блочного устройства (Ramdisk) с много-очередным режимом
    * иди дальше на уровень блоков
    * перевод на английский завершен, просьба прислать отзыв по нему.
  * [md driver of Linux kernel(Korean)](https://github.com/gurugio/book_linuxkernel_md)
    * как утилиты mdadm работают и как вызывает md driver
    * как работает сам md driver

#### <a name="References"></a>Ссылки

Посмотри здесь, если понадобится что-то еще

* [Free-electrons homepage](http://free-electrons.com/docs/)
  * множество презентаций, представляющих хорошие темы, особенно Linux на ARM
* [Julia Evans's posting: You can be a kernel hacker!](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * гид для входа в программирование уровня ядра

### <a name="Other-applications"></a>Прочие приложения

Да, ты можешь быть и не заинтересован в линуксе и прошивках. Если так, то можно найти и другие сферы:
* Системное программирование и драйвера устройств под Windows
* Безопасность
* Реверс инженеринг

У меня нет каких-либо знаний в данных сферах. Поэтому прошу отправить мне любую информацию о них для новичков.

**Ядра и драйверы - еще не все низкоуровневое программирование.** Одним из наиболее важных приложений низкоуровневого программирования являются распределенные файловые системы и хранилища. Подробное их описание находится на пределами фокуса этого документа, но существует отлличный курс, в котором можно попробовать себя в данной сфере. 
* Курс: https://pdos.csail.mit.edu/archive/6.824-2012/
* Исходный код для работы с ним: https://github.com/srned/yfs

## <a name="Future-of-low-level-programming"></a> Будущее низкоуровневого программирования

Мне неизвестно будущее, но я посматриваю на RUST.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Если бы у меня была свободная неделя в одиночестве, я бы его выучил.
Просто потому, что RUST - самый новый язык программирования, на котором возможна разработка драйверов устройств под Linux.
* https://github.com/tsgates/rust.ko

IoT теперь уже является трендом, поэтому стоит посмотреть на ОС для него.
ARM, Samsung и некоторые другие компании имеют свои собственные ОС реального времени, но, к сожалению, многие из них имеют закрытый исходный код.
Но Linux Foundation также имеет свое решение: Zephyr
* https://www.zephyrproject.org/

Обычные облачные сервера имеют множество слоев; в частности, хостовую ОС, драйвер kvm, процесс qemu, гостевая ОС и сервисное приложение. Контейнер был создан, чтобы предоставить легку. виртуализацию. В ближайшем будущем, новый концепт ОС, так называемый "библиотечная ОС" или Unikernel, может заменить типичный стэк SW для виртуализации.
* http://unikernel.org/

Big data и облачные вычисления требуют хранения все больших и больших объемов данных. Некоторые диски, напрямую подключенные к серверам, не могут удовлетворить требующуюся емкость, стабильность и производительность. Поэтому были проведены исследования для создания больших систем хранения данных с помощью множества машин, соединенных высокоскоростной сетью. Поначалу они были сфокусированы на создании одного большого тома-хранилища. Но теперь предлагаю множества томов, выделенных для множества виртуальных машин.
* https://en.wikipedia.org/wiki/Software-defined_storage
* https://en.wikipedia.org/wiki/Clustered_file_system
* https://en.wikipedia.org/wiki/Ceph_(software)

## <a name="How-to-start"></a>Как начать?

Однажды, я получил письмо с таким вопросом. На этой странице представлено множество информационных книг, курсов и проектов. И в том, что я забыл напистаь тут ответ на него - моя вина. Конечно, не существует единственного прямого пути. Я просто пишу, что делал сам и в каком порядке. Если ты уже знаком с чем-то, то можешь это пропустить. ПОВТОРЯЮ, это все лишь пример, которому ты можешь следовать. Если не знаешь, что делать, просто делай все ПО ПОРЯДКУ. 

* Чтение книг с теорией ОС: как минимум "The Design of the UNIX Operating System"
* Учеба ассемблера и C
  * [Программирование на ассемблере 8086 с помощью emu8086](https://github.com/gurugio/book_assembly_8086)
    * Этого достаточно для понимания базовых концептов программирования на ассемблере. Не нужно делать что-то на практике.
  * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
  * [Язык программирования C, 2-е издание](https://www.ozon.ru/context/detail/id/2480925/)
    * НЕ ЗАБУДЬ решить каждое управжнение!
  * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Сделай что-нибудь на C
  * [C Project Based Tutorials?](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): Найди один или два интересных проектов и сделай свой собственный.
  * [leetcode.com](https://leetcode.com/): Если не можешь найти интересный проект, будет так же полезно сфокусироваться на структурах данных и алгоритмах.
* Сделай проект с железом
  * Raspberry Pi или Arduino - это не принципиально. Тебе нужен опыт контроля железа непосредственно с помощью C. ТОЛЬКО C!
* Запрыгни в ядро Linux
  * Начни с драйверов
    * Прочти [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Или на русском: [Дж. Корбет, Linux. Драйверы устройств](http://padabum.net/d.php?id=137122)
    * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Прочти [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) для понимания внутренностей ядра Linux.
  * Или на русском: [Роберт Лав, Разработка ядра Linux](https://www.ozon.ru/context/detail/id/2918313/)
* Если ты хочешь стать разработчиком ядра Linux
  * то должен прочитать [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
  * После этого попробуй создать игручешное ядро
    * [Learning operating system development using Linux kernel and Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
    * [Making your own kernel](http://wiki.osdev.org/Getting_Started)
  * Прочитай исходный код ядра и документацию на https://lwn.net/
* Или найди другую тему.

# <a name="Translation"></a>Перевод

Присылайте мне pull-реквесты, если хотите перевести эту страницу. Я перечислю их здесь.

* [Английский (оригинал)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README.md)
* [Китайский](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cn.md)
* [Португальский (Бразильский)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_pt.md)
* [Итальянский](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_it.md)
* [Чешский](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_cz.md)
* [Русский (эта страница)](https://github.com/gurugio/lowlevelprogramming-university/blob/master/README_ru.md) 

# <a name="who-am-i"></a>Кто я такой?

Вдохновляясь [google-interview-university](https://github.com/jwasham/coding-interview-university), мне бы хотелось поделиться опытом и показать путь к становлению программистом низкого уровня, потому что соответствующие навыки перестали быть столь обыденными, каковыми были раньше. К тому же, многие учащиеся и просто новички часто меня сами спрашивают, как стать низкоуровневым программистом и разработчиком ядра Linux в частности.

Для информации, у меня более 10 лет опыта в качестве низкоуровневого программиста, мой опыт включает:
* Программирование на ассмемблере под 80x86 
* Аппаратные средства на чипах Atmel и прошивки для них
* Язык C и системное программирование под Unix
* Драйвера устройств под Linux
* Ядро Linux: подкачка страниц
* Ядро Linux: драйвер блочного устройства и md module
