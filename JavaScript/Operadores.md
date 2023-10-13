# Operadores

### Operadores Aritméticos

Los operadores aritméticos se utilizan para realizar operaciones matemáticas en números:

- **Suma (+):** Se utiliza para sumar dos valores.
    
    ```jsx
    const suma = 5 + 3; // suma será igual a 8
    ```
    
- **Resta (-):** Se utiliza para restar el valor de la derecha del valor de la izquierda.
    
    ```jsx
    const resta = 8 - 3; // resta será igual a 5
    ```
    
- **Multiplicación (*):** Se utiliza para multiplicar dos valores.
    
    ```jsx
    const multiplicacion = 4 * 6; // multiplicacion será igual a 24
    ```
    
- **División (/):** Se utiliza para dividir el valor de la izquierda por el valor de la derecha.
    
    ```jsx
    const division = 12 / 4; // division será igual a 3
    ```
    
- **Módulo (%):** Devuelve el resto de la división entre dos valores.
    
    ```jsx
    const modulo = 10 % 3; // modulo será igual a 1
    ```
    

### Operadores de Cadena

Los operadores de cadena se utilizan para concatenar cadenas de texto:

- **Concatenación (+):** Se utiliza para unir dos cadenas.
    
    ```jsx
    const cadena1 = "Hola, ";
    const cadena2 = "mundo!";
    const saludo = cadena1 + cadena2; // saludo será igual a "Hola, mundo!"
    ```
    

### Operadores de Comparación

Los operadores de comparación se utilizan para comparar valores y devolver un valor booleano (`true` o `false`):

- **Igual (==):** Compara si dos valores son iguales, sin tener en cuenta el tipo de dato.
    
    ```jsx
    const igualdad = 5 == "5"; // igualdad será igual a true
    ```
    
- **Igual estricto (===):** Compara si dos valores son iguales, teniendo en cuenta el tipo de dato.
    
    ```jsx
    const igualdadEstricta = 5 === "5"; // igualdadEstricta será igual a false
    ```
    
- **Distinto (!=):** Compara si dos valores no son iguales, sin tener en cuenta el tipo de dato.
    
    ```jsx
    const diferencia = 5 != "5"; // diferencia será igual a false
    ```
    
- **Distinto estricto (!==):** Compara si dos valores no son iguales, teniendo en cuenta el tipo de dato.
    
    ```jsx
    const diferenciaEstricta = 5 !== "5"; // diferenciaEstricta será igual a true
    
    ```
    
- **Mayor que (>):** Compara si un valor es mayor que otro.
    
    ```jsx
    const mayor = 8 > 4; // mayor será igual a true
    ```
    
- **Menor que (<):** Compara si un valor es menor que otro.
    
    ```jsx
    const menor = 3 < 7; // menor será igual a true
    ```
    
- **Mayor o igual que (>=):** Compara si un valor es mayor o igual que otro.
    
    ```jsx
    const mayorOIgual = 5 >= 5; // mayorOIgual será igual a true
    
    ```
    
- **Menor o igual que (<=):** Compara si un valor es menor o igual que otro.
    
    ```jsx
    const menorOIgual = 2 <= 1; // menorOIgual será igual a false
    ```
    

### Operadores Lógicos

Los operadores lógicos se utilizan para realizar operaciones lógicas en valores booleanos:

- **AND lógico (&&):** Devuelve `true` si ambos operandos son `true`.
    
    ```jsx
    const andLogico = true && false; // andLogico será igual a false
    ```
    
- **OR lógico (||):** Devuelve `true` si al menos uno de los operandos es `true`.
    
    ```jsx
    const orLogico = true || false; // orLogico será igual a true
    ```
    
- **NOT lógico (!):** Invierte el valor booleano.
    
    ```jsx
    const notLogico = !true; // notLogico será igual a false
    ```
    

### Operador Condicional Ternario

El operador condicional ternario (`? :`) es una forma concisa de escribir una expresión condicional:

```jsx
const edad = 20;
const mensaje = edad >= 18 ? "Eres mayor de edad" : "Eres menor de edad";
// Si la edad es mayor o igual a 18, mensaje será igual a "Eres mayor de edad"
// De lo contrario, mensaje será igual a "Eres menor de edad"
```