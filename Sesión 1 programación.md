# Guía de Aprendizaje para Alumnos - Sesión 1: Conceptos Básicos de Programación

¡Bienvenido/a a la primera sesión de nuestro taller de programación! A lo largo de 8 encuentros de dos horas de duración[cite: 1], aprenderás las bases del lenguaje JavaScript. Al finalizar el taller, serás capaz de crear tu propia función de animación en Turtle.js[cite: 1].

---

## 1. Introducción: ¿Qué hace un programa de computadora?

Todo programa de programación, sin importar su nivel de complejidad, permite realizar tres acciones principales[cite: 1]:
* **Aceptar datos:** Recibe la información que el usuario o el entorno le proporciona[cite: 1].
* **Procesarlos:** Ejecuta operaciones, cálculos o decisiones sobre esos datos[cite: 1].
* **Devolverlos procesados:** Entrega el resultado final obtenido[cite: 1].

> 📌 **Registro de asistencia:** No olvides registrar tu presencia al iniciar la clase siguiendo las indicaciones presentadas en pantalla[cite: 1].

---

## 2. Creación y Configuración del Entorno de Trabajo

Para desarrollar aplicaciones web, utilizaremos herramientas de edición de código y un navegador[cite: 1].

### ¿Qué es JavaScript?
* Es uno de los lenguajes de programación más populares por su sintaxis sencilla[cite: 1].
* Se ejecuta dentro de un navegador web (como Chrome o Firefox) sin necesidad de servidores[cite: 1].
* Es un lenguaje totalmente independiente y distinto de Java[cite: 1].
* Su código se guarda en archivos de texto con la extensión `.js` utilizando reglas especiales de redacción[cite: 1].

### Pasos para configurar tu equipo:
1. Busca y abre **Visual Studio Code** en tu computadora[cite: 1].
2. Ingresa a **Google Classroom** con tu cuenta e introduce el código de clase correspondiente[cite: 1].
3. Ubica en Classroom el enlace de descarga del archivo plantilla de JavaScript y HTML[cite: 1].
4. Abre la carpeta/archivo descargado dentro de Visual Studio Code[cite: 1].
5. Conecta el archivo JavaScript al archivo HTML siguiendo la estructura indicada[cite: 1].
6. Abre el archivo HTML en tu navegador web para comprobar que el código se ejecuta correctamente[cite: 1].

---

> 🎥 **[EJEMPLO EN VIDEO: Configuración del Entorno y Conexión JS-HTML]**
>
> *Demostración visual paso a paso sobre cómo abrir Visual Studio Code, descargar la plantilla desde Google Classroom, vincular el archivo `.js` dentro del código HTML y abrirlo en el navegador para verificar su funcionamiento.*
>
> ```html
> <iframe 
>   width="560" 
>   height="315" 
>   src="[https://www.youtube.com/watch?v=CxF3ykWP1H4](https://www.youtube.com/watch?v=CxF3ykWP1H4)" 
>   title="Configuración del Entorno y Conexión JS-HTML" 
>   frameborder="0" 
>   allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
>   allowfullscreen>
> </iframe>
> ```

---

## 3. Variables y Tipos de Datos

### ¿Qué es una Variable?
Una variable es un espacio de almacenamiento temporal en la memoria RAM de la computadora que nos permite guardar datos mientras se ejecuta un programa[cite: 1].

Piensa en una variable como un **frasco** etiquetado[cite: 1]:
* El **frasco** reservado en la memoria guarda la información[cite: 1].
* La **etiqueta** es el nombre con el que identificas la variable[cite: 1].
* El **contenido** del frasco es el valor asignado[cite: 1].
* Al declarar una variable, reservas ese espacio, le pones un nombre y le asignas un valor para usarlo más adelante[cite: 1].

### Reglas para nombrar variables:
* Puedes utilizar caracteres del alfabeto latino en mayúsculas y minúsculas[cite: 1].
* Puedes incluir números[cite: 1].
* Puedes utilizar los símbolos `_` (guion bajo) y `$` (signo de peso)[cite: 1].
* **Prohibido:** No pueden comenzar con un número[cite: 1].
* **Prohibido:** No se permite el uso de otros símbolos o caracteres especiales[cite: 1].

### Operaciones Algebraicas con Variables:
Puedes aplicar operaciones matemáticas sobre las variables mediante operadores algebraicos[cite: 1]:
* Suma (`+`)[cite: 1]
* Resta (`-`)[cite: 1]
* Multiplicación (`*`)[cite: 1]
* División (`/`)[cite: 1]

### Tipos de Datos Principales en JavaScript:
* **Numéricos:** Números enteros o decimales[cite: 1].
* **Cadenas (Strings):** Texto delimitado por comillas[cite: 1].
* **Booleanos:** Valores lógicos que solo pueden ser verdadero (`true`) o falso (`false`)[cite: 1].

---

> 🎥 **[EJEMPLO EN VIDEO: Declaración de Variables y Operadores en VS Code]**
>
> *Muestra práctica de la creación de variables en el editor de código, validación de reglas de nombres y aplicación de operaciones matemáticas de suma, resta, multiplicación y división con sus resultados expuestos.*
>
> ```html
> <iframe 
>   width="560" 
>   height="315" 
>   src="[https://www.youtube.com/watch?v=kXMpu07zjN4](https://www.youtube.com/watch?v=kXMpu07zjN4)" 
>   title="Declaración de Variables y Operadores en VS Code" 
>   frameborder="0" 
>   allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
>   allowfullscreen>
> </iframe>
> ```

---

## 4. Funciones Predeterminadas de JavaScript

JavaScript incluye funciones integradas que permiten interactuar con el usuario y analizar la ejecución de tu código[cite: 1]:

* **`prompt()`:** Solicita una entrada al usuario mediante una ventana emergente y guarda ese valor en una variable (el resultado devuelto es siempre una cadena de texto)[cite: 1].
* **`alert()`:** Muestra un cuadro de diálogo en pantalla con un mensaje y un botón de "Aceptar"[cite: 1].
* **`console.log()`:** Imprime información en la consola de herramientas del navegador, utilizada para depurar errores y observar el flujo interno del código[cite: 1].
* **`parseInt()`:** Convierte un valor de cadena de texto en un número entero[cite: 1].
* **`parseFloat()`:** Convierte un valor de cadena de texto en un número decimal (coma flotante)[cite: 1].

---

> 🎥 **[EJEMPLO EN VIDEO: Uso de Funciones de Entrada, Salida y Conversión]**
>
> *Ejemplo guiado que ilustra el despliegue de ventanas emergentes con `prompt()` y `alert()`, el envío de datos a la consola con `console.log()` y la transformación de datos de texto a números utilizando `parseInt()` y `parseFloat()`.*
>
> ```html
> <iframe 
>   width="560" 
>   height="315" 
>   src="[https://www.youtube.com/embed/TU_ID_DE_VIDEO](https://www.youtube.com/embed/TU_ID_DE_VIDEO)" 
>   title="Uso de Funciones de Entrada, Salida y Conversión" 
>   frameborder="0" 
>   allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
>   allowfullscreen>
> </iframe>
> ```

---

## 5. Estructuras Condicionales (`if` / `else`)

Las estructuras condicionales permiten que tu programa tome decisiones y ejecute distintas acciones según la información que reciba[cite: 1].

### Estructura y Reglas:
* La condición que se evalúa se escribe dentro de paréntesis `()`[cite: 1].
* El bloque de código que se ejecuta según el resultado se escribe dentro de llaves `{}`[cite: 1].
* Si la condición evalúa como verdadera (**booleano verdadero**), se ejecuta el bloque dentro del `if`[cite: 1].
* Si la condición es falsa, se ignora el bloque `if` y se ejecuta la instrucción `else`[cite: 1].
* Si existen múltiples condiciones, se evalúan de forma secuencial una a una hasta encontrar la primera respuesta verdadera[cite: 1].
* Tan pronto como una instrucción `if` resulta verdadera, su código se ejecuta y todas las demás condiciones subsiguientes son ignoradas[cite: 1].
* El bloque `else` solo se ejecutará si **todas** las comparaciones anteriores resultaron falsas[cite: 1].

---

> 🎥 **[EJEMPLO EN VIDEO: Evaluación de Estructuras Condicionales `if` / `else`]**
>
> *Explicación gráfica del flujo de decisión en un script, mostrando cómo cambia el camino de ejecución del código cuando el usuario ingresa diferentes valores.*
>
> ```html
> <iframe 
>   width="560" 
>   height="315" 
>   src="[https://www.youtube.com/watch?v=EakDnBLZOCg](https://www.youtube.com/watch?v=EakDnBLZOCg)" 
>   title="Evaluación de Estructuras Condicionales if / else" 
>   frameborder="0" 
>   allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
>   allowfullscreen>
> </iframe>
> ```

---

## 6. Proyecto Práctico: Creación de un Chatbot interactivo

¡Es momento de aplicar lo aprendido en tu primer proyecto práctico![cite: 1]

### Consigna:
Debes programar un chat interactivo que reciba preguntas del usuario y responda con mensajes personalizados[cite: 1].

### Requisitos del Proyecto:
* Integrar obligatoriamente las funciones `prompt()`, `alert()` y `console.log()`[cite: 1].
* Definir un tono o personalidad para tu chat (por ejemplo: divertido, educado, pícaro, misterioso)[cite: 1].
* Emplear condicionales para evaluar lo que escribe el usuario y mostrar distintas respuestas según la entrada[cite: 1].

---

## 7. Cierre y Entrega de la Sesión

1. Guarda todos los archivos en Visual Studio Code[cite: 1].
2. Sube la carpeta de tu proyecto a tu Google Drive[cite: 1].
3. Adjunta el enlace/archivo en la tarea correspondiente dentro de Google Classroom[cite: 1].
4. En la siguiente clase avanzaremos con nuevos conceptos básicos de JavaScript y comenzaremos a trabajar con **Turtle.js**[cite: 1].