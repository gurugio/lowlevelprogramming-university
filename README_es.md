NOTA1: Por favor, no copies el contenido de esta página a tu blog. Puedes compartir esta página, pero, por favor, compártela con el enlace original. Así es como agradecemos a los autores de buenos documentos y proyectos de código abierto

NOTA2: Por favor, téngase en cuenta que la programación a bajo nivel no está de moda y actualmente no hay muchas compañías contratando programadores de bajo nivel. Cada vez es más difícil encontrar trabajo de esto.
Si no has iniciado tu carrera profesional todavía, te recomiendo que consideres otros campos cuidadosamente.

NOTA3: Si quieres un inicio rápido, ve a la sección "¿Cómo empezar?"

* [Universidad de programación a bajo nivel](#Universidad-de-programación-a-bajo-nivel)
  * [Qué es](#Qué-es)
  * [Qué es el bajo nivel](#Qué-es-el-bajo-nivel)
  * [Teoría](#Teoría)
  * [Lenguajes](#Lenguajes)
    * [Ensamblador](#Ensamblador)
    * [Lenguaje C](#Lenguaje-C)
    * [Lenguaje Rust](#Lenguaje-Rust)
  * [Aplicaciones](#Aplicaciones)
    * [Hardware y firmware](#Hardware-y-firmware)
    * [Núcleo Linux y controladores de dispositivos](#Núcleo-Linux-y-controladores-de-dispositivos)
      * [Referencias](#Referencias)
    * [Otras aplicaciones](#Otras-Aplicaciones)
  * [Futuro del bajo nivel](#Futuro-del-bajo-nivel)
  * [Cómo empezar](#Cómo-empezar)
* [Traducción](#Traducción)
* [Quién soy](#Quién-soy)


# Universidad de programación a bajo nivel

## <a name="Qué-es"></a>¿Qué es?

Me inspiré en [google-interview-university](https://github.com/jwasham/coding-interview-university). Me gustaría compartir mi experiencia y mostrar un mapa de ruta para convertirse en un programador a bajo nivel porque he visto que estas habilidades ya no son tan comunes como fueron una vez. Además, muchos estudiantes y principiantes me preguntan cómo convertirse en programadores a bajo nivel e ingenieros del núcleo de Linux.

Esta página no puede incluir todos los enlaces, libros o cursos. Por ejemplo, esta página introduce Arduino, pero no información detallada sobre su relación con los sistemas embebidos. Deberás profundizar tú mismo. Tienes la palabra clave "Arduino" con la que empezar. Así que tu siguiente paso probablemente sea buscarla en Google, comprarte un kit y hacer algo por ti mismo, no acumular enlaces o libros gratis. Por favor, recuerda que esta página es sólo un mapa de ruta para principiantes.

La programación a bajo nivel es una parte de las ciencias de la computación.
Por supuesto, será mucho mejor educarse un poco sobre las ciencias de la computación primero.
* [Ruta para una educación autodidacta en ciencias de la computación](https://github.com/ossu/computer-science)

## <a name="Qué-es-el-bajo-nivel"></a>¿Qué es el bajo nivel?

Clasifico la programación a bajo nivel como aquella que es muy cercana a la máquina, usando un lenguaje de programación con capacidades de bajo nivel como C o ensamblador. En la otra mano está la programación a alto nivel, típica de las aplicaciones de espacio de usuario, utilizando lenguajes de alto nivel como Python o Java.
 * [Wikipedia: Lenguaje de bajo nivel](https://es.wikipedia.org/wiki/Lenguaje_de_bajo_nivel)

Sí, la programación de sistemas es un concepto muy cercano a la programación a bajo nivel. Esta página incluye el diseño hardware y el desarrollo de firmware, que no forman parte de la programación de sistemas.
 * [Wikipedia en inglés: Systems Programming](https://en.wikipedia.org/wiki/Systems_programming)

Por último, esta página incluye temas desde los componentes hardware hasta el núcleo Linux. Es un rango enorme con muchas capas. Un documento de una página nunca podría cubrir los detalles de todas ellas, así que el objetivo de este documento es servir como un punto de partida para la programación a bajo nivel.

## <a name="Teoría"></a>Teoría
La base teórica de la programación a bajo nivel tiene dos componentes principales:
 * La arquitectura de computadoras
 * Los sistemas operativos

Pienso que la mejor forma de aprender la teoría es tomando un curso. Leerse un libro no es mala opción, pero toma demasiado tiempo y esfuerzo. Puedes encontrar buenas clases en universidades en línea, por ejemplo [Coursera](https://www.coursera.org) y [edx](https://www.edx.org).
La teoría es teoría. No creo que necesites tener un 10 en clase, sólo entiende el panorama general.
La experiencia te hará cada vez mejor.

Déjame introducir varios libros que he leído. Son usados comúnmente como libros de texto en universidades. Si no hay ninguna clase con estos libros en tu universidad, merece la pena invertir un tiempo en leerlos. Muchos están en inglés, así como sus títulos:
* Arquitectura de computadoras
  * Computer Architecture: A Quantitative Approach, quinta edición.
  * Computer Systems: A Programmer's Perspective.
  * Computer Organization and Design: The Hardware/Software Interface, cuarta edición.
* Sistemas operativos
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design.
  * The Design of the UNIX Operating System.
  * Operating Systems: Internals and Design Principles by William Stallings.
* Cursos recomendados 
  * [CS401: Operating Systems from saylor.org](https://learn.saylor.org/course/view.php?id=94)
* Habilidad general de programación
  * [Estructura e interpretación de los programas de ordenador](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs)
    * Trata sobre cómo ser un buen programador. No necesitas sólo teoría, sino sólo técnica porque programar es un tipo de artesanía.
    * Si aprendes [Lisp](https://es.wikipedia.org/wiki/Lisp)/[Scheme](https://es.wikipedia.org/wiki/Scheme), deberías poder aprender cualquier otro lenguaje rápido.
    * [He resuelto aproximadamente el 80% de los ejercicios. Valdría la pena intentarlos todos](https://github.com/gurugio/sicp_exercise)
* Diseño Hardware
  * Kit para construir tu propio microprocesador 8086
    * Si no te construyes tu propia placa HW, no entenderás lo que es un dispositivo con memoria física mapeada.
    * Casi todo el hardware moderno está plagado de IPs (Propiedad Intelectual) de forma que no podrás saber cómo están conectados los procesadores con los periféricos, etc.
    * Cuando te haces tu propio kit 8086 podrás ver cómo está todo conectado, podrás encontrar los periféricos en la memoria física, cómo funcionan los componentes HW con tus propios ojos, etc.

Hay una listas infinita de libros buenos. No quiero decir que deberías leerlos todos, simplemente lee alguno cuidadosamente. Mientras aprendes la teoría, intenta implementar en código algo relacionado con ello. Implementar una cosa es mejor que conocer cien en teoría.

## <a name="Lenguajes"></a>Lenguajes

### <a name="Ensamblador"></a>Ensamblador

Elige uno entre x86 o ARM. No necesitas saber ambos y tampoco importa si no sabes escribirlo, pero será esencial entender el funcionamiento interno de un procesador. No necesitas practicar el ensamblador del último procesador. Elige 8086 o Corex-M.

* [Programación en ensamblador de 8086 con emu8086](https://github.com/gurugio/book_assembly_8086)
  * Conceptos básicos de un procesador y de la arquitectura de computador.
  * Conceptos básicos del lenguaje C.
* [Programación en ensamblador x64 (traducción en curso)](https://github.com/gurugio/book_assembly_64bit)
  * Conceptos básicos de arquitecturas y procesadores modernos.
  * Conceptos básicos de desensamblado y depurado de código C.
  * _se necesita ayuda con la traducción_.
* [Aprendiendo ensamblador para Linux-x64](https://github.com/0xAX/asm)
  * Programación en puro ensamblador de 64-bits con NASM y programación de *inline assembly* con GCC.
* [Manual de refernecia de la arquitectura ARM](http://www.mypearsonstore.ca/bookstore/arm-architecture-reference-manual-97802017)
  * Referencia completa para la programación en ARM.
* Estructura y diseño de computadoras
  * [Edición MIPS](https://www.amazon.ca/Computer-Organization-Design-MIPS-Interface/dp/0124077269/)
  * [Edición ARM](https://www.amazon.ca/Computer-Organization-Design-ARM-Interface/dp/0128017333/)
  * [Edición RISC-V](https://www.amazon.com/Computer-Organization-Design-RISC-V-Architecture/dp/0128122757)
  * Libros académicos que explican cómo funcionan los componentes de una computadora.
  * Explican en detalle los diferentes conceptos que forman parte de la arquitectura de la computadora.
  * No son para aquellos lectores que quieran profundizar en un dialecto específico de ensamblador.
  * Las ediciones de MIPS y ARM cubern los mismos temas pero diseccionando una arquitectura diferente.
  * Ambas ediciones contienen ejemplos del mundo real en x86.


### <a name="Lenguaje C"></a>Lenguaje C
* [Programación en C: Una aproximación moderna, 2ª edición](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* [El lenguaje de programación C: 2ª edición](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* Modern C: Jens Gustedt. Modern C. Manning, 2019, 9781617295812. ffhal-02383654f
  * For new standard of C                                                        
* [¿Es la progrmación paralela difícil? Y, de serlo, ¿Qué puedes hacer acerca de ello?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfbook/perfbook.html)
  * Ejemplo de sincronización con C.
  * Esencial para programación en C a gran escala (sobretodo para programación de núcleos de sistemas operativos).
* [Tutoriales de C de tipo proyecto](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * Después de terminar uno o dos libros sobre C, es importante ponerse a hacer algo con ello.
  * Haz tu versión primero y luego compárala con la de los demás. Es importante comparar tu código con el de otros. Puedes mejorar tus habilidades a partir de leer el código de otros.
* [Proyectos basados en C y otros lenguajes](https://github.com/danistefanovic/build-your-own-x)       
  * Sirve para encontrar proyectos interesantes.
* [El libro negro de la programación gráfica, por Michael Abrash. Edición especial](http://www.jagregory.com/abrash-black-book/)
  * Referencia acerca de la optimización en C y un poco de ensamblador de x86.
  * Comienza con el 8088 y progresa hasta hoy.
  * Énfasis en la optimización de gráficos a bajo nivel.
* [Framework and plugin design in C](https://github.com/gurugio/book_cprogramming)     
  * Cómo desarrollar frameworks y plugins en C para software de gran escala.
  * Pistas básicas de programación para leer el código del núcleo Linux.
                                                                                       
Si quieres convertirte en un experto de la programación en C, visita [Leetcode](https://leetcode.com/). ¡Buena suerte! 


### <a name="Lenguaje-Rust"></a>Lenguaje Rust

Estoy convencido de que Rust será el siguiente lenguaje para la programación de sistemas.
Haré una lista con lo que yo hice para aprender Rust.

[Linus Torvalds dijo "A no ser que algo suceda, [Rust] entrará en la versión 6.1."](https://www.zdnet.com/article/linus-torvalds-rust-will-go-into-linux-6-1/)

* [El lenguaje de programacíón Rust](https://doc.rust-lang.org/book/)              
  * Es una buena introducción, pero le faltan ejemplos y ejercicios.                     
* [Rust a través de ejemplos](https://doc.rust-lang.org/rust-by-example/)                 
  * Mientras lees "El lenguaje de programación Rust", puedes encontrar los ejemplos y los ejercicios en este.
  * Pero no contiene demasiados ejercicios en los que puedes hacer algo por ti mismo. Sólo algunos ejemplos incluyen ejercicios de "haz esto", y son muy simples.
* [Programando Rust, 2ª](https://www.oreilly.com/library/view/programming-rust-2nd/9781492052586/)
  * Introducción más en profundidad, pero siguen faltando ejercicios y ejemplos.              
* [Exercism](https://exercism.org/tracks/rust)                                  
  * Buenos ejercicios para practicar características individuales de Rust.
  * No estoy seguro de que los Mentores estén funcionando activamente, pero sería suficiente para comparar tus soluciones con las de otros.
    * Después de subir tu solución puedes ver las de otros en la pestaña de "Community solutions" (Exercism V3).
    * Muchos ejercicios de nivel fácil son para funcionalidades de tipo map/filter/any, etc.
* [Easy rust](https://dhghomon.github.io/easy_rust/)                            
  * Un libro escrito en inglés sencillo.                                             
  * Trae material de Youtube: https://www.youtube.com/playlist?list=PLfllocyHVgsRwLkTAhG0E-2QxCf-ozBkk
* [Let's get rusty](https://www.youtube.com/c/LetsGetRusty)                     
  * Hay muchos youtubers subiendo contenido de Rust, pero este lo he disfrutado especialmente.
  * Además ha estado subiendo las últimas noticias sobre Rust. Merece la pena suscribirse.
* [Rust for Linux](https://github.com/Rust-for-Linux)                           
  * Mira el código de ejemplo y comprueba cómo Rust se introducirá en el núcleo Linux.

## <a name="Aplicaciones"></a>Aplicaciones

### <a name="Hardware-y-firmware"></a>Hardware y firmware

Si quieres ser un ingeniero embebido, será mejor empezar por un kit de hardware sencillo en lugar de con el último de ARM, por ejemplo.

* [Kit de iniciación de Arduino](https://www.arduino.cc)
  * Hay muchas series de Arduino, pero su kit de iniciación (Start Kit) tiene un microprocesador muy simple (Atmega328P) y un libro guía.
  * Atmega328P tiene un procesador de 8 bitsA que es un buen punto de partida para empezar a diseñar circuitos digitales y desarrollo de firmware.
  * No necesitas saber dibujar esquemáticos ni diseños ni a soldar los chips.
  * Pero sí necesitas saber cómo leer los esquemáticos y entender cómo están conectados los chips.
  * Los desarrolladores de firmware deben ser capaces de leer los esquemáticos y averiguar cómo enviar datos al dispositivo que sea.
  * ¡Sigue el libro guía!
* [Manual de 8086](https://edge.edx.org/c4x/BITSPilani/EEE231/asset/8086_family_Users_Manual_1_.pdf)
  * Si eres un principiante con la arquitectura x86, 8086 puede servir muy bien como guía para aprender ensamblador de 80x86.
* [Manual de 80386](http://css.csail.mit.edu/6.858/2015/readings/i386.pdf)
  * La mejor guía sobre el modo protegido y el mecanismo de paginación en procesadores 80x86.
  * [Versión web](https://pdos.csail.mit.edu/6.828/2011/readings/i386/toc.htm)


Llegados a este punto podrías empezar con los últimos procesadores de ARM o x86:
* https://www.raspberrypi.org/                                                  
* https://beagleboard.org/                                                      
* https://www.arduino.cc/en/ArduinoCertified/IntelEdison

Por ejemplo, la placa Raspberry Pi tiene un Cortex-A53 y suporta un juego de instrucciones de 64 bits.
Esto permite que experimentes un procesador con arquitectura más moderna.
Sí, puedes comprarte una rPi, pero, ¿qué harás con ella?
Si no tienes un proyecto pensado, probablemente la rPi acabará en un cajón guardada y olvidada con los otros cachivaches.

Así que te recomiendo un proyecto:
* [Hacer tu propio núcleo](http://wiki.osdev.org/Getting_Started)
  * Buenas referencias en [Reddit](https://www.reddit.com/r/osdev)
* [Aprendiendo desarrollo de sistemas operativos usando el núcleo Linux y Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)

He hecho un [núcleo de juguete](https://github.com/gurugio/caos) que soporta el modo *long* de 64 bits, paginación y un cambio de contexto básico. Hacer un núcleo aficionado es una forma buena de entender las arquitecturas modernas y el control del hardware.

De hecho, es probable que tengas un procesador moderno con dispositivos hardware moderno.
¡Tu portátil! ¡Tu ordenador de escritorio! Ya tienes todo lo que necesitas para empezar.
No necesitas comprar nada más.
El emulador QEMU puede emularte los últimos procesadores de ARM y de Intel.
Así que todo lo que necesitas ya está al alcance de tu mano.
Hay muchos núcleos hechos por aficionados y documentos a los que acudir.
Tan solo instala QEMU y haz un núcleo pequñito que tan solo arranque, comience la paginación e imprima algunos mensajes.

Otros núcleos aficionados o de juguete:
* https://littleosbook.github.io/                                               
* https://tuhdo.github.io/os01/

### <a name="Núcleo-Linux-y-controladores-de-dispositivos"></a>Núcleo Linux y controladores de dispositivos

No necesitas hacer un sistema operativo completo.
Únete a la comunidad Linux y participa en el desarrollo.

Algunos recursos acerca del núcleo Linux y el desarrollo de controladores de novato a experto.
* Libros: Lee los siguientes en orden
  * [El diseño del sistema operativo Unix](https://www.amazon.com/Design-UNIX-Operating-System/dp/0132017997)
    * Los conceptos básicos de Unix se aplican en casi todos los sistemas operativos.
    * Este libro es un muy buen punto de partida para aprender los conceptos clave de los sistemas operativos.
  * [Linux Device Drivers (LDD)](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * Haz todos los ejemplos por ti mismo.
    * [Desarrollo del núcleo Linux](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel)
    * Entender el diseño del núcleo Linux.
  * [Entendiendo el núcleo Linux](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
    * Lee este libro y el código de Linux en la versión 2.6 al mismo tiempo
    * No empieces con la última versión, utiliza la 2.6.
    * Utiliza QEMU y GDB para correr el núcleo línea a línea.
      * [Depurar Linux con QEMU y GDB](http://stackoverflow.com/questions/11408041/how-to-debug-the-linux-kernel-with-gdb-and-qemu)
      * https://github.com/gurugio/linuxdeveloptip/blob/master/qemu-gdb-kdump.md
    * Utiliza busybox para hacer el sistema de ficheros más simple y que tome sólo un segundo el arrancarlo.
      * https://github.com/gurugio/linuxdeveloptip/blob/master/minikernelwithbusybox.md
* Otros recursos: recursos gratis que recomiendo
  * [Linux device driver labs](https://linux-kernel-labs.github.io/)            
    * Guía práctica y ejercicios excelentes para hacer controladores de Linux con APIs esenciales del núcleo.
    * Creo que este documento introduce casi todas las APIs esenciales de Linux.
  * [The Eudyptula Challenge](http://eudyptula-challenge.org/)                  
    * _Tristemente, este reto ya no acepta participantes porque ya no es retador_. La persona que mantiene el proyecto dijo que estaba planeando un nuevo formato. Esperemos que llegue pronto.
      * Pero puedes encontrar los enunciados del reto con Google. Algunas personas ya subieron sus respuestas. Encuentra los enunciados, intenta resolverlos por ti mismo y luego compara tu solución con la de otros.
    * Es como un profesor privado que te va guiando.     
    * Si no sabes bien qué hacer, este es un buen punto de partida también.                            
  *  [Aprendiendo desarrollo de sistemas operativos usando el núcleo Linux y Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
     * Este proyecto no está terminado todavía.                                       
     * Siempre pienso que hacer un núcleo similar a Linux es la mejor forma de entender Linux.
  * [Block layer and device driver](https://github.com/gurugio/book_linuxkernel_blockdrv)
    * Empieza con un ejemplo simple de controlador de dispositivo de bloques (Ramdisk) con modo multi-queue.
    * Avanza hasta llegar a la capa de bloques (*block layer*).
    * He terminado la traducción a inglés. Por favor, enviadme vuestra opinión. 
  * [Controlador md del núcleo Linux (coreano)](https://github.com/gurugio/book_linuxkernel_md)
    * Cómo funciona la herramienta `mdadm` y cómo llama al controlador `md`.
    * Cómo funciona el controlador `md`.
  * [Código de Linux muy comentado](http://www.oldlinux.org/)    
    * Versión 0.12 de Linux con un montón de comentarios útiles.                               
    * Puede ser bueno comenzar con un sistema operativo viejo y simple.                         
    * Versión Unix: [Comentarios de Lion a la sexta edición de Unix, con código fuente](https://en.wikipedia.org/wiki/Lions%27_Commentary_on_UNIX_6th_Edition,_with_Source_Code)


### <a name="Referencias"></a>Referencias

Échales un ojo cuando necesites algo:
* [Página principal de Free-electrons](http://free-electrons.com/docs/)                    
  * Muchas diapositivas/transparencias que introducen temas interesantes, especialmente ARM-Linux.
* [¡Puedes ser un Kernel Hacker! Post de Julia Evans](http://jvns.ca/blog/2014/09/18/you-can-be-a-kernel-hacker/)
  * Guía para empezar la programación de núcleos.


### <a name="Otras-aplicaciones"></a>Otras aplicaciones

Puede que no estés interesado en Linux o en el firmware. De ser así, puedes encontrar otros usos:
* Programación de sistemas y controladores para Windows.
* Seguridad
* Ingeniería inversa

No sé mucho acerca de estos usos. Por favor, enviadme cualquier información que sea para principiantes.

**Los núcleos y los controladores no son todo el mundo del bajo nivel.** Un uso también importante de la programación a bajo nivel es el almacenamiento definido por software (*sw-defined storage*) o los sistemas de ficheros distribuidos. Dar una descripción detallada de lo que son se sale del alcance de este documento, pero hay un curso excelente en el que se puede probar un sistema de ficheros distribuido simple:
* Curso: https://pdos.csail.mit.edu/archive/6.824-2012/
* Código de referencia: https://github.com/srned/yfs

## <a name="Futuro-del-bajo-nivel"></a>Futuro del bajo nivel

No sé qué deparará el futuro, pero me mantengo atento a Rust.
* https://hacks.mozilla.org/2016/11/rust-and-the-future-of-systems-programming/

Si tuviese una semana libre para pasarla solo, aprendería Rust.
Esto es porque es el último lenguaje en el que se pueden desarrollar controladores para Linux.
* https://github.com/tsgates/rust.ko

IoT es una tendencia nueva, así que merece la pena mirar qué S.O. se utiliza para IoT.
ARM, Samsung, y otras compañías tienen sus propios [sistemas operativos de tiempo real](https://es.wikipedia.org/wiki/Sistema_operativo_de_tiempo_real), pero lamentablemente muchos de ellos son de código cerrado.
La Fundación Linux tiene una solución: Zephyr
* [Zephyr](https://www.zephyrproject.org/)

Los servidores en la nube suele tener muchas capas. Por ejemplo, un S.O. anfitrión, un controlador KVM, un proceso QEMU, un S.O. huésped y el servicio de aplicación. Los contenedores se han desarrollado para aportar virtualización ligera. En el futuro cercano, un nuevo concepto de S.O llamado S.O. de librería o Unikernel podŕia reemplazar la pila típica de SW para virtualización.
* https://unikernel.org

El Big Data y la computación en la nube necesitan cada vez más y más almacenamiento. Algunos discos que están directamente dentro del servidor no pueden satisfacer la capacidad, estabilidad ni desempeño necesarios. Se ha investigado cómo hacer grandes sistemas de almacenamiento conectando muchos más pequeños a través de una red de alta velocidad. Solían estar enfocados en hacer un volumen de almacenamiento enorme, pero actualmente están dedicando varios volúmenes a las máquinas virtuales:
* `EN` https://en.wikipedia.org/wiki/Software-defined_storage                        
* `EN` https://en.wikipedia.org/wiki/Clustered_file_system                           
* https://es.wikipedia.org/wiki/Ceph_File_System

## <a name="Cómo-empezar"></a>Cómo empezar
Recibí un email preguntando cómo empezar. Hay mucha información sobre libros, cursos y proyectos en esta página. Es error mío olvidarme de escribir cómo empezar. Por desgracia, no hay una única forma de hacerlo. Me limitaré a escribir los pasos que yo di en orden. Si ya has hecho algo similar, por favor, sáltate ese paso. De nuevo, esto es SÓLO UN EJEMPLO de lo que podrías hacer en caso de que no sepas cómo empezar o qué hacer.

* Leer libros de teoría de sistemas operativos: al menos "El diseño del sistema operativo Unix" de Maurice J. Bach
* Aprender ensamblador y C
  * [8086 assembly programming with emu8086](https://github.com/gurugio/book_assembly_8086)
    * Es suficiente si entiendes el concepto de programación en ensamblador. No hace falta que hagas algo práctico.
  * [The C Programming Language 2nd Edition](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14_t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
    * Intenta resolver todos los ejercicios por ti mismo, es importante.
  * [C Programming: A Modern Approach, 2nd Edition](https://www.amazon.com/C-Programming-Modern-Approach-2nd/dp/0393979504)
* Haz algo práctico con C
  * [C Project Based Tutorials](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/): Encuentra un par de proyectos interesantes y haz el tuyo propio.
  * [leetcode.com](https://leetcode.com/): Si no encuentras un proyecto interesante, está bien centrarte en estructuras de datos y algoritmos, siempre es buena práctica.
* Haz un proyecto hardware
  * Raspberry Pi o Arduino, no importa. Necesitas experiencia para controlar el hardware directamente sólo con C. ¡SÓLO CON C!
  * Recomiendo que te compres un kit del Atmega128 y que hagas firmware para encender y apagar LEDs, detectar el estado de un interruptor, mostrar mensajes en el LCD. Un proyecto que incluya algún motor es también interesante, como un robot que siga líneas en el suelo ([búscalo en Youtube](https://www.youtube.com/results?search_query=robot+sigue+lineas+arduino)).
  * NO USES LIBRERÍAS. Deberías intentar hacerlo todo por ti mismo,
* Cosas básicas del núcleo Linux
  * Deberías entender antes las entrañas del sistema operativo.
  * Comienza con controladores
    * Lee [Linux Device Drivers](https://www.amazon.com/Linux-Device-Drivers-Jonathan-Corbet/dp/0596005903/ref=sr_1_4?ie=UTF8&qid=1483650712&sr=8-4&keywords=understanding+linux+kernel)
    * [Linux device driver labs](https://linux-kernel-labs.github.io/)
    * [The Eudyptula Challenge](http://eudyptula-challenge.org/)
  * Lee [Linux Kernel Development](https://www.amazon.com/Linux-Kernel-Development-Robert-Love/dp/0672329468/ref=sr_1_2?ie=UTF8&qid=1483650712&sr=8-2&keywords=understanding+linux+kernel) para entender el funcionamiento interno de Linux.
* Ve al sector profesional
  * Si quieres ser un desarrollador de Linux profesional
    * Obligatorio: [Understanding the Linux Kernel](https://www.amazon.com/Understanding-Linux-Kernel-Third-Daniel/dp/0596005652/ref=sr_1_1?ie=UTF8&qid=1483650712&sr=8-1&keywords=understanding+linux+kernel)
      * Intenta hacer un núcleo de juguete
      * [Aprende desarrollo de sistemas opeartivos con el núcleo Linux y Raspberry Pi](https://github.com/s-matyukevich/raspberry-pi-os)
      * [Haz tu propio núcleo](http://wiki.osdev.org/Getting_Started)
      * Pon un enlace a tu Github/Gitlab en tu CV (recuerda poner mensajes de commit claros).
    * Mantente actualizado con lo publicado en https://lwn.net/ ¡y suscríbete!
      * Comprueba los "Recent Kernel Patches" en https://lwn.net/Kernel/ o https://lwn.net/Kernel/Patches.
      * Encuentra un parche interesante. Intenta entender el código. Por supuesto será muy difícil, pero inténtalo, fuérzate. Cada vez que lo intentes estarás más cerca.
      * Compila el núcleo y pruébalo en tu sistema. Por ejemplo, hazle una prueba de rendimiento o de estabilidad con [LTP](https://linux-test-project.github.io/) o alguna herramienta de análisis estático del código dentro del núcleo.
      * Notifica cualquier problema que te encuentres: errores o avisos de compilación, bajadas de rendimiento, kernel panic/oops o cualquier otro problema.
      * Si funciona bien, notifícalo también junto a las especificaciones de tu sistema. El dueño del parche podrá escribir una etiqueta "Reviewed-by" con tu nombre.
      * ¡Encuentra tu nombre en el `git log` del núcleo!
* O encuentra otros temas
  * Hay muchos campos en los que puede trabajar un ingeniero a bajo nivel: seguridad, compiladores, firmware, industria robótica, automovilística, ferroviaria, militar, naval, aeroespacial, y un largo etcétera.

# <a name="Traducción"></a>Traducción

Por favor, mándame el Pull Request si te gustaría traducir esta página.

# <a name="Quién-soy"></a>Quién soy
Me inspiré en [google-interview-university](https://github.com/jwasham/coding-interview-university). Me gustaría compartir mi experiencia y mostrar un mapa de ruta para convertirse en un programador a bajo nivel porque he visto que estas habilidades ya no son tan comunes como fueron una vez. Además, muchos estudiantes y principiantes me preguntan cómo convertirse en programadores a bajo nivel e ingenieros del núcleo de Linux.

Para tu información, tengo más de 10 años de experiencia como programador a bajo nivel:
* Programación en ensamblador 80x86
* Dispositivos hardware y firmware con chips Atmel
* Programación de sistemas para Unix en C
* Controladore de dispositivos en Linux
* Núcleo Linux: paginación
* Núcleo Linux: Módulo `md` y controladores para dispositivos de bloques.
