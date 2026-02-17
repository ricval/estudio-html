# 26 - Trabajando con Elementos Semánticos de Texto y Tiempo

## ¿Cómo funcionan las citas en bloque e _inline_ en HTML?

En HTML, los elementos citados se usan para distinguir el texto citado del contenido circundante.
Si la fuente de la cita tiene una dirección, puedes citarla con el atributo `cite`.
```html
<blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
  "Can you imagine what it would be like to be a successful developer? To have built software systems that people rely upon?"
</blockquote>
```
Este elemento tiene un atributo `cite`. El valor del atributo `cite` es la URL de la fuente.

Si quieres atribuir la fuente visualmente, puedes agregar un elemento de cita, `cite`, fuera del elemento de cita en bloque.
 El elemento de cita es un elemento HTML que puedes usar para marcar el título de una obra creativa referenciada como un libro, artículo, canción, película, sitio web o trabajo de investigación. Aquí tienes un ejemplo:
```html
<div>
  <blockquote cite="https://www.freecodecamp.org/news/learn-to-code-book/">
    Can you imagine what it would be like to be a successful developer? To have built software systems that people rely upon?
  </blockquote>
  <p>—Quincy Larson, <cite>How to Learn to Code and Get a Developer Job [Full Book].</cite></p>
</div>
```

A veces solo necesitarás citar unas pocas palabras dentro de un párrafo más grande. Eso es exactamente para lo que sirve el elemento de cita en línea.
```html
<p>
  As Quincy Larson said,
  <q cite="https://www.freecodecamp.org/news/learn-to-code-book/">
    Momentum is everything.
  </q>
</p>
```
 No habrá cambios visuales, pero proporcionará a los lectores de pantalla y motores de búsqueda más información sobre la cita.


## ¿Cómo se muestran las abreviaturas en HTML?

Una abreviatura es una forma abreviada de una palabra o frase. Por ejemplo, "Dr" seguido de un punto, es una abreviatura de la palabra "doctor".

Hay dos formas comunes de abreviaturas:
  1. **acrónimos**: Un acrónimo es una palabra formada a partir de las iniciales de una frase, donde cada letra representa la primera letra de una palabra en esa frase.
  2. **inicialismos**: Son muy útiles para escribir texto más conciso, especialmente cuando son bien conocidos y fáciles de entender en un contexto determinado.

La diferencia es que los acrónimos se pronuncian como palabras y las siglas se pronuncian como letras individuales.

```html
<p><abbr title="HyperText Markup Language">HTML</abbr> is the foundation of the web.</p>
```

El atributo `title` es opcional, pero si decides incluirlo, debe ser una descripción legible para humanos de la abreviatura, acrónimo o sigla.

Aunque no es necesario usar el elemento de abreviatura para cada abreviatura en tu página web, se recomienda para aquellas que podrían ser confusas y para las que podrían necesitar contexto adicional.


## ¿Cómo se muestran las direcciones en HTML?

El elemento de dirección de contacto se utiliza para representar información de contacto para una sección de una página web. El elemento `address` es versátil y se puede usar para páginas de negocios, páginas de autores, sitios personales y más.

```html
<address>
  <h2>Company Name</h2>
  <p>
    1234 Elm Street<br />
    Springfield, IL 62701<br />
    United States
  </p>
  <p>Phone: <a href="tel:+15555555555">+1 (555) 555-5555</a></p>
  <p>Email: <a href="mailto:contact@company.com">contact@company.com</a></p>
</address>
```

Para el número de teléfono, tenemos un elemento de anclaje con el valor `href` configurado para números de teléfono. El valor `tel:+` dentro del atributo `href` crea un enlace clicable para iniciar una llamada telefónica en ciertos dispositivos que soportan eso.

Para la dirección de correo electrónico, se usa otro elemento anchor con el valor de `href` configurado en un enlace `mailto`. Los enlaces `mailto` se usan en documentos HTML para permitir que los usuarios abran un nuevo correo electrónico en su cliente de correo preferido.

### ¿Cuál es un inconveniente de usar enlaces mailto?

Estos enlaces son un objetivo de spammers para enviar correos electrónicos a los usuarios.


## ¿Cómo se muestran las horas y fechas en HTML?

El elemento `time` se utiliza para representar un momento específico en el tiempo.

```html
<p>The reservations are for <time datetime="20:00">20:00 </time></p>
```

El atributo `datetime` se utiliza para traducir fechas y horas a un formato legible por máquina.

Esto es importante porque ayuda con los resultados de los motores de búsqueda y ayuda al navegador a procesar la información de fecha y hora de manera más efectiva.

```html
<p>
  The graduation will be on <time datetime="2024-06-15T15:00">June 15</time>
</p>
```

Siempre que necesites representar eventos, fechas de publicación o citas, es mejor utilizar el elemento `time`.
