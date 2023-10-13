# Estructuras de Control

## Bucles en JavaScript

### 1. **Bucle `for`**

El bucle `for` se utiliza para ejecutar un bloque de código un número específico de veces. Tiene tres partes esenciales: inicialización, condición y actualización.

```jsx
for (inicialización; condición; actualización) {
  // Código a ejecutar en cada iteración
}
```

Ejemplo de un bucle `for` que cuenta del 1 al 5:

```jsx
for (let i = 1; i <= 5; i++) {
  console.log(i); // Imprime los números del 1 al 5
}
```

### 2. **Bucle `while`**

El bucle `while` se utiliza para ejecutar un bloque de código mientras una condición sea verdadera.

```jsx
while (condición) {
  // Código a ejecutar mientras la condición sea verdadera
}
```

Ejemplo de un bucle `while` que cuenta del 1 al 5:

```jsx
let i = 1;
while (i <= 5) {
  console.log(i); // Imprime los números del 1 al 5
  i++;
}
```

### 3. **Bucle `do-while`**

El bucle `do-while` es similar al bucle `while`, pero garantiza que el bloque de código se ejecute al menos una vez antes de verificar la condición.

```jsx
do {
  // Código a ejecutar al menos una vez
} while (condición);
```

Ejemplo de un bucle `do-while` que solicita un número al usuario hasta que ingrese un número mayor o igual a 5:

```jsx
let numero;
do {
  numero = parseInt(prompt("Ingrese un número mayor o igual a 5:"));
} while (numero < 5);

console.log("Número válido: " + numero);
```

### 4. **Bucle `for...in`**

El bucle `for...in` se utiliza para recorrer las propiedades de un objeto. Itera sobre todas las propiedades enumerables de un objeto.

```jsx
for (variable in objeto) {
  // Código a ejecutar para cada propiedad del objeto
}
```

Ejemplo de un bucle `for...in` que recorre las propiedades de un objeto:

```jsx
const persona = {
  nombre: "Juan",
  edad: 30,
  ciudad: "Madrid"
};

for (let propiedad in persona) {
  console.log(propiedad + ": " + persona[propiedad]);
}
```

### 5. **Bucle `for...of`**

El bucle `for...of` se utiliza para recorrer elementos de estructuras de datos iterables, como arrays y cadenas de texto.

```jsx
for (elemento of iterable) {
  // Código a ejecutar para cada elemento del iterable
}
```

Ejemplo de un bucle `for...of` que recorre los elementos de un array:

```jsx
const numeros = [1, 2, 3, 4, 5];

for (let numero of numeros) {
  console.log(numero); // Imprime los números del array
}
```

## Método `forEach`

El método `forEach` se utiliza para iterar sobre cada elemento de un array y ejecutar una función proporcionada en cada uno de esos elementos. No modifica el array original y no devuelve un nuevo array. Su sintaxis es la siguiente:

```jsx
array.forEach(function(elemento, índice, arreglo) {
  // Código a ejecutar para cada elemento
});
```

- `elemento`: El valor del elemento actual en el array.
- `índice`: El índice del elemento actual en el array.
- `arreglo`: El array sobre el cual se está iterando.

Ejemplo de uso de `forEach` para imprimir los elementos de un array:

```jsx
const frutas = ["manzana", "plátano", "naranja"];

frutas.forEach(function(fruta, indice) {
  console.log(`Índice ${indice}: ${fruta}`);
});
```

Este código imprimirá:

```
Índice 0: manzana
Índice 1: plátano
Índice 2: naranja
```

## Método `map`

El método `map` se utiliza para crear un nuevo array a partir de otro array al aplicar una función a cada elemento del array original. La función recibe cada elemento del array y debe retornar el valor que se colocará en el nuevo array. El array original no se modifica. Su sintaxis es la siguiente:

```jsx
const nuevoArray = array.map(function(elemento, índice, arreglo) {
  // Código a ejecutar para cada elemento
  return nuevoValor;
});
```

- `elemento`: El valor del elemento actual en el array.
- `índice`: El índice del elemento actual en el array.
- `arreglo`: El array sobre el cual se está iterando.

Ejemplo de uso de `map` para duplicar cada elemento en un array:

```jsx
const numeros = [1, 2, 3, 4, 5];

const duplicados = numeros.map(function(numero) {
  return numero * 2;
});

console.log(duplicados); // Resultado: [2, 4, 6, 8, 10]
```

En este ejemplo, `map` crea un nuevo array llamado `duplicados` que contiene los valores originales multiplicados por 2.

Es importante destacar que `map` devuelve un nuevo array y no modifica el array original.

Ambos métodos, `forEach` y `map`, son útiles para trabajar con arrays en JavaScript, pero se utilizan en diferentes situaciones. `forEach` es adecuado cuando solo necesitas iterar sobre los elementos y realizar acciones en cada uno de ellos, mientras que `map` es útil cuando deseas crear un nuevo array transformando los elementos del array original.