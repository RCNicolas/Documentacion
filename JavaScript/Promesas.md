# Promesas

Es una acción asíncrona que espera a qeu una acción se complete o finalice, cuando esta accción es finalizada se toma una acción dependiendo  y depende si fue finalizada correctamente o no.
Las promesas al ser asíncronas son asignadas a una pila de trabajo especial de JavaScript y hasta que se termine todo el código síncrono se ejecutará la promesa.

## Sintaxis

```jsx
const promesa = new Promise((resuelta, rechazada) => {
//Código asíncrono
})
```

Las promesas tienen tres metodos posibles:

| Metodo | Descripción  |
| --- | --- |
| promesa.thne() | Se utiliza para decirle que hacer si la promesa se resuelve correctamente. |
| promesa.catch() | Se utiliza para decirle que hacer si la promesa se NO resuelve correctamente. |
| promesa.finally() | Se utiliza para decirle que hacer una vez se termine la compilación de la promesa. |

## Funcionamiento de las promessa

1. **Creación de una promesa**: Puedes crear una promesa usando el constructor `Promise`. El constructor toma una función que recibe dos argumentos, `resolve` (para resolver la promesa) y `reject` (para rechazarla). Dentro de esta función, puedes realizar operaciones asincrónicas y llamar a `resolve` cuando la operación se complete correctamente o a `reject` cuando se produzca un error.

```jsx
const Promesa = new Promise((resolve, reject) => {
  // Realizar una operación asincrónica
  if (operacionExitosa) {
    resolve(valor);
  } else {
    reject(razon);
  }
});
```

1. **Manejo de promesas**: Puedes utilizar los métodos `.then()` y `.catch()` para manejar el resultado de una promesa:
    - `.then()`: Se llama cuando la promesa se resuelve con éxito y recibe el valor resuelto como argumento.
    - `.catch()`: Se llama cuando la promesa es rechazada y recibe la razón del rechazo como argumento.

```jsx
Promesa
  .then((valor) => {
    // Manejar la promesa resuelta
    console.log('Promesa resuelta:', valor);
  })
  .catch((razon) => {
    // Manejar la promesa rechazada
    console.error('Promesa rechazada:', razon);
  });
```

1. **Encadenamiento de promesas**: Puedes encadenar múltiples `.then()` para realizar operaciones secuenciales o transformaciones en el valor resuelto:

```jsx
Promesa
  .then((valor) => {
    // Realizar operación con el valor resuelto
    return transformar(valor);
  })
  .then((resultadoTransformado) => {
    // Realizar más operaciones
    console.log('Resultado transformado:', resultadoTransformado);
  })
  .catch((razon) => {
    // Manejar el rechazo en cualquier punto de la cadena
    console.error('Promesa rechazada:', razon);
  });
```

### Ejemplo

Se crea una promesa que se cumple o no basado en un valor booleano que se asigna manualmente.

Las promesas son una forma poderosa y flexible de manejar la asincronía en JavaScript y son ampliamente utilizadas en la programación moderna en el lado del cliente y del servidor.

```jsx
onst aprobar = true;
//Creamos la promesa
const promesa = new Promise((resuelta, rechazada) => {
setTimeout(() => {
if (aprobar) {
resuelta(); //resolver
} else {
rechazada(); //rechazar
}
}, 2000);
});
//Estados de la promesa
promesa
.then(() => console.log("La promesa se cumplió"))
.catch(() => console.log("La promesa no se cumplió"))
.finally(() => console.log("La promesa finalizó"))
```