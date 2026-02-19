# 28 - Trabajando con elementos semánticos especializados

## ¿Cómo muestras ecuaciones matemáticas y fórmulas químicas en HTML?

### Superíndice
El elemento de superíndice se usa para mostrar un texto como superíndice
```html
<p>2<sup>2</sup> (2 al cuadrado) es 4.</p>
```
<p>2<sup>2</sup> (2 al cuadrado) es 4.</p>

Las letras superiores se refieren a letras escritas en superíndice, generalmente para indicar abreviaturas.

### Subíndice
Para representar ecuaciones químicas dentro de HTML, usarías el elemento subíndice.
```html
<p>CO<sub>2</sub></p>
```
<p>CO<sub>2</sub></p>

Los casos de uso comunes para el elemento subíndice incluyen fórmulas químicas, notas al pie y subíndices de variables.


## ¿Cómo representas el código de computadora en HTML?

### Código
El elemento de código en línea se usa para representar fragmentos cortos de código dentro del texto. Los casos de uso comunes para el elemento de código serían para artículos técnicos y páginas de documentación.

```html
<p>
  Para establecer el texto en color azul en CSS, siga el siguiente código de ejemplo:
  <code>color: blue;</code>
</p>
```

### Preformateado
El elemento de texto preformateado se utiliza para representar texto preformateado. Es para todo un bloque de código y el anterior solo para un fragmento.
```html
<pre>
  <code>
    body {
      color: red;
    }
  </code>
</pre>
```
Al usar el elemento `pre`, necesitarán ser cuidados con los espacios porque se mostrará exactamente como está escrito dentro del documento HTML.

Cuando se trata de incluir ejemplos de código dentro del documento HTML, deberías usar el elemento `code` para ejemplos cortos en línea.

Si necesitas mostrar fragmentos de código más largos, entonces necesitarás usar los elementos `pre` y `code`.


## ¿Para qué se utilizan los elementos U, S y Ruby y cómo funcionan?

### Subrayado
El elemento de anotación no articulada, o elemento `u` para abreviar, sólo debe utilizarse para indicar que se ha aplicado una anotación no textual al texto.

El estilo predeterminado para el elemento `u` es un subrayado negro debajo del texto.

### Tachado
El elemento de tachado, o elemento s para abreviar, debería usarse para representar cuando un texto ya no es preciso ni relevante.

### Ruby
El elemento `ruby` representa texto pequeño que se muestra arriba o debajo del texto principal. Se utiliza principalmente para mostrar la pronunciación de caracteres del este asiático.
