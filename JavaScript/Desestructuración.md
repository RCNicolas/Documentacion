# Desestructuración

la desestructiración es una expresiín la cual permite extraer las propiedades de un objeto obteniendo su valor y dejando una variable asignada al mismo tiempo .

## Sintaxys

```jsx
const {atributos} = objeto;  
```

### Ejemplo

```jsx
const Empresa = {
	nombre: "Grupo bien pensado",
	ciudad: "Bucaramanga",
	direcccion: {
		valor: "Zona Franca Santander"
		}
}
```

Normalmente se accederia a los valores de la iguuente manera 

```jsx
console.log(`Nombre: ${Empresa.nombre}`);
console.log(`Ciudad: ${Empresa.ciudad}`);
console.log(`Direccion: ${Empresa.direccion.valor}`)
```

Con la desectructuración seria de la siguiente manera 

```jsx
const { nombre, ciudad, dirección: { valor } } = Empresa;
console.log(`Nombre: ${nombre}`);
console.log(`Ciudad: ${ciudad}`);
console.log(`Direccion: ${valor}`);
```

La salida en consola usando cualquier motodoe seria:

```
Nombre: Grupo Bien Pensado
Ciudad: Bucaramanga
Direccion: Zona Franca Santander
```