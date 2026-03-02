# 43 - Trabajando con Tablas y Formularios Accesibles

## ¿Cuáles son las mejores prácticas para tablas y accesibilidad?

 La primera mejor práctica que cubriremos es el uso de leyendas (`caption`) para las tablas.  Con ello puedes escribir la leyenda (o título) de una tabla. Para que puedan comprender rápidamente el propósito y contenido de la tabla.

 Debes colocar el elemento `caption` inmediatamente después de la etiqueta de apertura del elemento `table`. De esta manera, los lectores de pantalla y otras tecnologías de asistencia pueden ofrecer más contexto anunciando primero la leyenda antes de leer el contenido.

 ```html
 <table>
  <caption>Nuestras Mascotas</caption>
  <!-- Tabla con Rows y Columns -->
</table>
 ```

```html
<table>
  <caption>Nuestras Mascotas</caption>
  <thead>
    <tr>
      <!-- Encabezados de Columnas -->
      <th>Nombre</th>
      <th>Edad</th>
      <th>Tipo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th>Nora</th> <!-- Encabezado del Renglón -->
      <td>5</td>
      <td>Perro</td>
    </tr>
    <tr>
      <th>Gino</th> <!-- Encabezado del Renglón -->
      <td>2</td>
      <td>Gato</td>
    </tr>
  </tbody>
</table>
```
Observa que el código anterior tiene un elemento `caption` inmediatamente después del elemento `table`. Luego, dentro del elemento `thead` del encabezado de la tabla, están los encabezados de columna (Nombre, Edad, y Tipo). En la segunda y tercera filas, dentro del elemento `tbody`, encontramos los datos de cada una de nuestras mascotas. Los nombres de las mascotas son los encabezados de fila porque están dentro de los elementos de encabezado de tabla (`th`).

El atributo `scope` determina si un encabezado es un encabezado de fila o de columna. El atributo `scope` tiene cuatro valores posibles. Los dos valores que usarás más a menudo son `col` para columna y `row` para fila.
```html
...
<thead>
    <tr>
      <!-- Ahora tienen un atributo scope -->
      <th scope="col">Nombre</th>
      <th scope="col">Edad</th>
      <th scope="col">Tipo</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <th scope="row">Nora</th>
      <td>5</td>
      <td>Dog</td>
    </tr>
    ...
```


## ¿Por qué es importante que los elementos de entrada tengan una etiqueta asociada?

Los lectores de pantalla a menudo dependen de las etiquetas para describir el propósito de los campos de entrada. Para que esto funcione correctamente, la etiqueta debe estar asociada programáticamente con el `input`. Aunque hay varias formas de hacer eso, la más común es usar el elemento HTML `label`.

```html
<form>
   <label for="name">Tu Nombre</label>
   <input type="text" id="name" />
</form>
```

En este ejemplo, el atributo `for` del elemento `label` está asociado con el `id` del elemento `input`. Esta conexión permite a los lectores de pantalla anunciar la `label` cuando el `input` está en un estado enfocado, permitiendo a los usuarios de lectores de pantalla entender el propósito del `input`.
