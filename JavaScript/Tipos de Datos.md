# Tipos de Datos

JavaScript es un lenguaje de programación de tipado dinámico, lo que significa que no es necesario declarar explícitamente el tipo de dato de una variable antes de usarla. Los tipos de datos en JavaScript se dividen en dos categorías principales:

1. **Tipos de Datos Primitivos:**
    - `number`: Representa números, ya sean enteros o decimales.
    - `string`: Representa texto.
    - `boolean`: Representa un valor verdadero (`true`) o falso (`false`).
    - `undefined`: Representa un valor no definido.
    - `null`: Representa la ausencia de valor o un valor nulo.
    - `symbol` (nuevo en ECMAScript 6): Representa un valor único e inmutable que se puede usar como clave de propiedad de objetos.
    - `bigint` (nuevo en ECMAScript 11): Representa números enteros grandes.
2. **Tipos de Datos Compuestos:**
    - `object`: Representa una colección de pares clave-valor.
    - `array`: Representa una lista ordenada de valores.
    - `function`: Representa una función.
    - `date`: Representa una fecha y hora.
    - `regexp`: Representa una expresión regular.

## Métodos de Cadena (String)

Las cadenas (strings) son un tipo de dato primitivo en JavaScript que representan texto. A continuación, se describen algunos métodos comunes que se pueden usar con cadenas:

### 1. `length`

- **Descripción:** El método `length` se utiliza para obtener la longitud (número de caracteres) de una cadena.
- **Sintaxis:** `cadena.length`
- **Ejemplo:**
    
    ```jsx
    const texto = "Hola, mundo";
    const longitud = texto.length; // longitud será igual a 11
    ```
    

### 2. `includes()`

- **Descripción:** El método `includes()` verifica si una cadena contiene otra cadena como subcadena y devuelve un valor booleano.
- **Sintaxis:** `cadena.includes(subcadena)`
- **Ejemplo:**
    
    ```jsx
    const frase = "JavaScript es genial";
    const contieneJava = frase.includes("Java"); // contieneJava será igual a true
    ```
    

### 3. `startsWith()`

- **Descripción:** El método `startsWith()` verifica si una cadena comienza con cierta subcadena y devuelve un valor booleano.
- **Sintaxis:** `cadena.startsWith(subcadena)`
- **Ejemplo:**
    
    ```jsx
    const texto = "Hola, mundo";
    const comienzaConHola = texto.startsWith("Hola"); // comienzaConHola será igual a true
    ```
    

### 4. `endsWith()`

- **Descripción:** El método `endsWith()` verifica si una cadena termina con cierta subcadena y devuelve un valor booleano.
- **Sintaxis:** `cadena.endsWith(subcadena)`
- **Ejemplo:**
    
    ```jsx
    const texto = "Hola, mundo";
    const terminaConMundo = texto.endsWith("mundo");  // terminaConMundo será igual a true
    ```
    

### 5. `replace()`

- **Descripción:** El método `replace()` reemplaza una subcadena en una cadena con otra subcadena especificada.
- **Sintaxis:** `cadena.replace(subcadena_a_reemplazar, nueva_subcadena)`
- **Ejemplo:**
    
    ```jsx
    const mensaje = "Hola, amigo";
    const nuevoMensaje = mensaje.replace("amigo", "amiga"); // nuevoMensaje será igual a "Hola, amiga"
    ```
    

### 6. `slice()`

- **Descripción:** El método `slice()` extrae una porción de una cadena y la devuelve como una nueva cadena.
- **Sintaxis:** `cadena.slice(inicio, fin)`
- **Ejemplo:**
    
    ```jsx
    const texto = "JavaScript";
    const subcadena = texto.slice(0, 4); // subcadena será igual a "Java"
    ```
    

### 7. `substring()`

- **Descripción:** El método `substring()` extrae una porción de una cadena y la devuelve como una nueva cadena. A diferencia de `slice()`, no admite índices negativos.
- **Sintaxis:** `cadena.substring(inicio, fin)`
- **Ejemplo:**
    
    ```jsx
    const texto = "JavaScript";
    const subcadena = texto.substring(4, 7); // subcadena será igual a "Scr"
    ```
    

### 8. `repeat()`

- **Descripción:** El método `repeat()` crea y devuelve una nueva cadena que contiene la cadena original repetida el número de veces especificado.
- **Sintaxis:** `cadena.repeat(veces)`
- **Ejemplo:**
    
    ```jsx
    const palabra = "Hola";
    const repetida = palabra.repeat(3); // repetida será igual a "HolaHolaHola"
    ```