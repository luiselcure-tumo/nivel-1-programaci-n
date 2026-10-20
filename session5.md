# Clase 5: ¡Dándole vida a nuestro código!

¡Hola a todos! Hoy daremos un paso gigante en nuestro aprendizaje. En esta clase, nosotros aprenderemos a crear listas llenas de sorpresas y a usar los "controles remotos" para manejar nuestros bucles a nuestro antojo. Además, ¡haremos que nuestros proyectos cobren vida creando nuestro propio personaje animado! 🚀

---

## Rellenar un Arreglo con Números Aleatorios 🎲

Podemos imaginar un Array (o arreglo) como si fuera un tren largo, donde cada vagón nos sirve para guardar un dato diferente. Hoy, vamos a rellenar esos vagones con números generados al azar y usarlos para crear un fuego artificial.

1. Creamos nuestro arreglo vacío.
2. Usamos un bucle `for` para llenar la lista con números al azar.
3. Usamos otro `for` para leer e imprimir cada número de la lista.
4. ¡Dibujamos nuestro fuego artificial usando esos números!

```javascript
// 1. Creamos el array o arreglo vacio
let misNumeros = [];

// 2. Usamos un for para llenar la lista 36 veces
for (let i = 0; i < 36; i++) {
    // Generamos un número al azar entre 1 y 150
    let numeroAlAzar = Math.floor(Math.random() * 150 + 1);

    // Lo guardamos en nuestra lista (el vagón del tren)
    misNumeros.push(numeroAlAzar);
}

// 3. Ahora usamos otro for para imprimir cada número uno por uno
for (let i = 0; i < misNumeros.length; i++) {
    console.log(misNumeros[i]);
}

// 4. Creamos un fuego artificial con el nuevo array que rellenamos de números aleatorios
for (let i = 0; i < misNumeros.length; i++) {
    goto(0, 0);
    color("red");
    forward(misNumeros[i]);
    right(10);
}
```

---

## Conceptos de Control de Flujo: Break y Continue 🎮

Estos dos comandos son como los "controles remotos" de nuestros bucles. Un bucle repite una serie de tareas, y con estos controles tú tienes el poder de saltarte tareas o apagar el bucle por completo.

### 1. El break: ¡El botón de APAGAR! 🛑
El `break` sirve para detener el bucle por completo y salir de él, aunque todavía le falten vueltas por dar. Es como apagar la televisión de golpe.

```javascript
let misNumeros = [20, 4, 50, 77, 22, 75, 14, 34, 89, 1,
                  10, 15, 45, 78, 90, 43, 65, 78, 87, 5,
                  7, 23, 45, 78, 65, 43, 65, 98, 43, 9];

for (let i = 0; i < misNumeros.length; i++) {
    if (misNumeros[i] === 7) {
        console.log("¡Encontré el 7! Ya no quiero buscar más.");
        break; // Aquí el bucle se detiene por completo
    }
    console.log("Buscando en la posición " + i);
}
```

### 2. El continue: ¡El botón de SALTAR! ⏭️
El `continue` no apaga el bucle. Lo que hace es decir: "cumplí con esta tarea, salto a la siguiente". Es como presionar "Siguiente canción" en tu reproductor de música y omitir la que está sonando.

```javascript
for (let i = 0; i < misNumeros.length; i++) {
  console.log(misNumeros[i]);
    if (misNumeros[i] === 7) {
        console.log("Encontramos el número 7 pero lo saltamos y pasamos al siguiente, no se detiene el programa");
        continue; // Salta este número y vete directo a la siguiente vuelta del for
    }
}
```

---

## El Tiempo en el Código: setTimeout() y setInterval() ⏱️

Para poder animar a nuestros personajes, necesitamos controlar el tiempo.

- **setTimeout()**: Es como el temporizador del horno de tu cocina. Configuras un tiempo, y cuando finaliza la cuenta regresiva, se ejecuta una función una sola vez.
- **setInterval()**: Es como los latidos de un corazón. Esta función hace que una determinada acción se repita varias veces, de forma constante, cada vez que pasa el tiempo establecido.

---

## ¡Manos a la obra: Animando un Personaje! 👾

Aquí combinaremos todo lo que aprendimos. Haremos un cuadrado que rebota por la pantalla utilizando `setInterval`.

```javascript
let x = 0;      // Posición horizontal
let y = 0;      // Posición vertical
let velX = 5;   // Velocidad en X (qué tan rápido va a los lados)
let velY = 3;   // Velocidad en Y (qué tan rápido va arriba y abajo)

setInterval(function () {
  clear(); // Borramos la pantalla para que no se vea el rastro antiguo

  // 1. Movemos la figura sumando la velocidad
  x = x + velX;
  y = y + velY;

  // 2. ¿Chocó con la pared derecha (300) o izquierda (-350)?
  if (x > 300 || x < -350) {
    velX = velX * -1; // ¡Rebota! (cambia de dirección)
  }

  // 3. ¿Chocó con el techo (300) o el suelo (-350)?
  if (y > 300 || y < -350) {
    velY = velY * -1; // ¡Rebota!
  }

  // 4. Dibujamos la figura en la nueva posición
  goto(x, y);
  color("orange");
  width(10);

  // Hagamos un cuadrado simple
  for (let i = 0; i < 4; i++) {
    color(randomColor_h());
    forward(50);
    right(90);
  }

}, 20); // Se repite cada 20 milisegundos
```

---

## Tarea 📝

Crear un personaje animado utilizando todo lo aprendido hasta ahora.

Recuerden que la programación se trata de intentar, probar y divertirse en el proceso. No tengan miedo de experimentar con los colores y las velocidades para ver qué sucede.

**¡ÉXITOS Y A PROGRAMAR!**