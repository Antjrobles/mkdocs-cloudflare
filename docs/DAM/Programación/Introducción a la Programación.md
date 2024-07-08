# PROGRAMACIÓN

# UNIDAD 1

> # 1. INTRODUCCIÓN

¿Cuántas acciones de las que has realizado hoy, crees que están relacionadas con la programación? Hagamos un repaso de los primeros instantes del día: te ha despertado la alarma de tu teléfono móvil o radio-despertador, has preparado el desayuno utilizando el microondas, mientras desayunabas has visto u oído las últimas noticias a través de tu receptor de televisión digital terrestre, te has vestido y puede que hayas utilizado el ascensor para bajar al portal y salir a la calle, etc. Quizá no es necesario que continuemos más para darnos cuenta de que casi todo lo que nos rodea, en alguna medida, está relacionado con la programación, los programas y el tratamiento de algún tipo de información.

El volumen de datos que actualmente manejamos y sus innumerables posibilidades de tratamiento constituyen un vasto territorio en el que los programadores tienen mucho que decir.

En esta primera unidad realizaremos un recorrido por los conceptos fundamentales de la programación de aplicaciones. Iniciaremos nuestro camino conociendo con qué vamos a trabajar, qué técnicas podemos emplear y qué es lo que pretendemos conseguir. Continuaremos con el análisis de las diferentes formas de programación existentes, identificaremos qué fases conforman el desarrollo de una aplicación software y avanzaremos detallando las características relevantes de cada uno de los lenguajes de programación disponibles, para posteriormente, realizar una visión general del lenguaje de programación Java. Finalmente, tendremos la oportunidad de conocer con qué herramientas podríamos desarrollar nuestros programas, escogiendo entre una de ellas para ponernos manos a la obra utilizando el lenguaje Java.

---

> # 2. PROGRAMAS Y PROGRAMACIÓN

> ### 2.1 BUSCANDO UNA SOLUCIÓN

Generalmente, la primera razón que mueve a una persona hacia el aprendizaje de la programación es utilizar el ordenador como herramienta para resolver problemas concretos. Como en la vida real, la búsqueda y obtención de una solución a un problema determinado, utilizando medios informáticos, se lleva a cabo siguiendo unos pasos fundamentales. En la siguiente tabla podemos ver estas analogías

RESOLUCIÓN DE PROBLEMAS

**En la vida real…**

**En Programación**

Observación de la situación o problema.

**Análisis del problema:** requiere que el problema sea definido y comprendido claramente para que pueda ser analizado con todo detalle.

Pensamos en una o varias posibles soluciones.

**Diseño o desarrollo de algoritmos:** se establece una solución al problema sin entrar en detalles tecnológicos. Se aplican diferentes técnicas y principios para establecer de forma detallada los pasos a seguir para resolver el problema.

Aplicamos la solución que estimamos más adecuada.

**Resolución del algoritmo elegido en la computadora:** consiste en convertir el algoritmo en programa, ejecutarlo y comprobar que soluciona verdaderamente el problema.

¿Qué virtudes debería tener nuestra solución?

- **Corrección y eficacia:** si resuelve el problema adecuadamente.

- **Eficiencia:** si lo hace en un tiempo mínimo y con un uso óptimo de los recursos del sistema.

Para conseguirlo, cuando afrontemos la construcción de la solución tendremos que tener en cuenta los siguientes conceptos:

1. **Abstracción:** se trata de realizar un análisis del problema para descomponerlo en problemas más pequeños y de menor complejidad, describiendo cada uno de ellos de manera precisa. **Divide y vencerás,** esta suele ser considerada una filosofía general para resolver problemas y de aquí que su nombre no sólo forme parte del vocabulario informático, sino que también se utiliza en muchos otros ámbitos.

2. **Encapsulación:** consiste en ocultar la información que manejan de los diferentes elementos que forman el sistema. La forma de manejar es información no debe influir en el resto de elementos del sistema.

3. **Modularidad:** un proyecto software será dividido en módulos independientes, dependiendo de su tamaño, donde cada uno de ellos tendrá su función correspondiente. Los demás módulos del sistema podrán utilizar su funcionalidad sin necesidad de conocer cómo funciona internamente.

> ### 2.2 ALGORITMOS Y PROGRAMAS

Después de analizar en detalle el problema a solucionar, hemos de diseñar y desarrollar el algoritmo adecuado. Pero, **¿Qué es un algoritmo?**

**Algoritmo\*\***:\*\* secuencia ordenada de pasos, descrita sin ambigüedades, que conducen a la solución de un problema dado.

Los algoritmos son independientes de los lenguajes de programación y de las computadoras donde se ejecutan. Un mismo algoritmo puede ser expresado en diferentes lenguajes de programación y podría ser ejecutado en diferentes dispositivos. Piensa en una receta de cocina, ésta puede ser expresada en castellano, inglés o francés, podría ser cocinada en fogón o vitrocerámica, por un cocinero o más, etc.  Pero independientemente de todas estas circunstancias, el plato se preparará siguiendo los mismos pasos.

La diferencia fundamental entre algoritmo y **programa** es que, en el segundo, los pasos que permiten resolver el problema, deben escribirse en un determinado **lenguaje de programación** para que puedan ser ejecutados en el ordenador y así obtener la solución.

**Los lenguajes de programación** son sólo un medio para expresar el algoritmo, es decir, establece una serie de normas sintácticas y semánticas para expresarlo. El diseño de los algoritmos será una tarea que necesitará de la creatividad del desarrollador y de los conocimientos de las técnicas de programación. Estilos distintos, de distintos programadores a la hora de obtener la solución del problema, darán lugar a algoritmos diferentes, igualmente válidos.

En esencia, todo problema se puede describir por medio de un algoritmo y las características fundamentales que éstos deben cumplir son:

- Debe ser **preciso** e indicar el orden de realización paso a paso.

- Debe estar **definido**, si se ejecuta dos o más veces con los mismos datos de entrada, debe obtener el mismo resultado cada vez. Además, debe dar una respuesta a cualquier dato de entrada.

- Debe ser **finito**, debe tener un número finito de pasos.

Para representar gráficamente los algoritmos que vamos a diseñar, tenemos a nuestra disposición diferentes herramientas que ayudarán a describir su comportamiento de una forma precisa y genérica, para luego poder codificarlos con el lenguaje que nos interese. Entre otras tenemos:

- **Diagramas de flujo\*\***:\*\* Esta técnica utiliza símbolos gráficos para la representación del algoritmo. Suele utilizarse en las fases de análisis.

- **Pseudocódigo\*\***:\*\* Esta técnica se basa en el uso de palabras clave en lenguaje natural, [constantes](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387830/mod_resource/content/11/PROG01_Contenidos_Imprimible/index.html#tb390ec93-f7a3-9276-87b0-b7c29b05144c), [variables](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387830/mod_resource/content/11/PROG01_Contenidos_Imprimible/index.html#teaefc966-5da5-beb8-7e24-be4c8814ba7e), otros objetos, instrucciones y estructuras de programación que expresan de forma escrita la solución del problema. Es la técnica más utilizada actualmente.

- **Tablas de decisión\*\***:\*\* En una tabla son representadas las posibles condiciones del problema con sus respectivas acciones. Suele ser una técnica de apoyo al pseudocódigo cuando existen situaciones condicionales complejas.

### **Debes conocer**

A continuación te ofrecemos algunos recursos interesantes:

- [Elementos visuales de los diagramas de flujo](https://www.heflo.com/es/blog/modelado-de-procesos/significado-simbolos-diagrama-flujo/): En este enlace podrás aprender los elementos gráficos más utilizados en la construcción de diagramas de flujo.

- Software **DFD**: Se trata de una aplicación que permite construir diagramas de flujo de forma gráfica. Es una aplicación portable: tras su descarga tan solo tienes que ejecutar la aplicación.

  - Descárgala [aquí](https://www.descargarsoft.com/descargar-dfd-para-crear-diagramas-de-flujo/).

  - Observa en el siguiente vídeo su funcionamiento.

[Descripción Textual Alternativa para el vídeo "DFD"](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387830/mod_resource/content/11/PROG01_Contenidos_Imprimible/PROG01_Descripcion_DFD.html)

- **Pseint**: Se trata de una aplicación que permite la construcción de algoritmos a través de un fácil e intuitivo pseudocódigo, complementado con un editor de diagramas de flujo. Es una de las herramientas más utilizadas para iniciarse en el mundo de la algoritmia, proporcionando un entorno con numerosas ayudas y recursos didácticos.

Como vemos en la siguiente, dispondremos de 2 paneles principales, el central para incorporar pseudocódigo directamente, y el de la derecha, con los comandos disponibles para ayudar, si se desconoce la sintaxis en la escritura de instrucciones o estructuras de control.

En la segunda imagen se puede ver un ejemplo de pseudocódigo en Pseint que calcula el área de un cuadrado. Observa como las instrucciones están escritas en un pseudolenguaje bastante parecido al lenguaje natural. Los elementos del panel derecho permiten la introducción de código de forma alternativa a la escritura de sentencias en pseudocódigo.

Por último, la tercera imagen muestra el resultado de interpretar el algoritmo tras pulsar el botón verde de reproducción de la barra de tareas.

Toda la información sobre Pseint.

[Pseint](http://pseint.sourceforge.net/)

---

> ## 3. PARADIGMAS DE LA PROGRAMACIÓN

¿Cuántas formas existen de hacer las cosas? Supongo que estarás pensando: varias o incluso, muchas. Pero cuando se establece un patrón para la creación de aplicaciones nos estamos acercando al significado de la palabra paradigma. Si establecemos una serie de normas y principios que recojan experiencia y buenas prácticas de otros desarrolladores para su uso en la resolución de problemas, estaremos creando un paradigma de programación.

**Paradigma de programación:** es un modelo básico para el diseño y la implementación de programas. Este modelo determinará como será el proceso de diseño y la estructura final del programa.

El paradigma representa un enfoque particular o filosofía para la construcción de software. Cada uno tendrá sus ventajas e inconvenientes, será más o menos apropiado, pero no es correcto decir que exista uno mejor que los demás. Algunos de ellos son:

- **Programación Declarativa:** Se basa en el desarrollo de algoritmos aplicando una especificación de un conjunto de condiciones, proposiciones, afirmaciones y restricciones que describen el problema. Las sentencias utilizadas describen el problema que se quiere solucionar, pero no la instrucciones necesarias para llegar a la solución. El lenguaje SQL está basado en este paradigma. Dentro de este paradigma se encuentran la programación funcional y la programación lógica.

- **Programación Imperativa:** Se basa en el desarrollo de algoritmos detallando de forma clara y específica los comandos a ejecutar para, a través del paso por diferentes estados,  llegar a la solución. Se basa en el uso de variables, tipos de datos, expresiones y estructuras de control del flujo de ejecución. Lenguajes como Python, Java, C++, C# ... son lenguajes imperativos. Dentro de este paradigma se encuentran la programación convencional (programación no estructurada), la programación estructurada, la programación orientada a objetos, la programación orientada a eventos, la programación orientada a aspectos ...

Existen múltiples paradigmas, incluso puede haber lenguajes de programación que no se clasifiquen únicamente dentro de uno de ellos. Un lenguaje como [Smalltalk](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387830/mod_resource/content/11/PROG01_Contenidos_Imprimible/index.html#t88dd2841-24e6-2469-ffb0-7b670ea19f26) es un lenguaje basado en el paradigma orientado a objetos. El lenguaje de programación [Scheme](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387830/mod_resource/content/11/PROG01_Contenidos_Imprimible/index.html#taaf64e7a-599c-7cdf-5579-61bf6e0e05f4), en cambio, soporta sólo programación funcional. [Python](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387830/mod_resource/content/11/PROG01_Contenidos_Imprimible/index.html#t0d9c4b63-2499-977b-9348-8a0448bc0ef8), soporta múltiples paradigmas.

## **Para saber más**

Te proponemos el siguiente enlace en el que encontrarás información adicional sobre los diferentes paradigmas de programación.

[Paradigmas de programación y lenguajes](http://javierleal.wordpress.com/2009/08/27/paradigmas-de-programacion/)

¿Cuál es el objetivo que se busca con la aplicación de los diferentes enfoques? Fundamentalmente, reducir la dificultad para el desarrollo y mantenimiento de las aplicaciones, mejorar el rendimiento del programador, reutilizando código en la medida de lo posible y, en general, mejorar la productividad y calidad de los programas.

---

> ## 4. FASES DE LA PROGRAMACIÓN

Sea cual sea el estilo que escojamos a la hora de automatizar una determinada tarea, debemos realizar el proceso aplicando un método a nuestro trabajo. Es decir, sabemos que vamos a dar solución a un problema, aplicando una filosofía de desarrollo y lo haremos dando una serie de pasos que deben estar bien definidos.

El proceso de creación de software puede dividirse en diferentes fases:

- **Fase de resolución del problema.**

- **Fase de implementación.**

- **Fase de explotación y mantenimiento.**

A continuación, analizaremos cada una de ellas.

> ### 4.1 RESOLUCIÓN DEL PROBLEMA

Para el comienzo de esta fase, es necesario que el problema sea definido y comprendido claramente para que pueda ser analizado con todo detalle. A su vez, la fase de resolución del problema puede dividirse en dos etapas:

**Análisis**

Por lo general, el análisis indicará la especificación de requisitos que se deben cubrir. Los contactos entre el analista/programador y el cliente/usuario serán numerosos, de esta forma podrán ser conocidas todas las necesidades que precisa la aplicación. Se especificarán los procesos y estructuras de datos que  se van a emplear. La creación de prototipos será muy útil para saber con mayor exactitud los puntos a tratar.

El análisis inicial ofrecerá una idea general de lo que se solicita, realizando posteriormente sucesivos refinamientos que servirán para dar respuesta a las siguientes cuestiones:

- ¿Cuál es la información que ofrecerá la resolución del problema?.

- ¿Qué datos son necesarios para resolver el problema?.

La respuesta a la primera pregunta se identifica con los resultados deseados o las salidas del problema. La respuesta a la segunda pregunta indicará qué datos se proporcionan o las entradas del problema.

En esta fase debemos aprender a analizar la documentación de la empresa , investigar, observar todo lo que rodea el problema y recopilar cualquier información útil.

**Diseño**

En esta etapa se convierte la especificación realizada en la fase de análisis en un diseño más detallado, indicando el comportamiento o la secuencia lógica de instrucciones capaz de resolver el problema planteado. Estos pasos sucesivos, que indican las instrucciones a ejecutar por la máquina, constituyen lo que conocemos como algoritmo.

Durante la fase de diseño, se plantea la aplicación a desarrollar como una única operación global, y se va descomponiendo en operaciones más sencillas, detalladas y específicas. El nivel de descomposición dependerá del tamaño del problema. En cada nivel de refinamiento, las operaciones identificadas se asignan a módulos separados.

Hay que tener en cuenta que antes de pasar a la implementación del algoritmo, hemos de asegurarnos que tenemos una solución adecuada. Para ello, todo diseño requerirá de la realización de la **prueba o traza** del programa. Este proceso consistirá en un seguimiento paso a paso de las instrucciones del algoritmo utilizando datos concretos. Si la solución aportada tiene errores, tendremos que volver a la fase de análisis para realizar las modificaciones necesarias o tomar un nuevo camino para la solución. Sólo cuando el algoritmo cumpla los requisitos y objetivos especificados en la fase de análisis se pasará a la fase de implementación.

> ### 4.2 IMPLEMENTACIÓN

Si la fase de resolución del problema requiere un especial cuidado en la realización del análisis y el posterior diseño de la solución, la fase de implementación cobra también una especial relevancia. Llevar a la realidad nuestro algoritmo implicará cubrir algunas etapas más que se detallan a continuación.

**Codificación o construcción**

Esta etapa consiste en transformar o traducir los resultados obtenidos a un determinado lenguaje de programación. Para comprobar la calidad y estabilidad de la aplicación se han de realizar una serie de pruebas que comprueben las funciones de cada módulo (pruebas unitarias), que los módulos funcionan bien entre ellos (pruebas de interconexión) y que todos funcionan en conjunto correctamente (pruebas de integración).

Cuando realizamos la traducción del algoritmo al lenguaje de programación debemos tener en cuenta las reglas gramaticales y la sintaxis de dicho lenguaje. Obtendremos entonces el código fuente, lo que normalmente conocemos por programa.

Pero para que nuestro programa comience a funcionar, antes debe ser traducido a un lenguaje que la máquina entienda. Este proceso de traducción puede hacerse de dos formas, compilando o interpretando el código del programa.

**Compilación:** Es el proceso por el cual se traducen las instrucciones escritas en un determinado lenguaje de programación a lenguaje que la máquina es capaz de interpretar, nomalmente código binario.

El proceso de compilación se puede llevar a cabo de dos formas:

- **A través de un compilador**: programa informático que realiza la traducción. Recibe el código fuente, realiza un análisis lexicográfico, semántico y sintáctico, genera un código intermedio no optimizado, optimiza dicho código y finalmente, genera el código objeto/máquina ejecutable en una plataforma específica.

- **A través de un Intérprete**: programa informático capaz de analizar y ejecutar otros programas, escritos en un lenguaje de alto nivel. Los intérpretes se diferencian de los compiladores en que mientras éstos traducen un programa escrito en un lenguaje de programación al código de máquina del sistema, los intérpretes sólo realizan la traducción a medida que sea necesaria, típicamente, instrucción por instrucción, y normalmente no guardan el resultado de dicha traducción.

Una vez traducido, sea a través de un proceso de compilación o de interpretación, el programa podrá ser ejecutado.

**Prueba de ejecución y validación**

Para esta etapa es necesario implantar la aplicación en el sistema donde va a funcionar, debe ponerse en marcha y comprobar si su funcionamiento es correcto. Utilizando diferentes datos de prueba se verá si el programa responde a los requerimientos especificados, si se detectan nuevos errores, si éstos son bien gestionados y si la interfaz es amigable. Se trata de poner a prueba nuestro programa para ver su respuesta en situaciones difíciles.

Mientras se detecten errores y éstos no se subsanen no podremos avanzar a la siguiente fase. Una vez corregido el programa y testeado se documentará mediante:

- **Documentación interna:** Encabezados, descripciones, declaraciones del problema y comentarios que se incluyen dentro del código fuente.

- **Documentación externa:** Son los manuales que se crean para una mejor ejecución y utilización del programa.

> ### 4.3 EXPLOTACIÓN

Cuando el programa ya está instalado en el sistema y está siendo de utilidad para los usuarios, decimos que se encuentra en fase de explotación.

Periódicamente será necesario realizar evaluaciones y, si es necesario, llevar a cabo modificaciones para que el programa se adapte o actualice a nuevas necesidades, pudiendo también corregirse errores no detectados anteriormente. Este proceso recibe el nombre de mantenimiento del software.

Será imprescindible añadir una documentación adecuada que facilite al programador la comprensión, uso y modificación de dichos programas.

---

> ## 5. CICLOS DE VIDA DEL SOFTWARE

Sean cuales sean las fases en las que realicemos el proceso de desarrollo de software, y casi independientemente de él, siempre se debe aplicar un modelo de ciclo de vida.

**Ciclo de vida del software:** es una sucesión de estados o fases por las cuales pasa un software a lo largo de su "vida".

El proceso de desarrollo puede involucrar siempre las siguientes etapas mínimas:

- Especificación y Análisis de requisitos.

- Diseño.

- Codificación.

- Pruebas.

- Instalación y paso a Producción.

- Mantenimiento.

Aprenderás mucho más sobre el ciclo de vida del software en el Módulo Profesional "Entornos de Desarrollo".

---

> ## 6 LENGUAJES DE PROGRAMACIÓN

Como hemos visto, en todo el proceso de resolución de un problema mediante la creación de software, después del análisis del problema y del diseño del algoritmo que pueda resolverlo, es necesario traducir éste a un lenguaje que exprese claramente cada uno de los pasos a seguir para su correcta ejecución. Este lenguaje recibe el nombre de lenguaje de programación.

**Lenguaje de programación:** Conjunto de reglas sintácticas y semánticas, símbolos y palabras especiales establecidas para la construcción de programas. Es un lenguaje artificial, una construcción mental del ser humano para expresar programas.

Además, cada lenguaje de programación, al igual que otro tipo de lenguajes, se basa en una gramática.

**Gramática del lenguaje:** Reglas aplicables al conjunto de símbolos y palabras especiales del lenguaje de programación para la construcción de sentencias correctas.

Además, cada gramática dispone de:

1. **Léxico\*\***:\*\* Es el conjunto finito de símbolos y palabras especiales, es el vocabulario del lenguaje.

2. **Sintaxis\*\***:\*\* Son las posibles combinaciones de los símbolos y palabras especiales. Está relacionada con la forma de los programas.

3. **Semántica\*\***:\*\* Es el significado de cada construcción del lenguaje, la acción que se llevará a cabo.

Hay que tener en cuenta que pueden existir sentencias sintácticamente correctas, pero semánticamente incorrectas. Por ejemplo, _“Un avestruz dio un zarpazo a su cuidador”_ está bien construida sintácticamente, pero es evidente que semánticamente no.

Una característica relevante de los lenguajes de programación es, precisamente, que más de un programador pueda usar un conjunto común de instrucciones que sean comprendidas entre ellos. A través de este conjunto se puede lograr la construcción de un programa de forma colaborativa.

Los lenguajes de programación pueden ser clasificados en función de lo cerca que estén del lenguaje humano o del lenguaje de los computadores. El lenguaje de los computadores son los códigos binarios, es decir, secuencias de unos y ceros. Detallaremos seguidamente las características principales de los lenguajes de programación.

### 6.1 LENGUAJE MÁQUINA

Este es el lenguaje utilizado directamente por el procesador, consta de un conjunto de instrucciones codificadas en binario. Es el sistema de códigos directamente interpretable por un [circuito microprogramable](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387830/mod_resource/content/11/PROG01_Contenidos_Imprimible/index.html#t82d46d38-91c1-05d2-be33-c9015f5c1f4f).

Este fue el primer lenguaje utilizado para la programación de computadores. De hecho, cada máquina tenía su propio conjunto de instrucciones codificadas en ceros y unos. Cuando un algoritmo está escrito en este tipo de lenguaje, decimos que está en código máquina.

Programar en este tipo de lenguaje presentaba los siguientes inconvenientes:

- Cada programa era válido sólo para un tipo de procesador u ordenador.

- La lectura o interpretación de los programas era extremadamente difícil y, por tanto, insertar modificaciones resultaba muy costoso.

- Los programadores de la época debían memorizar largas combinaciones de ceros y unos, que equivalían a las instrucciones disponibles para los diferentes tipos de procesadores.

- Los programadores se encargaban de introducir los códigos binarios en el computador, lo que provocaba largos tiempos de preparación y posibles errores.

A continuación, se muestran algunos códigos binarios equivalentes a las operaciones de suma, resta y movimiento de datos en lenguaje máquina.

Operación

SUMAR - 00101101

RESTAR - 00010011

MOVER - 00111010

Dada la complejidad y dificultades que ofrecía este lenguaje, fue sustituido por otros más sencillos y fáciles utilizar. No obstante, hay que tener en cuenta q

Dada la complejidad y dificultades que ofrecía este lenguaje, fue sustituido por otros más sencillos y fáciles utilizar. No obstante, hay que tener en cuenta que todos los programas para poder ser ejecutados, han de traducirse siempre al lenguaje máquina que es el único que entiende la computadora.
