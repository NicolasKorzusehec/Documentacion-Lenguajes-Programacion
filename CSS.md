# CSS 
CSS3 cascade style sheet

[Volver al inicio](./README.md)

## Contenidos
- [Comentarios](#comentarios)
- [Vinculacion a un html](#vinculacion-a-un-html)
- [Estructura basica](#estructura-basica)
- [BOX-MODEL](#box-model)
- [Selectores especificos](#selectores-especificos)
	- [Selectores de atributo](#selectores-de-atributo)
	- [Pseudoclases](#pseudoclases)
	- [Pseudoelementos](#pseudoelementos)
	- [Selectores complejos](#selectores-complejos)
		- `Combinadores descendientes`
		- `Combinador de hermano siguiente`
		- `hermano siguiente con selector universal`
		- `Combinador secundario`
		- `Selectores compuestos`
- [LA CASCADA](#la-cascada)
	- `Posicion y orden de aparicion`
	- `Especificidad`
	- `Origen`
	- `Importancia`
- [PENDIENTE FORMATEAR](#pendiente-formatear)

### Comentarios
Para comentar seleccionamos comentario y atajo shift + alt + A 

### Vinculacion a un html
Primero se debe vincular la hoja de estilos a la pagina html en el tag de head.

	```html
	<link rel="stylesheet" type="text/css" href="Carpeta/Archivo.css">
	```

### Estructura basica
La estructura básica de CSS es:
`Selector`: Elemento a modificar su formato
`Propiedad`: Parámetro a modificar
`Valor`: resultado de la propiedad

	```css
	.selector {
		propiedad: valor;
	}
	```

### BOX-MODEL
Se estructura el formato de los elementos de html como un conjunto de cajas, una dentro de otra:
		
	MARGIN -> BORDER -> PADDING -> CONTENT
		
`BOX-SIZING`

	```css
	.elemento {
	box-sizing: content-box;
	/*Cuando estableces dimensiones de alto y ancho se aplican al cuadro de contenido. Los valores dde padding y border se agregan al valor del tamaño de caja de contenido.*/
	box-sizing: border-box;
	/*Este modelo le dice a CSS que aplique el width a la caja de borde en vez de a la de contenido. Concluyendo que el border y el padding se empuje hacia dentro. Siendo el width definido el ancho al que se renderiza	.
	Este modelo de caja alternativo se suele aplicar con una regla de CSS para todos los elementos, todos los ::before y todos los ::after*/
	}
	
			*,
			*::before,
			*::After { 
					box-sizing: border-box;
			}
			/*Se suele agregar a resets y normalizers porque es un modelo de caja más predecible.*/
	```

### Selectores especificos

### Selectores de atributo
El selector de atributos CSS coincide con los elementos en función de la presencia o el valor de un atributo determinado.
	Elementos <a> con un href que contenga "example"

		```css
		a[href*="example"] {
			font-size: 2rem;
		}
		```
					
### Pseudoclases 
Los elementos HTML se encuentran en varios estados, ya sea porque interactúan con ellos o porque uno de sus elementos secundarios está en un estado determinado. Se definen con un signo (:).

### Pseudoelementos
Los pseudoelementos se diferencian de las pseudoclases porque en lugar de responder al estado de la plataforma, actúan como si estuvieran insertando un nuevo elemento con CSS.
También son sintácticamente diferentes de las pseudoclases, ya que en vez de usar un solo signo de dos puntos (:), utilizamos un signo de dos puntos dobles (::).

	Puede usar el pseudoelemento ::before para insertar contenido al comienzo de un elemento, o el pseudoelemento ::after para insertar contenido al final de un elemento.

		```css
		.my-element::before {
			content: 'Prefix - ';
		}
		``` 			

	También puede usarlos para apuntar a partes específicas de un elemento. 

		```css
		/*suponga que tiene una lista. Utilice ::marker para diseñar cada viñeta (o número) en la lista.*/
		li::marker {
			color: red;
		}		
		/* Su lista ahora tendrá puntos rojos o números rojos */
		```

	También puede usar ::selection para agregarle un estilo al contenido que un usuario ha resaltado.

		```css
		.contenido::selection {
			background: black;
			color: white;
		}
		```

### Selectores complejos
Aplica estilos a los elementos secundarios de un elemento partiendo de la recursividad.

`Combinadores descendientes`
Un combinador descendiente nos permite apuntar a un elemento secundario. Esto usa un espacio ( ) para indicarle al navegador que busque elementos secundarios:

	```css
	p strong {
		color: blue;
	}
	```

`Combinador de hermano siguiente`
Puede buscar un elemento que siga inmediatamente a otro elemento si usa un cáracter `+` en su selector, la posicion se considera dentro del mismo padre, siendo un elemento paralelo y no interno.
	Util para espaciar elementos equitativamente sin un espacio extra.

	```css
	.SelectorPadre .SelectorInicial + .SelectorConsecuente {
			margin-top: 5em;
		}
	/*Agrega el margin a cada elemento dentro del elemento padre con clase .SelectorPadre que sea consecutivo a algun elemento dentro del mismo 
	(SE CONDICIONA LA CONSECUCION NECESARIA. */
	```

`hermano siguiente con selector universal`
Puede agregar margen a todos los elementos secundarios dentro del `selector padre` 
	Puede presentar un espaciado excedente

	```css
	.top * {
		margin-top: 1em;
	}
	```

`Combinador secundario` (también conocido como descendiente directo) 
Le permite más control sobre la recursividad que viene con los selectores de combinador. Al usar el carácter >, limita el selector de combinador para que se aplique solo a los secundarios directos.	
	El espacio se agrega a cada hermano siguiente, pero si uno de esos elementos también tiene elementos del hermano siguiente como secundarios, puede resultar en un espaciado adicional no deseado.

	Para aliviar este problema, cambie el selector de hermanos siguientes para incorporar un combinador de secundarios: > * + *. La regla ahora solo se aplicará a los secundarios directos de .top.

	```css
	.top > * + * {
		margin-top: 1.5em;
	}
	```

`Selectores compuestos`
Puede combinar selectores para aumentar la especificidad y la legibilidad. Por ejemplo, para apuntar a los elementos <a>, que también tienen una clase de .my-class

	```css
	a.class {
		color: red;
	}
	```




### LA CASCADA
Dos o más reglas CSS pueden aplicarse a un elemento, el navegador elige cuál usar en función de diversos casos.
`La cascada` es el algoritmo para resolver conflictos donde se aplican `múltiples reglas CSS` a un `elemento HTML`. 

El algoritmo en cascada se divide en 4 etapas distintas:
		
#### Posición y orden de aparición
El orden en el que aparecen tus reglas CSS.
Se vuelven más `específicos` cuanto más `abajo` están en el archivo CSS, contrario a lo que ocurre en un archivo html con la posición de las etiquetas que dan estilo. 
	Ya sean etiquetas links que vinculen páginas de estilos o bien directamente reglas CSS en un archivo CSS.
Este enfoque de declarar la misma propiedad dos veces funciona porque los navegadores ignoran los valores que no comprenden. 

	```js
	//Si el navegador es compatible con clamp(), se descartará la declaración de font-size. Si clamp() no es compatible, se respetará la declaración inicial y el tamaño de fuente será 1.5rem.
			.my-element {
				font-size: 1.5rem;
				font-size: clamp(1.5rem, calc(1rem + 3vw), 2rem);
			}
	```

#### Especificidad
La especificidad es un algoritmo que `determina qué selector de CSS es el más específico`, utilizando un sistema de ponderación o puntuación para realizar esos cálculos. 
	Al hacer una regla más específica, puede hacer que se aplique incluso si algún otro CSS que coincida con el selector aparece más adelante en el CSS.		
- El CSS dirigido a una `class` en un elemento hará que la regla sea más específica.
- Una `id` hace que el CSS sea aún más específico, por lo que los estilos aplicados a una id anularán los aplicados de muchas otras formas. 
		Esta es una de las razones por las que generalmente no es una buena idea adjuntar estilos a una id. Puede dificultar la sobrescritura de ese estilo con otra cosa.
- Si apuntas a un elemento con una lista de selección , será bastante difícil de sobrescribir con otro CSS.
	```css
		a .my-class .another-class[href]:hover {

		}
	```
	Para ayudar a que tu CSS sea más reutilizable, es una buena idea mantener tus selectores lo más simples posible. Usa la especificidad como una herramienta para llegar a los elementos cuando lo necesites, pero siempre considera refactorizar listas de selectores largas y específicas, si es posible.


#### Origen
El CSS propio no es el único CSS que se aplica a una página. `La cascada tiene en cuenta el origen del CSS.` Este origen incluye la hoja de estilo interna del navegador, los estilos agregados por las extensiones del navegador o el sistema operativo y el CSS creado propio.

Siendo del menos específico al más específico:
- Estilos base de agente de usuario. 
	`Estos son los estilos que tu navegador aplica a los elementos HTML de forma predeterminada.`
- Estilos de usuarios locales. 
	`Estos pueden provenir del nivel del sistema operativo, como un tamaño de fuente base o una preferencia de movimiento reducido. También pueden provenir de extensiones de navegador, como una extensión de navegador que permite al usuario escribir su propio CSS personalizado para una página web. */`
- CSS creado propio.
- Los `!important` creados.
	`Cualquier !important que agregues a tus declaraciones creadas.`
- Estilos de usuarios locales `!important`. 
	`Cualquier !important que provenga del nivel del sistema operativo o del nivel de extensión del navegador CSS.`
- Agente de usuario `!important`. 
	`Cualquier !important que se define en el CSS predeterminado, proporcionado por el navegador.`

#### Importancia
El orden de importancia, de menor a mayor, es el siguiente:
- Regla normal, `como font-size , background o color`
- Regla de animation
- Regla de !important `siguiendo el mismo orden que el origen`
- Regla de transition
		Los tipos de reglas de transition (transición) y animation (animación) tienen más importancia que las reglas normales. En el caso de las transiciones, es más importante que los tipos de reglas !important. Esto se debe a que cuando una animación o transición se activa, su comportamiento esperado es cambiar el estado visual. 

### PENDIENTE FORMATEAR



```css

El body suele venir con un margen predeterminado indeseado, se resetea la prop con margin: 0;

Height y width son medidas del contenido.

Propiedades del background:
	Background-image: url('######')
	
	Background-size: siempre se usa después de la prop. background
	Valor= Cover -- La foto se adapta al ancho del fondo de pantalla
	Valor= Auto -- Mantiene el tamaño original de la imagen
	
	Orden abreviatura Background: 
			color urlImagen repeat ubicar(eje x) ubicar(eje y) / bckgrsizeX bckgrsizeY
				* Siempre se debe ubicar de manera independiente el height del elemento

Overflow: ; -- Valor= (visible, hidden, scroll)
	Define como se verá un elemento que supera el tamaño de boxmodel que tiene a su disposición
	
Outline: ; borde externo al borde normal, mismos valores que la propiedad border

Propiedades del texto:
	Text-decoration: ; -- (línea debajo, a traves o arriba del texto)

	Text-shadow:  CorrimientoDerecha CorrimientoInferior Blur ColorSombra;
			Establece una sombra para el texto con los respectivos valores a definir
			/*Aplicable un sistema similar con la prop box shadow pero para divs. Usado para que parezca que se levanta en evento hover. Ejemplo:
			.div {
				transition: box-shadow 0.3s 
			.div:hover {
				box-shadow: DespDerecha DespAbajo Blur ColorSombra;
				cursor: pointer;
			}*/

	*Google fonts*

Propiedades de los links: 
El selector sedesigna como a: *estado del link* {}

Se debe respetar el siguiente orden para establecer dichos formatos
	a:link {} /*Sin visitar el sitio*/
	a:visited {} /*Sitio ya visitado*/
	a:hover {} /*Cursor del mouse sobre el link*/
	a:active {} /*Link siendo clickeado*/

Propiedades de las listas:    
	list-style-type: ; -- Define si es con puntos o numeros, etc
	list-style-position: ; (inside- Ubica la señalética de la lista dentro del margen del contenido)

Propiedades de tablas:
	Selector aplicable
		table, th, td {
		}
	Puede figurar un doble borde corregible con la propiedad en el selector table
		border-collapse: collapse;
	Combinas dos celas para un contenido con la propiedad
		colspan="número de celdas a combinar horizontamente"
		rowspan="número de celdas a combinar verticalmente"
	
	Selector usual
	table{}
	th,td{}
	
	Esimportante que el orden en el colocamos los selectores con sus seudoclases se respete ya que sino se desestimaran algunas
		:nth-child() => :hover
	
	Darle propiedades a filas o columnas en función de si se encuentran en una posición par o impar u otros parametros con la seudoclase de tr nth-child()
		tr:nth-child(valor)
			Los valores pueden ser odd (par) even (impar)

	Ver cambio de color cuando estemos sobre una celda y el ícono del dedo en el cursor
		tr:hover {
			background-color: valor;
			cursor: pointer;
		}

Propiedad de display:
		#ejemplo {
			display: block; /*Valor predeterminado, el elemento ocupa todo el ancho*/
			display: inline; /*Valor de la etiqueta span, reduce el tamaño del elemento al del contenido.
			No se le podra asignar la propiedad de width ni de height al lemento*/
			display: none; /*Desaparece el elemento, resultado identico a la prop: visibility:hidden; */
			display: inline-block; /*Similar a inline pero permite manipular ancho y alto de los elementos. Usualmente usado en los menus de navegación para darles uniformidad*/
		}

Propiedad para variar ancho:
		max-width: ; -- solo define el ancho maximo pero puede ser menos.
		Width: min-content; el ancho del elemento es el mínimo necesario

Propiedad para posicionar elementos:
		article {
			position: static; /*Valor predeterminado*/
			position: relative; /*Relativa a donde debiese estar posicionado este elemento, lo ubica a donde vos desees*/
			left: distancia a moverse desde la izquierda; 
			top: idem prop left;
			/*Estas dos propiedades pueden encimar elementos, existiendo tambien right y bottom*/
			position: fixed; /*Posición con respecto a lo que nosotros deberiamos estar viendo en el ordenador, se fija el elemento en la pantalla*/ 
			position: absolute; /*Se posiciona relativo a la etiqueta padre más cercana que tenga*/
			position: sticky; /*Mezcla entre relative y fixed*/
		}

Propiedad para hacer flotar elementos de html dentro del documento:
		Ubica los elementos con la propiedad en la ubicación que desees y los demas elementos en el lado contrario acomodandose con respecto al definido con float, en especial si recibe propiedades de ancho y alto. Aplica a divs.
		div.left {
			float: left;
		}
		div.right {
			float: right;
		}
	Permite alinear elementos uno al lado del otro si se les aplica la misma propiedad de float

Valores de Propiedades Padding y Margin:
	Propiedad: DespArriba DespDerecha DespAbajo DespIzquierda;
	Propiedad: DepArriba DespLaterales DespAbajo;
	Propiedad: DespVerticales DespLaterales;
	Propiedad: DespGeneral;

Centrar un elemento 
	Indicarle siempre un ancho menor al 100%. Centrará el elemento y no el contenido.
	p {
		width: 200px;
		margin: 0 auto;
	}
	Para el verticar se recurre al padding: DespVertical 0;

Propiedad Transión de css
	Requiere una propiedad definida por un evento que empiece y termine, un tiempo y un algoritmo para desarrollarlo. Se ubica en el selector principal.

	Ejemplo el evento puede ser hover, la propiedad cualquiera dentro del mismo, y el algoritmo ease.


/*

Para centrar algo se utiliza adentro del style="text-align:center"

ejemplo
<p style="text-align:center">Parrafo</p>


Para cambiar el color del fondo se utiliza style="background-color:un color"

ejemplo, si queremos cambiar el fondo de un div, ponemos:
<div style="background-color="yellow>
	<p>Parrafo</p>
</div>
el fondo del div es amarillo




<SELECTORES>


Universales= *
Para seleccionar todos los elementos se pone un selector universal "*"
ejemplo
* {
	color: red;
}
en este caso, selecciona todas las propiedades y las pinta de un color





DE TIPO= elementos

Para seleccionar un elemento en específico ponemos el selector de tipo
ejemplo
h1 {
	color: red;
}
En este caso, selecciona solo la propiedad que queremos y la pinta de rojo


De clase

Se le agrega a una etiqueta de html la palabra class=""
Luego, en CSS, para seleccionar los que sean de clase se pone: .nombre de clase

ejemplo

Supongamos que decidimos ponerle un class al h2
quedaría en HTML
<h2 class="Subtítulo">Subtítulo</h2>
en CSS
.Subtítulo{ 
	color: red;
}

Esto sirve por el caso en el que tengamos muchos <p> por ejemplo, que seleccione los que queramos


De ID

Se le agrega a una etiqueta de HTML la palabra id=""
Luego en CSS, para seleccionarlo, se pone: #nombre de id

ejemplo
supongamos que decidimos ponerle un id al h2
quedaría en HTML
<h2 id="subtitulo">Subtítulo</h2>
en CSS
#subtitulo{
	color:green;
}

Esto sirve para seleccionar de forma más específica que la de class


DE ATRIBUTO

Se le agrega a una etiqueta de HTML un atributo cualquiera, por ejemplo Messi="el goat"
Luego en CSS, para seleccionarlo se pone: [Messi="el goat"]

ejemplo
supongamos que decidimos ponerle un atributo="algo" al button
quedaría en HTML
<button Messi="el goat">Seguinos para más información</button>
en CSS
[Messi="el goat"] {
	color:purple;
}

Esto tiene la misma función que el id



De PSEUDO CLASE


El elemento hover sirve para que cuando alguien tenga el mouse sobre una palabra, se pueda poner de un color

 p:hover{
	color: red;
}

en este caso cuando el mouse este en el párrafo, este se va a ver en rojo




<ESPECIFICIDAD>

Cuando se pone 2 veces un selection, siempre va a mostrar el ultimo

ejemplo

p{
	color: red;
}

p{
	color:blue;
}

En este caso, el parrafo va a ser azul en vez de rojo, porque fue lo ultimo


En el caso que pongamos un título y adentro una clase en HTML, si en CSS ponemos:

HTML:
<h2 class="color-rojo">Hola</h2>

CSS:
.color-rojo{
	color:red;
}

h2{
	color:blue;
}

En este caso, el subtítulo "hola" se va a ver en rojo, porque es más específico


Tambien se pueden hacer con los atributos o id, pero si hay un class y un atributo por ejemplo, será el ultimo el color

En el caso que haya un id y un class, se toma el id


En el caso que haya un style, se coloca directo en el HTML y se pone como style="" como si fuese un atributo
El style le gana a todo,
ejemplo
<h2 class="color-rojo" atributo="color-verde" id="color-violeta" style="color:yellow"></h2>
el subtitulo sera amarillo no importa en que orden este


!IMPORTANT:

el !important es lo que le gana literalmente a todo
ejemplo
<h1 style="color:red">Hola mundo</h1>

pero en CSS ponemos
h1{
	color:blue !important;
}
va a ser azul si o si



<METODOLOGIA BEM>

ejemplo, si en HTML ponemos esto

	<div class="form">
		<h2 class="form-h2">Preguntas?</h2>
			<p class="form-h2-p">Contactanos</p>
	</div>

en CSS, si quiero cambiar el color del div, pongo
.form{
	color:red;
}
en este caso, todo lo que está en el div, se cambia a color rojo

si quiero cambiar el color del h2, pongo
.form-h2{
	color:blue;
}
se cambia a azul

en el caso del p
.form-h2-p{
	color:yellow;
}
se cambia a amarillo



<UNIDADES>

Ya vimos la própiedad color,
font.size sirve para cambiar el tamaño de la letra

ejemplo
h2 {
	font-size: 30px
}
en este caso, cambia la letra del h2 a 30px(pueden ser px,mm,cm o pt)


además de px o cm, están los em, que su valor default es 16px
pero nosotros lo podemos cambiar con el contenedor, ejemplo

.h2{
	font-size:20px; 
}
.h2-p{
	font-size:2em;
}
en este caso, 1em vale 20px, y el párrafo va a valer 40px porque es 2em



Los viewports, son para personalizar una cantidad de pantalla que queremos editar

Se utiliza adentro de un selection por ejemplo
.class{
	background-color:#000;
	height:50vh;
	width:50vw;
}
dentro del height se pone cualquier numero y vh
dentro del width se pone cualquier numero y vw
en este ejemplo, un cuarto de la pagina va a ser negro



<PROPIEDADES DE TEXTO>

La propiedad font-family se utiliza para cambiar la tipografía del texto
ejemplo
.class{
	font-family: georgia;
}


La propiedad font size viene por defecto de 16px.

Podemos representar el color rojo con el nombre red, el hexadecimal #FF0000 y el RGB rgb(255,0,0)
