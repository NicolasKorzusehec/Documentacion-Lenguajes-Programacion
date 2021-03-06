[Volver al inicio](./README.md)

```html

html <!--HTML5 hyper text markup language-->
	Lenguaje de Programación computacional que estructura todas las paginas Web en internet.
	
Front End
	Área o aquel equipo de personas que se encargan de la creación de páginas web y de la creación de la interfaz de muchos sistemas entre un usuario, entre el cliente, y el sistema. <!--Toda la interacción en sí que esa persona va a tener con una página web.-->

	Equipo de Front-End
		Programador Front-End
		Responsable por UX (User experience)
		Responsable por UI (User interface)
		Copywriter (Generador de Contenido)
		SEO (Search Engine Optimization)

	Comando útiles:
		Abrir un archivo del ordenador en Google Chrome = Ctrl + O + Seleccionar un archivo. 
		Abrir las herramientas para desarrolladores (Dev Tools) = Ctrl + SHIFT + I.

Para empezar con la creación de una página web, se debe poner la etiqueta <html> y estructurar del siguiente modo:
	<!DOCTYPE html>
	<html>
		<head>
			<title></title>
		</head>
		<body>

		</body>
	</html>

Marcador de posición-lorem ipsum:
	Los desarrolladores web tradicionalmente usan el texto lorem ipsum como texto de marcador de posición. El texto de lorem ipsum se extrae aleatóriamente de un famoso pasaje de Cicerón de la Antigua Roma.

Comentar 
	Es una forma de dejar comentarios para otros desarrolladores dentro de su código sin afectar el resultado que se muestra al usuario final. También es una forma conveniente de desactivar el código sin tener que eliminarlo por completo.
	Los comentarios en HTML comienzan con <!-- y terminan con un -->

Elemento
	<Open tag>´contenido delelemento´</Clossing tag>
		La mayoría de las etiquetas se usan con un open tag y un clossing tag. Solo algunas funcionan unicamente con un open tag llamandose empty tag.

Atributos
	Brindan información extra y van dentro de un tag: href, color, etc.

Etiquetas/tags y Comandos:
	<nombre caracteristica="valor"></nombre>
		Ejemplo=<button color="red" tamaño="grande" borde="negros"></button>

			Botón tag
				<button>´texto en el botón´</button>

			Título/heading tag
				<h1>´texto título´</h1>
				El tamaño de los heading varía en función del valor del tag. h1==>h6

			Párrafo tag
				<p>´contenido del párrafo´</p>
			
			Line break tag
				<br>  Es un empty tag que separa renglones y posición de botones

	doctype
		Le dice al navegador que versión de html uso, sino el navegador decide. Empty tag. 
		<!doctype html>
	
	html 
		Elemento para cear una página web
		<html>
		
		</html>

	body
		Elemento para definir el body de una webpage
		<body>
			
		</body>
	
	head 
		Elemento que contiene información de la webpage. Se ubica antes del body tag.
			<head>

			</head>
		
			Elemento del head==> título
				<title>´título de la webpage´</title>
				Figura en el tab o ventana del navegador

		Ejemplo:
			<html>
				<head>
					<title>
						Prueba
					</title>
				</head>
				<body>
					<h1>My favorite things</h1>
					<p>
						Raindrops on roses <br>
						Whiskers on kittens <br>
						bright coppes kettles <br>
					</p>
				</body>
			</html>

	Estilo de texto-Elementos
		Emfasis tag
			<em>´texto en italic (inclinada)´</em>

		Importante tag
			<strong>´textoen negrita´</strong>

	Link tag 
		Combina Webpages en Websites.
			<a href="URL">´texto linkeado´</a>
		URL: Uniform Resource Locator

			Es un ejemplo en el cual en la página pone un enlace para llevarlo a google.
				<a href="https://google.com" target="_BLANK">Google</a>
			<!--El valor _BLANK de la propiedad target hace que el link se abra en una pestaña nueva y no cambie la actual. Es util por si el usuario cierra la pestaña que emergio pueda seguir navegando en nuestra WebPage.-->

	Personalizar letras
		<b>negrita</b>
		<i>italica</i>
		<strike>tachada</strike>
		<small>chiquita</small>

	Listas
		Utiles para organizar información en una webpage
			List Item <li>´texto del item´</li>
			Desordenada-Items punteados
				<ul>
					<li></li>
				</ul>
			Ordenada-Items numerados
				<ol>
					<li></li>
				</ol>

Multimedia
		Imagen: 
				<img src="URL">		Emptytag. src es un atributo.
				<!--Los atributos para el tag img como width="Ancho" height="Altura" modifican las medidas del recurso multimedia. No es recomendable porque cuando utilizamos CSS no vamos a poder cambiarlo.-->
			Se puede poner una foto de google al inspeccionar, copiar y pegar el enlace, pero si la pagina borra la foto, a nosotros tambien, por lo tanto, la forma segura es guardando la foto en una carpeta y poniendo entre las comillas el nombre de la carpeta.
					De un URL: https://dominio/carpeta/archivo.formato
						https://dominio/ es el nombre de la computadora que guarda el archivo
						carpeta/ es la carpeta donde está el archivo
						archivo.formato es el nombre del archivo
					Para acceder a archivos locales en nuestro dispositivo => /carpeta/archivo.formato
						Usando /img/ accedemos a la carpeta imagenes
			ejemplos
				<img src="messi.jpg">
				<img src="https://media.puntal.com.ar/p/301e2d50496355c01ad7702fd320fce1/adjuntos/270/imagenes/001/460/0001460545/1200x0/smart/messijpg.jpg">

		Video:
			<video src="nombre de carpeta o enlace.formato" controls></video>
				tag completo

		Audio:
			<audio src="nombre de carpeta o enlace.formato" controls></audio>
				tag completo

Imput element y formularios
		Para obtener cualquier tipo de entrada de usuarios: mails, passwords, datos y más. imput tag es un emptytag.
		2 atributos principales: Type y Placeholder.
			<form>
				<input type="entrada del usuario" placeholder="nombre del campo a completar">
			</form>

			Casos
				<input type="text"> entrada de texto
				<input type="password"> entrada de texto oculta en pantalla
				<input type="number">
				<input type="email">
				<input type="color">
				<input type="range" min="" max="">
				<input type="date">
				<input type="time">
				<input type="button" value="boton">
				<input type="submit">
				<input type="checkbox">
			
		El atributo required se utiliza cuando se le obliga al usuario a llenar un "type" antes de enviar.
				por ejemplo
				<form>
					<input type="text" required="">
				</form>

Agrupando elementos
	Los desarrolladores crean grupos de elementos para crear capas unicas para sus websites. Seccionan la webpage y reciben diversos formatos.
			Un Group of elements basico:
					<div></div>
	<!--Los elementos dentro de otros elementos se llaman ´ELEMENTOS ANIDADOS´ o bien ´NESTED ELEMENTS´-->

Metadatos
	Se ubican en el apartado <head></head>
	
	Corrección visual de tildes
		Para que se puedan agregar acentos en la página, y que no aparezca el signo raro, se debe poner la etiqueta <meta> y el atributo "charset" con el  valor ="utf-8"
			Ej.: 
				<head>
					<title>Título</title>
					<meta charset="utf-8">
				</head>

	Asignación de palabras claves para mejor posicionamiento en busquedas de los usuarios en internet:
		<meta name="keywords" content="harina,huevo,leche">
		<!--Considerar desestimación de este criterio por curso ´SEO y Monetización´-->

	Descripción de página:
		<meta name="description" content="esta es una página relacionada con alimentos y sus características">
		<!--Esto figurará en los resumenes debajo de los links de entrada a las Webpage en las búsquedas de Google-->

	Mención del autor:
		<meta name="author" content="Tomás Korzusehec">

	Si hay contenido con copyright:
		<meta name="copyright" content="Nombre de la empresa o página">

Tablas:
Se le  dara formato con css
	<table> 
		<!--Primero se hace una fila con tr (table row).
			Despues las columas y se empieza con los encabezados con th (table head)
			Los th apareceran en negrita-->
		<tr>
			<th>Nombre</th>
			<th>Apellidos</th>
			<th>Email</th>
		</tr>
		<!--Luego se hacen las demas filas con tr y td-->
		<tr>
			<td>Nico</td>
			<td>Korzu</td>
			<td>mail1</td>
		</tr>
		<tr>
			<td>Nico</td>
			<td>Korzu</td>
			<td>mail1</td>
		</tr>
	</table>


<!--	Pendiente revisión y correción:	
Etiqueta NAV
Se encuentra adentro de la etiqueta <body>, pero antes de poner <nav></nav> se debe ponerlo adentro de una etiqueta llamada <header></header>

Se pueden poner por ejemplo 3 enlaces de forma de listas, y cuando el usuario toque una de esas, se llevará a aquella pestaña, pero para eso, se tienen que crear 3 enlaces. para hacer eso se debe hacer:
<header>
	<nav>
		<ul>
			<li><a href="nombre_De_Carpeta_1.html">Primer enlace</a></li>
			<li><a href="nombre_De_Carpeta_2.html">Segundo enlace</a></li>
			<li><a href="nombre_De_Carpeta_3.html">Tercer enlace</a></li>
		</ul>
	</nav>
</header>
Luego de eso, supongamos que el nombre de la actual carpeta se llama index.html, lo primero que hay que hacer es agregar todo lo que queramos que esté en el primer enlace y luego guardarlo.
Luego, para crear la segunda carpeta, se guarda como: y pones el nombre que queres que se llame. supongamos que se llama por ejemplo index2.html, agregamos lo que queremos que esté en el segundo enlace y luego lo guardamos.
Y asi, infitas carpetas al gusto.


Section y Articles

Para generar articulos se debe poner adentro en la parte de <body></body>.
Con las etiquetas 
<article>
	<section>
	</section>
</article>

Adentro de <section></section> pueden ir parrafos o títulos, etc.


<aside></aside> usualmente es información extra que está en un costado, 

Para generar un pie de página, se utiliza la etiqueta <footer></footer>, que usualmente se utiliza para poner enlaces, redes sociales, etc.

Ejemplo general de selection y articulos

<article>
	<section>
		<h1>
			Nuestra página alcanzó las 10.000 visitas
		</h1>
		<h2>
			El sitio Web de alimentación sana alcanza las 10.000 visitas
		</h2>
		<p>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
		tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
		quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
		consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
		cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
		proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</p>
	</section>
</article>
<aside>
	<h2>
		Información extra
	</h2>
	<p>
		Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
		tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
		quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
		consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
		cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
		proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
	</p>
</aside>
<footer>
	<h2>
		Copyright:"......"
	</h2>
	<ul>
		<li><a href="instagram.com">Instagram</a></li>
		<li><a href="facebook.com">Facebook</a></li>

	</ul>
</footer>


Tablas

Para crear una tabla se debe poner la etiqueta <table></table>

para crear una fila se debe poner la etiqueta <tr></tr>
los <td></td> se utilizan adentro de los <tr></tr>

si a la tabla le queremos agregar un borde, tendriamos que poner <table border="1px"></table>

ejemplo

<body>
	<table>
		<tr>
			<td>Nombre</td>
			<td>Apellido</td>
			<td>Edad</td>
			<td>Curso</td>
		</tr>
		<tr>
			<td>Tomás</td>
			<td>Korzusehec</td>
			<td>15</td>
			<td>1°AO</td>
		</tr>

	</table>
</body>


Volviendo a las imagenes, por si no se muestra las imagenes, se pone <img src="foto.jpg" alt="nombre que queremos que aparezca"> es CLAVE para el SEO

La función del atributo title en una imagen es de poner un nombre que aparece cuando el mouse está en la imagen. sería<img src="" alt="" title="">

ejemplo

<img src="messi.jpg" alt="Foto de messi" title="Messi">


Para centrar una imagen o un parrafo o un texto, se utiliza la etiqueta <center>
NO ES RECOMENDABLE


Para omitir un texto largo por ejemplo, debe poner <a href="#Palabra clave"></a>
Esto sirve por ejemplo cuando hay un texto muy largo y el objetivo es omitirlo y llevar al usuario a lo que quiere saber, ya sea un código,etc.

por ejemplo

	<a href="#codigo">Omitir texto</a>
<h1>Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.
Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod
tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam,
quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo
consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse
cillum dolore eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non
proident, sunt in culpa qui officia deserunt mollit anim id est laborum.</h1>
<h2 id="codigo">El Código es: 1737847</h2>



Iconos

Los iconos son lo que están al lado del título de la página

Se coloca adentro de los <head></head>

La etiqueta tendría que tener el atributo rel y el href
y se llamaría link

<link rel="icon" href="nombre_de_imagen.ico">


<input type="" placeholder="">

Cuando queremos que el usuario ponga por ejemplo su nombre, tendríamos que poner adentro de la caja donde tiene que poner su nombre, letras que digan por ejemplo "ingrese su nombre"

ejemplo

<input type="name" placeholder="Ingrese su nombre">

<span></span>
sirve por ejemplo cuando queremos colorear unas palabras en específico
ejemplo
<p>Aquí están mis nenas, ella es <span>eimy</span>, ella es <span>briana</span></p>

Luego en CSS le podemos poner un color a los span por ejemplo



<hr>

Para poner una linea que separe un p y un h2 por ejemplo se pondría

<h2>Subtítulo</h2>
<hr>
<p>Parrafo</p>


<pre></pre>

La etiqueta pre sirve para que el contenido de adentro este en forma de un poema


<sub></sub>
sirve por ejemplo para poner h20
ejemplo

<p>
	h
	<sub>
		2
	</sub>
	o
</p>


Fin del curso HTML