# Introducción
**Temario**
- [comentarios](#comentarios)
- La consola.
- Naiming.
## comentarios
Es la parte dentro de mi arcivo de codigo que noleído ni ejecutado por el interprete de `js`.
> [!TIP]
> Los comentarios nos ayudan a entender nueestro codigo, y en ocacionea¿s podemos usarlo para silenciar temporañmente partes del codigo *(comentar un código)*.
### Tipos de comentarios
**Una sola línes**
```js
/*
comentario de una sola línea
*/
```
**Multiples líneas**
```js
/*
comentario de multi linea
*/
```
**Js Doc**
```js
/**
*este es una linea
*esta es otra linea
*/
```
E ste tipo de comentario es muy usado para documentar el código, generalmente usado para la explicación




## Consola
la herramienta de javascript mas 


### Tipos de mensajes por consola
#### 1. Notificaciones
mostrar un mensaje por consola
```js
console.log("hola mundo")
```
Mostrar un menaje de estilo informativo
```js
console.info("mensaje informativo")
```
Mostrar un mensaje de estilo o tipo alerta
```js
console.warn("mensaje de tipo alerta")
```
Mostrar un mensaje de estilo o tipo error
```js
console.error("mensaje error")
```
#### 2. Gestion de tiempo
este tipo de mensaje nos sirve para ver la duracion de ejecucion de nuestro
codigo y por optimizaro para hacer uso de esta herramienta
tenemos que iniciar la consola con un `time()` luego vendra el codigo 
que deseamos ver la duracion y finalmente terminar el time de la consola con `timeEnd()`
```js
console.time(" inicio de tiempo")

edad=18
if(edad >=18){
    console.log("eres mayor de edad")
}else{
    console.warn("eres pulpin")
}
console.timeEnd("fin del tiempo")
```
#### 3. Tablas