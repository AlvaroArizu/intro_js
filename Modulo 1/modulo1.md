# Modulo 1
- Intro a Js
- Operadores
- Cuadro de dialogo
- Errores

### JavaScript como lenguaje de programación

JavaScript es el centro de todo porque es un lenguaje de programación interpretado por el propio navegador (Chrome, Firefox, Opera, IE, y otros), sin necesidad de nada más en absoluto. La web domina el mundo de la tecnología, desde la creación de interfaces para fábricas de autos, cajeros automáticos, o simplemente aplicaciones para lograr que los empleados puedan desde cualquier lugar donde haya conexión a Internet resolver cualquier problema laboral o trabajar sin necesidad de movilizarse. Esto reduce costos y mejora el rendimiento. Entre las tantas cosas que podemos hacer con JavaScript se pueden mencionar:

- Abrir cuadros de diálogo.
- Mostrar mensajes.
- Validar datos en un formulario.
- Hacer una galería de imágenes.

### Implementar JS en línea

Los documentos HTML cuentan con una etiqueta `<script>`, que permite definir código JS. Si bien se puede implementar en pruebas de código rápidas, desde 1999 se recomienda crear y escribir código JS en archivos dedicados, y nunca en un documento HTML. Esto hace más fácil el mantenimiento del código JS, utilizado en múltiples documentos HTML. Vemos un ejemplo de la implementación de JS desde el archivo HTML en el siguiente slide.

### Implementar JS de manera externa

Para crear un archivo JavaScript, antes de comenzar a escribir la lógica de las aplicaciones, se debe contar con un documento HTML. Los archivos JS se referencian dentro del encabezado `<head>` de los documentos HTML. El atributo `defer`, que acompaña al archivo JS, solo es necesario incluirlo cuando interactuemos desde JS con elementos HTML. Siempre conviene crear subcarpetas dedicadas, para mantener ordenado los diferentes tipos de archivos que conforman a un proyecto. Veamos un ejemplo en el siguiente slide.

El atributo `defer` se terminó de soportar, en todos los navegadores web, en el año 2014, con el objetivo de permitir declarar los archivos JS dentro del apartado `<head>` de un documento HTML. Si bien, todavía es posible declarar un archivo JS, al final de un documento HTML, es importante referenciarlo dentro del apartado `<head>` cuando trabajamos con sitios web que requieren un manejo de SEO efectivo. De hacerlo erróneamente, perjudicaremos el posicionamiento de estos sitios web en los resultados de búsqueda de: Google, Bing, y otros tantos buscadores conocidos.

### Realizar comentarios en el código

Al igual que casi todos los lenguajes de programación, JS permite dejar comentarios de texto intercalados con el código. Estos comentarios se pueden crear como de una sola línea `//`. Si se debe escribir un contenido más extenso, es posible recurrir a la combinación de caracteres que permite escribir múltiples líneas de comentarios `/* */`.

Los comentarios sirven para hacer anotaciones que permitan entender, en una lectura rápida, qué es lo que realiza determinado algoritmo. Estos caracteres dedicados, también son útiles para comentar código que no deseamos que se ejecute. El código del ejemplo de la derecha, no se podrá ejecutar porque fue comentado.

### Herramientas integradas de JS

Para programar aplicaciones, JS ofrece una serie de herramientas integradas que ayudan a analizar y trabajar de manera más eficiente. Las herramientas se dividen en dos categorías:

- Cuadros de diálogo.
- Herramientas de consola.

Su uso principal es poder analizar y depurar nuestras aplicaciones.

### Primer script: cuadro de diálogo alert()

Este cuadro de diálogo alerta al usuario sobre diferentes situaciones. Aunque, actualmente, los cuadros de diálogo fueron reemplazados, en su gran mayoría, por ventanas modales más vistosas. La realidad es que nos ayudarán, a nosotros desarrolladores, a aprender la sintaxis de JS y poder depurar y analizar el comportamiento de los algoritmos que escribiremos a continuación. En tu `codigo.js` escribe lo siguiente:

```js
alert("Hola, mundo. Soy JavaScript!");
```
El resultado será el siguiente: "Hola, mundo. Soy JavaScript!"

## Uso del punto y coma

JavaScript es un lenguaje de programación que evoluciona todos los años, ininterrumpidamente, desde el año 2015. En la versión conocida como EcmaScript v6, lanzada ese mismo año, transformó a opcional el uso del punto y coma `;` para finalizar cada sentencia JS. Está en nosotros usarlo o no. En algunos casos dará claridad en la lectura de la sintaxis, delimitando dónde comienza y dónde termina. Pero si ya programamos en otros lenguajes de programación donde no se utiliza el punto y coma, podremos obviarlo para así sentirnos más cómodos.

## El objeto JS: console

JavaScript `console` es un objeto, nativo de este lenguaje, que cuenta con una serie de métodos incorporados que permiten sacar provecho al momento de analizar el código o comportamiento de estas aplicaciones. La mayoría de sus métodos arrojan resultados en la pestaña Console de las Herramientas para el Desarrollador (DevTools). En las próximas slides, veremos estos métodos:

- `console.log()`.
- `console.warn()`.
- `console.error()`.
- `console.table()`.

### `console.log()`

El método `console.log()` permite visualizar un mensaje definido, en la Consola JS. El texto puede provenir de un texto definido manualmente por nosotros, o desde el valor contenido en una variable o constante.

### `console.warn()`

El método `console.warn()` visualiza también un mensaje en la Consola JS con un énfasis de color refiriendo a un tipo de mensaje de advertencia. A su vez, incorpora el ícono de alerta, para que le prestemos más atención al mismo al identificarlo en la consola JS.

### `console.error()`

El método `console.error()` visualiza también un mensaje en la Consola JS, pero con un énfasis de color refiriendo a un tipo de mensaje de error.

### `console.table()`

El método `console.table()` es de gran utilidad para representar en pantalla datos tabulares. Por ejemplo, cuando se trabaja con arrays de elementos, arrays de objetos, u objetos literales, que contienen múltiples datos, son mejor representados por este método que por `console.log()`. Más adelante veremos ejemplos concretos sobre cómo implementarlo de manera efectiva.

## Revisión

- Repasar los conceptos básicos de un lenguaje de programación.
- Trabajar con pseudocódigos para empezar a adaptarse a esta lógica.
- Implementar un cuadro de diálogo `alert()` y utilizar `console.log()`, de forma interna y externa.
- Aplicar todas las propiedades en el proyecto integrador.
- Realizar todas las preguntas necesarias antes de continuar.

# Operadores

| Tipo de operador     | Descripción                                                                                               |
|----------------------|-----------------------------------------------------------------------------------------------------------|
| Asignación   `==`         | Se utiliza para guardar un valor en una variable.                                                         |
| Incremento   `++`        | Se indica mediante el prefijo ++. Incrementa la variable en una unidad.                                    |
| Decremento     `--`      | Se indica mediante el prefijo --. Decrementa la variable en una unidad.                                    |

### Operadores matemáticos

| Operador | Descripción                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------|
| +        | Permite sumar dos valores numéricos o concatenar valores de variables.                                    |
| -        | Realiza una resta entre dos valores numéricos.                                                            |
| *        | Permite multiplicar dos valores numéricos.                                                                |
| /        | Realiza una división entre dos valores numéricos.                                                          |
| %        | Retorna el resto de la división entre dos valores numéricos.                                               |

### Operadores de comparación

| Operador | Descripción                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------|
| ===      | Igualdad estricta: compara si dos valores son iguales.                                                    |
| >        | Mayor que: compara si un valor es mayor que otro.                                                          |
| >=       | Mayor o igual que: compara si un valor es mayor o igual que otro.                                          |
| <        | Menor que: compara si un valor es menor que otro.                                                          |
| <=       | Menor o igual que: compara si un valor es menor o igual que otro.                                          |
| !==      | Distinto de: compara si dos valores son diferentes.                                                         |

### Operadores lógicos

| Operador | Descripción                                                                                               |
|----------|-----------------------------------------------------------------------------------------------------------|
| &&       | Operador lógico AND: retorna true si ambas condiciones se cumplen, false de lo contrario.                  |
| \|\|     | Operador lógico OR: retorna true si al menos una de las condiciones se cumple, false de lo contrario.     |
| !        | Operador lógico NOT: retorna true si la condición es false, y false si la condición es true.              |

### Herramientas integradas de JavaScript

En JavaScript, existen herramientas integradas que facilitan la programación y depuración de aplicaciones web. Estas se dividen en dos categorías principales:

#### Cuadros de diálogo

Los cuadros de diálogo son herramientas gráficas nativas del navegador web que permiten interactuar con el usuario. Los principales son:

- **alert()**: Muestra un cuadro de diálogo con un mensaje de una sola vía, donde el usuario solo puede aceptar.
```javascript
  alert("Hola Team Frontend!");
```

- **confirm()**: Muestra un cuadro de diálogo con dos opciones (Aceptar - Cancelar), permitiendo al usuario tomar una decisión.
```js
var decision = confirm("¿Desea aprender el lenguaje JavaScript?");
```
- **rompt():** Muestra un cuadro de diálogo con una caja de texto y dos botones (Aceptar - Cancelar), permitiendo al usuario ingresar un dato.
```js
var nombre = prompt("Identifícate: ingresa tu nombre:");
```

Es importante capturar el resultado de estos cuadros de diálogo mediante variables para utilizar la información ingresada o la decisión del usuario en la lógica del código.

## Revisión

- Repasar los conceptos básicos de JavaScript.
- Investigar sobre los diferentes tipos de cuadros de diálogo.
- Combinar variables, operadores y cuadros de diálogo.
- Aplicar todas las propiedades en el Proyecto Integrador.


# Errores

## Tipos de errores

En las próximas diapositivas, explicaremos los siguientes tipos de errores:

- Errores de sintaxis.
- Errores en tiempo de ejecución (runtime).
- Errores lógicos.

### Errores de sintaxis

Es normal que se cometan errores de sintaxis. Pueden ser de diferentes tipos. Lo importante es aprender a detectarlos y corregirlos en consecuencia. Los errores de sintaxis se comparan con un error “ortográfico”, propio del lenguaje natural de las personas.

**¿Qué consecuencias traen?**

En lenguajes compilados: un error sintáctico no permitirá que el programa se compile. Se debe corregir para compilar el programa y poder ejecutarlo.

Por ejemplo: los editores de código actuales, pueden detectar errores en la sintaxis e indicarnos los mismos en el momento en el cual escribimos la lógica del programa.

### Errores en tiempo de ejecución

Un programa puede estar perfectamente bien escrito, libre de errores de sintaxis, pero puede generar errores durante su ejecución.

Estos errores suceden en “tiempo de ejecución” (runtime: intervalo de tiempo que va desde que el programa inicia hasta que finaliza).

Son producidos por acciones / operaciones imposibles de realizar (incompatibilidad entre tipos de dato y operadores u operaciones sin solución).

**Por ejemplo:**

- Una división por cero.
- Cálculo de la raíz cuadrada de un número negativo.
- Bucles infinitos.
- Que el programa intente hacer un cálculo aritmético con valores de tipo string.

### Errores lógicos

Son aquellos relacionados con acciones inesperadas que comete el programa:

Estos errores son los peores con los que nos podemos encontrar ya que requerirá una revisión en la lógica de alguna funcionalidad en particular o bien una revisión de toda la aplicación.

**Por ejemplo:**

- Que el programa realice una suma aritmética cuando en realidad debió haber restado.
- Que el programa borre datos de la aplicación en lugar de agregar datos nuevos.
- Que el programa no arroje mensajes en pantalla cuando debió haberlo hecho.

## Características de los errores

Los errores tienen dos formas de manejarse:

- **El error técnico**: Sirve para poder analizar qué sucede, y luego buscar una solución.
- **Error de cara al usuario**: Debe ser un error genérico, coloquial, y que le transmita de la forma más clara posible que la aplicación no se comporta de la forma esperada.

Como programadores, tenemos que probar nuestra aplicación y entender que nunca lograremos tener un control total de posibles errores. Por más que la probemos decenas, cientos o miles de veces, debemos siempre buscar la forma de manejar cualquier posible error.

## La consola JS

En el desarrollo de aplicaciones web, cuando una aplicación construida con JS falla de manera inesperada, los errores que acontecen se representan en la Consola JS.

Todos ellos suelen estar descriptos con un mensaje, donde se explica el error en particular.

Además, casi siempre encontramos una referencia del archivo JS donde se produce el error, y también el número de línea donde está la sentencia de código que lo provoca.

### Ver y analizar errores en JS

Esta guía es el punto de partida, para ir a ese archivo y línea, y así poder analizar qué problema ocurre.

Luego de su análisis, podremos decidir cuál es la mejor forma de resolver el error y controlarlo cuando ocurra o anticiparnos para que no suceda.

## Controlar un error: bloque try-catch

JavaScript brinda muchas formas de controlar errores. La más apropiada es mediante el uso de un bloque conocido como try-catch.

Esta estructura se utiliza para manejar excepciones o errores que pueden ocurrir durante la ejecución de un bloque de código.

Permite proteger ciertas partes del código que pueden generar errores y capturar esas excepciones para realizar una acción específica en caso de que ocurran.

**Funcionamiento**

Cuando se ejecuta un bloque de código dentro del try, si ocurre una excepción, en lugar de detener todo el programa, se captura el error y se ejecuta el bloque catch.

Dentro del bloque catch, se puede acceder al objeto error, que contiene información sobre la excepción que se produjo, como el tipo de error y el mensaje asociado.

### Sintaxis

La sintaxis básica del bloque try-catch, es la siguiente:

```javascript
try {
  // Bloque de código susceptible a errores
} catch (error) {
  // Manejo de errores
}
```
### Ejemplo
Veamos un ejemplo práctico de cómo implementamos el bloque try-catch dentro de nuestro código JavaScript.

Dentro del bloque try intentamos multiplicar la variable nroA por 1996.

La variable en cuestión nunca fue declarada dentro de nuestra aplicación. Como la misma no existe, la aplicación arrojará un error. Este error será capturado por el bloque catch y mostrado a continuación en la consola JS.

```js
try {
  let resultado = nroA * 1996;
  console.log(resultado);
} catch (error) {
  console.error('Ha ocurrido un error:', error.message);
}
```
Al probar el bloque de código en la Consola JS, se verifica que, efectivamente, causa un error en la aplicación por no haber declarado previamente la variable `nroA`.

El bloque try-catch controla y maneja este error de forma efectiva.

Si corregimos nuestro algoritmo asignándole un valor numérico, al ejecutar nuestro código veremos que éste no arrojará ningún error en la consola JS.

Se ejecutará solamente el bloque try, y se visualizará el resultado de la operación aritmética.

## Revisión

- Repasar los conceptos básicos de un error en JavaScript.
- Investigar sobre los diferentes tipos de errores.
- Generar un error voluntario para indagar desde la consola.
- Implementar los bloques try-catch en nuestro código.
- Aplicar todas las propiedades en el Proyecto integrador.
- Realiza las preguntas necesarias antes de continuar.
