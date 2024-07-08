---
type: b7179839-30ff-4f73-b5ed-073b6e9789e2
title: PROG - UNIDAD 2
icon: null
createdAt: '2023-10-30T22:39:19.906Z'
creationDate: 2023-10-30 23:39
modificationDate: 2023-11-12 07:28
tags: []
coverImage: descarga
author: null
---




> # PROGRAMACIÓN

- Tutor => Manuel González Ariza




> ## UNIDAD 2

- **Java SE** (Standar Edition): Plataforma de desarrollo de programas en java compuesta por el lenguaje de programación java, un conjunto de bibliotecas estandard, un conjunto de herramientas para el desarrollo de y la máquina virtual para ejecutar lo programas en código de bytes.

- La plataforma **Java SE** está formada principalmente por dos productos: el [JDK](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/1_introduccin.html#t18b43ba2-871d-dd9b-0b11-4ee55682210b), que contiene los [compiladores](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/1_introduccin.html#t45341739-911d-c141-fcff-30c4826ff2cb) y [depuradores](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/1_introduccin.html#t09cdbb79-d7b0-e77d-933e-cfb12dd10f05) necesarios para programar, y el [JRE](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/1_introduccin.html#t2d298918-ca31-841b-ab95-2ae215c71e35), que proporciona las librerías o bibliotecas y la [JVM](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/1_introduccin.html#t28fedae0-164d-a87d-e783-0cb271872bde), entre otra serie de componentes.

- [https://docs.oracle.com/en/java/javase/14/](https://docs.oracle.com/en/java/javase/14/)

- [https://docs.oracle.com/javase/specs/](https://docs.oracle.com/javase/specs/)



> #  2. Las variables e identificadores

- Una [variable](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/2_las_variables_e_identificadores.html#t4c2f6dfc-b9e5-24c8-907a-808a76b865c0) es una zona en la memoria del computador con un valor que puede ser almacenado para ser usado más tarde en el programa.

Las variables vienen determinadas por:

- Un nombre, que permite al programa acceder al valor que contiene en memoria. Debe ser un identificador válido.

- Un [tipo de dato,](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/2_las_variables_e_identificadores.html#tdb107421-a49c-9aea-2962-4fde06db9a80) que especifica qué clase de información guarda la variable en esa zona de memoria

- Un rango de valores que puede admitir dicha variable, que vendrá determinado por el tipo de dato.

Al nombre que le damos a la variable se le llama **identificador**. Los identificadores permiten nombrar los elementos que se están manejando en un programa. Vamos a ver con más detalle ciertos aspectos sobre los identificadores que debemos tener en cuenta.

- [Thinking in Java - Bruce Eckel](https://app.capacities.io/76334381-c842-46cb-9d17-31741118c229/b6505041-33d2-4512-b8f8-ae02c22879e8)



- IDENTIFICADORES

- Un `identificador `en Java es una secuencia ilimitada sin espacios de letras y dígitos [Unicode](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/21_identificadores.html#t286080d3-071a-459f-7fc6-f58a8dd9492a), de forma que **el primer símbolo de la secuencia debe ser una letra, un símbolo de subrayado (_) o el símbolo dólar ($)**.

- El estándar Unicode originalmente utilizaba 16 bits, pudiendo representar hasta 65.536 caracteres distintos, que es el resultado de elevar dos a la potencia dieciséis. Actualmente Unicode puede utilizar más o menos bits, dependiendo del formato que se utilice: **UTF-8**, **UTF-16** ó **UTF-32. A cada carácter le corresponde unívocamente un número entero perteneciente al intervalo de 0 a 2 elevado a n, siendo n el número de bits utilizados para representar los caracteres. Por ejemplo, la letra** ñ es el entero 164. Además, el código Unicode es “compatible” con el código ASCII, ya que para los caracteres del código ASCII, Unicode asigna como código los mismos 8 bits, a los que les añade a la izquierda otros 8 bits todos a cero. La conversión de un carácter ASCII a Unicode es inmediata.



- CONVENIOS Y REGLAS PARA NOMBRAR VARIABLES

A la hora de nombrar un identificador existen una serie de normas de estilo de uso generalizado que, no siendo obligatorias, se usan en la mayor parte del código Java. Estas reglas para la nomenclatura de variables son las siguientes:

- **Java distingue las mayúsculas de las minúsculas**. Por ejemplo, `Alumno` y `alumno` son variables diferentes.

- **No se suelen utilizar identificadores que comiencen con «****$****» o «****_****»****,** además el símbolo del dólar, por convenio, no se utiliza nunca.

- **No se puede utilizar el valor booleano** (`true` o `false`) **ni el valor nulo** (`null`).

- Los **identificadores deben ser lo más descriptivos posibles**. Es mejor usar palabras completas en vez de abreviaturas crípticas. Así nuestro código será más fácil de leer y comprender. En muchos casos también hará que nuestro código se autodocumente. Por ejemplo, si tenemos que darle el nombre a una variable que almacena los datos de un cliente sería recomendable que la misma se llamara algo así como `FicheroClientes` o `ManejadorCliente`, y no algo poco descriptivo como `Cl33`.



Además de estas restricciones, en la siguiente tabla puedes ver otras convenciones, que no siendo obligatorias, sí son recomendables a la hora de crear identificadores en Java.

- **Nombre de variable.** Comienza por letra minúscula, y si tienen más de una palabra se colocan juntas y el resto comenzando por mayúsculas. `numAlumnos, suma`

- **Nombre de constante**. En letras mayúsculas, separando las palabras con el guión bajo, por convenio el guión bajo no se utiliza en ningún otro sitio. `TAM_MAX, PI`

- **Nombre de una clase**. Comienza por letra mayúscula.`String, MiTipo`Nombre de función.Comienza con letra minúscula.`modifica_Valor, obtiene_Valor`

- **Nombre de función**. omienza con letra minúscula.`modifica_Valor, obtiene_Valor`



- PALABRAS RESERVADAS

Las palabras reservadas, a veces también llamadas palabras clave o keywords , son secuencias de caracteres formadas con letras ASCII cuyo uso se reserva al lenguaje y, por tanto, **no pueden utilizarse para crear identificadores.**

Las palabras reservadas en Java son:



Hay palabras reservadas que no se utilizan en la actualidad, como es el caso de `const` y `goto`, que apenas se utilizan en la actual implementación del lenguaje Java. Por otro lado, puede haber otro tipo de palabras o texto en el lenguaje que aunque no sean palabras reservadas tampoco se pueden utilizar para crear identificadores. Es el caso de `true` y `false` que, aunque puedan parecer palabras reservadas, porque no se pueden utilizar para ningún otro uso en un programa, técnicamente son **literales booleanos**. Igualmente, `null` es considerado un literal, no una palabra reservada.



- TIPOS DE VARIABLES

En un programa nos podemos encontrar distintos tipos de variables. Las diferencias entre una variable y otra dependerán de varios factores, por ejemplo, el tipo de datos que representan, si su valor cambia o no durante la ejecución, o cuál es el papel que llevan a cabo. De esta forma, el lenguaje de programación Java define los siguientes tipos de variables:

1. **Variables de tipos primitivos y variables referencia,** según el tipo de información que contengan. En función de a qué grupo pertenezca la variable, tipos primitivos o tipos referenciados, podrá tomar unos valores u otros, y se podrán definir sobre ella unas operaciones u otras.

2. **Variables y constantes**, dependiendo de si su valor cambia o no durante la ejecución del programa. La definición de cada tipo sería:

    - **Variables**. Sirven para almacenar los datos durante la ejecución del programa, pueden estar formadas por cualquier tipo de dato primitivo o referencia. Su valor puede cambiar a lo largo de la ejecución del programa. Realmente una variable representa una zona de memoria del ordenador que contiene un determinado valor (del tipo de datos de la variable) y al que se accede a través del identificador.

    - **Constantes o variables finales:** Son aquellas variables cuyo valor no cambia a lo largo de todo el programa.

3. **Variables miembro y variables locales**, en función del lugar donde aparezcan en el programa. La definición concreta sería:

    - **Variables miembro:** Son las variables que se crean dentro de una [clase](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/24_tipos_de_variables.html#t927a49e3-6a6f-6640-b6ea-6456cb692cb4), fuera de cualquier [método.](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/24_tipos_de_variables.html#tc122665f-eb8a-f8f7-63ac-afd3e923842a) Pueden ser de tipos primitivos o referencias, variables o constantes. En un lenguaje puramente orientado a objetos como es Java, todo se basa en la utilización de [objetos](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/24_tipos_de_variables.html#t0045217a-e7fc-7d52-590f-e3adef80336c), los cuales se crean usando clases. En la siguiente unidad veremos los distintos tipos de variables miembro que se pueden usar.

    - **Variables locales:** Son las variables que se crean y usan dentro de un método o, en general, dentro de cualquier bloque de código. La variable deja de existir cuando la ejecución del bloque de código o el método finaliza. Al igual que las variables miembro, las variables locales también pueden ser de tipos primitivos o referencias.



- TIPOS DE VARIABLES II

- **Variable constante llamada** `PI`: esta variable por haberla declarado como constante no podrá cambiar su valor a lo largo de todo el programa.

- **Variable miembro llamada** `x`**:** Esta variable pertenece a la clase `ejemplovariables`. La variable x puede almacenar valores del tipo primitivo `int`. El valor de esta variable podrá ser modificado en el programa, normalmente por medio de algún otro método que se cree en la clase.

- **Variable local llamada** `valorantiguo`**:** Esta variable es local porque está creada dentro del método `obtenerX()`. Sólo se podrá acceder a ella dentro del método donde está creada, ya que fuera de él no existe.

- [PROG02_CONT_R10_ejemplovariables](https://app.capacities.io/76334381-c842-46cb-9d17-31741118c229/2e8333e8-65ed-484f-b060-ebdd3c35f5fa)



---


> # 3. Los tipos de datos

- En los [lenguajes fuertemente tipados](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/3_los_tipos_de_datos.html#t339f0b74-324c-1b4b-15fd-e61acd8a543b), a todo dato (constante, variable o expresión) le corresponde un tipo que es conocido antes de que se ejecute el programa.

El tipo limita el valor de la variable o expresión, las operaciones que se pueden hacer sobre esos valores, y el significado de esas operaciones. Esto es así porque **un tipo de dato no es más que una especificación de los valores que son válidos para esa variable , y de las operaciones que se pueden realizar con ellos.**

- Debido a que el tipo de dato de una variable se conoce durante la revisión que hace el compilador para detectar errores, o sea en tiempo de compilación, esta labor es mucho más fácil, ya que no hay que esperar a que se ejecute el programa para saber qué valores va a contener esa variable. Esto se consigue con un control muy exhaustivo de los tipos de datos que se utilizan, lo cual tiene sus ventajas e inconvenientes, por ejemplo cuando se intenta asignar un valor de un tipo, a una variable de otro tipo. Sin embargo, en Java, puede haber conversión entre ciertos tipos de datos, como veremos posteriormente.

Los tipos de datos en Java se dividen principalmente en dos categorías:

- **Tipos de datos sencillos o primitivos**. Representan valores simples que vienen predefinidos en el lenguaje; contienen valores únicos, como por ejemplo un carácter o un número.

- **Tipos de datos referenci****a.** Se definen con un nombre o referencia (puntero) que contiene la dirección en memoria de un valor o grupo de valores. Dentro de este tipo tenemos por ejemplo los vectores o arrays, que son una serie de elementos del mismo tipo, o las clases, que son los modelos o plantillas a partir de los cuales se crean los objetos.



- TIPO DE DATOS PRIMITIVOS I

- Los tipos primitivos son aquéllos datos sencillos que constituyen los tipos de información más habituales: números, caracteres y valores lógicos o booleanos.

- ***Al contrario que en otros lenguajes de programación orientados a objetos, estas variables en*** ***Java no son objetos******.***

- Una de las mayores ventajas de tratar con tipos primitivos en lugar de con objetos, es que el compilador de Java puede optimizar mejor su uso. Otra importante característica, es que cada uno de los tipos primitivos tiene **idéntico** tamaño y comportamiento en todas las versiones de Java y para cualquier tipo de ordenador. Esto quiere decir que no debemos preocuparnos de cómo se representarán los datos en distintas plataformas, y asegura la **portabilidad** de los programas, a diferencia de lo que ocurre con otros lenguajes. Por ejemplo, el tipo `int` siempre se representará con 32 bits, con signo, y en el formato de representación [complemento a 2](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/31_tipos_de_datos_primitivos_i.html#t6018a373-01ce-c0ee-2095-ee2b75765d3d), en cualquier plataforma que soporte Java.



- Tipos de datos primitivos en Java:

1. **byte:** Este tipo de dato se utiliza para representar números enteros de 8 bits con signo. Tiene un rango de -128 a 127.

2. **short:** Los valores de tipo `short` representan enteros de 16 bits con signo, con un rango de -32,768 a 32,767.

3. **int:** El tipo de dato `int` se usa para representar enteros de 32 bits con signo y tiene un rango de -2,147,483,648 a 2,147,483,647. Es uno de los tipos de datos más utilizados para números enteros.

4. **long:** Para representar números enteros de 64 bits con signo, puedes utilizar el tipo `long`. Su rango es muy amplio, desde -9,223,372,036,854,775,808 hasta 9,223,372,036,854,775,807.

5. **float:** El tipo `float` se utiliza para representar números en punto flotante de precisión simple (32 bits). Se usa para números decimales y su representación es aproximada.

6. **double:** Los valores de tipo `double` son números en punto flotante de precisión doble (64 bits). Proporcionan una mayor precisión que los `float` y se utilizan comúnmente para cálculos científicos y financieros.

7. **char:** El tipo `char` se emplea para representar un carácter Unicode de 16 bits. Puedes almacenar letras, números y otros caracteres en una variable de tipo `char`.

8. **boolean:** Este tipo de dato es booleano y solo puede tener dos valores: `true` o `false`. Se utiliza para expresar condiciones lógicas




- TIPO DE DATOS PRIMITIVOS II

El tipo de dato `real `permite representar cualquier número con decimales. Al igual que ocurre con los enteros, la mayoría de los lenguajes definen más de un tipo de dato real, en función del número de bits usado para representarlos. Cuanto mayor sea ese número:

- **Más grande podrá ser el número real representado en valor absoluto.**

- **Mayor será la precisión** de la parte decimal.

Entre cada dos números reales cualesquiera, siempre tendremos infinitos números reales, por lo que **la mayoría de ellos los representaremos de forma aproximada.** Por ejemplo, en la aritmética convencional, cuando dividimos 10 entre 3, el resultado es 3.3333333…, con la secuencia de 3 repitiéndose infinitamente. En el ordenador sólo podemos almacenar un número finito de bits, por lo que el almacenamiento de un número real será siempre una aproximación.

Los números reales se representan en coma flotante, que consiste en trasladar la coma decimal a la primera cifra significativa del valor, con objeto de poder representar el máximo de números posible.

Un número se expresa como: 

En concreto, sólo se almacena la **mantisa** y el exponente al que va elevada la base. Los bits empleados por la mantisa representan la **precisión** del número real, es decir, el número de cifras decimales significativas que puede tener el número real, mientras que los bits del exponente expresan la diferencia entre el mayor y el menor número representable, lo que viene a ser el **intervalo de representación**.

En Java las variables de tipo `float` se emplean para representar los números en coma flotante de simple precisión de 32 bits, de los cuales 24 son para la mantisa y 8 para el exponente. La mantisa es un valor entre -1.0 y 1.0 y el exponente representa la potencia de 2 necesaria para obtener el valor que se quiere representar. Por su parte, las variables tipo `double` representan los números en coma flotante de doble precisión de 64 bits, de los cuales 53 son para la mantisa y 11 para el exponente.

La mayoría de los programadores en Java emplean el tipo `double` cuando trabajan con datos de tipo real, es una forma de asegurarse de que los errores cometidos por las sucesivas aproximaciones sean menores. De hecho, Java considera los valores en coma flotante como de tipo `double` por defecto.




- DECLARACION E INICIALIZACIÓN

Las variables se pueden declarar en cualquier bloque de código, dentro de llaves. Y lo hacemos indicando su identificador y el tipo de dato, separadas por comas si vamos a declarar varias a la vez, por ejemplo: 

```java
int nmAlumnos = 15;
double radio = 3.14, importe = 102.95;
```



De esta forma, estamos declarando `numAlumnos` como una variable de tipo `int`, y otras dos variables `radio` e `importe` de tipo double. Aunque no es obligatorio, hemos aprovechado la declaración de las variables para inicializarlas a los valores 15, 3.14 y 102.95 respectivamente.

Si la variable va a permanecer inalterable a lo largo del programa, la declararemos como `constante`, utilizando la palabra reservada `final` de la siguiente forma:

```java
final double PI = 3.1415926536;
```



En ocasiones puede que al declarar una variable no le demos valor, ¿Qué crees que ocurre en estos casos? Pues que el compilador le asigna un valor por defecto, aunque depende del tipo de variable que se trate:

- Las **variables miembro** sí se inicializan automáticamente, si no les damos un valor. Cuando son de tipo numérico, se inicializan por defecto a `0`, si don de tipo carácter, se inicializan al carácter `null` (\0), si son de tipo `boolean` se les asigna el valor por defecto `false`, y si son tipo referenciado se inicializan a `null`.

- Las **variables locales** no se inicializan automáticamente. Debemos asignarles nosotros un valor antes de ser usadas, ya que si el compilador detecta que la variable se usa antes de que se le asigne un valor, produce un error. Por ejemplo en este caso:

```java
int p;

if (. . . )

     p = 5 ;

int q = p; // error
```




- TIPOS REFENCIADOS

A partir de los ocho tipos datos primitivos, se pueden construir otros tipos de datos. Estos tipos de datos se llaman **tipos referenciados** o **referencias**, porque se utilizan para almacenar la dirección de los datos en la memoria del ordenador.

```java
int[] arrayDeEnteros;

Cuenta cuentaCliente;
```



En la primera instrucción declaramos una lista de números del mismo tipo, en este caso, enteros. En la segunda instrucción estamos declarando la variable u objeto `cuentaCliente` como una referencia de tipo `Cuenta`.

Como comentábamos al principio del apartado de Tipos de datos, cualquier aplicación de hoy en día necesita no perder de vista una cierta cantidad de datos. Cuando el conjunto de datos utilizado tiene características similares se suelen agrupar en estructuras para facilitar el acceso a los mismos, son los llamados **datos estructurados**. Son datos estructurados los **arrays, listas, árboles**, etc. Pueden estar en la memoria del programa en ejecución, guardados en el disco como ficheros, o almacenados en una base de datos. Trabajaremos en profundidad con datos estructurados en unidades posteriores.

Además de los ocho tipos de datos primitivos que ya hemos descrito, Java proporciona un tratamiento especial a los textos o cadenas de caracteres mediante el tipo de dato `String`. Java crea automáticamente un nuevo objeto de tipo `String` cuando se encuentra una cadena de caracteres encerrada entre comillas dobles. En realidad se trata de objetos, y por tanto son tipos referenciados, pero se pueden utilizar de forma sencilla como si fueran variables de tipos primitivos:

```java
String mensaje;

mensaje= "El primer programa";
```



Para mostrar por pantalla un mensaje utilizamos `System.out`, conocido como la salida estándar del programa. Este método lo que hace es escribir un conjunto de caracteres a través de la línea de comandos. En Netbeans esta línea de comandos aparece en la parte inferior de la pantalla. Podemos utilizar `System.out.print` o `System.out.println`. En el segundo caso lo que hace el método es que justo después de escribir el mensaje, sitúa el cursor al principio de la línea siguiente. El texto en color gris que aparece entre caracteres // son comentarios que permiten documentar el código, pero no son tenidos en cuenta por el compilador y, por tanto, no afectan a la ejecución del programa.

[https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/PROG02_CONT_R18_Ejemplotipos.jpg](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/PROG02_CONT_R18_Ejemplotipos.jpg)



- TIPOS ENUMERADOS

Los **tipos de datos enumerados** son una forma de declarar una variable con un conjunto restringido de valores. Por ejemplo, los días de la semana, las estaciones del año, los meses, etc. Es como si definiéramos nuestro propio tipo de datos.

La forma de declararlos es con la palabra reservada `enum`, seguida del nombre de la variable y la lista de valores que puede tomar entre llaves. A los valores que se colocan dentro de las llaves se les considera como constantes, van separados por comas y deben ser valores únicos.

La lista de valores se coloca entre llaves, porque un tipo de datos `enum` no es otra cosa que una especie de clase en Java, y todas las clases llevan su contenido entre llaves.

Al considerar Java este tipo de datos como si de una clase se tratara, no sólo podemos definir los valores de un tipo enumerado, sino que también podemos definir operaciones a realizar con él y otro tipo de elementos, lo que hace que este tipo de dato sea más versátil y potente que en otros lenguajes de programación.



En el siguiente ejemplo puedes comprobar el uso que se hace de los tipos de datos enumerados. Tenemos una variable `Dias` que almacena los días de la semana. Para acceder a cada elemento del tipo enumerado se utiliza el nombre de la variable seguido de un punto y el valor en la lista. Más tarde veremos que podemos añadir métodos y campos o variables en la declaración del tipo enumerado, ya que como hemos comentado un tipo enumerado en Java tiene el mismo tratamiento que las clases.



En este ejemplo hemos utilizado el método `System.out.print`. Como podrás comprobar si lo ejecutas, la instrucción número 18 escribe el texto que tiene entre comillas pero no salta a la siguiente línea, por lo que el la instrucción número 19 escribe justo a continuación.

Sin embargo, también podemos escribir varias líneas usando una única sentencia. Así lo hacemos en la instrucción número 20, la cual imprime como resultado tres líneas de texto. Para ello hemos utilizado un carácter especial, llamado **carácter escape** (`\`). Este carácter sirve para darle ciertas órdenes al compilador, en lugar de que salga impreso en pantalla. Después del carácter de escape viene otro carácter que indica la orden a realizar, juntos reciben el nombre de **secuencia de escape**. La secuencia de escape `\n` recibe el nombre de **carácter de nueva línea**. Cada vez que el compilador se encuentra en un texto ese carácter, el resultado es que mueve el cursor al principio de la línea siguiente. En el próximo apartado vamos a ver algunas de las secuencias de escape más utilizadas.



---


> # 4. Literales de los tipos primitivos

Un **literal**, **valor literal** o **constante literal** es un valor concreto para los tipos de datos primitivos del lenguaje, el tipo `String` o el tipo `null`.

Los **literales booleanos** tienen dos únicos valores que puede aceptar el tipo: `true` y `false`. Por ejemplo, con la instrucción `boolean encontrado = true;` estamos declarando una variable de tipo booleana a la cual le asignamos el valor literal `true`.

Los **literales enteros** se pueden representar en tres notaciones:

- **Decimal**: por ejemplo `20`. Es la forma más común.

- **Octal**: por ejemplo `024`. Un número en octal siempre empieza por cero, seguido de dígitos octales (del 0 al 7).

- **Hexadecimal**: por ejemplo `0x14`. Un número en hexadecimal siempre empieza por `0x` seguido de dígitos hexadecimales (del 0 al 9, de la ‘a’ a la ‘f’ o de la ‘A’ a la ‘F’).



Las constantes literales de tipo `long` se le debe añadir detrás una **l** ó **L**, por ejemplo `873L`, si no se considera por defecto de tipo `int`. Se suele utilizar **L** para evitar la confusión de la ele minúscula con 1.

Los **literales** **reales** o en coma flotante se expresan con coma decimal o en notación científica, o sea, seguidos de un exponente **e** ó **E**. El valor puede finalizarse con una f o una F para indica el formato float o con una d o una D para indicar el formato `double` (por defecto es `double`). Por ejemplo, podemos representar un mismo literal real de las siguientes formas: `13.2, 13.2D, 1.32e1, 0.132E2`. Otras constantes literales reales son por ejemplo: `.54, 31.21E-5, 2.f, 6.022137e+23f, 3.141e-9d.`

Un **literal carácter** puede escribirse como un carácter entre comillas simples como `'a', 'ñ', 'Z', 'p'`, etc. o por su código de la tabla Unicode, anteponiendo la secuencia de escape `‘\’` si el valor lo ponemos en octal o `‘\u’` si ponemos el valor en hexadecimal. Por ejemplo, si sabemos que tanto en ASCII como en Unicode, la letra A (mayúscula) es el símbolo número 65, y que 65 en octal es 101 y 41 en hexadecimal, podemos representar esta letra como `'\101'` en octal y `'\u0041'` en hexadecimal. Existen unos caracteres especiales que se representan utilizando secuencias de escape:

Secuencias de escape en Java

Secuencia de escape

`\b `Retroceso

`\r `Retorno de carro

`\t `Tabulador

`\'' `Carácter comillas dobles

`\n `Salto de línea

`\' `Carácter comillas simples

`\f `Salto de página

`\\ `Barra diagonal



N**ormalmente, los objetos en Java deben ser creados con la orden** `new`**. Sin embargo, los literales String no lo necesitan ya que son objetos que se crean implícitamente por Java.**

Los **literales de cadenas de caracteres** se indican entre comillas dobles. En el ejemplo anterior “`El primer programa`” es un literal de tipo cadena de caracteres. Al construir una cadena de caracteres se puede incluir cualquier carácter Unicode excepto un carácter de retorno de carro, por ejemplo en la siguiente instrucción utilizamos la secuencia de escape \’’ para escribir dobles comillas dentro del mensaje:

```java
String texto = "Juan dijo: \"Hoy hace un día fantástico…\"";
```




> ## 5.  Operadores y expresiones

- Los ***operadores***llevan a cabo operaciones sobre un conjunto de datos u operandos, representados por literales y/o identificadores. Los operadores pueden ser unarios, binarios o terciarios, según el número de operandos que utilicen sean uno, dos o tres, respectivamente. Los operadores actúan sobre los tipos de datos primitivos y devuelven también un tipo de dato primitivo.

       Los operadores se combinan con los literales y/o identificadores para formar ***expresiones.***



- Una **expresión** es una combinación de operadores y operandos que se evalúa produciendo un único resultado de un tipo determinado.

       El resultado de una expresión puede ser usado como parte de otra expresión o en una sentencia o instrucción. Las expresiones, combinadas con             algunas palabras reservadas o por sí mismas, forman las llamadas **sentencias** o **instrucciones**.

       Por ejemplo, pensemos en la siguiente expresión Java:

```java
i + 1:
```

Con esta expresión estamos utilizando un operador aritmético para sumarle una cantidad a la variable i, pero es necesario indicar al programa qué hacer con el resultado de dicha expresión.

```java
suma = i + 1;
```

Como curiosidad comentar que las expresiones de asignación, al poder ser usadas como parte de otras asignaciones u operaciones, son consideradas tanto expresiones en sí mismas como sentencias.



5.1 OPERADORES ARITMÉTICOS

- [https://www.arkaitzgarro.com/java/capitulo-4.html](https://www.arkaitzgarro.com/java/capitulo-4.html)

- Los operadores aritméticos son aquellos operados que combinados con los operandos forman expresiones matemáticas o aritméticas.



El resultado de este tipo de expresiones depende de los operandos que utilicen:

Resultados de las operaciones aritméticas en Java

- Un operando de tipo `long` y ninguno real (`float` o `double`)   =**>** `long`

- Ningún operando de tipo `long` ni real (`float` o `double`) =**>** `int`

- Al menos un operando de tipo `double`  =**>** `double`

- Al menos un operando de tipo `float` y ninguno `double` =**>** `float`



Otro tipo de operadores aritméticos son los operadores unarios incrementales y decrementales. Producen un resultado del mismo tipo que el operando, y podemos utilizarlos con **notación prefija**, si el operador aparece antes que el operando, o **notación** **postfija**, si el operador aparece después del operando. En la tabla puedes un ejemplo de de utilización de cada operador incremental.




5.2 OPERADORES DE ASIGANCION

El principal operador de esta categoría es el operador asignación `“=”,` que permite al programa darle un valor a una variable, y ya hemos utilizado varias ocasiones en esta unidad. Además de este operador, Java proporciona otros operadores de asignación combinados con los operadores aritméticos, que permiten abreviar o reducir ciertas expresiones.

Por ejemplo, el operador `“+=”` suma el valor de la expresión a la derecha del operador con el valor de la variable que hay a la izquierda del operador, y almacena el resultado en dicha variable. En la siguiente tabla se muestran todos los operadores de asignación compuestos que podemos utilizar en Java.







5.3 OPERADORES DE CONDICIONAL

El operador condicional “`?:`” sirve para evaluar una condición y devolver un resultado en función de si es verdadera o falsa dicha condición. Es el único operador ternario de Java, y como tal, necesita tres operandos para formar una expresión.

El primer operando se sitúa a la izquierda del símbolo de interrogación, y siempre será una expresión booleana, también llamada condición. El siguiente operando se sitúa a la derecha del símbolo de interrogación y antes de los dos puntos, y es el valor que devolverá el operador condicional si la condición es verdadera. El último operando, que aparece después de los dos puntos, es la expresión cuyo resultado se devolverá si la condición evaluada es falsa.

```java
condicion ? exp1 : exp2;

(x>y)?x:y;  // Se evalúa la condición de si x es mayor que y, en caso afirmativo se devuelve el valor de la variable x, y en caso contrario se devuelve el valor de y.
```

El operador condicional se puede sustituir por la sentencia `if…then…else` que veremos en la siguiente unidad de Estructuras de control.




5.4 OPERADORES DE RELACION

Los operadores relacionales se utilizan para comparar datos de tipo primitivo (numérico, carácter y booleano). El resultado se utilizará en otras expresiones o sentencias, que ejecutarán una acción u otra en función de si se cumple o no la relación.

Estas expresiones en Java dan siempre como resultado un valor booleano true o false. En la tabla siguiente aparecen los operadores relacionales en Java.



Hasta ahora hemos visto ejemplos que creaban variables y se inicializaban con algún valor. Pero ¿y si lo que queremos es que el usuario introduzca un valor al programa? Entonces debemos agregarle interactividad a nuestro programa, por ejemplo utilizando la clase `Scanner`. Aunque no hemos visto todavía qué son las clases y los objetos, de momento vamos a pensar que la clase `Scanner` nos va a permitir leer los datos que se escriben por teclado, y que para usarla es necesario importar el paquete de clases que la contiene. El código del ejemplo lo tienes a continuación. El programa se quedará esperando a que el usuario escriba algo en el teclado y pulse la tecla intro. En ese momento se convierte lo leído a un valor del tipo `int` y lo guarda en la variable indicada. Además de los operadores relacionales, en este ejemplo utilizamos también el operador condicional, que compara si los números son iguales. Si lo son, devuelve la cadena iguales y sino, la cadena distintos.





5.5 OPERADORES LOGICOS

Los operadores lógicos realizan operaciones sobre valores booleanos, o resultados de expresiones relacionales, dando como resultado un valor booleano.

Los operadores lógicos los podemos ver en la tabla que se muestra a continuación. Existen ciertos casos en los que el segundo operando de una expresión lógica no se evalúa para ahorrar tiempo de ejecución, porque con el primero ya es suficiente para saber cuál va a ser el resultado de la expresión.

Por ejemplo, en la expresión `a && b` si `a` es falso, no se sigue comprobando la expresión, puesto que ya se sabe que la condición de que ambos sean verdadero no se va a cumplir. En estos casos es más conveniente colocar el operando más propenso a ser falso en el lado de la izquierda. Igual ocurre con el operador `||`, en cuyo caso es más favorable colocar el operando más propenso a ser verdadero en el lado izquierdo.





```java
OPERADORES LÓGICOS
Negacion:
 ! false es : true
 ! true es : false
Operador AND (&):
 false & false es : false
 false & true es : false
 true & false es : false
 true & true es : true
Operador OR (|):
 false | false es : false
 false | true es : true
 true | false es : true
 true | true es : true
Operador OR Exclusivo (^):
 false ^ false es : false
 false ^ true es : true
 true ^ false es : true
 true ^ true es : false
Operador &&:
 false && false es : false
 false && true es : false
 true && false es : false
 true && true es : true
Operador ||:
 false || false es : false
 false || true es : true
 true || false es : true
 true || true es : true
```

En el siguiente código puedes ver un ejemplo de utilización de operadores lógicos:



5.6 OPERADORES DE BITS

Los operadores a nivel de bits se caracterizan porque realizan operaciones sobre números enteros (o `char`) en su representación binaria, es decir, sobre cada dígito binario.



5.7 OPERADORES CON CADENAS

Ya hemos visto en el apartado de literales que el objeto `String` se corresponde con una secuencia de caracteres entrecomillados, como por ejemplo “`hola`”. Este literal se puede utilizar en Java como si de un tipo de datos primitivo se tratase, y, como caso especial, no necesita la orden `new` para ser creado.

Para aplicar una operación a una variable de tipo `String`, escribiremos su nombre seguido de la operación, separados por un punto. Entre las principales operaciones que podemos utilizar para trabajar con cadenas de caracteres están las siguientes:

- **Creación**. Como hemos visto en el apartado de literales, podemos crear una variable de tipo `String` simplemente asignándole una cadena de caracteres encerrada entre comillas dobles.

- **Obtención de longitud**. Si necesitamos saber la longitud de un String, utilizaremos el método `length()`.

- **Concatenación**. Se utiliza el operador + o el método `concat()` para concatenar cadenas de caracteres.

    - **Comparación**. El método `equals()` nos devuelve un valor booleano que indica si las cadenas comparadas son o no iguales. El método `equalsIgnoreCase()` hace lo propio, ignorando las mayúsculas de las cadenas a considerar.

- **Obtención de subcadenas**. Podemos obtener cadenas derivadas de una cadena original con el método `substring()`, al cual le debemos indicar el inicio y el fin de la subcadena a obtener.

- **Cambio a mayúsculas/minúsculas**. Los métodos `toUpperCase()` y `toLowerCase()` devuelven una nueva variable que transforma en mayúsculas o minúsculas, respectivamente, la variable inicial.

- `Valueof`. Utilizaremos este método para convertir un tipo de dato primitivo (`int`, `long`, `float`, etc.) a una variable de tipo `String`.

A continuación varios ejemplos de las distintas operaciones que podemos realizar concadenas de caracteres o String en Java:





5.8 PRECEDENCIA DE OPERADORES

El orden de precedencia de los operadores determina la secuencia en que deben realizarse las operaciones cuando en una expresión intervienen operadores de distinto tipo.

Las reglas de precedencia de operadores que utiliza Java coinciden con las reglas de las expresiones del álgebra convencional. Por ejemplo:

- La multiplicación, división y resto de una operación se evalúan primero. Si dentro de la misma expresión tengo varias operaciones de este tipo, empezaré evaluándolas de izquierda a derecha.

- La suma y la resta se aplican después que las anteriores. De la misma forma, si dentro de la misma expresión tengo varias sumas y restas empezaré evaluándolas de izquierda a derecha.

A la hora de evaluar una expresión es necesario tener en cuenta la `asociatividad `de los operadores. La asociatividad indica qué operador se evalúa antes, en condiciones de igualdad de precedencia. Los operadores de asignación, el operador condicional (`?:`), los operadores incrementales (`++, --`) y el casting son asociativos por la derecha. El resto de operadores son asociativos por la izquierda, es decir, que se empiezan a calcular en el mismo orden en el que están escritos: de izquierda a derecha. Por ejemplo, en la expresión siguiente:

```java
10 / 2 * 5;
```

Realmente la operación que se realiza es `(10 / 2 ) * 5`, porque ambos operadores, división y multiplicación, tienen igual precedencia y por tanto se evalúa primero el que antes nos encontramos por la izquierda, que es la división. El resultado de la expresión es `25`. Si fueran asociativos por la derecha, puedes comprobar que el resultado sería diferente, primero multiplicaríamos `2 * 5` y luego dividiríamos entre `10`, por lo que el resultado sería 1. En esta otra expresión

```java
x = y = z = 1;
```

Realmente la operación que se realiza es `x = (y = (z = 1))`. Primero asignamos el valor de `1` a la variable `z`, luego a la variable `y`, para terminar asignando el resultado de esta última asignación a `x`. Si el operador asignación fuera asociativo por la izquierda esta operación no se podría realizar, ya que intentaríamos asignar a `x` el valor de `y`, pero `y` aún no habría sido inicializada.

En la tabla se detalla el orden de` precedencia y la asociatividad de los operadores` que hemos comentado en este apartado. Los operadores se muestran de mayor a menor precedencia.



---



> ## 6. CONVERSION DE TIPO

Imagina que queremos dividir un número entre otro ¿tendrá decimales el resultado de esa división? Podemos pensar que siempre que el denominador no sea divisible entre el divisor, tendremos un resultado con decimales, pero no es así. Si el denominador y el divisor son variables de tipo entero, el resultado será entero y no tendrá decimales. Para que el resultado tenga decimales necesitaremos hacer una `conversión de tipo`.

Las conversiones de tipo se realizan para hacer que el resultado de una expresión sea del tipo que nosotros deseamos, en el ejemplo anterior para hacer que el resultado de la división sea de tipo real y, por ende, tenga decimales. Existen dos tipos de conversiones:

- `Conversiones automáticas`. Cuando a una variable de un tipo se le asigna un valor de otro tipo numérico con menos bits para su representación, se realiza una conversión automática. En ese caso, el valor se dice que es promocionado al tipo más grande (el de la variable), para poder hacer la asignación. También se realizan conversiones automáticas en las operaciones aritméticas, cuando estamos utilizando valores de distinto tipo, el valor más pequeño se promociona al valor más grande, ya que el tipo mayor siempre podrá representar cualquier valor del tipo menor (por ejemplo, de `int` a `long` o de `float` a `double`).

- `Conversiones explícitas`. Cuando hacemos una conversión de un tipo con más bits a un tipo con menos bits. En estos casos debemos indicar que queremos hacer la conversión de manera expresa, ya que se puede producir una pérdida de datos y hemos de ser conscientes de ello. Este tipo de conversiones se realiza con el **operador** `cast`. El operador `cast` es un operador unario que se forma colocando delante del valor a convertir el tipo de dato entre paréntesis. Tiene la misma precedencia que el resto de operadores unarios y se asocia de izquierda a derecha.

Debemos tener en cuenta que **un valor numérico nunca puede ser asignado a una variable de un tipo menor en rango, si no es con una conversión explícita**. Por ejemplo:

```java
int a;

byte b;

a = 12;			// no se realiza conversión alguna

b = 12;         	// se permite porque 12 está dentro  del rango permitido de valores para b

b = a;          	// error, no permitido (incluso aunque 12 podría almacenarse en un byte)

byte b = (byte) a;     	// Correcto, forzamos conversión explícita
```



---



> ## 7. COMENTARIOS

Los comentarios son muy importantes a la hora de describir qué hace un determinado programa. A lo largo de la unidad los hemos utilizado para documentar los ejemplos y mejorar la comprensión del código. Para lograr ese objetivo, es normal que cada programa comience con unas líneas de comentario que indiquen, al menos, una breve descripción del programa, el autor del mismo y la última fecha en que se ha modificado.

Todos los lenguajes de programación disponen de alguna forma de introducir comentarios en el código. En el caso de Java, nos podemos encontrar los siguientes tipos de comentarios:

- `Comentarios de una sola línea`. Utilizaremos el delimitador `//` para introducir comentarios de sólo una línea.

```java
// comentario de una sola línea
```



- `Comentarios de múltiples líneas`. Para introducir este tipo de comentarios, utilizaremos una barra inclinada y un asterisco (`/*`), al principio del párrafo y un asterisco seguido de una barra inclinada (`*/`) al final del mismo.

```java
/* Esto es un comentario

de varias líneas */
```



- `Comentarios Javadoc.` Utilizaremos los delimitadores /** y */. Al igual que con los comentarios tradicionales, el texto entre estos delimitadores será ignorado por el compilador. Este tipo de comentarios se emplean para generar documentación automática del programa. A través del programa javadoc, incluido en JavaSE , se recogen todos estos comentarios y se llevan a un documento en formato .html.

- [https://docs.oracle.com/javase/6/docs/technotes/guides/javadoc/index.html](https://docs.oracle.com/javase/6/docs/technotes/guides/javadoc/index.html)

```java
/** Comentario de documentación.

Javadoc extrae los comentarios del código y

genera un archivo html a partir de este tipo de comentarios

*/
```



- [Enlace a Conversion de tipos. Anexo I del Tema 2.](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/387843/mod_resource/content/7/anexo_i_conversin_de_tipos_de_datos_en_java.html)

---



> ## 8. CONCLUSIONES

Durante el desarrollo de esta unidad hemos trabajado con los diferentes tipos de datos del lenguaje Java, los diferentes tipos de variables existentes y los diferentes operadores que permiten la realización de operaciones con datos. Además, hemos aprendido a declarar los diferentes tipos de variables y a utilizar un amplio rango de operadores, analizando la precedencia en el  uso de los mismos. En el mapa conceptual se pueden observar los conceptos que hay que tener claros antes de abordar la siguiente unidad:



---

---

---
