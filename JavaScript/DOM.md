# DOM

## DOM (Document Object Model) en JavaScript

El DOM es una representación de la estructura de un documento HTML que permite a JavaScript acceder y manipular los elementos en la página web.

### getElementByClassName

El método `getElementByClassName` se utiliza para seleccionar elementos en el DOM que tienen una clase específica. Devuelve una colección de elementos HTML que coinciden con la clase proporcionada.

```jsx
const elementos = document.getElementsByClassName("nombre-de-clase");
```

Ejemplo de uso:

```html
<div class="nombre-de-clase">Elemento 1</div>
<div class="nombre-de-clase">Elemento 2</div>
```

```jsx
const elementos = document.getElementsByClassName("nombre-de-clase");
```

### getElementById

El método `getElementById` se utiliza para seleccionar un elemento en el DOM por su ID único. Devuelve el elemento que tiene el ID especificado.

```jsx
const elemento = document.getElementById("mi-id");
```

Ejemplo de uso:

```html
<div id="mi-id">Elemento con ID único</div>
```

```jsx
const elemento = document.getElementById("mi-id");
```

### querySelector

El método `querySelector` permite seleccionar el primer elemento que coincida con un selector CSS especificado. Devuelve el primer elemento que cumple con el criterio de selección.

```jsx
const elemento = document.querySelector("selector-css");
```

Ejemplo de uso:

```html
<div class="clase">Elemento 1</div>
<div id="mi-id">Elemento 2</div>
```

```jsx
const elemento = document.querySelector(".clase"); // Selecciona el primer elemento con la clase "clase"
```

### querySelectorAll

El método `querySelectorAll` se utiliza para seleccionar todos los elementos que coincidan con un selector CSS especificado. Devuelve una colección de elementos que cumplen con el criterio de selección.

```jsx
const elementos = document.querySelectorAll("selector-css");
```

Ejemplo de uso:

```html
<div class="clase">Elemento 1</div>
<div class="clase">Elemento 2</div>
```

```jsx
const elementos = document.querySelectorAll(".clase"); // Selecciona ambos elementos con la clase "clase"
```

## Manipulación de Estilos con JavaScript

La manipulación de estilos con JavaScript implica cambiar o modificar las propiedades de estilo de un elemento HTML directamente a través de JavaScript. Esto te permite controlar la apariencia de tus elementos en respuesta a eventos o condiciones específicas.

### Cambiar Propiedades de Estilo

Puedes cambiar propiedades de estilo como color de texto, fondo, tamaño de fuente, margen, etc., utilizando JavaScript. Para hacerlo, primero seleccionas el elemento al que deseas aplicar los cambios y luego accedes a sus propiedades de estilo.

```jsx
const elemento = document.getElementById("mi-elemento");
elemento.style.color = "red";
elemento.style.backgroundColor = "yellow";
elemento.style.fontSize = "20px";
```

En el ejemplo anterior, estamos seleccionando un elemento con el ID "mi-elemento" y cambiando su color de texto a rojo, su fondo a amarillo y su tamaño de fuente a 20 píxeles.

### Agregar o Quitar Clases CSS

Otra forma común de manipular estilos es agregar o quitar clases CSS de un elemento. Esto es especialmente útil cuando tienes estilos definidos en hojas de estilo CSS separadas.

```jsx
const elemento = document.getElementById("mi-elemento");
elemento.classList.add("nueva-clase");
elemento.classList.remove("clase-antigua");
```

En este ejemplo, estamos agregando una nueva clase llamada "nueva-clase" al elemento y eliminando una clase llamada "clase-antigua". Esto permite cambiar el aspecto del elemento según las reglas de estilo definidas en el CSS.

## Generación de HTML con JavaScript

La generación de HTML con JavaScript implica crear elementos HTML dinámicamente y agregarlos al DOM en tiempo de ejecución. Esto es útil cuando deseas agregar contenido o elementos de forma dinámica en respuesta a eventos o datos.

### Crear Elementos

Puedes crear elementos HTML utilizando el método `document.createElement()` y luego configurar sus atributos y contenido antes de agregarlos al DOM.

```jsx
const nuevoElemento = document.createElement("div");
nuevoElemento.textContent = "Nuevo elemento";
```

En este ejemplo, hemos creado un nuevo elemento `div` y le hemos asignado un contenido de texto.

### Agregar Elementos al DOM

Una vez que hayas creado un elemento, puedes agregarlo al DOM utilizando métodos como `appendChild()` o `insertBefore()`.

```jsx
const contenedor = document.getElementById("contenedor");
contenedor.appendChild(nuevoElemento);
```

Aquí, estamos agregando el elemento `nuevoElemento` como un hijo del elemento con el ID "contenedor".

```html
<html lang="en">
<body>
 <!--Elementos-->
<div class="contenedor"></div>
<script>
//Creamos el elemento y lo asignamos
const parrafo = document.createElement('p');
//Añadimos contenido
parrafo.textContent = 'Grupo Bien Pensado'
//Seleccionamos el elemento donde insertaremos
const contenedor = document.querySelector('.contenedor');
//Inyectamos el párrafo creado anteriormente
contenedor.appendChild(parrafo);
</script>
</body>
</html>
```

La generación de HTML con JavaScript es útil para crear componentes dinámicos, como listas, tablas o elementos de formulario, en función de datos o eventos en tu aplicación web.

En resumen, la manipulación de estilos con JavaScript te permite cambiar dinámicamente la apariencia de elementos HTML, mientras que la generación de HTML con JavaScript te permite crear y agregar elementos HTML al DOM en tiempo de ejecución, lo que es útil para la construcción dinámica de contenido web.