# INDICE
- [INDICE](#indice)
- [FUNCIONES](#funciones)
  - [Estructura de una funcion (como se crea una funcion)](#estructura-de-una-funcion-como-se-crea-una-funcion)
  - [Tipos de Argumentos y Parametros](#tipos-de-argumentos-y-parametros)
    - [Argumentos y parametros posicionales](#argumentos-y-parametros-posicionales)
    - [Argumentos y parametros Nominales](#argumentos-y-parametros-nominales)
  - [Tipos de funciones por su notacion](#tipos-de-funciones-por-su-notacion)
  - [Funcioenes como valor](#funcioenes-como-valor)
    - [funcion como declaracion](#funcion-como-declaracion)
    - [Funcion de flecha(arrow function)](#funcion-de-flechaarrow-function)
    - [Diferencias](#diferencias)
# FUNCIONES
Las funciones en javascript son `bloques de codigo ejecutable`, a los que podemos pasar parametros y operar con ellos.
Nos sirve para modular (modularizar) nuestro programa y estructurarlos en bloques que `realicen una tarea concreta`, de esta manera nuestro codigo es mas legible y mantenible.
Las funciones normalmente, al acabar su ejecucion `devuelven un valor`, que conseguimos con el parametro `return`.

## Estructura de una funcion (como se crea una funcion)
para crear una funcion debemos realizar los siguientes pasos:
1. hacer uso del keyword `function`.
2. darle normbre a la funcion
3. crear los parametros que recibira entre parentesis `()`.
4. crear el cuerpo de la funcion `{}`.
```js
//funcion sin parametros, lleva parentesis igual
function miFuncion(){
    console.log("esta es mi funcion")
}
//funcion con un parametro
function miFuncionParametros(texto){
    console.log("tu parametro es", a)
}
//funcion con varios parametros
function funcionVariosParametros(a,b,c){
    console.log(a + b + c)
}
```
**¿como ejecutamos una funcion**
Para ejecutar una funcion debemos ahcer el llaamdo de la misma, haciendo uso unicamente de su nombre y los parametros que recibira.
```js
//crear funcion
function saludo(){
    console.log("hola")
}
//ejecutar funcion
saludo()
// o
dunction salu2(texto){
    console.log("hola: ", texto)
}
//ejecutar
salu2("jory")
```
> [!NOTE]
> ** Reglas para poner el nombre a una funcion** -
Los nombres de las funciones deben representar acciones por lo que deben construirse usando el `verbo` que representa la accion seguido de un `sustantivo` representara a la entidad.
```js
function crearUsuario(){

}
function enviarCorreo(){

}
```
## Tipos de Argumentos y Parametros
Es la manera como se remplaza los argumentos con los parametros
### Argumentos y parametros posicionales
Se les llama posicionales por que los argumentos tomara los parametros en el orden que se le pase a la funcion, segun la posicion entre argumento y parametro.
```js
function sumaNumeros(a,b,c,d){
    let suma=a+b+c+d
    return suma
}
//argumentos posicionales
let respuesta=sumaNumeros(1,2,3,4)
console.log(respuesta)
//a toma el valor de 1 y asi sucesivamente en el orden que corresponda
```
### Argumentos y parametros Nominales
Se les llama nominales se les conoce a los argumentos que en su creacion se asocian a un parametro en especifico.
```js
//nominal
function registroAlumno(nombre,apellido,sexo){
    let respuesta=`${nombre},${apellido},${sexo}`
    return respuesta
}
registroAlumno(sexo="primo",nombre="edwin",apellido="del mar")
//posicional
registroAlumno("jory", "rodriguez", "todos los dias")
```
> [!INFO]
> Posicionales en orden y Nominales especificar el parametro y su valor.

## Tipos de funciones por su notacion
## Funcioenes como valor
en este caso se crea una funcion como si fuera el valor de un enlace.
```js
let saludo=function(){
    console.log("bienvenido")
}
saludo()
```
en este caaso el no,bre de la funcion sera el nombre que le pongamos al enlace y para llamarlo o ejecutarlo debemois poner el nombre del enlace mas los parentesis.
al igual que una funcion clasica podemos tambien pasarle parametros
### funcion como declaracion
se le conoce como funcion `declarativa` a la manera clasica de como creamos una funcion.
```js
function saludo(){
    return "saludos a todos"
}
console.log(saludo())
```
### Funcion de flecha(arrow function)
esta funcion es introducida a partir de la version de ecma script 5
`es5`.
se implemento para la creacion y ejecusion rapida y mas entendible de las funciones.
la funcion flecha evita la `verbosidad` en jvascript
> [!NOTE]
> `verbosidad`o`verboso` se utiliza en la programacion para referirse a un codigo que necesita demaciadas lineas de codigo o necesitas cumplir estrictamente una serie de reglas podemos comprar la `verbosidad` a un texto demaciado extenso o redundante.
se crea de la misma manera que una funcion como valor, eso quiere decir que la funcion flecha sera el valor de un enlace.
la funcion flecha tiene la siguiente estructura.
el parametro seguido del simbolo flecha `=>` y del cuerpo de ser necesario o solo de codigo que se retornara
```js
function saludo(){
    return "hola mundo"
}
console.log(saludo())

let saludo=()=>("hola mundo")
console.log(saludo())

let mensaje=texto=>console.log("hola,"texto)
console.log(mensaje("el primo"))
//en el caso de tener mas de un paarametro y ejecutar mas de una sola linea de codigo
let registroUsuario=(nombre,apellido)=>{
    let alumno=`${nombre}, ${apellido}`
    return alumno
}
console.log(registroUsuario("edwin","cachondo"))
```
### Diferencias

