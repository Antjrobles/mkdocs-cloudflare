

# BASE DE DATOS





# BASE DE DATOS RELACIONALES



> # 1 MODELO DE DATOS

Según el [DRAE](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/1_modelo_de_datos.html#td8fa412c-1fab-efec-948a-91f04af0b248), un modelo es, entre otras definiciones, el esquema teórico, generalmente en forma matemática, de un sistema o de una realidad compleja. Podemos decir que es la representación de cualquier aspecto o tema extraído del mundo real.

¿Qué sería entonces un modelo de datos? Aquél que nos permite describir los elementos que intervienen en una realidad o en un problema dado y la forma en que se relacionan dichos elementos entre sí.

*Contextualizando, un modelo de datos es por tanto un conjunto de métodos y reglas que indican cómo se ha de almacenar la información y cómo se han de manipular los datos.*

![Untitled](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/BD02_CONT_R03_modelodedatos.png)

En informática, el modelo de datos se implementa con un lenguaje utilizado para la descripción de una base de datos. Con este lenguaje vamos a poder describir las estructuras de los datos (tipos de datos y relaciones entre ellos), las restricciones de integridad (condiciones que deben cumplir los datos, según las necesidades de nuestro modelo basado en la realidad) y las operaciones de manipulación de los datos (insertado, borrado, modificación de datos).

Ese lenguaje, por lo general, presenta dos sublenguajes:

- `Lenguaje de Definición de Datos o DDL (Data Definition Language )` , cuya función es describir, de una forma abstracta, las estructuras de datos y las restricciones de integridad.

- `Lenguaje de Manipulación de Datos o DML (Data Manipulation Language)`, que sirve para describir las operaciones de manipulación de los datos.

Existen tres **fases de modelado** en el diseño de una base de datos basadas en el nivel de abstracción, es decir, en lo alejado que esté del mundo real y que deben ser realizadas en orden:

1. **Modelo de datos conceptual**: Se utiliza en el diseño conceptual. Es una representación (normalmente gráfica) de la realidad no comprometida con ningún entorno informático. Describen las estructuras de datos y restricciones de integridad. Se utilizan durante la etapa de análisis de un problema dado, y están orientados a representar los elementos que intervienen y sus relaciones. Es una fase muy importante ya que cualquier error en esta fase es arrastrado a las siguientes.

    Ejemplo, Modelo Entidad-Relación.

2. **Modelo Lógico**: Se utiliza en el diseño lógico. Determinan unos criterios de almacenamiento (formas de almacenar la información) y de operaciones de manipulación de datos dentro de un tipo de entorno informático. Los SGBD comerciales se basan en un modelo lógico concreto. Ejemplo, Modelo Relacional.

3. **Modelo Físico**: Se utiliza en el diseño físico. Es la implementación física del modelo anterior. Son estructuras de datos a bajo nivel, implementadas dentro de un sistema gestor de base de datos comercial, por ej. Oracle, mysql, etc,,

Los SGBD comerciales se basan en un modelo lógico concreto. Por ej. Oracle en el modelo relacional.



---



> # 2. TERMINOLOGIA DEL MODELO RELACIONAL

¿Sabes que el modelo relacional te va a permitir representar la información del mundo real de una manera intuitiva? Así es, pudiendo introducir conceptos cotidianos y fáciles de entender por cualquiera, aunque no sea experto en informática.

El modelo relacional fue propuesto por [Edgar Frank Codd](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/2_terminologa_del_modelo_relacional.html#t8e5085c7-6da0-a5fa-ff06-97720bfaa908) en los laboratorios de [IBM](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/2_terminologa_del_modelo_relacional.html#t644fde05-f688-33a1-e6e6-d13c5c2c9195) en California. Como hemos visto, se trata de un modelo lógico que establece una estructura sobre los datos, independientemente del modo en que luego los almacenemos. Es como si guardamos nuestra colección de libros, dependiendo del número de habitaciones que tenga en casa, del tamaño y forma de nuestras estanterías, podremos disponer nuestros libros de un modo u otro para facilitarnos el acceso y consulta. Los libros serán los mismos pero puedo disponerlos de distinta forma.

Es importante recordar que el diseño de las tablas del modelo relacional es la segunda fase del diseño de la base de datos y previamente se ha realizado el diseño conceptual identificando, tras el análisis,  las tablas o relaciones resultantes, sus atributos, restricciones y relaciones. 

El nombre de modelo relacional viene de la estrecha relación entre el elemento básico de este modelo y el concepto matemático de relación. Si tenemos dos conjuntos A y B, una relación entre estos dos conjuntos sería un subconjunto del [producto cartesiano](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/2_terminologa_del_modelo_relacional.html#tad59de70-3ed5-9f28-e3eb-b30142b4a050) AxB.


**Producto Cartesiano****:** Imagina que tienes dos conjuntos, digamos el conjunto A y el conjunto B. El producto cartesiano de A y B es como hacer todas las combinaciones posibles tomando un elemento de A y emparejándolo con cada elemento de B. Si A tiene 2 elementos y B tiene 3 elementos, el producto cartesiano tendría 6 combinaciones (2x3).

**En términos más simples:** Supongamos que A es un conjunto de colores (rojo, azul) y B es un conjunto de tamaños (pequeño, grande). El producto cartesiano sería todas las combinaciones posibles, como (rojo, pequeño), (rojo, grande), (azul, pequeño), (azul, grande).

**Relación con Bases de Datos:** En bases de datos, especialmente en el contexto de tablas relacionales, el producto cartesiano se utiliza al combinar datos de dos o más tablas. Si tienes una tabla con información sobre estudiantes y otra con información sobre cursos, el producto cartesiano podría ayudarte a crear una tabla que relacione cada estudiante con cada curso posible.

El producto cartesiano nos dará la relación de todos los elementos de un conjunto con todos los elementos de los otros conjuntos de ese producto. Al estar trabajando con conjuntos, no puede haber elementos repetidos.

Por ejemplo para los dos conjuntos que se presentan en la imagen, uno denominado Marcas que contiene marcas de coches y otro denominado Modelos que contiene diferentes modelos el resultado de la operación de producto cartesiano será la combinación de todos los elementos de un conjunto con los del otro.



> ## 2.1. RELACIÓN O TABLA. TUPLAS. DOMINIOS

A partir de ahora, nosotros veremos una relación como una **tabla** con **filas** y **columnas**. Podemos asociar atributos a columnas y tuplas a filas. 

- `Atributos`**:** es el nombre de cada dato que se almacena en la relación (tabla). En la tabla Alumnos, que se muestra, los atributos o columnas serían  DNI, nombre y  apellidos...



    El nombre del atributo debe describir el significado de la información que representa. En la tabla **Empleados**, el atributo **Sueldo** almacenará el valor en euros del sueldo que recibe cada empleado. A veces es necesario añadir una pequeña descripción para aclarar un poco más el contenido. Por ejemplo, si el sueldo es neto o bruto.

- `Tuplas`**:** Se refiere a cada elemento de la relación o tabla. En la tabla alumnos hay 5 tuplas con los atributos  DNI, nombre y apellidos de cada uno de los alumnos..

    Cada una de las filas de la tabla se corresponde con la idea de registro y tiene que cumplir que:

    - Cada tupla se debe corresponder con un elemento del mundo real.

    - No puede haber dos tuplas iguales (con todos los valores iguales).

Está claro que un atributo en una tupla no puede tomar cualquier valor. No sería lógico que en un atributo Población se guarde "250€". Estaríamos cometiendo un error, para evitar este tipo de situaciones obligaremos a que cada atributo sólo pueda tomar los valores pertenecientes a un conjunto de valores previamente establecidos, es decir, un atributo tiene asociado un `dominio `de valores.

A menudo un dominio se define a través de la declaración de un tipo para el atributo (por ejemplo, diciendo que es un número entero entre 1 y 16), pero también se pueden definir dominios más complejos y precisos. Por ejemplo, para el atributo Sexo de los usuarios, podemos definir un dominio en el que los valores posibles sean "M" o "F" (masculino o femenino).

Una característica fundamental de los dominios es que sean **atómicos**, es decir, que los valores contenidos en los atributos no se pueden separar en valores de dominios más simples.

Un dominio debe tener: `Nombre, Definición lógica, Tipo de datos y Formato`**.**

Por ejemplo, si consideramos el Sueldo de un empleado, tendremos:

- **Nombre**: Sueldo.

- **Definición** **lógica**: Sueldo neto del empleado

- **Tipo de datos**: número entero.

- **Formato**: 9.999€.




> ## 2.2. GRADO. CARDINALIDAD

ya hemos visto que una relación es una tabla con filas y columnas. Pero ¿hasta cuántas columnas puede contener? ¿Cuántos atributos podemos guardar en una tabla?

Llamaremos `grado `al tamaño de una tabla en base a su número de atributos (columnas). Mientras mayor sea el grado, mayor será la complejidad para trabajar con ella.

¿Y cuántas tuplas (filas o registros) puede tener?

Llamaremos `cardinalidad `al número de tuplas o filas de una relación o tabla.

Vamos a verlo con un ejemplo. Dadas las relaciones

 A={Carlos, María}, B={Matemáticas, Lengua}, C={Aprobado, Suspenso}.

Las posibles relaciones que obtenemos al realizar el producto cartesiano AxBxC da como resultado una relación de grado 3, ya que tiene 3 columnas.

Producto Cartesiano AxBxC.


Si cogemos un subconjunto de ésta con 5 filas, tendríamos una relación de cardinalidad 5. Por ej.

Subconjunto del Producto Cartesiano AxBxC con cardinalidad 5.





> ## 2.3. SINÓNIMOS

Los términos vistos hasta ahora tienen distintos sinónimos según la nomenclatura utilizada. Trabajaremos con tres:

- **En el modelo relacional**: RELACIÓN - TUPLA - ATRIBUTO - GRADO - CARDINALIDAD.

- **En tablas**: TABLA - FILA - COLUMNAS - NÚMERO COLUMNAS - NÚMERO FILAS.

- **En términos de registros**: FICHEROS - REGISTROS - CAMPOS - NÚMERO CAMPOS - NÚMERO REGISTROS.



---


> # 3. RELACIONES. CARACTERÍSTICAS DE UNA RELACION TABLA

¿En un modelo relacional se puede utilizar cualquier relación? ¿Es válida cualquier tabla o se deben cumplir algunas propiedades?

Debes saber que:

- Cada tabla tiene un **nombre distinto.**


- Como hemos visto antes, cada atributo (columna) de la tabla **toma un solo valor** en cada tupla (fila).

- Cada atributo (columna) tiene un **nombre distinto** en cada tabla (pero puede ser el mismo en tablas distintas).

- **No** puede haber dos tuplas (filas) **completamente iguales**.



- El **orden** de las tuplas (filas) **no importa**.

- El **orden** de los atributos (columnas) **no importa**.

- Todos los datos de un atributo (columna) deben ser del **mismo dominio**.Si hemos definido que el dominio del atributo Nota sólo admite los valores Aprobado o Suspenso entonces el dato NOTABLE sería incorrecto ya que no pertenece al dominio.





> ## 3.1. TIPOS DE REALCIONES TABLAS

Existen varios tipos de relaciones o tablas y las vamos a clasificar en:

- `Persistentes`: Sólo pueden ser borradas por los usuarios. 

    - **Base**: Independientes, se crean indicando su estructura y sus ejemplares (conjunto de tuplas o filas).

    - **Vistas**: son tablas que sólo almacenan una definición de consulta, resultado de la cual se obtiene datos que proceden de otras tablas base o de otras vistas e instantáneas. Si los datos de las tablas base cambian, los de la vista que utilizan esos datos también cambiarán ya que se obtienen a partir de ellas.

    - **Instantáneas**: son vistas (se crean de la misma forma) pero sí almacenan los datos que muestran, además de la consulta que la creó. Solo modifican su resultado cuando el sistema se refresca cada cierto tiempo. Es como una fotografía de la relación, que sólo es válida durante un periodo de tiempo concreto.

- `Temporales`: Son tablas que son eliminadas automáticamente por el sistema.



---


> # 4 TIPOS DE DATOS

¿Qué es un DNI? ¿Con qué datos lo representamos? El DNI es una información que es susceptible de ser guardada. Normalmente el DNI está formado por dígitos y una letra al final. Si tuviéramos que clasificarlo diríamos que es un conjunto de caracteres alfanuméricos. ¿Y si pensamos en Sueldo? Aquí lo tenemos un poco más claro, evidentemente es un número entero o con decimales.

Hasta ahora hemos visto que vamos a guardar información relacionada en forma de filas y columnas. Las columnas son los atributos o información que nos interesa incluir del mundo real que estamos modelando.

Hemos visto que esos atributos se mueven dentro de un dominio, que formalmente es un conjunto de valores. Pues bien, en términos de sistemas de base de datos, se especifica indicando el tipo de dato (de forma general) y el conjunto de valores que puede tomar (de forma restringida). El conjunto de valores restringidos se le indicará en la definición de la tabla si el SGBD lo permite. 

Por ejemplo para un atributo que va a guardar el género (M masculino o F femenino), el tipo de datos será carácter o texto de longitud 1. Los valores posibles M o F se indicarán en la definición de la tabla.

Al crear la relación (tabla) decidimos qué conjunto de datos deberá ser almacenado en los atributos de las filas. Tenemos que asignar un tipo de dato a cada atributo.

Con la asignación de tipos de datos, también habremos seleccionado un dominio para cada atributo. 

Cada campo:

- debe poseer un `Nombre `(relacionado con los datos que va a contener) y

- debe tener asociado un `Tipo de dato` que determinará qué valores puede tomar y qué operaciones se pueden realizar con ellos.

Existen distintas formas de nombrar los tipos de datos dependiendo del lenguaje que utilicemos ([C](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/4_tipos_de_datos.html#t455db250-67a1-7ae7-d74e-2e26b1643fcd), [Java](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/4_tipos_de_datos.html#t0adc4b3d-fa1c-b328-25c0-713ac71a40c2), [PHP](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/4_tipos_de_datos.html#t9c64195a-104a-0819-7a73-bf77684bbc1b), [MySQL](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/4_tipos_de_datos.html#te0040af3-9c97-242d-cfae-0f238e2fa3b2), [SQL](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/4_tipos_de_datos.html#t30da1463-248a-8c78-a3e4-cb7be3309394), [Pascal,](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/4_tipos_de_datos.html#t13306f3e-992d-97ca-ff2a-a9d0096ae4a3) etc.).

Veamos cuales son los tipos de datos más comunes y habituales, existentes en la mayoría de los lenguajes, que posteriormente se definirán utilizando la sintaxis específica del  lenguaje elegido.

- **Texto**: almacena cadenas (conjunto) de caracteres: números con los que **no** vamos a realizar operaciones matemáticas, letras o símbolos.

- **Numérico**: almacena números. Si dudamos entre numérico o texto tendremos en cuenta si vamos a realizar operaciones matemáticas con ellos, en cuyo caso será numérico.

- **Fecha/hora**: almacena fechas y horas.

- **Sí/No**: almacena datos que solo tienen dos posibilidades (verdadero/falso).

- **Autonumérico**: se puede considerar un subtipo de Numérico ya que almacena valores numéricos secuenciales que el SGBD incrementa de modo automático al añadir un registro (fila).

- **Memo**: almacena texto largo (mayor que un tipo texto).

- **Moneda**:  pero con una característica especial, y es que los valores representan cantidades de dinero.

- **Objeto OLE**: almacena gráficos, imágenes o textos creados por otras aplicaciones.

Para determinar qué tipo de dato se asocia a cada atributo se tiene en cuenta el conjunto de valores que puede tomar y las operaciones que hay que realizar con él.

Un código postal, por ejemplo 06800, a pesar de estar formado por dígitos numéricos, es mejor definirlo como una cadena de 5 caracteres por dos motivos: porque no se va a realizar operaciones matemáticas con él y porque los ceros a la izquierda no deben ser obviados como si fuera numérico. El número de teléfono se encuentra en un caso similar.

Es fundamental determinar de forma correcta el tipo de dato y tamaño para cada atributo, ya que si se define mal, no permitirá almacenar la información deseada o puede que almacene información incompleta. Por ejemplo, si se define de un tamaño o longitud inferior al valor que va a contener. Supongamos que nos precipitamos y definimos el DNI como un campo de tipo cadena de 8 caracteres; si se quiere registrar el  DNI 89234432B que tiene 9 caracteres, es posible que el sistema lo almacene mal, dejando atrás el carácter sobrante. De ahí la importancia de este proceso.



---



> # 5. CLAVES

¿Cómo diferenciamos unos usuarios de otros? ¿Cómo sabemos que no estamos recogiendo la misma información? ¿Cómo vamos a distinguir unas tuplas de otras? Lo haremos mediante los valores de sus atributos. Para ello, buscaremos un atributo o un conjunto de atributos que identifiquen de modo único las tuplas (filas) de una relación (tabla). A ese atributo o conjunto de atributos lo llamaremos **superclaves**.

Hemos visto que una característica de las tablas era que no puede haber dos tuplas (filas) completamente iguales, con lo que podemos decir que toda la fila como conjunto sería una `superclave`.

Por ejemplo, en la tabla Usuarios tenemos las siguientes superclaves:

- {Nombre, Apellidos, login, e_mail, F_nacimiento}

- {Nombre, Apellidos, login, e_mail}

- {login, e_mail}

- {login}

Tendríamos que elegir alguna de las superclaves para diferenciar las tuplas. En el modelo relacional trabajamos con tres tipos de claves:

- Claves **candidatas**.

- Claves **primarias**.

- Claves **alternativas.**

- Claves **ajenas**.

A continuación veremos cada una de ellas.



> ## 5.1 CLAVE CANDIDATA. CLAVE PRIMARIA. CLAVE ALTERNATIVA

Si puedo elegir entre tantas claves, ¿con cuál me quedo? Tendremos que elegir entre las claves "candidatas" la que mejor se adapte a mis necesidades. ¿Y cuáles son éstas? Las claves `candidatas `serán aquel conjunto de atributos que identifiquen de manera única cada tupla (fila) de la relación (tabla). Es decir, las columnas cuyos valores no se repiten en ninguna otra fila de la tabla. Por tanto, cada tabla debe tener **al menos una clave candidata** aunque puede haber más de una.

Siguiendo con nuestro ejemplo, podríamos considerar los atributos Login o E_mail como claves candidatas, ya que sabemos que el Login debe ser único para cada usuario, a E_mail le sucede lo mismo. Pero también cabe la posibilidad de tomar: Nombre, Apellidos y F_nacimiento, las tres juntas como clave candidata.

Las claves candidatas pueden estar formadas por más de un atributo, siempre y cuando éstos identifiquen de forma única a la fila. Cuando una clave candidata está formada por más de un atributo, se dice que es una` clave compuesta`.

Una clave `candidata `debe cumplir los siguientes requisitos:

- **Unicidad**: no puede haber dos tuplas (filas) con los mismos valores para esos atributos.

- **Irreductibilidad**: si se elimina alguno de los atributos deja de ser única.

Si elegimos como clave candidata **Nombre, Apellidos y F_nacimiento**, cumple con la unicidad puesto que es muy difícil encontrarnos con dos personas que tengan el mismo nombre, apellidos y fecha de nacimiento iguales. Es irreductible puesto que sería posible encontrar dos personas con el mismo nombre y apellidos o con el mismo nombre y fecha de nacimiento, por lo que son necesarios los tres atributos (campos) para formar la clave.

Para identificar las claves candidatas de una relación no nos fijaremos en un momento concreto en el que vemos una base de datos. Puede ocurrir que en ese momento no haya duplicados para un atributo o conjunto de atributos, pero esto no garantiza que se puedan producir. El único modo de identificar las claves candidatas es conociendo el significado real de los atributos (campos), ya que así podremos saber si es posible que aparezcan duplicados. Es posible desechar claves como candidatas fijándonos en los posibles valores que podemos llegar a tener. Por ejemplo, podríamos pensar que Nombre y Apellidos podrían ser una clave candidata, pero ya sabemos que cabe la posibilidad de que dos personas puedan tener el mismo Nombre y Apellidos, así que lo descartamos.

Hasta ahora, seguimos teniendo varias claves con la que identificamos de modo único nuestra relación. De ahí el nombre de candidatas. Hemos de quedarnos con una.

La` clave primaria` de un relación es aquella clave candidata que se escoge para identificar sus tuplas de modo único. Ya que una relación no tiene tuplas duplicadas, siempre hay una clave candidata y, por lo tanto, la relación siempre tiene clave primaria. En el peor caso, la clave primaria estará formada por todos los atributos de la relación, pero normalmente habrá un pequeño subconjunto de los atributos que haga esta función. En otros casos, podemos crear un campo único que identifique las tuplas, por ejemplo un código de usuario, que podrían estar constituidos por valores autonuméricos.

**Las claves candidatas que no son escogidas como clave primaria** son denominadas` claves alternativas`.

Si en nuestra tabla Usuarios escogemos Login como clave primaria, el E_mail o {Nombre, Apellidos, F_Nacimiento} serán nuestras claves alternativas.



> ## 5.2 CLAVE EXTERNA, AJENA O SECUNDARIA 

Hasta ahora no nos hemos planteado cómo se relacionan unas tablas con otras dentro de una base de datos. Si tenemos las tablas Usuarios y Partidas, necesariamente habrá una "relación" entre ellas. Deben compartir algún dato en común que las relacione. Una partida es jugada por un jugador (Usuarios), por lo que en la tabla Partida deberíamos guardar algún dato del usuario-jugador, pero ¿cuál?

Una clave **ajena, también llamada externa, foránea o secundaria****,** es un atributo o conjunto de atributos de una relación cuyos valores coinciden con los valores de la clave primaria de alguna otra relación (o de la misma). Las claves ajenas **representan relaciones entre datos**. Dicho de otra manera, son los datos de atributos de una tabla cuyos valores están relacionados con atributos de otra tabla.

En la tabla Partidas, se recogen datos como **Cod_partida**, **Fecha** y **Hora de creación**, **Nombre de la partida**, etc. ¿Qué campo utilizaremos para relacionarla con la tabla Usuarios? Si nos basamos en la definición, deberíamos utilizar la clave primaria de la tabla Usuarios. Por tanto, el atributo Login que es la clave principal en su tabla aparecerá en la tabla Partidas como clave ajena, externa o secundaria. El Login en Partidas hace referencia a cada jugador que juega esa partida. En lugar de guardar todos los datos de ese jugador en la misma tabla, lo hacemos en otra y lo "referenciamos" por su clave primaria tomándola como ajena.

Es lógico que las claves ajenas no tengan las mismas propiedades y restricciones que tienen como clave primaria en su tabla, por tanto, sí que pueden repetirse en la tabla. En nuestro ejemplo, un mismo jugador puede jugar varias partidas.

Las claves ajenas tienen por objetivo establecer una conexión con la clave primaria que referencian. Por lo tanto, **los valores de una clave ajena deben estar presentes como clave primaria  en la tabla a la que hacen referencia** **,** **o bien deben ser valores nulo****s**. En caso contrario, la clave ajena representaría una referencia o conexión incorrecta, lo que supondría que la información almacenada es inconsistente (no fiable). Imagina un código de jugador en la tabla Partidas que no se corresponde con ningún jugador de la tabla Usuarios.

No podemos tener una partida de un jugador que previamente no se ha registrado y no existe en la tabla Usuarios. Pero sí podemos tener los datos de una partida y desconocer el jugador de ésta, es decir  la columna jugador puede tener el valor nulo (sin valor).



---



> # 6. INDICES. CARACTERÍSTICAS 

Imagina que estás creando un diccionario de términos informáticos. Podrías elegir la opción de escribirlo en una única hoja muy larga (estilo pergamino) o bien distribuirlo por hojas. Está claro que lo mejor sería distribuirlo por páginas. Y si buscamos el término "informática" en nuestro diccionario, podríamos comenzar a buscar en la primera página y continuar una por una hasta llegar a la palabra correspondiente. O bien crear un índice al principio, de manera que podamos consultar a partir de qué página podemos localizar las palabras que comienzan por "i". Esta última opción parece la más lógica.

Pues bien, en las bases de datos, cada tabla se divide internamente en páginas de datos, y se define el índice a través de un campo (o campos) y es a partir de este campo desde donde se busca.

Un **índice** es una estructura de datos que permite acceder a diferentes filas de una misma tabla a través de un campo o campos . Esto permite un acceso mucho más rápido a los datos.

Los índices son útiles cuando se realizan consultas frecuentes a un rango de filas o una fila de una tabla. Por ejemplo, si consultamos los usuarios cuya fecha de ingreso es anterior a una fecha concreta.

Los cambios en los datos de las tablas (agregar, actualizar o borrar filas) son incorporados automáticamente a los índices con transparencia total.

Debes saber que los índices son independientes, lógica y físicamente de los datos, es por eso que pueden ser creados y eliminados en cualquier momento, sin afectar a las tablas ni a otros índices.

¿Cuándo indexamos? No hay un límite de columnas a indexar, si quisiéramos podríamos crear un índice para cada columna, pero no sería operativo. Normalmente tiene sentido crear índices para ciertas columnas ya que agilizan las operaciones de búsqueda de base de datos grandes. Por ejemplo, si la información de nuestra tabla Usuarios se desea consultar por apellidos a menudo y se necesita agilidad en los accesos,  tiene sentido indexar por esa columna. No conviene indexar por columnas de gran tamaño porque puede resultar contraproducente.

Al crear índices, las operaciones de modificar o agregar datos se ralentizan, ya que al realizarlas es necesario actualizar tanto la tabla como el índice. Por tanto hay que pensar bien cuándo interesa definir o no un índice.

Si se elimina un índice, el acceso a datos puede ser más lento a partir de ese momento.

El SGBD utiliza índices para la gestión de las claves ajenas y de las claves primarias. En el caso de las claves primarias serán índices únicos (no admiten valores repetidos).



---



> # 7. EL VALOR $NULL$. OPERACIONES CON ESTE VALOR

Qué sucede si al guardar los datos de los Usuarios hay algún dato que no tengo o no necesito guardarlo porque no corresponde?

Independientemente del dominio al que pertenezca un campo, éste puede tomar un valor especial denominado **NULO** (**NULL** en inglés) que designará la ausencia de dato.

Cuando por cualquier motivo se desconoce el valor de un campo, por ejemplo, desconocemos el teléfono del usuario, o bien ese campo carece de sentido (siguiendo con el mismo ejemplo, puede que el usuario no tenga teléfono), podemos asignar a ese campo el valor especial NULO.

Cuando trabajamos con claves secundarias el valor nulo indica que la tupla o fila no está relacionada con ninguna otra tupla o fila. Este valor NULO es común a cualquier dominio.

Pero ten en cuenta una cosa, no es lo mismo valor NULO que ESPACIO EN BLANCO.

Tampoco será lo mismo valor NULO que el valor CERO.

Un ordenador tomará un espacio en blanco como un carácter como otro cualquiera. Por tanto, si introducimos el carácter "espacio en blanco" estaríamos introduciendo un valor que pertenecería al dominio **texto** y sería distinto al concepto "ausencia de valor" que sería **no incluir nada** (nulo).

Este valor se va a utilizar con frecuencia en las bases de datos y es imprescindible saber cómo actúa cuando se emplean operaciones lógicas sobre ese valor. En la [lógica booleana](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/7_el_valor_null_operaciones_con_este_valor.html#t9bd32562-032c-c615-881a-1788e9240424) tenemos los valores VERDADERO y FALSO, pero un valor NULO no es ni verdadero ni falso.

Cuando necesitemos comparar dos campos, si ambos son nulos no podremos obtener ni verdadero ni falso. Necesitaremos definir la lógica con este valor. Veamos los operadores lógicos más comunes y sus resultados utilizando el valor nulo:

- VERDADERO Y (AND) NULO daría como resultado NULO.

- FALSO Y (AND) NULO daría como resultado FALSO.

- VERDADERO O (OR) NULO daría como resultado VERDADERO.

- FALSO O NULO daría como resultado NULO.

- NO (NOT) NULO daría como resultado NULO.

En todas las bases de datos relacionales se utiliza un operador llamado  IS NULL (ES NULO) que devuelve VERDADERO si el valor con el que se compara es NULO.



---



> # 8 VISTAS

Cuando vimos los distintos tipos de relaciones, aprendimos que, entre otros, estaban las vistas. Ahora ya tenemos más conocimientos para comprender mejor este concepto.

Una **vista** es una tabla "virtual" cuyas filas y columnas se obtienen a partir de una o de varias tablas que constituyen nuestro modelo. Lo que se almacena no es la tabla en sí, sino su definición, por eso decimos que es "virtual". Una vista actúa como filtro de las tablas a las que hace referencia en ella.

La consulta que define la vista puede provenir de una o de varias tablas, o bien de otras vistas de la base de datos actual u otras bases de datos.

No existe ninguna restricción a la hora de consultar vistas pero sí hay algunas restricciones a la hora de modificar los datos de éstas establecidas para mantener la integridad y consistencia de los datos.

Podemos dar dos razones por las que queramos crear vistas:

- `Seguridad`**,** nos puede interesar que los usuarios tengan acceso a una parte de la información que hay en una tabla, pero no a toda la tabla.

- `Comodidad`, como veremos al pasar nuestras tablas/relaciones a un lenguaje de base de datos, puede que tengamos que escribir sentencias bastante complejas, las vistas no son tan complejas.

Las vistas no tienen una copia física de los datos, son sentencias de consultas a los datos que hay en las tablas, por lo que si actualizamos los datos de una vista, estamos actualizando realmente la tabla, y si actualizamos la tabla estos cambios serán visibles desde la vista.

Aunque **no siempre** podremos actualizar los datos de una vista, dependerá de la complejidad de la misma y del gestor de base de datos. No todos los gestores de bases de datos permiten actualizar vistas, [Oracle](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/8_vistas.html#t328fe911-7e8d-c565-a171-8e88de174ccd), por ejemplo, no lo permite, mientras que [SQL Server](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/8_vistas.html#t5110e88c-f1d9-4531-f228-c10962c35277) sí.



---


> # 9 USUARIOS. ROLES. PRIVILEGIOS

A la hora de conectarnos a la base de datos es necesario que utilicemos un modo de acceso, de manera que queden descritos los permisos de que dispondremos durante nuestra conexión. En función del nombre de usuario tendremos unos permisos u otros.

Un **usuario** es un conjunto de permisos que se aplican a una conexión de base de datos. 

Tiene además otras características: 

- Es el propietario de ciertos objetos (tablas, vistas, etc.).

- Realiza las copias de seguridad.

- Tiene asignada una cuota de almacenamiento.

- TIene asignado un [tablespace](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/9_usuarios_roles_privilegios.html#tf6d8ca94-2bde-7ca0-d711-b41f514cb9c6) por defecto para los objetos en Oracle.

Pero no todos los usuarios deberían poder hacer lo mismo cuando acceden a la base de datos. Por ejemplo, un [administrador](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/9_usuarios_roles_privilegios.html#tb4c27a97-13ba-4e7b-2048-e73093a5fbf9) debería tener más privilegios que un usuario que quiere realizar una simple consulta.

¿Qué es un **privilegio**? No es más que un permiso dado a un usuario para que realice ciertas operaciones, que pueden ser de dos tipos:

- **De sistema**: necesitará el permiso de sistema correspondiente.

- **Sobre objeto**: necesitará el permiso sobre el objeto en cuestión.

¿Y no sería interesante poder agrupar esos permisos para darlos juntos? Para eso tenemos el rol.

Un **rol** de base de datos no es más que una agrupación de permisos de sistema y de objeto.

Podemos tener a un grupo determinado de usuarios que tengan permiso para consultar los datos de una tabla concreta y no tener permiso para actualizarlos. Luego un rol permite asignar un grupo de permisos a un usuario. De este modo, si asignamos un rol con 5 permisos a 200 usuarios y luego queremos añadir un permiso nuevo al rol, no tendremos que ir añadiendo este nuevo permiso a los 200 usuarios, ya que el rol se encarga de propagarlo automáticamente.



---



> # 10. SQL

**SQL** (Structured Query Language ) es un lenguaje de dominio específico utilizado en programación, diseñado para administrar, y recuperar información de sistemas de gestión de bases de datos relacionales.es el lenguaje fundamental de los SGBD relacionales. Es uno de los lenguajes más utilizados en informática en todos los tiempos. Es un [lenguaje declarativo](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#td3944bf0-ba03-f6f5-c3c4-90914e98f896) y por tanto, lo más importante es definir **qué** se desea hacer, y **no cómo** hacerlo. De esto último ya se encarga el SGBD.

Hablamos por tanto de un lenguaje normalizado que nos permite trabajar con cualquier tipo de lenguaje ([ASP](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#te06a5a15-9b58-3822-afc6-af3ed776cadd) o [PHP](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#t841107f4-a46e-11c3-1fec-f97e00ce1339)) en combinación con cualquier tipo de base de datos ([Access,](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#t584e0e29-2c42-89a4-59d5-aca445a16f3e) [SQL Server](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#t26e22d29-0f6c-7c58-d988-3407c7bad7f7), [MySQL](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#ta7e77bee-d331-ff74-72ce-69a375887c4c), [MariaDB,](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#t4e35aff2-54b9-aa51-03e5-fcd79cecd72d) Oracle, etc.).

El hecho de que sea [estándar](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#t2bd93138-0dbc-af64-ca10-f936e340a1c8) no quiere decir que sea idéntico para cada base de datos. Así es, determinadas bases de datos implementan funciones específicas que no tienen necesariamente que funcionar en otras.

Aunque SQL está estandarizado, siempre es recomendable revisar la documentación del SGBD con el que estemos trabajando para conocer su sintaxis concreta, ya que algún comando, tipo de dato, etc., puede no seguir el estándar.

SQL posee dos características muy apreciadas, **potencia** y [versatilidad,](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#te27aefa7-71c2-2bb7-6180-a9684850dd62) que contrastan con su facilidad para el aprendizaje, ya que utiliza un lenguaje bastante natural. Es por esto que las instrucciones son muy parecidas a órdenes humanas. Por esta característica se le considera un [Lenguaje de Cuarta Generación.](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#tb5dc136c-b9bd-98c3-48a1-923cc1204348)

Aunque frecuentemente oigas que SQL es un "lenguaje de consulta", ten en cuenta que no es exactamente solo eso ya que contiene muchas otras capacidades además de la de consultar la base de datos:

- la definición de la propia estructura de los datos (DDL)

- su manipulación (DML)

- y la especificación de conexiones seguras (DCL)

Por tanto, el lenguaje estructurado de consultas SQL es un lenguaje que permite operar con los datos almacenados en las bases de datos relacionales.

Se puede trabajar de dos formas con SQL:

- SQL embebido: las sentencias se escriben dentro de un programa escrito en otro lenguaje como [Java](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#td0e393d7-85aa-0108-79a6-4f78584c7144), PHP,etc..

- SQL interpretado: Podemos usar un entorno gráfico para escribir y ejecutar las sentencias (nosotros utilizaremos SQLDeveloper) o bien desde [SQL*Plus](https://es.wikipedia.org/wiki/SQL*Plus) que es el programa de línea de comandos de Oracle que permite ejecutar  comandos SQL y  [PL/SQL](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/10_sql.html#t76a4ee4c-d2f1-56e6-85aa-554576f2e6ed) de forma interactiva. 

En la unidad 1 utilizaste SQLPlus para conectarte a la base de datos y crear tu usuario. Es importante que tengas soltura en su uso, aunque manejes de forma más habitual el interface gráfico SQLDeveloper,  ya que permite hacer más operaciones.

En el Anexo III de esta unidad y en el siguiente enlace tienes los pasos a seguir para descargarte e instalarte SQLDeveloper y dar los primeros pasos:

[SQLDEVLOPER. Instalación y primeros pasos](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/SQLDeveloper.pdf)




> ## 10.1. ELEMENTOS DEL LENGUAJE. NORMAS DEC ESCRITURA

Imagínate que cada programador utilizara sus propias reglas para escribir. Esto sería un caos. Es muy importante establecer los elementos con los que vamos a trabajar y unas normas que seguir.

El lenguaje SQL está compuesto por comandos, cláusulas, operadores, funciones y literales . Todos estos elementos se combinan en las instrucciones o setencias y se utilizan para crear, actualizar y manipular bases de datos. Estos conceptos son bastante amplios por eso será mejor que vayamos por partes.

- **COMANDOS**: Van a ser las instrucciones que se pueden crear en SQL. Se pueden distinguir en tres grupos que veremos con más detenimiento a lo largo de las siguientes unidades:

    - De definición de datos (DDL, Data Definition Language), que permiten crear y definir nuevas bases de datos, tablas, campos, etc.

    - De manipulación de datos (DML, Data Manipulation Language), que permiten generar consultas para ordenar, filtrar y extraer datos de la base de datos.

    - De control y seguridad de datos (DCL, Data Control Language), que administran los derechos y restricciones de los usuarios.

- **CLÁUSULAS****:** Llamadas también condiciones o criterios, son palabras especiales que permiten modificar el funcionamiento de un comando.

- **OPERADORES**: Permiten crear expresiones complejas. Pueden ser aritméticos (+, -, *, /, ...) o lógicos (< , >, , < >, And, Or, etc.).

- **FUNCIONES****:** Para conseguir valores complejos. Por ejemplo, la función promedio para obtener la media de un salario.

- **LITERALES**: Les podemos llamar también constantes y serán valores concretos, como por ejemplo un número, una fecha, un conjunto de caracteres, etc.

Y tendremos que seguir unas normas sencillas pero primordiales:

- Todas las instrucciones **terminan con un signo de punto y coma**.

- No se distingue entre mayúsculas y minúsculas.

- Cualquier comando puede ser partido con saltos de línea o espacios para facilitar su lectura y comprensión.

- Los comentarios comienzan por /* y terminan con */ (excepto en algunos SGBD).

Juan le ha dicho a Ana que es hora de ponerse a trabajar con la aplicación. Para aprender mejor le ha pedido permiso a Juan para instalar Oracle en su ordenador y así ir probando todo sobre la marcha para no cometer errores. El SQL estándar y el SQL de Oracle son bastante parecidos, pero con algunas diferencias.

**Debes conocer:**

- [Elementos del lenguaje SQL](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/BD02_CONT_R25_01_elementosLenguaje.pdf)

- [Pasos instalación Oracle 18c XE](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/Instalacion_de_Oracle_Database_18c_XE.pdf)

- [Manual SQL](https://dev.mysql.com/doc/)

- [MySQL con clase](http://mysql.conclase.net/curso/index.php)



---



> # 11. LENGUA DE DESCRIPCIÓN DE DATOS (DDL)

La primera fase del trabajo con cualquier base de datos comienza con sentencias DDL, puesto que antes de poder almacenar y recuperar información debemos definir las estructuras donde almacenar la información. Las estructuras básicas con las que trabaja SQL son las tablas.

Conocer el Lenguaje de Definición de Datos (DDL) es imprescindible para crear, modificar y eliminar objetos de la base de datos (es decir, los metadatos). En el mercado hay suficientes aplicaciones y asistentes que nos facilitan esta labor, a través de una interfaz visual que nos oculta el lenguaje SQL y en los cuales nos limitamos a poner nombres a los campos, elegir el tipo de datos y activar una serie de propiedades.

Es cierto que estas herramientas nos facilitan el trabajo, pero resulta imprescindible comprender y conocer en profundidad el lenguaje, ya que nos veremos en muchas situaciones donde necesitaremos crear un objeto, modificarlo o eliminarlo sin depender de esas herramientas visuales.

En Oracle, cada usuario de una base de datos tiene un esquema, que tendrá el mismo nombre que el usuario con el que se ha accedido y sirve para almacenar los objetos que posea ese usuario.

¿De qué objetos estamos hablando? Éstos podrán ser tablas, vistas, índices u otros objetos relacionados con la definición de la base de datos. ¿Y quién puede crear y manipularlos? En principio el usuario propietario (el que los creó) y los administradores de la base de datos. Más adelante veremos que podemos modificar los privilegios de los objetos para permitir el acceso a otros usuarios.

Las instrucciones DDL generan acciones que no se pueden deshacer, por eso es conveniente usarlas con precaución y tener copias de seguridad cuando manipulamos la base de datos.

PARA SEBER MAS

- [Lenguaje de definición de datos](http://es.wikipedia.org/wiki/Lenguaje_de_definici%C3%B3n_de_datos)



> ## 11.1 CREACIÓN DE BASES DE DATOS. OBJETOS DE LA BASE DE DATOS

Básicamente, la creación de la base de datos consiste en crear las tablas que la componen. Aunque antes de ésto tendríamos que definir un espacio de nombres separado para cada conjunto de tablas. Es lo que antes hemos llamado `esquemas `o `usuarios`.

Crear una base de datos implica indicar los archivos y ubicaciones que se van a utilizar además de otras indicaciones técnicas y administrativas. Es obvio que todo esto sólo lo puede realizar si se tiene privilegio de Administrador.

Con el estándar de SQL la instrucción a usar sería `Create Database`, pero cada SGBD tiene un procedimiento para crear las bases de datos. Crearíamos una base de datos con el nombre que se indique a continuación.

```text
CREATE DATABASE NombredemiBasedeDatos;
```

  Save

Por ejemplo, a la base de datos que están creando Juan y Ana se le va a llamar RyMjuegos, entonces nos quedaría:

```text
CREATE DATABASE
```

  Save

Hemos estado hablando de objetos de la base de datos, ahora veremos a qué nos referimos.

Según los estándares, **una base de datos es un conjunto de objetos que nos servirán para gestionar los datos**. Estos objetos están contenidos en esquemas y éstos a su vez suelen estar asociados a un usuario. De ahí que antes dijéramos que cada base de datos tiene un esquema que está asociado a un usuario. 

En oracle la sentencia "create database" tiene un sentido distinto a otros SGBD como Mysql.

Nosotros trabajaremos en oracle creando las tablas en el esquema del usuario creado previamente, es decir, no utilizaremos la sentencia "create database"



> ## 11. 2. CREACIÓN DE TABLAS

Qué necesitamos para poder guardar los datos? Lo primero será definir los objetos donde vamos a agrupar esos datos. Los objetos básicos con los que trabaja SQL son las tablas, que como ya sabemos es un conjunto de filas y columnas cuya intersección se llama celda. Es ahí donde se almacenarán los elementos de información, los datos que queremos recoger.

Antes de crear la tabla es conveniente tener a mano la siguiente información que se obtiene en la fase de diseño lógico de la BD

- **Qué nombre** le vamos a dar **a la tabla**.

- **Qué nombre** le vamos a dar a cada una de las **columnas**.

- **Qué tipo y tamaño de datos** vamos a almacenar en cada columna.

- **Qué restricciones** tenemos sobre los datos.

- Alguna otra **información adicional** que necesitemos.

Y debemos tener en cuenta otras **reglas** que se deben cumplir **para los nombres de las tablas**:

- No podemos tener nombres de tablas duplicados en un mismo esquema (usuario).

- Deben comenzar por un carácter alfabético.

- Su longitud máxima es de 30 caracteres.

- Solo se permiten letras del alfabeto inglés, dígitos o el signo de guión bajo.

- No puede coincidir con las palabras reservadas de SQL (por ejemplo, no podemos llamar a una tabla WHERE).

- No se distingue entre mayúsculas y minúsculas.

- En el caso de que el nombre tenga espacios en blanco o caracteres nacionales (permitido sólo en algunas bases de datos), entonces se suele entrecomillar con comillas dobles. En el estándar [SQL99](https://es.wikipedia.org/wiki/SQL:1999) (respetado por Oracle) se pueden utilizar comillas dobles al poner el nombre de la tabla a fin de hacerla sensible a las mayúsculas (se diferenciará entre "USUARIOS"y "Usuarios").

La sintaxis básica del comando que permite crear una tabla es la siguiente:

```sql
CREATE TABLE [esquema.] nombredeTabla ( columna1 Tipo_Dato,columna2 Tipo_Dato, ...  columnaN Tipo_Dato );
```

  

donde:

- columna1, columna2, ..., columnaN son los nombres de las columna que contendrá la tabla.

- Tipo_Dato indica el tipo de dato de cada columna.

Ana va a crear la primera tabla llamada USUARIOS con un solo campo de tipo VARCHAR:

```sql
CREATE TABLE USUARIOS (Nombre VARCHAR(25));
```

**Recuerda** que solo podrás crear tablas si posees los permisos necesarios para ello.



> ## 11.3. RESTRICCIONES

Hay veces que necesitamos que un dato se incluya en una tabla de manera obligatoria, otras veces necesitaremos definir uno de los campos como llave primaria o ajena. Todo esto podremos hacerlo cuando definamos la tabla, además de otras opciones.

Una **restricción** es una condición que una o varias columnas deben cumplir obligatoriamente.

Cada restricción que creemos llevará un nombre, si no se lo ponemos nosotros lo hará Oracle o el SGBD que estemos utilizando. Es conveniente que le pongamos un nombre que nos ayude a identificarla y que sea único para cada esquema (usuario). Es buena idea incluir de algún modo el nombre de la tabla, los campos involucrados y el tipo de restricción en el nombre de la misma. La sintaxis en SQL estándar es la siguiente: 

```sql
CREATE TABLE NOMBRETABLA (
     Columna1 Tipo_Dato
          [CONSTRAINT nombredelarestricción]
          [NOT NULL]
          [UNIQUE]
          [PRIMARY KEY]
          [FOREIGN KEY]
          [DEFAULT valor]
          [REFERENCES nombreTabla [(columna [, columna ])]
          [ON DELETE CASCADE]]
          [CHECK condición],
     Columna2 Tipo_Dato
          [CONSTRAINT nombredelarestricción]
          [NOT NULL]
          [UNIQUE]
          [PRIMARY KEY]
          [FOREIGN KEY]
          [DEFAULT valor]
          [REFERENCES nombreTabla [(columna [, columna ])]
          [ON DELETE CASCADE]]
          [CHECK condición],...);
```

  

Los corchetes, caracteres [ y ],  se utilizan en informática en  los formatos de la sintaxis de los lenguajes para especificar opcionalidad, es decir, está indicando que lo contiene se puede utilizar o no. 

Veamos un ejemplo: 

```sql
CREATE TABLE USUARIOS (
    Login VARCHAR(15) CONSTRAINT usu_log_PK PRIMARY KEY,
    Password VARCHAR (8) NOT NULL,
    Fecha_Ingreso DATE DEFAULT SYSDATE);
```

  

Otra opción es definir las columnas de la tabla y después especificar las restricciones, de este modo podrás referir varias columnas en una única restricción.

En los siguientes apartados veremos cada una de las restricciones, su significado y su uso.

# Recomendación

Oracle nos aconseja la siguiente regla a la hora de poner nombre a las restricciones:



- Tres letras para el nombre de la tabla.

- Carácter de subrayado.

- Tres letras con la columna afectada por la restricción.

- Carácter de subrayado.

- Dos letras con la abreviatura del tipo de restricción. La abreviatura puede ser:

    - `PK` = Primary Key.

    - `FK` = Foreign Key.

    - `NN` = Not Null.

    - `UK` = Unique.

    - `CK` = Check (validación).




> ### 11.3.1 RESTRICCIÓN `NOT NULL` 

Con esta restricción obligaremos a que esa columna tenga un valor o lo que es lo mismo, prohíbe los valores nulos para una columna en una determinada tabla.

Podremos ponerlo cuando creamos o modificamos el campo añadiendo la palabra `NOT NULL` después de poner el tipo de dato.

Si en la tabla USUARIOS queremos que el campo "F_Nacimiento" sea obligatorio ponerlo, nos quedaría así:

```sql
CREATE TABLE USUARIOS (
    F_Nacimiento DATE
    CONSTRAINT Usu_Fnac_NN NOT NULL);
```

  Save

o bien, de esta otra forma:

```sql
CREATE TABLE USUARIOS (
    F_Nacimiento DATE NOT NULL);
```

  Save

Debemos tener cuidado con los valores nulos en las operaciones, ya que 1*NULL es igual a NULL.




> ### 11.3.2 RESTRICCIÓN `UNIQUE `

Habrá ocasiones en la que nos interese que no se puedan repetir valores en la columna, en estos casos utilizaremos la restricción `UNIQUE`. Oracle crea un índice automáticamente cuando se habilita esta restricción y lo borra al deshabilitarla.

También para esta restricción tenemos dos posibles formas de ponerla, veámoslo con un ejemplo. Supongamos que el campo Login de nuestra tabla va a ser único. Lo incluiremos en la tabla que estamos creando. Nos quedaría así:

```sql
CREATE TABLE USUARIOS (
    Login VARCHAR2 (25)
    CONSTRAINT Usu_Log_UK UNIQUE);
```

 

 Veamos otra forma:

```sql
CREATE TABLE USUARIOS (
    Login VARCHAR2 (25) UNIQUE);
```

  

 También podemos poner esta restricción a varios campos a la vez, por ejemplo, si queremos que Login y correo electrónico sean únicos podemos ponerlo así:

```sql
CREATE TABLE USUARIOS (
    Login VARCHAR2 (25),
    Correo VARCHAR2 (25),
    CONSTRAINT Usuario_UK UNIQUE (Login, Correo));
```

  

Si te fijas, detrás del tipo de datos de Correo hay una coma, eso es así porque la restricción es independiente de ese campo y común a varios. Por eso después de `UNIQUE` hemos puesto entre paréntesis los nombres de los campos a los que afecta la restricción.



> ### 11.3.3 RESTRICCIÓN `PRIMARY KEY `

En el modelo relacional las tablas deben tener una clave primaria. Es evidente que cuando creamos la tabla tendremos que indicar a quién corresponde.

Sólo puede haber una clave primaria por tabla pero ésta puede estar formada por varios campos. Dicha clave podrá ser referenciada como clave ajena en otras tablas.

La clave primaria hace que los campos que forman sean `NOT NULL` y que los valores de los campos sean de tipo `UNIQUE`.

Veamos como quedaría si la clave fuese el campo Login:

- Si la clave la forma un único campo:

```sql
CREATE TABLE USUARIOS (
	Login VARCHAR2 (25) PRIMARY KEY);
```

- O bien poniendo un nombre a la restricción:

```sql
CREATE TABLE USUARIOS (
     Login VARCHAR2 (25)
          CONSTRAINT Usu_log_PK PRIMARY KEY);
```

- Si la clave está formada por más de un campo, por ejemplo Nombre, Apellidos y Fecha de Nacimiento, entonces hay que utilizar este formato, después de la definición de todos los campos y antes del paréntesis de cierre de la sentencia:

```sql
CREATE TABLE USUARIOS (
	Nombre VARCHAR2 (25),
	Apellidos VARCHAR2 (30),
	F_Nacimiento DATE,
	CONSTRAINT Usu_PK PRIMARY KEY(Nombre, Apellidos, F_Nacimiento));
```




> ### 11.3.4 RESTRICCIÓN `REFERENCES. FOREIGN KEY`

Ya vimos que las claves ajenas, secundarias o foráneas eran campos de una tabla que se relacionaban con la clave primaria (o incluso con la clave candidata) de otra tabla.

Cuando creemos la tabla tendremos que indicar de alguna forma quién es clave ajena. Lo haremos "haciendo referencia" a la tabla y los campos de donde procede.

En nuestra tabla vamos a tener una clave ajena procedente de la tabla PARTIDAS que será su Cod_Partida, por tanto tendremos que hacer referencia a éste:

```sql
 CREATE TABLE USUARIOS (
    Cod_Partida NUMBER(8)
        CONSTRAINT Cod_Part_FK
        REFERENCES PARTIDAS(Cod_Partida));
```

Si el campo al que hace referencia es clave principal en su tabla no es necesario indicar el nombre del campo:

```sql
CREATE TABLE USUARIOS (
    Cod_Partida NUMBER(8)
        CONSTRAINT Cod_Part_FK
        REFERENCES PARTIDAS);
```

Si la definición de la clave ajena se pone al final, tendremos que colocar el texto `FOREIGN KEY` para especificar a qué campo se está refiriendo.

Vamos a verlo en el caso en que la clave ajena estuviera formada por Cod_Partida y Fecha de la partida de la tabla PARTIDAS:

```sql
CREATE TABLE USUARIOS (
    Cod_Partida NUMBER(8),
    F_Partida DATE,
    CONSTRAINT Partida_Cod_F_FK FOREIGN KEY (Cod_Partida, F_Partida)
    REFERENCES PARTIDAS);
```

Al relacionar campos necesitamos que el dato del campo que es clave ajena en una tabla (que llamaremos secundaria) previamente haya sido incluido en su tabla de procedencia donde es clave primaria o candidata. En nuestro ejemplo, cualquier código de partida que incluyamos en la tabla USUARIO, debería estar previamente en la tabla de la que procede, es decir, en la tabla PARTIDAS. **A esto se le llama Integridad Referencial.**

Esto puede crear algunos errores, pues puede ocurrir lo siguiente:

- Si hacemos referencia a una tabla que no está creada: Oracle buscará la tabla referenciada y al no encontrarla dará fallo. Esto se soluciona creando en primer lugar las tablas que no tengan claves ajenas.

- Si queremos borrar las tablas tendremos que proceder al contrario, borraremos las tablas que tengan claves ajenas antes.

Tenemos otras soluciones y es añadir tras la cláusula `REFERENCE`:

- `ON DELETE CASCADE`: te permitirá borrar todos los registros cuya clave ajena sea igual a la clave del registro borrado.

- `ON DELETE SET NULL`: colocará el valor `NULL` en todas las claves ajenas relacionadas con la borrada.

- `ON DELETE DEFAULT xxxx`: colocará el valor  `xxxx`  en todas las claves ajenas relacionadas con la borrada.

esas opciones son válidas también para la operación de modificación especificando `ON UPDATE` en lugar de `ON DELETE.`




> ### 11.3.5 RESTRICCIÓN `DEFAULT Y VALIDATION KEY`

A veces es muy tedioso insertar siempre lo mismo en un campo. Imagínate que casi todos los jugadores fuesen de España y tenemos un campo País. ¿No sería cómodo asignarle un valor por defecto? Eso es lo que hace la restricción `DEFAULT`.

En nuestro ejemplo vamos a añadir a la tabla USUARIOS el campo País y le daremos por defecto el valor "España".

```sql
CREATE TABLE USUARIOS (
    Pais VARCHAR2(20) DEFAULT ' España ' );
```

  Save

  Save

En las especificaciones de `DEFAULT` vamos a poder añadir distintas expresiones: constantes, funciones SQL y variables.

Si queremos incluir en un campo la fecha actual, independientemente del día en el que estemos, podremos utilizar la función `SYSDATE` como valor por defecto:

```sql
CREATE TABLE USUARIOS (
      Fecha_ingreso DATE DEFAULT SYSDATE);
```

También vamos a necesitar que se compruebe que los valores que se introducen son adecuados para ese campo. Para ello utilizaremos `CHECK`.

Esta restricción comprueba que se cumpla una condición determinada al rellenar una columna. Dicha condición se puede construir con columnas de esa misma tabla.

Si en la tabla USUARIOS tenemos el campo Crédito y éste sólo puede estar entre 0 y 2000, lo especificaríamos así:

```sql
CREATE TABLE USUARIOS (
    Credito NUMBER(4) CHECK (Crédito BETWEEN 0 AND 2000));
```

Una misma columna puede tener varios `CHECK` asociados a ella, para ello ponemos varios `CONSTRAINT` seguidos y separados por comas.



# Debes conocer

Si queremos obtener una descripción de una tabla, sinonimo, paquete o función, podemos utilizar el comando de SQLPlus  `DESCRIBE.`

[http://ora.u440.com/sqlplus/describe.html](http://ora.u440.com/sqlplus/describe.html)

En el siguiente enlace tienes información sobre los comandos básicos de SQLPlus

[Entorno SQLPlus Oracle](https://www.mundoracle.com/entorno-sql-plus.html?Pg=sql_plsql_10.htm)




---



> ## 11.4. ELIMINACION DE TABLAS

Cuando una tabla ya no es útil y no la necesitamos es mejor borrarla, de este modo no ocupará espacio y podremos utilizar su nombre en otra ocasión.

Para eliminar una tabla utilizaremos el comando `DROP TABLE`.

```sql
DROP TABLE NombreTabla [CASCADE CONSTRAINTS];
```

Esta instrucción borrará la tabla de la base de datos incluido sus datos (filas). También se borrará toda la información que existiera de esa tabla en el Diccionario de Datos.

La opción `CASCADE CONSTRAINTS` se puede incluir para los casos en que alguna de las columnas sea clave ajena en otra tabla secundaria, lo que impediría su borrado. Al colocar esta opción las restricciones donde es clave ajena se borrarán antes y a continuación se eliminará la tabla en cuestión.

Vamos a eliminar la tabla con la que hemos estado trabajando:

```sql
DROP TABLE USUARIOS ;
```

Ten cuidado al utilizar este comando, el borrado de una tabla es irreversible y no hay una petición de confirmación antes de ejecutarse.

Al borrar una tabla:

- Desaparecen todos sus datos

- Cualquier vista asociada a esa tabla seguirá existiendo pero ya no funcionará.

Oracle dispone de la orden `TRUNCATE TABLE` que te permitirá eliminar los datos (filas) de una tabla sin eliminar su estructura.

Y recuerda que solo podrás borrar aquellas tablas sobre las que tengas permiso de borrado.




> ## 11.5. MODIFICACIÓN DE TABLAS (I)

Es posible que después de crear una tabla nos demos cuenta que se nos ha olvidado añadir algún campo o restricción, quizás alguna de las restricciones que añadimos ya no es necesaria o tal vez queramos cambiar el nombre de alguno de los campos. ¿Es posible esto? Ahora veremos que sí y en casi todos los casos utilizaremos el comando ALTER TABLE.

- **Si queremos cambiar el nombre de una tabla:**

```sql
RENAME NombreViejo TO NombreNuevo;
```

- **Si queremos añadir columnas a una tabla: l**as columnas se añadirán al final de la tabla.

```sql
ALTER TABLE NombreTabla ADD
( ColumnaNueva1 Tipo_Datos [Propiedades]
[, ColumnaNueva2 Tipo_Datos [Propiedades]
... );
```

- **Si queremos eliminar columnas de una tabla:** se eliminará la columna indicada sin poder deshacer esta acción. Además de la definición de la columna, se eliminarán todos los datos que contuviera. No se puede eliminar una columna si es la única que forma la tabla, para ello tendremos que borrar la tabla directamente.

```sql
ALTER TABLE NombreTabla DROP COLUMN (Columna1 [, Columna2, ...]);
```

- **Si queremos modificar columnas de una tabla:** podemos modificar el tipo de datos y las propiedades de una columna. Todos los cambios son posibles si la tabla no contiene datos. En general, si la tabla no está vacía podremos aumentar la longitud de una columna, aumentar o disminuir en número de posiciones decimales en un tipo NUMBER, reducir la anchura siempre que los datos no ocupen todo el espacio reservado para ellos.

```sql
ALTER TABLE NombreTabla MODIFY
(Columna1 TipoDatos [propiedades] [, columna2 TipoDatos [propiedades] ...] );
```

- **Si queremos renombrar columnas de una tabla:**

```sql
ALTER TABLE NombreTabla RENAME COLUMN NombreAntiguo TO NombreNuevo;
```

Tenemos la siguiente tabla creada:

```sql
 CREATE TABLE USUARIOS (
    Credito NUMBER(4) CHECK (Crédito BETWEEN 0 AND 2000));
```

Nos gustaría incluir una nueva columna llamada User que será tipo texto y clave primaria:

```sql
ALTER TABLE USUARIO ADD
    (User VARCHAR(10) PRIMARY KEY);
```

Nos damos cuenta que ese campo se llamaba Login y no User, vamos a cambiarlo:

```sql
ALTER TABLE USUARIO RENAME COLUMN User TO Login;
```

```sql
// Ejemplo modificación fila
// TEnemos estatabla

CREATE TABLE EMPLEADOS (
    Cod_Cliente VARCHAR(5) PRIMARY KEY,
    Nombre VARCHAR(10),
    Apellidos VARCHAR(25),
    Sueldo NUMBER(4));

// Ahora queremos poner una restricción a sueldo para que tome valores entre 1000 y 1200, ¿cómo lo harías?
ALTER TABLE EMPLEADOS MODIFY (Sueldo NUMBER(4) CHECK (Sueldo BETWEEN 1000 AND 1200));
```



> ### 15.5.1. MDIFICACION DE TABLAS (II)

Utilizando el comando `ALTER TABLE`, podemos modificar las restricciones o bien eliminarlas:

- **Si queremos borrar restricciones:**

    ```sql
    ALTER TABLA NombreTabla DROP CONSTRAINT NombreRestriccion;
    ```

- **Si queremos modificar el nombre de las restricciones:**

    ```sql
    ALTER TABLE NombreTabla RENAME CONSTRAINT NombreViejo TO NombreNuevo;
    ```

- **Si queremos activar o desactivar restricciones:**

    A veces es conveniente desactivar temporalmente una restricción para hacer pruebas o porque necesitemos saltarnos esa regla. Para ello usaremos esta sintaxis:

    ```sql
    ALTER TABLE NombreTabla DISABLE CONSTRAINT NombreRestriccion [CASCADE];
    ```

    La opción `CASCADE` desactiva las restricciones que dependan de ésta.

    Para activar de nuevo la restricción:

    ```sql
    ALTER TABLE NombreTabla ENABLE CONSTRAINT NombreRestriccion [CASCADE];
    ```


## Recomendación

Al final de los contenidos encontrarás el "[Anexo IV. Ejercicios DDL con solución](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/anexo_iv_ejercicios_ddl_con_solucin.html)" donde tienes enunciados de creación y modificación de tablas y restricciones con una posible solución. Lee los enunciados, entiéndelos y escribe las sentencias SQL correspondientes (si lo haces en SQLDeveloper, mejor, porque eliminarás los errores de sintaxis y comprobarás si están correctas). 




> ## 11.6. CREACION Y ELIMINACION DE INDICES

Sabemos que crear índices ayuda a la localización más rápida de la información contenida en las tablas. Ahora aprenderemos a crearlos y eliminarlos:

```sql
CREATE INDEX NombreIndice ON NombreTabla (Columna1 [, Columna2 ...]);
```

No es aconsejable que utilices índices sobre campos de tablas pequeñas o que se actualicen con mucha frecuencia. Tampoco es conveniente si esos campos no se usan en consultas de manera frecuente o en expresiones.

El diseño de indices es un tema bastante complejo para los Administradores de Bases de Datos, ya que una mala elección ocasiona ineficiencia y tiempos de espera elevados. Un uso excesivo de ellos puede dejar a la Base de Datos colgada simplemente con insertar alguna fila.

Para eliminar un índice es suficiente con poner la instrucción:

```sql
DROP INDEX NombreIndice;
```

La mayoría de los índices se crean de manera implícita cuando ponemos las restricciones `PRIMARY KEY, FOREIGN KEY o UNIQUE`.



---



> # 12. LENGUAJE DE CONTROL DE DATOS (DCL)

Ya hemos visto que necesitamos una cuenta de usuario para acceder a los datos de una base de datos. Las claves de acceso se establecen cuando se crea el usuario y pueden ser modificados por el Administrador o por el propietario de dicha clave. La Base de Datos almacena [encriptadas](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/12_lenguaje_de_control_de_datos_dcl.html#tb4322b9f-0668-d737-31ec-9de16e7369a7) las claves en una tabla del diccionario llamada DBA_USERS.

¿Cómo se crean los usuarios? La sintaxis es:

```sql
CREATE USER NombreUsuario
IDENTIFIED BY ClaveAcceso
[DEFAULT TABLESPACE tablespace ]
[TEMPORARY TABLESPACE tablespace]
[QUOTA int {K | M} ON tablespace]
[QUOTA UNLIMITED ON tablespace]
[PROFILE perfil];
```

donde:

- `CREATE USER`: crea un nombre de usuario que será identificado por el sistema.

- `IDENTIFIED BY`: permite dar una clave de acceso al usuario creado.

- `DEFAULT TABLESPACE`: asigna a un usuario el Tablespace por defecto para almacenar los objetos que cree. Si no se asigna ninguna, será `SYSTEM`.

- `TEMPORARY TABLESPACE`: especifica el nombre del Tablespace para trabajos temporales. Por defecto será `SYSTEM`.

- `QUOTA`: asigna un espacio en Megabytes o Kilobytes en el Tablespace asignado. Si no se especifica el usuario no tendrá espacio y no podrá crear objetos.

- `PROFILE`: asigna un perfil al usuario. Si no se especifica se asigna el perfil por defecto.

Recuerda que para crear usuarios debes tener una cuenta con privilegios de Administrador.

Para ver todos los usuarios creados utilizamos las vistas ALL_USERS y DBA_USERS. Y para ver en mi sesión los usuarios que existen pondría: `DESC SYS.ALL_USERS;`

Practiquemos un poco con este comando. Creemos una cuenta de usuario limitado, que no tenga derecho ni a guardar datos ni a crear objetos, más tarde le daremos permisos:

```sql
CREATE USER UsuarioLimitado IDENTIFIED BY passworddemiusuariolimitado ;
```

Podemos modificar usuarios mediante el comando ALTER USER, cuya sintaxis es la siguiente:

```sql
ALTER USER NombreUsuario
IDENTIFIED BY clave_acceso
[DEFAULT TABLESPACE tablespace ]
[TEMPORARY TABLESPACE tablespace]
[QUOTA int {K | M} ON tablespace]
[QUOTA UNLIMITED ON tablespace]
[PROFILE perfil];
```

Un usuario sin privilegios de Administrador únicamente podrá cambiar su clave de acceso.

Para eliminar o borrar un usuario utilizamos el comando `DROP USER` con la siguiente sintaxis:

```sql
DROP USER NombreUsuario [CASCADE];
```

La opción `CASCADE` borra todos los objetos del usuario antes de borrarlo. Sin esta opción no nos dejaría eliminar al usuario si éste tuviera tablas creadas.



> ## 12.1. PERMISOS (I)

Ningún usuario puede llevar a cabo una operación si antes no se le ha concedido el permiso para ello. En el apartado anterior hemos creado un usuario para iniciar sesión, pero si con él intentáramos crear una tabla veríamos que no tenemos permisos suficientes para ello.

Para poder acceder a los objetos de una base de datos necesitas tener privilegios (permisos). Éstos se pueden agrupar formando **roles**, lo que simplificará la administración. Los roles pueden activarse, desactivarse o protegerse con una clave. Mediante los roles podemos gestionar los comandos que pueden utilizar los usuarios. Un permiso se puede asignar a un usuario o a un rol.

Un privilegio o permiso se concede con el comando `GRANT` (conceder).

Si se dan privilegios **sobre los objetos**:

```sql
GRANT {privilegio_objeto [, privilegio_objeto]...|ALL|[PRIVILEGES]}
ON [usuario.]objeto
FROM {usuario1|rol1|PUBLIC} [,{usuario2|rol2|PUBLIC] ...
[WITH GRANT OPTION];
```

donde:

- `ON` especifica el objeto sobre el que se conceden los privilegios.

- `TO` señala a los usuarios o roles a los que se conceden privilegios.

- `ALL` concede todos los privilegios sobre el objeto especificado.

- `[WITH GRANT OPTION]` permite que el receptor del privilegio se lo pueda conceder a otros.

- `PUBLIC` hace que un privilegio esté disponible para todos los usuarios.

En el siguiente ejemplo Juan ha accedido a la base de datos y ejecuta los siguientes comandos:

- `GRANT INSERT TO Usuarios TO Ana;` (permitirá a Ana insertar datos en la tabla Usuarios)

- `GRANT ALL ON Partidas TO Ana;` (Juan concede todos los privilegios sobre la tabla Partidas a Ana)

Los privilegios **de sistema** son los que dan derecho a ejecutar comandos SQL o acciones sobre objetos de un tipo especificado. Existen gran cantidad de privilegios distintos.

La sintaxis para dar este tipo de privilegios la tienes aquí:

```sql
GRANT {Privilegio1 | rol1 } [, privilegio2 | rol2}, ...]
TO {usuario1 | rol1| PUBLIC} [, usuario2 | rol2 | PUBLIC} ... ]
[WITH ADMIN OPTION];
```

Donde

- `TO` señala a los usuarios o roles a los que se conceden privilegios.

- `WITH ADMIN OPTION` es una opción que permite al receptor de esos privilegios que pueda conceder esos mismos privilegios a otros usuarios o roles.

- `PUBLIC` hace que un privilegio esté disponible para todos los usuarios.

Veamos algunos ejemplos:

```sql
GRANT CONNECT TO Ana;
```

Concede a Ana el rol de `CONNECT` con todos los privilegios que éste tiene asociados.

```sql
GRANT DROP USER TO Ana WITH ADMIN OPTION;
```

Concede a Ana el privilegio de borrar usuarios y que ésta puede conceder el mismo privilegio de borrar usuarios a otros.

# Para saber más

Si quieres conocer más sobre permisos y objetos sobre los que se conceden privilegios, visita este enlace:

[Gestión de privilegios y recursos.](https://ora.u440.com/usuarios/grant.html)




> ## 12.2. PERMISOS (II)

Hasta ahora hemos aprendido a conceder permisos o privilegios. Será importante aprender a retirarlos:

Con el comando `REVOKE` se retiran los privilegios:

- Sobre **objetos**:

```sql
REVOKE {privilegio_objeto [, privilegio_objeto]...|ALL|[PRIVILEGES]}
ON [usuario.]objeto
FROM {usuario|rol|PUBLIC} [,{usuario|rol|PUBLIC] ...;
```

- **Del sistema o roles a usuarios**:

```sql
REVOKE {privilegio_stma | rol} [, {privilegio_stma | rol}]...|ALL|[PRIVILEGES]}
ON [usuario.]objeto
FROM {usuario|rol|PUBLIC} [,{usuario|rol|PUBLIC] ...;
```

Juan va a quitar el permiso de seleccionar y de actualizar sobre la tabla Usuarios a Ana:

```sql
REVOKE SELECT, UPDATE ON Usuarios FROM Ana;
```

y va a quitarle el permiso de eliminar usuarios:

```sql
REVOKE DROP USER FROM Ana;
```



---


# [ANEXO I. ELEMETOS DEL LENGUAJE SQL](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/anexo_i_elementos_del_lenguaje_sql.html)



# [ANEXO II. INSTALACION DE ORACLE 18C XE](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/anexo_ii_instalacin_de_oracle_18c_xe.html)



# [ANEXO III. INSTALACION DE SQLDEVELOPER Y PRIMERO PASOS](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/anexo_iii_instalacin_de_sqldeveloper_y_primeros_pasos.html)



# [ANEXO IV. EJERCICIOS DDL CON SOLUCION](https://www.mecd.es/cidead/aulavirtual/pluginfile.php/392694/mod_resource/content/4/DAM_BD02_Contenidos_Web/anexo_iv_ejercicios_ddl_con_solucin.html)



