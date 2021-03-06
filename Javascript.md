# JavaScript
Se define como orientado a objetos, basado en prototipos, imperativo, debilmente tipado y dinámico.

[Volver al inicio](./README.md)

## Contenidos
- [Introduccion a Javascript](#introduccion-a-javascript)
    - [Variables y sus Ambitos](#variables-y-sus-ambitos)
        - VAR
        - LET
        - CONST
    - [Tipos de datos](#tipos-de-datos)
        - [Strings](#strings)
        - [Valores Booleanos](#valores-booleanos)
            - Coerciones resultantes en FALSE
            - Coerciones resultantes en TRUE
        - [null](#null)
        - [Undefined](#undefined)
    - [typeof](#typeof)
    - [Funcion](#funcion)
        - [Parametros](#parametros)
        - [Return](#return)
        - [Recursividad](#recursividad)
            - [Funcion alert](#funcion-alert)
            - [Funcion prompt](#funcion-prompt)
            - [Impresion en consola](#impresion-en-consola)
        - [Algunas funciones](#algunas-funciones)
    - [Metodos](#metodos)
        - [De strings](#de-strings)
            - .replace
            - .indexOf 
            - .lastIndexOf
            - .lenght
        - [De Arrays](#de-arrays)
            - .filter
            - .forEach
            - .map
            - .reduce
            - .push
                .unshift `similar`
                .pop `analogo`
                .shift `analogo`
            - .reverse
            - .slice
            - .splice
            - [Operador de propagacion](#operador-de-propagacion)
    - [Arreglos - ARRAY](#arreglo-array)
        - [Reemplazar y agregar elementos](#reemplazar-y-agregar-elementos)
    - [Indexacion de Arreglos y Strings](#indexacion-de-arreglos-y-strings)
    - [CONDICIONALES](#condicionales)
        - [If statement](#if-statement)
        - [If else](#if-else)
    - [Pruebas condicionales](#pruebas-y-operaciones)
        - [Igualdad regular](#igualdad-regular)
            - Desigualdad regular
        - [Igualdad estricta](#igualdad-estricta)
            - Desigualdad estricta
        - [Comparacion de null y undefined](#comparacion-de-null-y-undefined)
            - Igualados estrictamente
            - Igualados no estrictamente
            - Comparaciones matematicas
            - Casos particulares
        - [Comparacion de cadenas](#comparacion-de-cadenas)
        - [Compuertas logicas](#compuertas-logicas)
    - [Operadores matematicos](#operadores-matematicos)
            - Concatenar
            - Operador Modulo %
            - Operador Exponenciacion **
            - Conversion numerica UNARIO
        - [Operadores de asignacion](#operadores-de-asignacion)
        pendiente
    - [ciclos](Ciclos)
        - [For loop](#for-loop)
        - [Classic for loop](#classic-for-loop)    
        - [Ciclos anidados](#ciclos-anidados)
        - [Otros ciclos](#otros-ciclos)
            - While
            - Do while
            - [.forEach](#de-strings)
        - [SWITCH](#switch)

- [DOM](#dom)
    - [Nodos del DOM](#nodos-del-dom)
    - [NodeList o HTMLCollection](#nodelist-o-htmlcollection)
        - NodeList Estatica o Dinamica
    - [Metodos de NodeList](#metodos-de-nodelist)
        - Indexacion de NodeList
            - `.item()`
        - `.entries()` itera los `pares` clave / valor
        - `.keys()` itera las `claves` de los pares
        - `.values()` itera los `valores` de los pares
            - .forEach
    - [Seleccionar elementos del DOM](#seleccionar-elementos-del-dom)
        - .getElementById('`id`') 
        - .querySelector('`CSS Selector`')
        - Recibir `NodeList o HTMLCollection`
            - .querySelectorAll('`CSS Selector`') 
            - .getElementsByClassName(`class CSS`)
            - .getElementsByTagName(`Tags HTML`)
    - [Agregar elementos al DOM](#agregar-elementos-al-dom)
        - .createElement('')
        - .appendChild()
        - .textContent
            - [Ejemplos crear elementos](#ejemplos-crear-elementos)
    - Otras formas de agregar elementos al DOM:
        - [Ubicar elementos en el DOM](#ubicar-elementos-en-el-dom)
            - .insertAdjacentHTML(`pos`, `content`)
        - [Crear nodos de elementos y de texto](#crear-nodos-de-elementos-y-de-texto)
            - .innerHTML
        - [Clonar nodos](#clonar-nodos)
        - [Eliminar nodos](#eliminar-nodos)
    - [Asignar atributos HTML a un elemento](#asignar-atributos-html-a-un-elemento  )
        - .style  `CSS inline`
        - .className   `CSS class`
        - .classlist
        - .id
        - [Recuperar el valor del tributo class](#recuperar-el-valor-del-tributo-class-pendiente)
            - articulo.attributes.class
    - [Eventos en una Webpage](#eventos-en-una-webpage)
        - .addEventListener()
            - [Ejemplos de eventos]()
    - [Importar js](#importar-js)
        - [Bibliotecas js](#biblioteca-js)

- [Estructurar datos](#estructurar-datos)
    - [Object](#object)
        - [Par clave / valor](#par-clave--valor)
        - Borrar un par clave / valor
            - delete object.key
        - [this en objects](#this-en-objects)
        - [Prueba key existente](#prueba-key-existente)
    - [metodos de objects](#metodos-de-objects)
    - [Bucle for in](#bucle-for-in)
    - [JSON](#json)
        - [Sintaxis JSON](#sintaxis-json)
    - [Metodos JSON, toJSON](#metodos-json-tojson)
        - .parse
        - JSON.stringify()
        - JSON.parse()
    - [Convertir un objeto en JSON](#convertir-un-objeto-en-json)

- [API Fetch](#api-fetch)
    - [Arquitectura SOAP](#arquitectura-soap)
    - [Arquitectura REST](#arquitectura-rest)
        - [REST - Interfaz](#rest---interfaz)
            - GET
            - POST 
            - PUT
            - DELETE
        - [REST - Ventajas](#rest---ventajas)
    - [Sintaxis Fetch](#sintaxis-fetch)
        - URL
        - fetch
        - .then
        - .catch
    - [Response](#response)
        - Propiedades
        - [Metodos Response](#metodos-response)
            - .clone
            - .text
            - .json
            - .blob
    - [Async/await](#asyncawait)
    - [API Fetch - Casos](#api-fetch---casos)
        - [Comprobando estado del Fetch](#comprobando-estado-del-fetch)
        - [Enviar peticion con credencial](#enviar-peticion-con-credencial)
        - [XMLHttpRequest - Ejemplo](#xmlhttprequest---ejemplo)
    - [Otras APIs](#otras-apis)

- [Promesas y Callbacks](#promesas-y-callbacks)
    - [Callback](#callbacks)
        - [Ejemplo de Callbacks](#ejemplo-de-callbacks)

- [Buenas practicas](#buenas-practicas)

- [Pendiente](#pendiente)

`Para comprimir la vista temporalmente le di mas jerarquia a variables y sus ambitos`    

## Introduccion a Javascript
Se debe tener en cuenta que si escribimos algo que se ejecute inmediatamente sin requerir un llamado a una `funcion` sera necesario que el elemento `script` aparezca al final del `body` para que se leen todos los `id` y recien ahi se `ejecute`.

### Variables y sus Ambitos
Debe tener un nombre para ser referenciada `identificador`. Almacena un valor que corresponde a un `número`, un `string` o datos más complejos (como un `arreglo` o un `objeto`).
El `ámbito` de una variable es el bloque de codigo dónde se puede ejecutar.

    Se pueden declarar variables vacías y luego asignarseles un valor.
    Se pueden asignar variables a otras variables.

Definiendo variables, sus sintaxis y sus ámbitos

        ```js
            var nombrevariable = value;
        ```
#### VAR
Son variables `globales` que se pueden referir en cualquier parte del código.

#### LET
Son variables `locales` que se ejecutan únicamente en el bloque de codigo dónde se encuentren {}.

    /*Ambas se pueden ver modificadas o reasignadas.*/

#### CONST
Tipo de variable que no se puede reasignar su valor una vez que se ha creado, en los arreglos o objects todavía se pueden agregar valores pero no reasignar.

    /*Tanto let como const suelen ser usados en bloques, contrario a var que es usado globalmente*

### Tipos de datos
Hay seis tipos de datos `primitivos`: 
    `string`, `number`, `bigint`, `boolean`, `undefined` y `symbol`.

#### Strings
`Cadenas de texto`
Letras, palabras y textos ubicados entre comillas `''`.
Si se desea incluir una comilla `simple` o `doble` en el `string` es conveniente colocar una `\` justo antes de la `comilla`.

- `Strings en JavaScript son codificados usando UTF-16.`
- `backticks`
    Permiten ingresar expresiones dentro del string, envolviéndolos en ${…}

        ```js
        ${variable o funcion a incluir}
        ```
- `String extensos`
Es posible crear strings de múltiples líneas usando comillas simples, usando un llamado `carácter de nueva línea`, escrito como `\n`, lo que denota un salto de línea:


#### Valores Booleanos
Binarios referidos a la verdad, TRUE o FALSE.
`JavaScript genera coerción de tipo para concluir un valor truthy o falsy en distinto casos sin que sea explícito.`
Esto refiere a que si en una espacio donde deberia haber una prueba hay otra cosa,dependiendo de lo que este en su interior JavaScript devolverá un True o un False en esa prueba.

`Coerciones resultantes en FALSE`
    False(directo y explícito)
    null
    undefined
    NaN
    0
    -0
    0n, -0n (BigInt)
    " ", ' ', ` ` (cadena de texto vacía)
    document.all

`Coerciones resultantes en TRUE`
    True
    Strings (cadenas de texto)
    Cualquier valor que no cuercione resultantente en False.

#### null
El valor especial `null` no pertenece a ninguno de los tipos descritos anteriormente.
Es sólo un valor especial que representa `nada`, `vacío` o` valor desconocido`

#### Undefined
Valor `falsy`. 
Significa `valor no asignado`
Se devuelve en funciones que no tienen declaración return. De igual modo en índices de arreglo o propiedades de objects que no existan.
    `undefined` 

### typeof
Devuelve el tipo de dato que almacena una variable u objeto.

    ```js
    let num = 8;
    console.log(typeof num); //"number"
    ```


### Funcion
Pueden tomar argumentos y darle información adicional a la computadora.
Una función de cualquier tipo lleva SIEMPRE los paréntesis ().
Guarda un bloque de codigo para ser usado posteriormente, siendo su principal objetivo permitir la reutilizacion de codigo constante.
Son independietes del objeto al que se aplican , estando condicionadas al uso correcto por parte del programador.

    ```js
    function nombrefunción(argumentos){
        Codigo a ejecutar;
    };

    () => {}
    //No requiere ni siquiera nombre. Corresponde guardarlo dentro de una variable.
        var nombrefunción = (argumentos) => {
            Código a ejecutar;
        };

    //Se pueden crear funciones sin argumentos, simplemente se ejecutara su bloque al llamarla, util cuando no depende de ninguna eleccion del usuario.
    var num1=x;
    var num2=y;
        function suma(){
            return console.log(num1+num2);
        };
            /*En consola */
            suma() // x+y
    ```
    Las funciones devuelven undefined por defecto. 
Una función debe hacer exactamente lo que sugiere su nombre, no más.
Dos acciones independientes por lo general merecen dos funciones, incluso si generalmente se convocan juntas `en ese caso, podemos hacer una tercera función que llame a esas dos`.

#### Parametros
Si se llama una `funcion` sin declararle un `parametro` su valor correspondiente se convierte en `undefined`. Podemos especificar un valor llamado `predeterminado` o `default` (que se usa si el argumento fue omitido) en la declaración de función usando `=`

    ```js
    function showMessage(from, text = "sin texto") {
        alert( from + ": " + text );
    }
    showMessage("Ann"); // Ann: sin texto

    Tambien se pudo haber desarrollado otra solucion mas compleja:
    function showMessage(from, text = anotherFunction()) {
    // anotherFunction() solo se ejecuta si text no fue asignado
    // su resultado se convierte en el valor de texto
    }
    ```

#### Return
Una función puede devolver un valor al código de llamada como resultado utilizando el `return`
La directiva `return` puede estar en cualquier lugar de la función. Cuando la ejecución lo alcanza, la función se detiene y el valor se devuelve al código de llamada `asignado al result anterior`.
Se puede utilizar el `return` para terminar una funcion inmediatamente.

#### Recursividad
Es cuando una funcion se llama a si misma desde su propia definicion.
Siempre debe haber una condicion o final, o caso base, para que la funcion no se llame a si misma para siempre.

    ```js
    function ftl(n){
        if (n===1){
            return 1;
        }
        return n * ftl(n-1);
    };
    ```

#### Funcion alert   
Al iniciar la website salta un mensaje que contiene el argumento de la funcion.

    ```js
    alert('Mensaje a abrir');
    ```

#### Funcion prompt
Esta funcion es similar a la de alert pero solicita al usuario un dato bajo la premisa escrita en el argumento. En otras palabras el argumento es lo que le explica al usuario que debe ingresar en el campo.

    ```js
    prompt('Ingrese un dato:')
    ```
    Podemos guardar este prompt en una variable

    ```js
    var dato = prompt('Ingrese un dato')
    ```

#### Impresion en consola
Corre en consola aquello que se encuentre en el paréntesis.

        ```js
        console.log('muestreo pantalla');
        ```

#### Algunas funciones
    ```js
    //Number, trasnforma strings a numeros
    var myString = '123';
    var myNum = Number(myString);
    console.log( myNum ); //123

    //.tofixed, define cuantos decimales tiene un numero.
    var myFirstNum = 8.3333339;
    var myCorrectNum = myFirstNum.toFixed(2);
    console.log(myCorrectNum) //8.33

    //toString, Convierte un elemento en un string equivalente.
    var myNum = 123;
    var myString = myNum.toString();
    console.log( myString ); //'123'
    ```


### Metodos
Conjunto de funcionalidades, o funciones que dependen del objeto sobre el que actuan. Siempre llevan `()` aunque no lleven argumento.
`La mayoría de funciones de JavaScript para estos propósitos toman el valor que le damos y retornan un nuevo valor, sin modificar el valor que le pasamos.`

#### De strings
[Listado de metodos de strings](https://tutobasico.com/string-javascript/)

- `.replace`
Toma 2 valores: los caracteres que queremos sacar y los caracteres que los van a reemplazar. No modifica el `string` original.

    ```js
    var example = "perros hermosos"
    example.replace("perros", "gatos") // gatos hermosos
    Para guardar este valor se tiene que reasignar este metodo a la variable.
    example = example.replace("perros", "gatos") 
    // Seguardo

    Caso particular
    var palabra = 'Fullstack';
    let palabraConGuiones = palabra.replace( /./g, '_ ');
    //reemplaza las letras por guiones y un punto.
    console.log(palabraConGuiones) // _ _ _ _ _ _ _ _ _ 
    ```

- `.indexOf`
Busca el argumento de la funcion dentro de el `string` al que se le esta aplicando elmetod. Cuenta desde el `0`. 
Devuelve el `indice` de la primer coincidencia.

    ```js
    var example = "Hola"
    console.log ( example.indexOf("o") ) // 1
    ```

- `.lastIndexOf`
Analogo a `.indexOf` pero busca las coincidencias de atras para adelante.

- `.lenght`
Evalua y devuelve la contidad de caracteres que tene un string.

#### De Arrays
- `.filter`
Aplica una prueba a cada elemento en un arreglo y devuelve un nuevo arreglo que solo contiene los elementos que pasan, `return TRUE`. No modifica el arreglo original.

    ```js
    function lessThanTen ( number ){
        return number < 10;
    }
    let numbers = [
        3,
        42,
        7,
    ];
    let numbersUnderTen = numbers.filter( lessThanTen );
    //Se evalua cada elemento del array y de pasar la prueba lo incluye al nuevo array declarado, sin modificar el anterior. 
    ```

- `.forEach`
Es una forma util de ejecutar una funcion de `devolucion de llamada` una vez para cada `elemento` de un `arreglo`, y cada elemento se convierte en el `argumento` de la devolucion de llamada.

    ```js
    let example = [
        'case1',
        'case2',
        'case3'
    ];
    function print( element ){
        console.log( element );
    };
    example.forEach(print); 
    ```

- `.map`
Ejecuta cada elemento a traves de una funcion y luego devuelve un nuevo arreglo con el resultado de cada elemento. `El arreglo original no se modifica`.

    ```js
    let array = [
        1,
        2,
        3
    ];
    let doubled = array.map( (i) => { return i*2;
    });
    // doubled = [2, 4, 6]
    ```

- `.reduce`
Toma todos los valores de una `lista`, aplica una funcion de `devolucion de llamada` a cada uno de ellos y acumula el resultado en un valor de salida. 
`.map` se diferencia de `.reduce` porque crea un `array nuevo` con los resultados individuales, mientras que `.reduce` reduce todos los resultados a un `unico valor`.

    ```js
    const resultado = lista.reduce( function callback(valorAnterior, valorActual){
        return; /*Resultado de la funcion callback*/
    }, valorInicial );
    ```
    resultado: variable que recoge el valor despues de aplicar .reduce

    reduce: Es el metodo usado. Todos los array tienen una funcion .reduce que se puede invocar. 
    Recibe dos parametro: una funcion Callback y el valor inicial.

    callback: Funcion que recibe como primer parametro el metodo reduce. Recibe 2 parametro, el valor anterior y el actual. 

    valorAnterior: resultado devuelto por la ejecucion anterior de callback. Llamese tambien accumulator.

    valorActual: elemento en el cual se encuentra iterando .reduce

    valorInicial: Opcional. De ser la primera vez que se ejecuta .reduce, se tomara como valorAnterior al parametro valorInicial que hayamos incluido en el .reduce y el cual se interpreta como un valor del que puede partir la funcion callback().

    Ejemplos:

    ```js
    const demoArray = [2, 4, 6, 8];
    let reducedArray = demoArray.reduce((accumulator, currentValue) => {
    return accumulator + currentValue
    }, 10); 
    //Se declara como primer parametro de la funcion .reduce una funcion flecha de devolucion de llamada y como segundo parametro un valor inicial del que se parte en la funcion flecha que es 10.
    //La funcion flecha suma el elemento actual en el que esta iterando .reduce al valor acumulado hasta el momento.
    //.reduce en este caso esta siendo usado para sumar todos los elementos de un Array.
    console.log(reducedArray); // 30
    ```

    ```js
    const partesDelCoche = ['asientos', 'volante', 'puertas', 'ruedas'];
    const coche = partesDelCoche.reduce( function (accumulator, currentValue) {
        return `${accumulator} ${currentValue}, `;
    }, 'Mi coche tiene: ');
    console.log(coche); 
    // Mi coche tiene: asientos, volante, puertas, ruedas
    ```    

- `.push`
`Agrega` su argumentos al `final` de un `arreglo`.

Similar:
    `.shift`: `elimina` el elemento  al `principio` de un arreglo. A su vez lo `retorna`.

Analogo:
    `.pop`: `elimina` un valor al `final` de un arreglo. A su vez lo `retorna`.
    `.unshift`: `Agrega` su argumentos al `principio` de un `arreglo`.

- `.reverse`
Invierte el orden de los elementos. `No requiere argumento`. `Modifica el Array original`.

- `.slice`
Crea un arreglo que es un `subconjunto` de otro arreglo. 
Toma `2 argumentos` en funcion de la `indexacion de arreglos`: 
El `inicio` - `incluido`
El `fin` - `no incluido`
No modifica el arreglo original

    ```js
    var example = [
        'case1',
        'case2',
        'case3',
        'case4'
    ];
    var subexample = example.slice(1, 3);
    //subexample = [case2, case3];
    ```

- `.splice`
`Reemplaza` una seccion de un arreglo con nuevos elementos. 
De forma particular permite `insertar` o `eliminar` elementos de manera controlada en cuanto a su posicion, `sin ser necesario que ocurran ambas`.
Toma `2 argumentos`:
El `indice` para comenzar la seleccion.
El numero de elementos para eliminar al comienzo del indice `0 si quieres insertar sin reemplazar`.
Los siguientes argumentos son los nuevos elementos para insertar en el indice `en blanco si solo estas eliminando`.
`No busca devolver llamada`
Modifica el arreglo original.

    ```js
    let array = [
        'A',  //[0]
        'L',  //[1]
        'A',  //[2]
        'S',  //[3]
        'K',  //[4]
        'A',  //[5]
    ];
    array.splice(3, 2, 'B', 'A', 'M');
    //Se posiciona en array[3] = 'S'
    //Elimina dos elementos, desde esa posicion => 'S', 'K'
    //Queda array = [ 'A', 'L', 'A', (...), 'A' ]
    //Inserta los elementos 'B', 'A', 'M'
    //Finalmente array = [ 'A', 'L', 'A', 'B', 'A', 'M', 'A' ] 
    ```

#### Operador de propagacion
`...`
El operador de propagacion de usa para agregar todos los elementos individuales de un arreglo a otro arreglo.

    ```js
    let dogs = [ 'Retriever', 'Sheperd', 'Terrier' ];
    let pets = [ 'Hedgehog', ...dogs, 'Turtle' ];
    //En un loop que consolee los elementos se veria cada elemento de manera individual como en cualquier array gracias al operador de propagacion.
    //Si no se implementara este operador se veria de la siguiente manera:
    // Hedgehog;
    // Retriever, Sheperd, Terrier;
    // Turtle;
    ```
Puede convertir `strings` en `arrays`.

### Arreglo ARRAY
Lista de elementos enmarcados en una variable. Puede compenerse por `números`, `strings`, o incluso otros `arreglos`, llamándose `anidamiento de arreglos`.

    ```js
        var secondArray=[1, 2, 3, 4];
        var exampleArray=[
            1, 'string', [secondArray]
        ];
    ```
Objetos tipo lista de alto nivel

#### Reemplazar y agregar elementos
    ```js
    let fruits = ['Apple', 'Orange', 'Plum']
    //reemplazar un elemento
    fruits[1] = Watermelon // ahora ["Apple", "Watermelon", "Pear"]
    //Agregar un elemento
    fruits[3] = 'Lemon'; // ahora ["Apple", "Orange", "Pear", "Lemon"]      
    ```

### Indexacion de arreglos y strings:
Los elementos de un arreglo se indexan comenzando por índice 0. De igual modo ocurre en los strings.

    ```js
        var firstArray=[
            'ok', // [0]
            'xd', // [1]
            'nashei', // [2]
            'fiumba' // [3]
            ];
        var secondArray = first array [1];  // secondArray = 'xd'
    ```

### CONDICIONALES
Compuertas binarias que se guian por `TRUE` y `FALSE` para tomar un camino a realizar, llamandose `Control de flujo de los datos`.
La condicion dentro del parentesis realiza `coercion de tipo booleana`, vista en el apartado [Valores booleanos](#valores-booleanos), llamandose `valores booleanos directos a esa conversion`.

#### If statement
Permite ejecutar una sección de código específica cuando una prueba es `verdadera`, también se aplica en `valores booleanos directos`

    ```js
        if (prueba){
            bloque a ejecutar si prueba=true;
        };
    ```

#### If else
Ejecutan una sección de codigo tanto en caso de `true` como de `false`.


    ```js
        if (prueba) {ejecución si true} else {ejecución si false};
    ```

#### Operador ternario
Ejecutan if else con menos código aunque son menos legibles.
Su principal uso radica en asignar una variable dependiendo alguna condicion.

    ```js
        let result = condition ? value1 : value2;       
    ```

- Ejemplo:

    ```js
        let accessAllowed = (age > 18) ? true : false;
        // Este ejemplo se podria realizar de la siguiente manera, dado que la comparacion devuelve directamete true o false.
        let accessAllowed = age > 18;
    ```

    ```js
        Caso convencional:
        if (age < 3) {
            message = '¡Hola, bebé!';
            } else if (age < 18) {
            message = '¡Hola!';
            } else if (age < 100) {
            message = '¡Felicidades!';
            } else {
            message = '¡Qué edad tan inusual!';
            }

        Caso ternario:
        let age = prompt('¿edad?', 18);

        let message = (age < 3) ? '¡Hola, bebé!' :
            (age < 18) ? '¡Hola!' :
            (age < 100) ? '¡Felicidades!' :
            '¡Qué edad tan inusual!';

        alert( message );
    ```

### Pruebas condicionales
Si se cumplen devuelven true, de lo contrario false.
    `Igualdad estricta`: a === b
    `Igualdad regular`: a==b
    `Desigualdad estricta`: a !== b
    `Menor` y `mayor` que: a < b   a > b
    `Menor` y `mayor` o igual que: a <= b     a >= b

#### Igualdad regular
Un operador de igualdad regular `==` compara valores de diferentes tipos, donde JavaScript convierte los valores a números. `No diferencia 0 o un string vacio de false`.

`Ejemplos`:

    ```js
    alert( '2' > 1 ); // true, '2' se convierte en 2
    alert( '01' == 1 ); // true, '01' se convierte 1

    alert( true == 1 ); // true
    alert( false == 0 ); // true
    ```
Es posible que al mismo tiempo:
    - Dos valores sean iguales.
    - Uno de ellos sea true como booleano y el otro sea false como booleano.

    ```js
    let a = 0;
    alert( Boolean(a) ); // false

    let b = "0";
    alert( Boolean(b) ); // true

    alert( a == b ); // true!
    //Una comparación de igualdad convierte valores utilizando la conversión numérica ("0" se convierte en 0), mientras que la conversión explícita Boolean utiliza otro conjunto de reglas.
    ```

`Desigualdad regular`
Analogo a la igualdad regular y su conversion de tipo numerica.
    a `!=` b

#### Igualdad estricta
Un operador de igualdad estricto `===` comprueba la igualdad sin conversión de tipo.
    `Si a y b son de diferentes tipos, entonces a === b retorna inmediatamente false sin intentar convertirlos.`

`Desigualdad estricta`
Analogo a la igualdad estricta sin conversion alguna.
    a `!==` b

#### Comparacion de null y undefined
Hay un comportamiento `no intuitivo` cuando se compara `null` o `undefined` con otros valores.

- Frente a una `igualdad estricta ===`
Estos valores son `diferentes`, porque son de tipo diferente.

    ```js
        alert( null === undefined ); // false
    ```

- Frente a una `igualdad no estricta ==`
Hay una regla especial. 
`Son iguales entre sí (en el sentido de ==), pero no a ningún otro valor.`

    ```js
        alert( null == undefined ); // true
    ```

- `Comparaciones matematicas`
    < > <= >=
null/undefined se convierten en números: 
    `null` se convierte en `0`
    `undefined` se convierte en `NaN`.

- `Casos particulares de null y undefined`
Tener cuidado al usar comparaciones como > o < con variables que ocasionalmente pueden ser null/undefined. Revisar por separado si hay `null`/`undefined` es una buena idea.

    ```js     null y 0
        alert( null > 0 ); /// (1) false
        alert( null == 0 ); /// (2) false
        alert( null >= 0 ); // (3) true
        //Una comparación de igualdad == y las comparaciones > < >= <= funcionan de manera diferente. Las comparaciones convierten a null en un número, tratándolo como 0. Es por eso que null >= 0 es verdadero y null > 0 es falso.
        
        //El control de igualdad == para undefined y null se define de tal manera que, sin ninguna conversión, son iguales entre sí y no son iguales a nada más. Es por eso que null == 0 es falso.
    ```

    ```js    undefined y 0
        alert( undefined > 0 ); // false (1)
        alert( undefined < 0 ); // false (2)
        alert( undefined == 0 ); // false (3)
        Las comparaciones (1) y (2) retornan falso porque no definido se convierte en NaN y NaN es un valor numérico especial que retorna falso para todas las comparaciones.
        La comparación de igualdad (3) retorna falso porque undefined sólo equivale a null y a ningún otro valor.
    ```

#### Comparacion de cadenas
Js utiliza el orden de `diccionario` o `Lexicografico` para definir que cadenas es mas grande, comparando letra por letra.

- Compare ordenadamente caracter por caracter de ambos strings, siendo determinante que en alguno de los dos un caracter sea mayor que el paralelo y dando por terminada instantaneamente la comparacion.
    `Si ambas cadenas tienen la misma longitud, entonces son iguales. De lo contrario, la cadena más larga es mayor.`
- No es un diccionario real, sino un orden Unicode
    `El algoritmo de comparación dado arriba es aproximadamente equivalente al utilizado en los diccionarios o guías telefónicas, pero no es exactamente el mismo.`
- A mayor posicion en el alfabeto, mayor es el indice en la tabla de codificacion interna.
- Los caracteres en minúsculas tiene un mayor índice en la tabla de codificación interna que utiliza JavaScript (Unicode). 

#### Compuertas logicas
Combinan pruebas
    Compuerta AND: casoA `&&` casoB
    Compuerta OR: casoA `||` casoB
    Negacion: `!`condicion /*Negara el resultado de la preposicion.*/

### Operadores matematicos
`Concatenar`
Para concatenar `strings` usamos `+`, pudiendo usarse en cualquier suma que involucre al menos un `string`. Si hay una combinacion larga de strings y numeros, se ejecuta en funcion de su `presedencia`, realizandose las sumas de manera simple hasta alcanzar el primer string y a partir de ahi se concatenara ese resutado con todo lo demas.

    ```js
    var word = ('So'+' cool')
    console.log(word)  //   So cool
    ```

`Operador modulo %`
Devuelve el resto de la division entre ambos operandos, hace un return con ese resultado.
        a % b

`Operador exponenciacion **`
De igual modo esta definida para numeros no enteros,aplicandose la radicacion cuando el exponente es fraccion.
        a ** b

`Conversion numerica UNARIO`
Si se le aplica un signo `+` a un valor que no es de tipo `numerico`, dicho
valor es convertido en un numero, respondiendo a las semejansas con los `valores booleanos`.

    ```js
    alert( +true);  //  1
    alert( +' ' );  // 0
    ```
La funcion `number()` ejecuta lo mismo

#### Operadores de asignacion
`///////////////////`

### CICLOS
Repite la sección del código dentro de `{}` una determinada cantidad de veces

#### For loop
`For... Of loop`
Pasa por cada elemento de un `string` o `arreglo`, repitiendo el código para cada elemento.

    ```js
    var exampleArray=[a, b, c, d];

    for (let element of exampleArray){
        codigo a ejecutar;
        };
    ```

#### Classic for loop
Repite el código una cantidad definida de veces.
Se difine en 3 partes.
`for (variable de ciclado definida, prueba que determina continuidad del ciclo, modificador del valor por ciclo){Código a interar hasta que el límite termine el ciclo}`

    ```js
    for (var i=valorInicial, i prueba(<,>,===) valorLimite, i=i+-valordeActualización){
    código a ejecutar;
    };
    ```

#### Ciclos anidados
Ciclos dentro de otros ciclos que pueden ser muy útiles. 
Si tiene demasiados puede causar que la ejecución sea lenta o difícil de entender.

#### Otros ciclos
while, do while, forEach
    
`while` 

    ```js
    var variable;
    while(variable!=='condicion'){
        accion();
        variable++;
    };
    ```

`dowhile`
Ejecuta la accion y luego analiza la variable para ver si lo repite.

    ```js
    var variable;
    do {
        accion();
        variable++;                
    } while (variable!=='condicion');
    ```

`.forEach`
Vease en la seccion de [Metodos de Arrays](#de-arrays)

#### SWITCH:
Tiene una sintaxis practica para el analisis recurrente de una variable que derive en muchos casos distintos.

    ```js
    var ejemplo;
    switch(variable){
        case 'valor1':
            accion1();
                break;
        case 'valor2':
            accion2();
                break;
        case 'valor3':
            accion3();
                break;
        default:
            acciondefault();
                break; /*termina el case.*/
    };      
    /*Aplicable a loops en funcion de un horario especifico. */
    ```

## DOM
Es la representación en `JavaScript` del documento `HTML`, esto permite crear, cambiar y/o remover elementos del mismo usando todas las herramientas de un lenguaje de programación como lo es JS.
También podemos agregar `eventos` a esos elementos para hacer más `dinámica` nuestra página.

El nombre de la variable global que representa el `DOM` es `document`.

El `DOM` visualiza el documento de HTML como un `árbol de tres nodos`. Un nodo representa un documento de HTML.

Nuestro documento se llama `nodo raíz` y contiene un `nodo hijo` el cual es el elemento <html>. El elemento <html> contiene dos hijos los cuales son los elementos <head> y <body>. Ambos elementos <head> y <body> tienen hijos propios. Podemos acceder a estos elementos en el documento y hacer cambios a ellos usando `JavaScript`.

### Nodos del DOM
La `raíz` del `árbol de nodos` de cualquier página `XHTML` siempre es la misma: un nodo de `tipo especial` denominado `Documento`.

A partir de ese `nodo raíz`, cada etiqueta XHTML se transforma en un nodo de tipo `Elemento`. La conversión de etiquetas en nodos se realiza de forma `jerárquica`. De esta forma, del `nodo raíz` solamente pueden derivar los nodos `HEAD` y `BODY`. A partir de esta derivación inicial, cada etiqueta XHTML se transforma en un nodo que deriva del nodo correspondiente a su `etiqueta padre`.

La transformación de las etiquetas XHTML habituales genera dos nodos: el primero es el nodo de tipo `Elemento` (correspondiente a la propia etiqueta XHTML) y el segundo es un nodo de tipo `Texto` que contiene el texto encerrado por esa etiqueta XHTML.

### NodeList o HTMLCollection
Aunque se hace referencia a `ARRAYS` realmente los métodos de búsqueda generalmente devuelven un tipo de dato `HTMLCollection` o `NodeList`, que aunque actúan de forma muy similar, `no son arrays`, y por lo tanto pueden carecer de algunos `métodos`, como por ejemplo `.forEach()`.

Estas `NodeList` son uno de los elementos simil `array` más utilizados cuando realizamos aplicaciones que implican un trabajo con el `DOM` y son el resultado de métodos como:

    ```js
    var myNodeLists = document. getElementsByTagName('a');
    ```
Al realizar una `búsqueda de elementos` y guardarlos en una `variable`, podemos realizar la búsqueda posteriormente sobre esa variable en lugar de hacerla sobre `document`. Esto permite realizar `búsquedas acotadas` por zonas, en lugar de realizarlo siempre sobre document, que buscará en todo el documento HTML.

Estas `listas` pueden ser iteradas como `pares clave / valor` donde cada `nodo elemento` forma un `objeto` con su `nodo de texto`.

#### NodeList Estatica o Dinamica
Es bueno tener en cuenta esta distinción cuando se elige cómo `iterar` sobre los elementos en `NodeList`, y cómo `guarda en caché` la longitud de la lista en particular.

En algunos casos, NodeList es una colección `en vivo`, lo que significa que los cambios en el `DOM` `se reflejan` en la `colección`. 

    ```js
    //Node.childNodes esta en vivo
    var parent = document.getElementById('parent');
    var child_nodes = parent.childNodes;
    console.log(child_nodes.length); // asumamos "2"
    parent.appendChild(document.createElement('div'));
    console.log(child_nodes.length); // debería imprimir "3" porque se actualiza.
    ```

En otros casos, NodeList es una colección `estática`, lo que significa que cualquier cambio posterior en el `DOM` `no afecta` el contenido de la `colección`. 
    `document.querySelectorAll ()` devuelve un NodeList estático.

### Metodos de NodeList

-  `Indexacion de NodeList`
Funciona de igual modo que con un arra `[]`. Una alternativa es `.item()` ubicandose el `indice` en el parentesis 

- `.entries()`
Devuelve un `iterator` que permite pasar por todos los `pares` clave / valor contenidos en este `objeto`.

    ```js
    var list = node.childNodes;

    // Using for..of
    for(var entry of list.entries()) {
        console.log(entry);
    };
    //Resultado:
    Array [ 0, <p> ];
    Array [ 1, #text "hey" ];
    Array [ 2, <span> ];
    ```

- `.keys()`
Devuelve un `iterator` que permite pasar por todas las `claves` de los pares clave / valor contenidos en este `objeto`.

    ```js
    var list = node.childNodes;

    // Using for..of
    for(var key of list.keys()) {
        console.log(key);
    };
    //Resultado:
    0
    1
    2
    ```

- `.values()`
Devuelve un `iterator` que permite recorrer todos los `valores` de los pares clave / valor contenidos en este `objeto`.

    ```js
    var list = node.childNodes;

    // Using for..of
    for(var entry of list.entries()) {
        console.log(entry);
    };
    //Resultado:
    <p>
    #text "hey"
    <span>
    ```

- `forEach`
vease [Metodos de arrays](#de-arrays).


### Seleccionar elementos del DOM

- `.getElementById('id')` 
Para acceder a un elemento en el archivo `html` con un `id` especifico recurrimos alsiguiente metodo.

    ```js
    var example = document.getElementById('ejemplo'); //ejemplo es el id
    ```

- `.querySelector('CSS Selector')` 
Este método permite encontrar elementos conociendo `selectores CSS`.
Busca el `primer elemento` que coincide con el selector CSS.

    ```js
    var exampl1 = document.querySelector('#ejemplo'); //ejemplo es el id.
    var example2 = document.querySelector('.list'); //list es una class de algun elemento.
    var example3 = document.querySelector('h1'); //h1 es un elemento.
    ```

- `.querySelectorAll('')`
Este método encuentra todos los elementos que coinciden con el `selector de CSS` y devuelve una `NodeList` de todos esos nodos.

    ```js
    //Para encontrar todos los elementos <li>, podría utilizar el combinador de hijos > para encontrar a todos los elementos hijos de <ul>.
    const listItems = document.querySelectorAll("ul > li");
    console.log(listItems); 
    //[object NodeList]
    ['<li/>', '<li/>', '<li/>', '<li/>'] //siendo que al tratarse de un Array se puede iterar con un forEach e imprimir en consola individualente.
    ```

- `.getElementsByClassName()` y `.getElementsByTagName()`
Los métodos `.getElementsByClassName()` y `.getElementsByTagName()` devuelven una `lista` de los elementos coincidentes, incluso si la coincidencia es un solo elemento.

    ```js
    //Alista todos los elementos del DOM con la class .rojo
    var elementsRojo = document.getElementsByClassName('rojo')

    //Alista todos los elementos del DOM que se formen con el tag div
    var elementsDiv = document.getElementsByTagName('div')
    ```

### Agregar elementos al DOM

- `document.createElement()`
Agrega nuevos elementos al árbol del DOM.

    ```js
    let exampleList = document.createElement("ul"); //examplList es una variable que almacena ele lemento lista creado
    //Un par de elementos <li>
    let element1 = document.createElement("li");
    let element2 = document.createElement("li");
    ```

- `.appendChild()`
Agrega ese elemento <ul> al documento usando el método `appendChild()`
Siempre al final del bloque.

    ```js
    document.body.appendChild(exampleList); //Lo incluye en el body
    //Incluimos los elementos de la lista en la lista.
    exampleList.appendChild(element1);
    exampleList.appendChild(element2);
    ```

- `.textContent`
Agrega texto para nuestros elementos del ejemplo de la lista.

    ```js
    element1.textContent = 'Content';
    ```

### Ubicar elementos en el DOM
Para Ubicar un `nuevo nodo` en el `DOM` recurrimos al `metodo` `.insertAdjacentHTML()`. Este metodo se aplica sobre un elemento ya definido

Toma 2 parametros (posicion y contenido):
- Posicion:
    `beforebegin` - Antes del elemento en cuestion
    `afterend` - Despues del elemento en cuestion
    `afterbegin` - Dentro del elemento en la primer posicion
    `beforeend` - Dentro del elemento en la ultima posicion.
- Contenido: a eleccion, pueden ser `nodos` en una variable o bien una `plantilla literal`.

    ```js
    foo=document.getElementById('footer')
    foo.insertAdjacentHTML('beforebegin','<div id="nuevodiv">...</div>') 
    ```

### Crear nodos de elementos y de texto
- `.innerHTML`
Inserta elementos al DOM pero interpretando el código HTML indicado y renderizando sus elementos.
Incluimos un nodo html en una variable y trabajamos sobre la misma

    ```js
    var datos = document.getElementById("datos"); 
    //ahora manipulamos el elemento desde la variable
    datos.innerHTML = `
    <h1>primer texto</h1>
    <h2>segundo texto</h2>
    <h3>Esto es una variable: $(nombre) </h3>
    `; //plantilla literal
    ```

La propiedad `.innerHTML` comprueba y `parsea` el marcado HTML escrito (corrigiendo si hay errores).

#### Clonar nodos
Se debe ser cuidadoso al crear y duplicar elementos HTML. Un error muy común es asignar un elemento a otra variable, donde solo se esta `referenciando denuevo`, mas `no clonando`

- `.cloneNode(deep)`
El método `.cloneNode(deep)` acepta un parámetro  `deep` opcional, a `false por defecto`, para indicar el tipo de clonación que se realizará:

true,:
    clonará también sus hijos, conocido como una `clonación profunda` (Deep Clone).
false:
no clonará sus hijos, conocido como una `clonación superficial` (Shallow Clone).


    ```js
    const div = document.createElement("div");
    div.textContent = "Elemento 1";

    const div2 = div.cloneNode();   // Se clono div en div2
    div2.textContent = "Elemento 2";
    ```

#### Eliminar nodos
La forma más sencilla de `eliminar nodos` o elementos HTML es utilizando el método `.remove()` sobre el nodo o etiqueta a eliminar.

    ```js
    const div = document.querySelector(".deleteme");
    div.isConnected;    // true
    div.remove();
    div.isConnected;    // false
    ```

#### Ejemplos crear elementos

    ```js
    //Insertar list items en una lista con id LISTA con 2 caminos.
    //Buscamos el elemento lista
    const LISTA = document.getElementById('lista');

    //A - Creamos el list item y le agregamos un nodo de texto con el contenido.
    let item = document.createElement("li");
    let texto = document.createTextNode("Elemento de prueba"); //Una opcion
    item.appendChild(texto);
    item.textContent = "Elemento de prueba"; //Otra opcion
        LISTA.appendChild(item); //Lo incluimos en la lista

    //B - Creamos el item en una plantilla literal
    var item = "<li>Texto de prueba</li>";
        LISTA.innerHTML += item; //Lo incluimos en la lista
    ```

### Asignar atributos HTML a un elemento
- `.style`
La propiedad `style` te da la habilidad de cambiar el CSS inline en tu documento de HTML.

    ```js
    const exampleh1 = document.querySelector('h1');
    exampleh1.style.color = 'red' // Aplicable a cualquier propiedad de estilo deseada.
    ```

- `.className`
Con el metodo `className` se puede agregar clases a un elemento previamente definido.
Es posible asignar a la propiedad className `varias clases` en un `string` separadas por espacio. Aunque es recomendable utilizar la propiedad `classList`.
Puede tanto leerse como reemplazarse.

    ```js
    element = document.getElementById('example');
    element.className += 'centrado'; 
    //Agrega la class centrado al elemento con id="example"
    ```

- `.classList` 
`Objeto` especial para manejar `clases CSS`. Contiene métodos y propiedades de ayuda.

    ```js
    const div = document.getElement('contenedor')

    div.classList.add(c1, c2, c3...)//Añade las clases c1, c2... al elemento HTML.
    ```

- `.id`
Asigna el atributo `id` al elemento deseado.

    ```js
    const div = document.createElement("div"); // <div></div>
    div.id = "page";
    ```

#### Recuperar el valor del tributo class `pendiente a completar`
Para recuperar el valor del atributo class de un elemento se recurre a la siguiente sintaxis

    ```html
    <article class='doscolumnas' id='articulo1'>...</article>
    ```

    Solo dispongo de la manera pero no de la sintaxis.

    ```js
    articulo.attributes.class
    ```

### Eventos en una Webpage
El `metodo` `.addEventListener()` permite agregar `eventos` a un elemento `html`.
Registra un `evento` a un `objeto` en específico. El `Objeto` especifico puede ser un simple `elemento` en un archivo, el mismo  `documento` , una `ventana` o un  `XMLHttpRequest`.
Permite agregar mas de un `listener` a un solo `evento`. 


- `.addEventListener()`
Toma un tipo de `evento` y una `función`.

    ```js
    target.addEventListener(tipo, listener[, useCapture]);
    target.addEventListener(tipo, listener[, useCapture, wantsUntrusted 
    ]);
    ```
`tipo`: 
`string`que representa el `tipo` de evento a escuchar.

`listener`: 
`objeto` que recibe una notificación cuando un evento del tipo especificado ocurre. Debe ser un `objeto` implementando la interfaz EventListener o solo una `function` en JavaScript.

`useCapture`: 
Si es `true`, `useCapture` indica que el usuario desea iniciar la captura. Después de iniciar la captura, todos los eventos del tipo especificado serán lanzados al `listener` registrado antes de comenzar  a ser controlados por algún EventTarget que esté por debajo en el arbol DOM del documento.


    ```js
    //declaramos un nodo en una variable
    const button = document.getElementById("btn");
    //evento click, funcion flecha declarando una alerta
    button.addEventListener("click", () => {
        alert("Gracias por dar Click");
    });
    ```

    ```js
    //DOMContentLoaded = la pagina carga por completo y recien ahi se ejecutan las funciones.
    //aca si alistamos funciones con eventos internos estamos planteando que se habiliten cuando cargue la pagina por completo y luego cada funcion tiene sus eventos necesario para funcionar.
    document.addEventListener("DOMContentLoaded", (e)=>{
    searchFilter(".card-filter", ".card");
    });
    ```

#### Ejemplos de eventos
- Cambiar texto en funcion de un click
    ```html
    <table id="t">
        <tr>
            <td id="t1">one</td>
        </tr>
        <tr>
            <td id="t2">two</td>
        </tr>
    </table>
    ```

    ```js
    // Function to change the content of t2
    function modifyText() {
        var t2 = document.getElementById("t2");
        t2.firstChild.nodeValue = "three";
    }

    // Function to add event listener to t
    function load() {
        var el = document.getElementById("t");
        el.addEventListener("click", modifyText, false);
    }

    document.addEventListener("DOMContentLoaded", load, false);
    ```

### Importar js
Para `importar` funciones u objetos de otro `archivo.js` se utiliza la siguiente sintaxis:

    ```js
    import {funcion} from "./archivo.js";
    ```

#### Biblioteca js
Se suele referir al JavaScript escrito por tercero como una `biblioteca` o `plugin`. 
Una reconocida es [Underscore.js](http://underscorejs.org/)
Para su inclusion en consola se escribe lo siguiente:

    ```js
    const script = document.createElement("script");
    script.type = "text/javascript";
    script.src = "https://cdn.jsdelivr.net/npm/underscore@1.13.3/underscoreumd-min.js"; // use this for linked script
    script.text = "alert('voila!');" // use this for inline script
    document.body.appendChild(script); //Lo incluye en el body creo que al final
    ```

## Estructurar datos

### Object
Los objetos son `arreglos asociativos` con varias características especiales.
El tipo de dato `object` es especial, mientras que los demás tipos de datos se llaman `primitivos` porque sus valores pueden contener una sola cosa; los objetos se utilizan para almacenar `colecciones de datos` y `entidades más complejas` asociados con un nombre `clave`.

El tipo de dato `symbol` se utiliza para crear identificadores únicos para los objetos. Se vera en mayor profundidad mas adelante

#### Par clave / valor
Un `Object` almacena varios valores que tienen nombres de `propiedades` tambien llamadas `claves` las cuales refieren un `valor`. De aqui surge que se contruyen los objects con `pares clave / valor`. Facilita el `acceso` mas adelante en el codigo.

    ```js
    var example = {
        key1: value1,
        key2: value2,
        "extended key": value3,
    };
    console.log(example.key1); // value1
    console.log(example["extended key"]); // value3
    ```
Se puede acceder a un `par clave / valor` de dos maneras:

- `Notacion de punto`
Es literal y simple pero con `restricciones`
object.key // value

- `Notacion de corchetes`
Funciona igual que la `notacion de punto` pero permite asignarle un valor a una variable y usar esa variable como `key`, considerando solamente el contenido `aplicable a asignar el valor de un input a una variable y usar en funcion de la misma`
A su vez, permite buscar `keys` de mas de una palabra.

##### Borrar un Par clave / valor
Para eliminar una propiedad podemos usar el operador delete

    ```js
        delete user.age;
    ```

#### this en objects
La palabra clave `this` se refiere al `objeto actual` en el que se está escribiendo el código.

    ```js
    var persona = {
    nombre: ['Bob', 'Smith'],
    edad: 32,
    //declaramos una propiedad de dos palabras como string usando this
    "quien es": this.nombre[0] + '' + this.nombre[1] + ' tiene ' + this.edad + ' años.',
    //exponemos "quien es" en un alert
    bio: function (){
        alert(this["quien es"]);
    },
    }
    ```

#### Prueba key existente
Para probar fácilmente si la propiedad existe; existe un operador especial para ello: `in`

    ```js
    let user = { name: "John", age: 30 };
    alert( "age" in user );    // mostrará "true"
    ```

### Metodos de objects
Al crear `keys` en object que contienen `funciones`, las mismas le permiten al objeto hacer algo con sus datos, y se les denomina `metodos` del `objeto`.

### Bucle for in
Para recorrer todas las claves de un objeto existe una forma especial de bucle: `for..in.`

    ```js
    let user = {
    name: "John",
    age: 30,
    isAdmin: true
    };

    for (let key in user) {

    // claves
    alert( key );  // name, age, isAdmin

    // valores de las claves
    alert( user[key] ); // John, 30, true
    }
    ```

### JSON
JSON es un `formato de datos` que tiene su propio estándar independiente y librerías para la mayoría de los lenguajes de programación.
Parte del concepto `par key / value`.

La `diferencia` entre los objetos de `js` y los objetos en una estructura de datos `JSON` es que JSON no te permite tener errores de sintaxis en el documento.

#### Sintaxis JSON
- Cualquier uso de comillas sera doble
- La estructura puede partir de un arreglo que contenga objetos.
- objetos:
        Es posible introducir una cantidad `infinita` de propiedades.
        Las propiedades se separan con coma. `La ultima propiedad nodebe terminar con una coma`
- propiedad-keys: 
        `Comillas dobles` tanto al inicio como al final.
        Unir palabras con una `mayuscula` en una nueva paabra o con un `guion bajo`.

- valor-value
        Acepta `strings`, `numeros enteros`, `numeros decimales`( delimitando el decimal con un `punto`), `booleanos`, `arrays`.


### Metodos JSON, toJSON
- `.parse()`
Transforma un json que esta en formato de string devuelta a JSON.
Para decodificar un string JSON.

- `JSON.stringify()`
Toma al objeto entre parentesis y lo convierte a un string.

    ```js
    let student = {
    name: 'John',
    age: 30,
    isAdmin: false,
    courses: ['html', 'css', 'js'],
    wife: null
    };

    let json = JSON.stringify(student);

    alert(typeof json); // ¡obtenemos un string!
    ```

- `JSON.parse()`
Para decodificar un string JSON, se necesita otro método llamado `JSON.parse`.

    ```js
    let value = JSON.parse(str, [reviver]);
    //str: string JSON para analizar.
    reviver: function(key,value) 
    //opcional que será llamado para cada par (propiedad, valor) y puede transformar el valor.
    ```

    ```js
    //Usando el reviver
    let str = '{"title":"Conference","date":"2017-11-30T12:00:00.000Z"}';
    //Al parsear el value de date vuelve como string.
    let meetup = JSON.parse(str, function(key, value) {
    if (key == 'date') return new Date(value);
    return value;
    });

    alert( meetup.date.getDate() ); // ¡Ahora funciona!
    //Sirve tambien para objetos anidados.
    ```

### Convertir un objeto en JSON

```js
let user = {
  name: "John Smith",
  age: 35
};
let user2 = JSON.parse(JSON.stringify(user));
//JSON.stringify invoca tojson dandole el formato necesario para habilitarse en JSON, luego JSON.parse(object) lo decodifica en JSON.
```


## API Fetch
En arquitectura cliente/servidor, el `cliente` hace un `fetch` al `servidor` para que nos envíe lo que se está pidiendo.
Esta `API` permite realizar `peticiones asincronas` mediante `promesas`.

Toda `REST API` tiene tres elementos. La `solicitud` (request), la `respuesta` (response) y los `encabezados` (header).

`Request` Estos son los datos que envías a la `API`, como una identificación de pedido (id) para obtener los detalles del pedido.

`Response` Los datos que obtengas del `servidor` después de una solicitud exitosa o fallida.

`Headers` Metadatos adicionales que se mandan a la API para ayudar al servidor a comprender qué tipo de solicitud se está mandando, por ejemplo, “content-type” (tipo de contenido).

### Arquitectura SOAP
Arquitectura `dividida por niveles` que se utilizaba para hacer un servicio, es `más complejo` de montar como de gestionar y solo trabajaba con `XML` a diferencia de `arquitectura REST`.

### Arquitectura REST
Lo más extendido hoy día.
Frente a nuestros pedidos al servidor se nos devolverá un JSON, que se puede traducir fácilmente a objetos javascript y con eso mostrarlo en pantalla usando al DOM y colocando las clases para dar el estilo necesario.
`Fetch` tiene la habilidad de leer archivos de `texto plano`, como `JSON` o
hasta un `.txt`.

#### REST - Interfaz
`REST` es una `interfaz` para conectar varios sistemas basados en el `protocolo HTTP`.
Sirve para obtener y `generar datos y operaciones`, devolviendo esos datos en `formatos` muy específicos, como `XML` y `JSON`.
Utiliza los verbos `GET`, `POST`, `PUT` y `DELETE`. De aquí surge una alternativa a `SOAP` solucionando la `complejidad` que la misma sumaba.
Facilitando asi el desarrollo de una `API REST`, en este caso de un `servicio` en el cual nosotros vamos a `almacenar nuestra lógica de negocio` y vamos `servir los datos` con una serie de `recursos URL` y una serie de datos que nosotros los limitaremos, es decir, será nuestro `BACKEND` nuestra `lógica pura de negocios` que nosotros vamos a utilizar.
Crea una petición `HTTP` que contiene toda la información necesaria, es decir, un `REQUEST` a un `servidor` tiene toda la información necesaria y solo espera una `RESPONSE`, ósea una respuesta en concreto.
Todos los objetos se manipulan mediante `URI`.

- `GET — Obtener` datos de la API. 
- `POST — Empujar` los datos a la API. Por ejemplo, crear un nuevo registro de usuario con nombre, edad y dirección de correo electrónico.
- `PUT — Actualizar` un registro existente con nuevos datos.
- `DELETE — Eliminar` un registro. 

#### REST - Ventajas
- Permite separar el `cliente` del `servidor` y las tecnologias que envuelve a ambas.
- Tiene una gran comunidad.
- Se puede crear `diseño de un microservicio orientado a un dominio` (DDD).
- Es completamente `independiente de la plataforma`, pudiendo usarse `REST` en cualquier sistema operativo.
- Se puede hacer a las APIs publicas.
- Brinda `escalabilidad` gracias a la separacion de los conceptos `CLIENTE` `SERVIDOR`.

### Sintaxis Fetch

    ```js
    fetch('https://randomuser.me/api/')
    .then( response => response.json())
    //El argumento de las promesas es como la respuesta que obtenemos del fetch, no importa el nombre que le pongamos (data, response, res).
    //Transformamos el dato en algo que podemos leer:
    //.blob() para imagenes.
    .then( response => {
    console.log(response.results['0']);
    contenido.innerHTML = `
    <img src="${response.results['0'].picture.large}" width="100px" class="img-fluid rounded-circle">
    <p>Nombre: ${response.results['0'].name.title} ${response.results['0'].name.first} ${response.results['0'].name.last}</p>
    `});
    ```
Un caso con una funcion:
Trabajamos todo desde una constante y no con promesas

    ```js
    async function obtenerDatos(){
        const response = await fetch("http://127.0.0.1:5500/JSONactividad/datos.json"); 
        //Al tratarlo con constantes se recurre al elemento async y await
        const json = await response.json();
    };
    ```

- `URL`
Se puede trabajar con URLs de APIs de la Web o bien con URLs Locales, que representan archivos JSON propios, bajo la siguiente sintaxis:
`http://127.0.0.1:5500/JSONactividad/datos.json`
Conformandose por el puerto `http://127.0.0.1:5500/` concatenado a la direccion del archivo `JSONactividad/datos.json`

- `fetch()`
`Metodo global` para obtener recursos de forma asincrona por la red facilmente. Por defecto toma el metodo GET
Ubica la solicitud que realizaremos por medio de un URL obligatorio.
    `fetch('URL')`
Hace promesas a traves de `.then`.
No envia ni recibe cookies a menos que se configuren `credentials de la opción init`
Cabe destacar que `fetch()` devuelve una `respuesta HTTP` y la misma debe ser atravesada por algun metodo para poder interpretarla. 

Tanto `.then()` como `.catch()` son promesas en funcion de lo que devuelve la `peticion`, si se resuelve `correctamente` se ejecuta `.then()` por el contrario si ocurre algun `error` y no se pudo resolver la peticion se ejecuta `.catch()`

- `.then()`
Es una `promesa`. `'Promete'` que va a traer una respuesta.
El objeto `Promise` devuelto desde `fetch()` no será rechazado con un estado de error HTTP incluso si la respuesta es un `error HTTP 404 o 500`; se resolverá normalmente `con un estado ok configurado a false`, y  este solo sera `rechazado` ante un fallo de red o si algo impidió completar la solicitud.

    ```js
    //Toma una data y la transforma, en este caso la data viene en formato txt.
    fetch('URL');
    .then( data => data.text )
    //la preformateamos en un archivo que podemos leer.
    //para imagenes se usa .bloob()    
    ```

- `.catch()`
Un `.catch()` es usado si se produce algún `error` en la peticion. Es analogo al funcionamiento de `.then()`.

    ```js
    fetch('https://swapi.co/api/people/1/')
    .then(res => res.json())
    .then(res => console.log(res)); 
    // imprime el objeto recibido.
    .catch( err => console.error(err)); 
    // muestra un mensaje de error en la consola.
    ```


### Response
La interfaz `Response` de la `Fetch API` representa la respuesta a una petición.

- Propiedades:
`Response.headers` 
    Contiene el objeto Headers asociado con la respuesta.
`Response.ok`
    Contiene un `estado` indicando si la respuesta fue exitosa (estado en el rango  200-299) o no.

#### Metodos Response
`response` también tiene algunos `métodos` interesantes, la mayoría de ellos para procesar mediante una `promesa` los datos recibidos y facilitar el trabajo con ellos

- `Response.clone()`
Clona un Objeto Respuesta `Response`.

    ```js
    var myRequest = new Request('flowers.jpg');
    var newRequest = myRequest.clone(); // a copy of the request is now stored in newRequest
    ```

- `.text()`
Una vez que se recibe un response mediante la siguiente estructura,     transforma el json a formato de string para poder interpretarlo.


    ```js
    async function obtenerDatos(){
        const response = await fetch("#url");
        const json = await response.text();
    };
    ```

- `.json()`
Al recibir un response por la siguiente estructura, lo deja en formato json para poder interpretarlo.

    ```js
    async function obtenerDatos(){
        const response = await fetch("http://127.0.0.1:5500/JSONactividad/datos.json");
        const json = await response.json();
    };
    ```

- `.formData()`
Al recibir un response por la siguiente estructura, devuelve una promesa para poder interpretarlo como datos de formulario.

    ```js
    async function obtenerDatos(){
        const response = await fetch("http://127.0.0.1:5500/JSONactividad/datos.json");
        const json = await response.formData();
    };
    ```

### Async/await
Realiza el mismo trabajo ue con .then y las funciones flechas.
`await` sólo se puede ejecutar si esta dentro de una función definida como `async`.

- Creamos una función request(url) que definimos con async
- Llamamos a fetch utilizando await para esperar y resolver la promesa
- Comprobamos si todo ha ido bien usando response.ok
- Llamamos a response.text() utilizando await y devolvemos el resultado

```js
const request = async (url) => {
    const response = await fetch(url);
    if (!response.ok)
    throw new Error("WARN", response.status);
    const data = await response.text();
    return data;
}

const resultOk = await request("/robots.txt");
const resultError = await request("/nonExistentFile.txt");
```

### API Fetch - Casos

#### Comprobando estado del Fetch 

    ```js
    fetch('flores.jpg')
        .then(function(response) {
        if(response.ok) {
            response.blob()
            .then(function(miBlob) {
                var objectURL = URL.createObjectURL(miBlob);
                miImagen.src = objectURL;
            });
        } else {
            console.log('Respuesta de red OK pero respuesta HTTP no OK');
        }
        })
        .catch(function(error) {
            console.log('Hubo un problema con la petición Fetch:' + error.message);
        });
    ```

#### Enviar peticion con credencial
Para producir que los navegadores envien una petición con las credenciales incluidas, incluso para una llamada de origen cruzado, añadimos credentials: 'include' en el el objeto init que se pasa al método fetch().

    ```js
    fetch('https://example.com', {
    credentials: 'include'
    })
    ```

#### XMLHttpRequest - Ejemplo
Usando `XMLHttpRequest`

    ```js
    var http_request = new XMLHttpRequest();
    var url = "http://example.net/jsondata.php"; // Esta URL debería devolver datos JSON
    
    // Descarga los datos JSON del servidor.
    http_request.onreadystatechange = handle_json;
    http_request.open("GET", url, true);
    http_request.send(null);
    
    function handle_json() {
    if (http_request.readyState == 4) {
        if (http_request.status == 200) {
        var json_data = http_request.responseText; 
        var the_object = eval("(" + json_data + ")");
        } else {
        alert("Ocurrió un problema con la URL.");
        }
        http_request = null;
    }
    }
    ```



### Otras APIs
- `Twitter API`
Obtener un usuario de Twitter en función de su nombre de usuario.

https://publicapis.dev/ 

https://www.coingecko.com/en/api/documentation
https://api.mercadolibre.com/sites/MLA/search?q=malabares
https://pokeapi.co/
https://rickandmortyapi.com/documentation
https://icanhazdadjoke.com/

## Promesas y Callbacks

### Callbacks

#### Ejemplo de callbacks

    ```js
    const suma = (n1, n2) => n1 + n2;
    const resta = (n1, n2) => n1 - n2;
    const multiplicacion = (n1, n2) => n1 * n2;
    const division = (n1, n2) => n1 / n2;
    /*función que recibe un callback que permite elegir qué
    operación realizar*/
    //Admite suma, resta, multiplicacion, division
    function calculadora(n1, n2, operacion) {
        return operacion(n1, n2);
    }
    ```

## Buenas practicas
- `consola`
    Podemos usar la consola desde VScode abriendo la terinal de `powershell`. En la misma ejecutamos el codigo descrito al usar el comando `node` `ruta del archivo`.

- `try catch`
    Controla el `flojo del programa`. Sirve cuando ya sabes como funciona el programa. Previo a esta etapa se controla con `console.log()`

- `sintaxis en variables`
Se sigue el estandar internacional del formato de js
    `constantes`: en MAYUSCULAS separado con guiones bajos `_`
    `clases de js`: empiezan en mayuscula, siguen con minuscula y cada nueva palabra comienza con mayuscula
    `variable`: empiezan en minuscula, cada nueva palabra comienza con mayuscula y sigue con minuscula 
    `funciones`: en minuscula




## `pendiente`

##### Sintaxis interesante para vincular funciones a partes del `html`

    ```html
    <button>Press me</button>
    ```

    ```js
    var button = document.querySelector('button');
    button.onclick = function() {
        var name = prompt('What is your name?');
        alert('Hello ' + name + ', nice to see you!');
    }
    ```

    

##### Para recibir la entrada de un `input` se recurre a la siguiente sintaxis

    ```js
    let temperatura = document.getElementById('temperatura').value;
    ```

    En caso de tratarse de marcar una casilla o un elemento se termina la estructura con un `.checked` en vez de un `.value`

##### Write en elementos
    Se elige el elemento en el que se escribira el argumento de la funcion.

    ```js
    document.write('contenido');
    ```




