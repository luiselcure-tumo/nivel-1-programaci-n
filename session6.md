# Clase 6: ¡Inventarios, Matemáticas y Robots! 

¡Hola a todos! Hoy daremos un nuevo paso en nuestra aventura de programación. En esta clase, nosotros vamos a recordar cómo guardar nuestros objetos como si fuera un videojuego, jugaremos un poco con las matemáticas mágicas de JavaScript, y aprenderemos a crear pequeños "robots" que trabajen por nosotros. 

Verificamos que todos tengamos nuestro editor de código abierto, la consola lista y... **¡ESTAMOS LISTOS PARA EMPEZAR!** 🚀

---

## Recordemos qué son los Arreglos o Arrays 🎒

Los arrays son contenedores donde podemos almacenar datos de forma ordenada. Imaginen que es como la mochila o el inventario de su personaje en un videojuego: tiene diferentes espacios (o "slots") para guardar espadas, pociones o escudos.

```javascript
// Así creamos nuestro inventario inicial
let miInventario = ["🗡️espada", "🛡️escudo", "🧪poción", "🐴caballo", "📜mapa"];
console.log(miInventario);

// También podemos guardar listas de canciones o números
let misCancionesFavoritas = ["Wish you were here", "Run to the hills", "In the End"];
let arrayDeNumeros = [2, 5, 7, 89, 34, 46, 98];
```

### Herramientas para manipular nuestro Inventario:

JavaScript nos da "poderes" especiales para modificar estas listas:

1. **split(",")**: Corta un texto largo y lo convierte en una lista ordenada.
2. **push()**: Agrega un elemento nuevo al final de la lista.
3. **pop()**: Elimina el último elemento de la lista.
4. **shift()**: Elimina el primer elemento de la lista.
5. **unshift()**: Agrega un elemento nuevo al inicio de la lista.

```javascript
// 1. split(): Cortamos el texto donde haya un punto para hacer una lista
let regaloEnTexto = "josefa. eres una gran persona. todo lo puedes lograr. exitos. pepe";
let nuevosItems = regaloEnTexto.split("."); 
console.log(nuevosItems);

// 2. push(): Agregamos un arco al final del inventario
miInventario.push("🏹arco");

// 3. pop(): Tiramos el último elemento que agregamos (el arco)
miInventario.pop();

// 4. shift(): Se nos cae el primer elemento de la mochila (la espada)
miInventario.shift();

// 5. unshift(): Encontramos una corona y la guardamos en el primer espacio
miInventario.unshift("👑corona");
console.log(miInventario);
```

---

## Funciones Matemáticas Básicas 🧮

A veces necesitamos hacer cálculos, pero no queremos hacerlos mentalmente. ¡Para eso existe el objeto `Math`, que es como nuestra calculadora científica integrada!

```javascript
// 1. Math.round() -> El Redondeador
let precio = 4.7;
let precioFinal = Math.round(precio); // Resultado: 5 (Porque está más cerca del 5)

// 2. Math.sqrt() -> La Raíz Cuadrada
let areaCuadrado = 64;
let lado = Math.sqrt(areaCuadrado); // Resultado: 8 (Porque 8 x 8 = 64)

// 3. Math.abs() -> El Optimizador de Positivos (ignora el signo negativo)
let puntajePerdido = -50;
let modulo = Math.abs(puntajePerdido); // Resultado: 50

// 4. Math.random() -> El Número Loco (lanza un número al azar entre 0 y 1)
let numeroLoco = Math.random(); 
console.log(numeroLoco); // Resultado: Puede ser 0.123456... ¡Siempre cambia!
```

---

## ¡Creando nuestros propios Robots: Las Funciones! 🤖

Sabemos que las funciones son bloques de código que realizan tareas, pero para entenderlo mejor, **pensemos en las funciones como robots o como los NPC (Personajes No Jugables) de un videojuego**. 

Existen robots a los que no necesitamos darles nada para que trabajen, y otros a los que debemos entregarles herramientas (llamadas **argumentos**) para que cumplan su tarea.

### Funciones sin argumentos
El robot sabe exactamente qué hacer sin que le des nada.

```javascript
// Creamos al NPC
function saludarNPC() {
  console.log("¡Hola, aventurero! Bienvenido al juego. ⚔️");
}

// Lo llamamos para que trabaje
saludarNPC(); 
```

### Funciones con argumentos
Los argumentos son los datos o "herramientas" que tú le lanzas al robot para que él los use.

```javascript
// El (nombre) es el argumento, como una etiqueta en blanco que nosotros llenaremos
function saludarPersonalizadoNPC(nombre) {
  console.log("¡Hola, " + nombre + "! Bienvenido al juego. 🌟");
}

// Ahora, cuando lo llamamos, le pasamos el dato:
saludarPersonalizadoNPC("Zelda"); // Resultado: "¡Hola, Zelda!..."
saludarPersonalizadoNPC("Mario"); // Resultado: "¡Hola, Mario!..."
```

### Funciones que devuelven algo (Return) 🎁

Siguiendo con la idea de los robots, la diferencia está en si el robot hace su trabajo y se queda callado (función vacía), o si después de trabajar **vuelve corriendo hacia ti para entregarte un resultado en la mano (return)**.

```javascript
// 1. Funciones que NO devuelven nada
function pintarPared(color) {
  console.log("¡He pintado la pared de color " + color + "!");
  // El robot termina su tarea y se apaga.
}

let resultadoPintura = pintarPared("Azul");
console.log(resultadoPintura); // ¡Saldrá 'undefined'! Porque el robot no te entregó nada.

// 2. Funciones que DEVUELVEN algo (return)
function exprimirNaranjas(cantidad) {
  let jugo = cantidad * 2; // Digamos que cada naranja da 2 chorritos
  return jugo; // <-- LA MAGIA: El robot vuelve y te entrega el jugo
}

// Ahora sí podemos guardar lo que el robot nos entregó en una variable:
let miVaso = exprimirNaranjas(5); 
console.log("Tengo " + miVaso + " chorritos de jugo. 🧃"); // Resultado: 10
```

---

## Tarea: ¡Nuestra Obra de Arte con Triángulos! 🎨

Vamos a utilizar los arreglos (nuestras mochilas de datos), la función `Math.random` (nuestro número loco) y nuestras funciones personalizadas para crear un programa que dibuje triángulos de diferentes tamaños, colores y en diferentes lugares.

```javascript
// --- 1. TAREA: CREAR NUESTROS DEPÓSITOS DE DATOS (ARRAYS) ---
let x = [];
let y = [];
let tamaños = [];
let colores = [];

// --- 2. TAREA: LLENAMOS LOS ARRAYS CON INFORMACIÓN ---
for (let i = 0; i < 100; i++) {
  // Coordenadas al azar entre -350 y 350
  x.push(Math.round(Math.random() * 700 - 350));
  y.push(Math.round(Math.random() * 700 - 350));

  // Tamaños al azar entre 0 y 100
  tamaños.push(Math.round(Math.random() * 100));

  // Colores al azar (asumiendo que tenemos una función randomColor_h disponible)
  let colorAzar = randomColor_h();
  colores.push(colorAzar);
}

// --- 3. CREAMOS LA FUNCIÓN (NUESTRO ROBOT) QUE DIBUJA EL TRIÁNGULO ---
// Este robot recibe 4 herramientas (argumentos): posx, posy, tam, col
function dibujarTrianguloPro(posx, posy, tam, col) {
  goto(posx, posy);
  color(col);
  width(Math.random() * 7); // Grosor de línea al azar
  left(Math.random() * 10); // Rotación inicial al azar

  // Bucle para dibujar los 3 lados del triángulo
  for (let i = 0; i < 3; i++) {
    forward(tam);
    right(120);
  }
}

// --- 4. UTILIZAMOS UN BUCLE PARA CREAR LOS TRIÁNGULOS ---
for (let i = 0; i < x.length; i++) {
  // Le pasamos a la función el dato guardado en la posición 'i' de cada array
  dibujarTrianguloPro(x[i], y[i], tamaños[i], colores[i]);
}

console.log("¡Obra de arte terminada! 🖌️");
```

Dedíquenle tiempo y paciencia. Si se equivocan al tipear algo, recuerden que de los errores es de donde más se aprende. ¡Revisen la consola, corrijan y vuelvan a intentar!

**¡ÉXITOS Y A PROGRAMAR!**