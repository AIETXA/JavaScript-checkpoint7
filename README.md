---
description: >-
  Documentación para principiantes sobre los conceptos esenciales de uno de los
  lenguajes de programación más populares y versátiles de la web.
---

# Fundamentos de JavaScript

**Temario:**

📋Introducción a JavaScript

📋¿Qué diferencia a JavaScript de otros lenguajes de programación?

📋Tipos de datos JS

📋¿Cuáles son las tres funciones de String en JS?

📋¿Qué es un condicional?

📋¿Qué es un operador ternario?

📋Declaración de función vs  Expresión de función.

📋¿Qué es la palabra clave "this" en JS?

<figure><img src=".gitbook/assets/java-script1.jpg" alt=""><figcaption></figcaption></figure>

&#x20;

1. ## Introducción

JavaScript es un lenguaje de programación multiplataforma orientado a objetos que se utiliza para hacer que las páginas web sean interactivas (ej., Que tienen animaciones complejas, botones en los que se puede hacer clic, menús emergentes, etc.).

💡Si pensamos en una página web como un coche, el HTML es el chasis y la estructura mecánica, el CSS es la carrocería y la pintura, y JavaScript es el motor — lo que hace que todo se mueva y funcione.

#### ¿Para qué sirve? (Su rol en la web)

Originalmente nació para hacer pequeños trucos en las páginas (como efectos de luces en los botones o validar formularios), pero hoy en día es un lenguaje monstruosamente potente que sirve para:

* **Crear interactividad en el navegador:** Animaciones, menús desplegables, galerías de fotos, mapas interactivos (como Google Maps) o actualizaciones de contenido en tiempo real sin tener que recargar toda la página (como cuando te llega un mensaje en una red social).
* **Desarrollo Frontend moderno:** Es la base de las aplicaciones web que usas a diario. Herramientas y frameworks como React, Vue o Angular permiten estructurar aplicaciones complejas (como Netflix, Spotify o Twitter) usando JavaScript de fondo.
* **Controlar el DOM (Document Object Model):** JavaScript puede leer, modificar, agregar o eliminar cualquier elemento de HTML y CSS sobre la marcha, respondiendo a lo que hace el usuario (hacer clic, escribir, hacer scroll).

#### Tres características clave de JavaScript

1. Es un lenguaje interpretado y orientado a objetos: No necesitas compilarlo (transformarlo a código binario antes de ejecutarlo). El propio navegador web (Chrome, Firefox, Edge) lee el código directamente y lo ejecuta línea por línea.
2. Basado en eventos: Gran parte de JavaScript se ejecuta cuando "algo pasa". Un evento puede ser que el usuario hizo un _click_, movió el ratón, presionó una tecla o terminó de cargar la página.
3. Es el estándar de la web: Es el único lenguaje de programación que todos los navegadores web del mundo entienden de forma nativa. No necesitas instalar nada en tu computadora para empezar a programar en JS; con un editor de texto y tu navegador ya tienes todo.

#### Un ejemplo básico de código:

Imagínate que quieres que aparezca un mensaje de alerta en la pantalla cuando alguien presione un botón. El código se vería algo así:

````
```JavaScript
// Definimos una función (una receta de pasos a seguir)
function saludarUsuario() {
    alert("¡Hola! Bienvenida al mundo de JavaScript.");
}
```
````

#### ¿Cómo se usa JavaScript en una página web?

JavaScript se puede escribir directamente dentro del archivo HTML usando la etiqueta `<script>`, o en un archivo separado con extensión `.js` que luego se enlaza al HTML.

**Directamente en el HTML:**

````
```html
<script>
  alert("¡Hola mundo!");
</script>
```
````

**En un archivo externo:**

````
```html
<script src="mi-script.js"></script>
```
````

Lo más recomendado es usar un archivo externo para mantener el código organizado.<br>



## ¿Qué diferencia a JavaScript de otros lenguajes de programación?

JavaScript ocupa un lugar único en el mundo de la programación. Aunque comparte conceptos lógicos con lenguajes como Python, Java o C++, tiene características que lo diferencian radicalmente de cualquier otro.

Las principales diferencias que hacen único a JavaScript son:

#### 1. 👑 El rey absoluto del navegador (Monopolio Frontend)

Esta es su mayor diferencia: JavaScript es el único lenguaje de programación que todos los navegadores web (Chrome, Safari, Firefox, Edge) entienden de forma nativa.&#x20;

* Si quieres programar en Python, el usuario tiene que instalar Python en su computadora.
* Si programas en Java, se necesita una máquina virtual.
* Con JavaScript, el motor para ejecutar el código ya viene integrado en el navegador de cualquier celular, computadora o tablet del mundo. No hay competencia en este terreno.

#### 2. 🌍 El lenguaje que está en todos lados (Full-Stack)

Históricamente, los lenguajes se dividían estrictamente: unos servían para el diseño visual (Frontend) y otros para los servidores y bases de datos (Backend). JavaScript rompió esa barrera. Gracias al nacimiento de Node.js, hoy en día un programador puede usar el mismo y único lenguaje para crear la interfaz visual de una página web, programar el servidor, crear una aplicación móvil (con React Native) y gestionar bases de datos.

#### 3. 📐⚒️ Su arquitectura basada en eventos y asincronía

A diferencia de lenguajes tradicionales donde el código se ejecuta estrictamente de arriba a abajo bloqueando la pantalla hasta que termina una tarea, JavaScript fue diseñado para no quedarse "congelado".

Funciona mediante un bucle de eventos (_Event Loop_):

* El usuario puede hacer clic en un botón para descargar un archivo pesado.
* En lugar de congelar la página web mientras se descarga, JavaScript delega esa tarea en el fondo (_asincronía_) y permite que el usuario siga haciendo scroll o interactuando con otros botones de la página. Cuando la descarga termina, JavaScript avisa y muestra el resultado.

#### 4. ✏️ Tipado dinámico y débil (Flexibilidad extrema)

En lenguajes como C++ o Java (tipado estricto), tienes que decirle a la computadora exactamente qué tipo de dato va a guardar una variable (un número entero, texto, etc.) y no puedes cambiarlo después.

JavaScript es extremadamente permisivo y "adivina" el tipo de dato sobre la marcha:

````
```JavaScript
let dato = "Hola"; // JavaScript sabe que es texto (String)
dato = 2026; // Ahora pasa a ser un número sin lanzar ningún error
```
````

Esta flexibilidad es genial para programar rápido, aunque en proyectos grandes puede causar dolores de cabeza (por eso hoy en día es tan popular usar TypeScript, que le añade reglas estrictas a JavaScript).

<figure><img src=".gitbook/assets/tabla_comparativa.png" alt=""><figcaption></figcaption></figure>

💡 En resumen, mientras que otros lenguajes nacieron para calcular datos o manejar sistemas operativos pesados, **JavaScript** nació para dar vida a la web, y su capacidad de adaptarse lo convirtió en el lenguaje más versátil y demandado de la actualidad.

***

## Tipos de datos en JavaScript

En JavaScript hay 8 tipos de datos fundamentales que se dividen en dos grandes categorías: **Primitivos** (inmutables y guardados por valor) y **De Objeto** (mutables y guardados por referencia).

Se organizan así:&#x20;

#### 1. Tipos de Datos Primitivos

<figure><img src=".gitbook/assets/datos primitivos.jpg" alt=""><figcaption></figcaption></figure>

�&#xDCA1;_&#x45;n la siguiente guía ampliaremos esta lista con los tipos modernos `bigint` y `symbol`_.



* `number`: Representa tanto números enteros como de punto flotante. También incluye valores especiales como `Infinity`, `-Infinity` y `NaN` (Not a Number).

````
```javascript
let edad = 37;
let precio = 22.50;
```
````

* `string`: Cadenas de texto. Se pueden definir con comillas simples (`'`), dobles (`"`) o backticks (`` ` ``) para plantillas literales.

````
```javascript
let nombre = 'Ana';
let saludo = `Hola, ${nombre}`;
```
````

* `boolean`: Solo puede tener dos valores: `true` (verdadero) o `false` (falso). Se usa para lógica y condicionales.

````
```javascript
let esMayorDeEdad = true;
```
````

* `undefined`: Es el valor que se le asigna automáticamente a una variable que ha sido declarada pero aún no tiene un valor asignado.

````
```javascript
let x; // Su valor es undefined
```
````

* `null`: Representa la ausencia intencional de cualquier valor. Es un "vacío" programado.

````
```javascript
let vacio = null;
```
````

⚠️ Dato curioso: Si haces `typeof null`, JavaScript te dirá que es `"object"`. Esto es un error histórico del lenguaje que no se ha cambiado por temas de compatibilidad.



* `bigint`: Sirve para representar números enteros que son demasiado grandes para el tipo `Number` estándar (mayores a $$2^{53} - 1$$). Se crean agregando una `n` al final del número.

````
```javascript
let numeroGigante = 9007199254740991n;
```
````

* `symbol`: Es un valor único e inmutable que se utiliza a menudo como clave para las propiedades de los objetos, evitando colisiones de nombres.

````
```javascript
let id = Symbol("id");
```
````

#### 2. Tipos de Objeto (Complejos o de Referencia)

<figure><img src=".gitbook/assets/datos por objeto.png" alt=""><figcaption></figcaption></figure>

💡 Cuando copias un objeto, copias la _referencia_ a su lugar en la memoria, no el _valor real_.



* `object`: La estructura base de JavaScript para almacenar datos en pares clave-valor.

````
```javascript
let persona = { nombre: "Ailén", edad: 37};
```
````

* `array`: Técnicamente son objetos especiales ordenados por índices numéricos.

````
```javascript
let colores = ["rojo", "verde", "azul"];
```
````

* `function`: En JavaScript, las funciones también son objetos de primera clase, lo que significa que pueden guardarse en variables y pasarse como argumentos.

````
```javascript
function saludar() { return "Hola"; }
```
````

***
