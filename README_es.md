NOTA1: Por favor, no copies el contenido de esta página a tu blog. Puedes compartir esta página, pero, por favor, compártela con el enlace original. Así es como agradecemos a los autores de buenos documentos y proyectos de código abierto

NOTA2: Por favor, téngase en cuenta que la programación a bajo nivel no está de moda y actualmente no hay muchas compañías contratando programadores de bajo nivel. Cada vez es más difícil encontrar trabajo de esto.
Si no has iniciado tu carrera profesional todavía, te recomiendo que consideres otros campos cuidadosamente.

NOTA3: Si quieres un inicio rápido, ve a la sección "¿Cómo empezar?"


# Universidad de programación a bajo nivel

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
    * [Núcleo de Linux y controladores de dispositivos](#Núcleo-de-Linux-y-controladores-de-dispositivos)
      * [Referencias](#Referencias)
    * [Otras aplicaciones](#Otras-Aplicaciones)
  * [Futuro del bajo nivel](#Futuro-del-bajo-nivel)
  * [¿Cómo empezar?](#Cómo-empezar)
* [Traducción](#Traducción)
* [¿Quién soy?](#Quién-soy)


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

Déjame introducir varios libros que he leído. Son usados comúnmente como libros de texto en universidades. Si no hay ninguna clase con estos libros en tu universidad, merece la pena invertir un tiempo en leerlos.
* Arquitectura de computadoras
  * Computer Architecture: A Quantitative Approach, fifth edition
  * Computer Systems: A Programmer's Perspective
  * Computer Organization and Design: The Hardware/Software Interface, fourth edition
* Sistemas operativos
  * The Magic Garden Explained: The Internals of UNIX System V Release 4 an Open Systems Design
  * The Design of the UNIX Operating System
  * Operating Systems: Internals and Design Principles by William Stallings
* Recommended Courses
  * [CS401: Operating Systems from saylor.org](https://learn.saylor.org/course/view.php?id=94)
* General Programming SKill
  * [Structure and Interpretation of Computer Programs](https://en.wikipedia.org/wiki/Structure_and_Interpretation_of_Computer_Programs)
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
* [El lenguaje de programación C: 2ª edición](https://www.amazon.com/Programming-Language-Brian-W-Kernighan/dp/0131103628/ref=pd_sbs_14    _t_0?_encoding=UTF8&psc=1&refRID=60R1D2CHBA8DHYT6JNMN)
* Modern C: Jens Gustedt. Modern C. Manning, 2019, 9781617295812. ffhal-02383654f
  * For new standard of C                                                        
* [¿Es la progrmación paralela difícil? Y, de serlo, ¿Qué puedes hacer acerca de elo?](https://www.kernel.org/pub/linux/kernel/people/paulmck/perfb    ook/perfbook.html)
  * Ejemplo de sincronización con C.
  * Esencial para programación en C a gran escala (sobretodo para programación de núcleos)  
* [Tutoriales de C de tipo proyecto](https://www.reddit.com/r/C_Programming/comments/872rlt/c_project_based_tutorials/)
  * Después de terminar uno o dos libros sobre C, es importante ponerse a hacer algo con ello.
  * Haz tu versión primero y luego compárala con la de los demás. Es importante comparar tu código con el de otros. Puedes mejorar tus habilidades a partir de leer el código de otros.
* [Proyectos basasdos en C y otros lenguajes](https://github.com/danistefanovic/build-your-own-x)       
  * Sirve para encontrar proyectos interesantes.
* [El libro negro de la programación gráfica, por Michael Abrash. Edición especial](http://www.jagregory.com/abrash-black-book/)
  * Referencia acerca de la optimización en C y un poco de ensamblador de x86.
  * Comienza con el 8088 y progresa hasta hoy.
  * Énfasis en la optimización de gráficos a bajo nivel.
* [Framework and plugin design in C](https://github.com/gurugio/book_cprogramming)     
  * Cómo desarrollar frameworks y plugins en C para software de gran escala.
  * Pistas básicas de programación para leer el código del núcleo Linux.
                                                                                       
Si quieres convertirte en un experto de la programación en C, visita [Leetcode](https://leetcode.com/). ¡Buena suerte! 

