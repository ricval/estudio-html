# Capítulo 02: Fundamentos HTML #

## 02.01 - Estructura de un Documento HTML ##

### 02.01.01 - Estructura de un Documento ###

HTML que significa (_Hypertext Markup Language_) Lenguaje de Marcado de Hipertexto. Sirve como columna vertebral del contenido web. Se utiliza para especificar la estructura y organizar la información en la web. Es fundamental conocerlo para crear una estructura bien diseñada y páginas web accesibles.

#### La Declaración de `<!DOCTYPE>` ####

Es la primer línea en un documento HTML. Informa al navegador que versión de HTML va ha utilizarse y ayuda al navegador a _renderizar_ correctamente la página. Para indicar el uso de HTML5 se declara así: `<!DOCTYPE html>`

#### Estructura Básica de un Documento HTML ####

Un documento HTML consiste en dos secciones principales: el `<head>` y el `<body>`.
La sección `<head>` contiene los metadatos y links a recursos externos, mientras que el `<body>` contiene la parte visible de la página web.

```html
<!DOCTYPE html>
<html>
    <head>
        <title>Título de la página</title>
        <!-- Otros elementos del head como meta datos y links a CSS van aquí -->
    </head>
    <body>
        <!-- El contenido de tu página web va aquí -->
    </body>
</html>
```

#### Comentarios HTML ####

Los comentarios proveen a los desarrolladores una forma de añadir notas o explicaciones dentro del código sin afectarlo. Los comentario s comienzan con `<!--` y terminan con `-->`.

### 02.01.02 - Esqueleto de un Documento HTML ###

#### Elementos `<html>`, `<head>` y `<body>` ####

Son la columna vertebrar de un documento HTML, definen la estructura y contenido.
El elemento `<html>` sirve como raíz de un documento HTML. Encapsula el contenido completo, por lo general contiene dos elementos hijo: `<head>` y `<body>`.

El elemento `<head>` contiene los metadatos del documento, como el título, la codificación, los links a hojas de estilo y _scripts_. No tiene un impacto visual directo en la presentación, pero juega un papel crucial en la definición de como se procesará el documento.

```html
<head>
    <title>Título del Documento</title>
    <meta charset="utf-8">
    <!-- otros metadatos -->
</head>
```

La etiqueta `<title>` define el título que se verá en la pestaña del navegador.
La etiqueta `<meta charset="utf-8">` especifica que la codificación del documento se hará con UTF-8.

El elemento `<body>` contiene el contenido del documento, incluye texto, imágenes, enlaces y otros elementos que contribuyen a la parte visible de la página web.

```html
<body>
    <h1>Bienvenido a Mi Sitio Web</h1>
    <p>Este es un ejemplo de un párrafo.</p>
    <!-- Más contenido puede ir aquí -->
</body>
```

#### Etiquetas Meta para Información del Documento ####

Las etiquetas `<meta>` proveen información acerca del documento, influenciando como será procesado por los navegadores y los motores de búsqueda.

### 02.01.03 - Elementos y Etiquetas HTML ###

Cada elemento consiste en una etiqueta de inicio, contenido y una etiqueta de cierre. Ejemplo:

```html
<p>Este es un párrafo.</p>
```

Aquí, la etiqueta de inicio es: `<p>`, "Este es un párrafo." es el contenido, y `</p>` es la etiqueta de cierre. Los elementos pueden ser anidados dentro de cada uno, creando una estructura de jerarquía.

#### Etiquetas Comunes HTML ####

Encabezados:
Los encabezados definen la estructura jerárquica de un documento, van de `<h1>` para el encabezado principal hasta el `<h6>`.

Listas:
Las listas organizan la información con `<ul>` (_unordered list_) listas desordenadas y `<ol>` (_ordered list_) listas ordenadas. Los items de las listas se declaran con `<li>`.

```html
<ul>
    <li>item 1</li>
    <li>item 2</li>
</ul>

<ol>
    <li>Primero</li>
    <li>Segundo</li>
</ol>
```

Enlaces:
Los hipervínculos utilizan la etiqueta `<a>`, que enlaza a recursos externos o internos.

```html
<a href="https://www.ejemplo.com">Enlace de ejemplo</a>
```

Imágenes:
Las imágenes son embebidas utilizando la etiqueta `<img>`, especificando la fuente y el texto alternativo.

```html
<img src="imagen.jpg" alt="Descripción de la imagen">
```

#### Anidando y Jerarquía en HTML ####

Anidar elementos dentro unos de otros crear una jerarquía, definiendo la relación entre las diferentes partes del contenido. Ejemplo:

```html
<article>
    <h1>Título del Articulo</h1>
    <p>Introducción al articulo.</p>
    <img src="articulo-imagen.jpg" alt="Imagen del articulo">
</article>
```

En este ejemplo, `<h1>`, `<p>` y `<img>` están anidados dentro del elemento `<article>`.

## 02.02 - Formateando Texto y Multimedia ##

### 02.02.01 - Encabezados y Párrafos ###

Los encabezados son cruciales para la organización del contenido jerárquico. HTML ofrece seis niveles de encabezados que va desde `<h1>` el mayor hasta `<h6>` el menor.
Los encabezados no solo definen la estructura del contenido sino que también juegan un papel importante en el rol del SEO, ayudando a los motores de búsqueda a entender la jerarquía y la relevancia de la información.

#### Párrafos (Etiqueta `<p>`) ####

Presentan contenido en un formato legible. La etiqueta `<p>` es utilizada para definir los párrafos, permitiendo la separación y claridad dentro del documento.

#### Saltos de línea (Etiqueta `<br>`) ####

Mientras que los párrafos introducen un nuevo bloque de texto, los saltos de línea son empleados para pequeños cortes dentro del texto. La etiqueta `<br>` es una etiqueta auto-cerrada que inserta un salto de línea.

### 02.02.02 - Etiquetas para Formatear Texto ###

El formateo de texto es crucial para el aspecto del HTML que mejora la presentación visual del contenido en la página web.

#### Negritas `<strong>` e Itálicas `<em>` ####

Son etiquetas de énfasis que resaltan el texto dentro de un documento:

- `<strong>`: Es utilizado para representar importancia y seriedad.
- `<em>`: Enfatiza el texto, normalmente se ve en itálica.

#### Subrayado `<u>`y Tachado `<s>` ####

- `<u>`: Es empleado para subrayar el texto.
- `<s>`: Es para texto que ya no es relevante o es marcado para ser borrado.

#### Subíndice y Superindice ####

- `<sub>`: Es para subíndice, comúnmente encontrado en matemáticas y formulas químicas.
- `<sup>`: Es utilizado para exponentes o pie de notas.

### 02.02.03 - Trabajando con Imágenes y Videos ###

Enriquecen la experiencia de usuario.

#### Etiqueta `<img>`para imágenes ####

Embebe imágenes en la página web.
Atributos de la etiqueta `<img>`:

  1. `src` (_source_) fuente: Este atributo especifica la URL fuente de la imagen. Puede ser relativa o absoluta.
  2. `alt` (_alternate text_) Texto Alternativo: Provee un texto para cunado la imagen no puede ser desplegada o falla su carga, se utiliza para propósitos de accesibilidad.
  3. `width` y `height`: El ancho y la altura definen las dimensiones de una imagen en pixeles.
  4. `style`: El estilo, permite en-línea dar estilo CSS para ajustar la apariencia de una imagen.

Buenas prácticas:

- Siempre provee de un texto alternativo `alt` para accesibilidad y el SEO.
- Optimiza las imágenes para la web, comprimídnoslas sin perder tanta calidad.
- Utiliza formatos apropiados (JPEG para fotografías, PNG para transparencias, y SVG para logos).

#### Embeber Videos con la etiqueta `<video>` ####

Mientas que las imágenes mejoran el aspecto visual, los videos elevan el aspecto interactivo.

Atributos de la etiqueta `<video>`:

  1. `src` _source_ fuente: Designa la url fuente del video, siendo una ruta relativa o absoluta.
  2. `controls`: Añade controles de reproducción, permitiendo al usuario: reproducir, pausar y ajustar el volumen.
  3. `width` y `height`: Determinan las dimensiones dentro de la página web.
  4. `autoplay`: Habilita la reproducción automática cuando la página se cargue.
  5. `loop`: Hace que el video se reproduzca continuamente.

Buenas prácticas:

- Elige formatos de video apropiados (MP4, WebM, Ogg).
- Optimiza los archivos de video para balancear la calidad y el tiempo de carga.
- Provee subtítulos para accesibilidad.

### 02.02.04 - Embebiendo Audio ###

#### Etiqueta `<audio>` para archivos de audio ####

Los elementos multimedia juegan un rol de enriquecimiento de la experiencia de usuario.
La etiqueta acepta multiples atributos, entre ellos el de `src` para especificar la fuente del recurso. Los formatos de audio compatibles de la mayoría de navegadores son: MP3, OGG y WAV.
El atributo `controls` ofrece una interfaz de reproducción y control de volumen. Además el contenido dentro de la etiqueta `<audio>Mensaje</audio>` sirve para desplegar un mensaje cuando el navegador no soporta el elemento de audio.

Atributos:

  1. `src` _source_ fuente: Designa la url fuente del audio, siendo una ruta relativa o absoluta.
  2. `controls`: Añade controles de reproducción, permitiendo al usuario: reproducir, pausar y ajustar el volumen.
  3. `autoplay`: Habilita la reproducción automática cuando la página se cargue.
  4. `loop`: Hace que el video se reproduzca continuamente.
  5. `preload`: Determina cuando el audio debería cargarse. Si utilizas el atributo `autoplay` este atributo se ignora.
     1. `none`: No se descarga hasta que el usuario hace clic en el reproductor.
     2. `metadata`: Solo descarga los metadatos, como cuantos minutos dura la pista.
     3. `auto`: Se descarga el archivo una vez que la página termina de cargar.

## 02.03 Hipervínculos y Navegación ##

### 02.03.01 - Creando Hipervínculos ###

Los hipervínculos permiten al usuario navegar entre diferentes secciones o páginas. Se utiliza la etiqueta `<a>`.

Atributos de la etiqueta `<a>`:

- `href`: Especifica la URL de destino.
- `target`: Define como será abierto el enlace.
  - `_blank`: En otra pestaña o ventana.
- `title`: Provee información adicional acerca del enlace, cuando el usuario pasa sobre él.

Enlaces a secciones internas:
Utilizando la etiqueta de anclaje, puedes enlazar a diferentes secciones de la misma página.

```html
<a href="#seccion_01">Salta a la sección 1</a>
...
<h2 id="seccion_01">Sección 1</h2>
```

### 02.03.03 - Menús de Navegación ###

Proveen al usuario de una estructura intuitiva de navegar a través del sitio web.

En **HTML Semántico** se utiliza la etiqueta `<nav>` para encapsular el menú de navegación, indicando su propósito tanto al navegador como a la tecnología utilizada. También se utiliza una estructura de lista, ya sea ordenada `<ol>` o desordenada `<ul>`, con cada elemento representado con `<li>`. Cada item tiene una etiqueta de enlace con `<a>`.
