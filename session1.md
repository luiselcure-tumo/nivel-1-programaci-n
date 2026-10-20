# Clase 1

## ¿QUE ES LA PROGRAMACION?

---

La programación está fuertemente relacionada con los datos.

### todo buen programa realizan 3 acciones: 
 1. aceptar datos, 
 2. procesar o manipular los datos y 
 3. regresar los datos.

esto se ve a grande y pequeña escala, en el desarrollo de un sofware siempre se piden datos como; el nombre, 
el dni, la dirección, o los datos de pago. En pequeña escala el manejo de datos lo podemos ver en las funciones
o en los objetos, etc... 

---

## ¿QUÉ ES JAVASCRIPT?

- De los lenguajes más populares.
- Es un lenguaje interpretado, funciona en el navegador.
- No es igual a Java, son muy diferentes.
- Es un Archivo de texto .js que maneja unas reglas especiales.

---

## ¿QUÉ ES UNA VARIABLE?


Es un espacio de almacenamiento, que nos permite guardar información de diferentes tipos. Podemos pensar en una variable como cajas de mudanza con diferentes etiquetas para poder reconocer que tipo de objetos tiene dentro, los cuáles vamos a llamar "valores".

```javascript


let name = "Narek"
let age = 11
let age2= "11"

age2 + 1
```

1. Declaración (El Acto):

La declaración es el momento en que le avisas al lenguaje de programación que vas a necesitar un espacio 
en la memoria para guardar un dato. Es como "registrar" la existencia de la variable.

En código: Es el uso de palabras como let, const o var.
Volviendo al ejemplo de antes, es como prepararnos para la mudanza y armar las cajas con los nombres de lo que llevara adentro, por ejemplo: la caja "ropa", "cocina" o "escritorio".



2. Anuncio (El Alcance) relacionado con el término técnico Hoisting o el Scope)

El anuncio (a menudo relacionado con el término técnico Hoisting o el Scope) se refiere a cómo y dónde 
se da a conocer la variable al sistema. Es la visibilidad de la variable. Determina si una variable 
puede ser usada en todo el programa o solo dentro de una pequeña función.


SCOPE GLOBAL: Si una variable es declarada en el ámbito global, puede ser accedida desde cualquier 
parte del programa.

let a = 0; // scope global, se puede usar en cualquier parte del programa


SCOPE LOCAL: Si una variable es declarada dentro de una función, solo puede ser accedida 
dentro de esa función.

```Javascript 

function pruebaB(){
    let b = 1; // scope local, solo se puede usar dentro de esta función
}


console.log(a); // Esto funciona porque 'a' es global
console.log(b); // Esto no funciona porque 'b' es local a la función 'pruebaB()'

```

3. Nombre o Identificador

Es muy importante saber nombrar un variable, El nombre debe ser descriptivo. 

- Se pueden usar caracteres del alfabeto latino en mayúscula y minúscula.
- Se pueden usar números.
- Se pueden usar los símbolos _ y $.
- No se puede iniciar el nombre de la variable con un número.
- No puede tener espacios.

Ejemplos de nombres de variables

```Javascript
let a = 0;
let _a;
let $a;
let #a;
let 3a;
let a a;

```

### ¿Qué nombres son adecuados para una variable?



4. El dato (El Contenido)
El valor es el dato real, la información que está guardada dentro de la variable en un momento dado.

Tipos: Puede ser un número (15), un texto ("Hola"), un booleano (true) o incluso algo más complejo 
como un array o un objeto.


EJEMPLO DE DECLARACION DE UNA VARIABLE CON DECLARACION, ANUNCIO, NOMBRE Y DATO:

```Javascript
let a = 15
```

let : Es la instrucción que le dice al lenguaje qué tipo de "contenedor" se va a crear, en este caso una variable
que  puede cambiar su valor más adelante.
a :  Es el nombre de la variable.
= :  En JS el signo = no es igual, es un operador de asignación, lo que esta en la derecha se guarda a lo que esta
     en la izquierda
15:  Es el dato real que se quiere almacenar. En este caso, es un dato numérico entero .
---

## TIPOS DE DATOS QUE GUARDAS LAS VARIABLES 

Variables Simples o de tipo primitivo son los valores más básicos y son inmutables.

Number: Números de cualquier tipo (enteros o decimales). Ejemplo: 15 o 3.14.
let numero = 23;

String: Cadenas de texto. Siempre van entre comillas. Ejemplo: "Hola Mundo".
let nombre = "Pedro";

Boolean: Valores lógicos. Solo pueden ser true (verdadero) o false (falso).
let esMayor = false;

---

## VARIABLES Y OPERADORES ARIMÉTICOS

¿Qué son los operadores aritméticos?

+
-
*
/
```Javascript
let numero1 = 5; 
let numero2 = 7;


console.log(numero1+numero2)
console.log(numero1-numero2)
console.log(numero1*numero2)
console.log(numero1/numero2)


```
---

## FUNCIONES PREDETERMINADAS EN JAVASCRIPT

FUNCIÓN alert()
Esta es una función integrada a JavaScript que crea un cuadro de diálogo con un mensaje.

```Javascript
alert("Hola Mundo")


FUNCIÓN prompt()
// Esta función toma una entrada del usuario y la asigna a una variable.

let edad = prompt("cual es tu edad");
console.log("Hola mi edad es: " + edad);


FUNCIÓN console.log()
// Esta función se utiliza para imprimir informacion por consola

let centroDeEstudio = "TUMO";    
console.log(centroDeEstudio);


FUNCIÓN parseInt():
// Esta función convierte un valor de cadena en un número entero.
```
1. El usuario ingresa datos (con prompt siempre llegan como texto)

let entradaUsuario = "25"; 
let edadActual = 5;

2. Si intentamos sumar directamente:
console.log(entradaUsuario + edadActual); // Resultado: "255" (Mal, los concatenó)

3. Usamos parseInt para convertir el texto en un número real
let numeroConvertido = parseInt(entradaUsuario);

4. Ahora la operación matemática funciona correctamente

```Javascript
let total = numeroConvertido + edadActual;

console.log(total); // Resultado: 30 (¡Correcto!)


FUNCIÓN parseFloat():
// Esta función convierte un valor de cadena en un número de coma flotante o con decimal.

let precioTexto = "19.99"; // Viene como String
let impuesto = 1.15;      // 15% de impuesto

// 1. Usamos parseFloat para mantener la precisión

let precioDecimal = parseFloat(precioTexto);
console.log(precioDecimal); // Resultado: 19.99

// 2. Ahora la operación es correcta
let totalConImpuesto = precioDecimal * impuesto;
console.log(totalConImpuesto.toFixed(2)); // Resultado: 22.99


```
---
## ESTRUCTURA CONDICIONAL O DE CONTROL IF-ELSE

La estructura if es, básicamente, el "cerebro" de tu código. Es lo que permite que tu programa 
tome decisiones en lugar de solo seguir una lista de pasos como una receta de cocina.

En la vida real es como si tu mama de dice... "Si terminas la tarea, entonces puedes jugar videojuegos."
Es como dar otra opcióna tu programa.

Como se escribe 
```Javascript
if (condición) {
  // El código que se ejecuta si la condición es real
}
```
- La palabra if: Es el comando de inicio.
- Los paréntesis ( ): Adentro va la "pregunta" o condición.
- Las llaves { }: Son como una cajita. Todo lo que metas ahí dentro solo pasará si la condición se cumple.

Ejemplo

Imagina que estamos programando un juego y queremos saber si el jugador tiene suficientes monedas para 
comprar una poción que cuesta 10 monedas.
```Javascript
let misMonedas = 15;

if (misMonedas >= 10) {
  console.log("¡Compra exitosa! Tienes tu poción.");
}

// El plan B el Else

// 🎮 La lógica del "Si pasa esto... si no, haz esto otro"

// if
// El if (Si...): Es la condición. Si la condición es verdadera (True), el código entra en ese bloque.
// Ejemplo: if (¿tienes la llave?) -> Acción: Abrir puerta.

// else
// El else (Si no...): Es el "Plan B". Si la condición del if fue falsa (False), el código salta directamente aquí.
// Ejemplo: else -> Acción: Tocar el timbre.

// Ejemplo

let hambre = false;

if (hambre == true) {
    console.log("¡A comer pizza! 🍕");
} else {
    console.log("Sigue jugando videojuegos. 🎮");
}

```
---
## TAREA SESION 1: CREAR UN CHAT BOOT CON TODO LO VISTO EN CLASE

Crear un Chat Boot 🤖

```Javascript
let nameUser = prompt("¿Hola, cual es tu nombre?");
alert("Es un placer conocerte " + nameUser + ", espero que te encuentres muy bien");
let edadUser = parseInt(prompt("¿En que año naciste?"));

edad = 2026 - edadUser;

if (edad <= 14) {
    alert(edad + " Es una gran edad para aprender programación, felicitaciones")
}
else {
    alert("Genial, con " + edad + " seras un gran programador que ayude al mundo")
};

let saberMas = prompt("¡te gustaria contarme mas de ti?");

if (saberMas == "si") {
    alert("Genial, ahora mira la consola del navegador")
    console.log("Me encantaría saber todo sobre ti 🤗🥳")
}
else {
    alert("Te entiendo, algunos días preferimos guardar silencio, igual te dejo un regalo, mira la consola del navegador")
    console.log("Eres una gran persona, y espero que todos tus sueños se hagan realidad 🎈✨, te queremos mucho y en TUMO 🧡🧡🧡 y estamos muy orgullosos de ti por llegar hasta esta etapa, éxitos tu puedes... 🥰🫶")
};

```
