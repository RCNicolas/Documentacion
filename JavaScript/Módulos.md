# Módulos

## Módulos en JavaScript

Los módulos son una característica importante en JavaScript que permite organizar y estructurar el código en aplicaciones más grandes y mantener el código más modular y reutilizable. Los módulos permiten dividir tu programa en piezas más pequeñas, cada una de las cuales tiene su propio ámbito y puede exportar o importar funcionalidades.

## export

La declaración `export` se utiliza para exportar funciones, variables, clases u otros objetos desde un módulo para que estén disponibles para su uso en otros módulos. Puedes exportar elementos individualmente o agruparlos en un objeto.

### Exportar elementos individualmente:

```jsx
// En un archivo llamado miModulo.js

export const variable = 42;

export function sumar(a, b) {
  return a + b;
}
```

### Exportar elementos agrupados en un objeto:

```jsx
// En un archivo llamado miModulo.js

const variable = 42;

function sumar(a, b) {
  return a + b;
}

export { variable, sumar };
```

## import

La declaración `import` se utiliza para importar funcionalidades desde otros módulos en tu programa. Puedes importar elementos individuales o importar un objeto que contenga múltiples elementos.

### Importar elementos individualmente:

```jsx
import { variable, sumar } from './miModulo.js';

console.log(variable); // 42
console.log(sumar(5, 7)); // 12
```

### Importar un objeto que contiene elementos:

```jsx
import * as miModulo from './miModulo.js';

console.log(miModulo.variable); // 42
console.log(miModulo.sumar(5, 7)); // 12
```

## export default

La declaración `export default` se utiliza para exportar un solo valor, función o clase como la exportación predeterminada de un módulo. Cada módulo solo puede tener una exportación predeterminada.

### Exportar una exportación predeterminada:

```jsx
// En un archivo llamado miModulo.js

const valor = 42;

export default valor;
```

### Importar la exportación predeterminada:

```jsx
import valor from './miModulo.js';

console.log(valor); // 42
```