# Modulo 2
- Estructuras de control de flujo
- Condicionales avanzados
- Intro a Consola
- Intra a Debug
- Objeto fleca

## Estructuras de control de flujo

Si solamente se trabaja con operadores y variables, se genera una sucesión de pasos lineales. No se puede decidir si algo se mostrará o no según determinadas circunstancias o, en todo caso, repetir una instrucción varias veces. Para realizar estas secuencias más complejas y con múltiples posibilidades se debe trabajar con estructuras de control de flujo.

### Tipo booleano

Los tipos de variables de datos booleanos son aquellos conformados únicamente por dos posibles valores: `true/false`. Un booleano puede ser definido en forma explícita, por ejemplo, al asignar el valor `true` a una variable. Recordemos que, por ejemplo, si utilizamos el cuadro de diálogo `confirm()`, el resultado que retornará al pulsar alguno de los botones será verdadero o falso.

### Operadores de comparación

De igual forma, un valor booleano puede ser el resultante de la comparación de valores que parten de variables, constantes y otros tantos elementos que conforman una aplicación.

### Operadores lógicos

También podemos utilizar operadores lógicos para generar procesos más complejos donde decimos, por ejemplo, que un número es igual o mayor a otro pero también que debe cumplir o no con otra condición. Siempre es interesante graficar estas situaciones para entender el proceso de descarte, donde algo termina dando true o false.

### Estructuras condicionales

#### Condicionales

Permiten decisiones acerca de qué sentencias (órdenes) debe ejecutar el programa, en base a una condición/expresión booleana; es decir, si algo retorna true/false. Se puede decir que a diferencia de los programas que veníamos generando, en este caso, se seguirán una serie de pasos u otra, según el dato de entrada.

Los condicionales que explicaremos en las siguientes pantallas son:

- `if`.
- `if, else`.
- `if, else, else if`.

#### Ejemplo:

##### if

El condicional `if` es la estructura más utilizada al momento de necesitar planteos condicionales para tomar una u otra decisión.

```javascript
if (condición) {
    // Sentencias a ejecutar si la condición es verdadera
}
```
Si la condición se cumple (es decir, si su valor es true), se ejecutarán las instrucciones que se encuentran dentro de las llaves de bloque. Si la condición no se cumple (es decir, si su valor es false), no se ejecuta ninguna instrucción contenida en las llaves de bloque y el programa continúa con la ejecución de cualquier otra instrucción o instrucciones que estén por fuera del condicional.

### if, else
En este caso, se fija una alternativa.
```js
if (condición) {
    // Sentencias a ejecutar si la condición es verdadera
} else {
    // Sentencias alternativas a ejecutar
}
```
## Condicionales compuestos

La estructura `if`, `else if` y `else` permiten analizar condiciones simples, y también compuestas. En este último caso, podemos sumar diferentes condiciones, validando si una de las dos, si las dos, o si ninguna se cumple. Aquí entran en acción los condicionales compuestos, quienes se combinan con los operadores lógicos `&&` (and), `||` (or) y eventualmente `!` (not).

Los operadores lógicos son imprescindibles para realizar aplicaciones complejas, ya que se utilizan para tomar decisiones sobre las instrucciones que debería ejecutar el programa en función de ciertas condiciones. El resultado de cualquier operación que utilice operadores lógicos siempre es un valor lógico, o booleano.

### Revisión

- Repasar el concepto de estructura de control de flujo.
- Generar diferentes opciones de pseudocódigo para trabajar con condicionales.
- Implementar `if`, `else`, `else if`.
- Combinar los diferentes tipos de output vistos.
- Implementar los conocimientos en el Proyecto Integrador.

## Anidamiento de condicionales

Un condicional `if` se puede escribir dentro del bloque de otro `if` (en su camino principal o en el alternativo) para generar múltiples caminos de ejecución. Mediante este anidamiento de condicionales, el código comenzará a "ramificarse".

### Pseudocódigo de anidamiento

En este otro ejemplo de pseudocódigo, encontramos la utilización de condicionales anidados.

```javascript
if (condicion1) {
    if (condicion2) {
        // Sentencias para camino 1
    } else {
        // Sentencias para camino 2
    }
} else {
    // Sentencias para camino 3
}
```
## Condicional múltiple (switch)
La cláusula switch, en JavaScript, es una estructura de control que permite evaluar una expresión y comparar su valor con múltiples casos posibles. Cuando se encuentra un caso que coincide con el valor de la expresión, se ejecuta el bloque de código correspondiente a ese caso.

### Sintaxis
La sintaxis de un switch es similar a la siguiente:
```js
switch (expresion) {
    case valor1:
        // Sentencias caso 1
        break;
    case valor2:
        // Sentencias caso 2
        break;
    ...
    default:
        // Sentencias caso por defecto
}
```
Si ninguno de los casos coincide, se puede proporcionar un caso default (por defecto), que se ejecutará si no hay coincidencias.

### Ejemplos de parámetros para un switch - case:

- El estado civil de una persona (soltero, divorciado, viudo, casado).
- El sexo de una persona (M, F).
- El resultado de un partido (victoria, empate, derrota).
- Los colores del arcoíris (rojo, azul, violeta, y otros).
- Puntos ganados en un partido (3, 1 ó 0).
- Grupos sanguíneos.
- Provincias de Argentina.

### Revisión

- Repasar el concepto de estructura de control de flujo.
- Generar diferentes opciones de pseudocódigo para trabajar con anidamiento.
- Combinar los diferentes tipos de operadores lógicos y relacionales.
- Repasar el concepto de Condicional Múltiple o `switch`.
- `switch` se implementará luego de que, en el curso, se estudie con más profundidad el objeto Fecha.

# Consola de JavaScript

La consola de JavaScript es una herramienta disponible en todos los navegadores. Sirve para realizar la depuración del código.

Cuando hablamos de depuración (debug en inglés) nos referimos al mantenimiento y corrección de un código fuente.

La consola ofrece dos herramientas principales:
- La vista del navegador (mediante las teclas F12, Ctrl + Shift + I ó Click Derecho > Inspeccionar). Esta vista nos permite leer las salidas por consola.
- El objeto console (mediante la palabra ‘console’ en JavaScript). Este objeto nos permite escribir en la consola.

## Métodos de la consola:

- **console.assert**: Registra un mensaje y envía una traza de error a la consola si el primer argumento es falso. Útil para evaluar y probar un código mediante los Assertion Test.
  
- **console.clear**: Limpia la consola, borra todos los mensajes previos. Útil para hacer más legible el área de depuración de la aplicación web.

- **console.count** y **console.countReset**: Registra el número de veces que una línea ha sido llamada con la etiqueta dada. Además, reinicia el valor del contador para la etiqueta dada.

- **console.debug**: Registra un mensaje con el nivel de debug. El nivel debug es un nivel menos grave que el error.

## Cronómetros: temporizador

Una herramienta útil para medir el rendimiento de un programa es el temporizador. Con el temporizador es posible evaluar cuánto tarda el navegador en ejecutar un código determinado. Con esta información se puede verificar si es necesario cambiar el código para que funcione más rápido.

## Revisión

- Examinar la interfaz de la consola.
- Comprender que la consola te sirve como desarrollador para el mantenimiento de tu código.
- Hacer Assertion Test con la consola.
- Mostrar diferentes tipos de mensajes por la consola.
- Medir el tiempo de ejecución de un programa.

# Detección de errores

Programar es estar en constante proceso de resolución de errores. La velocidad de la retroalimentación es una de las características propias de este trabajo, donde es posible tener una retroalimentación inmediata sobre si estás haciendo las cosas bien o mal.

Si bien hay errores más difíciles de detectar, muchos pueden ser identificados mientras se está escribiendo código. Para detectar estos errores, existen herramientas como el editor de texto o el depurador de código.

## Depurador de código

### Paso a paso
1. Abrir el navegador.
2. Hacer clic derecho en cualquier parte de la página.
3. Hacer clic en Inspeccionar.
4. En el panel que se abra, hacer clic en Fuentes (se puede llamar Código o Sources también).

Hay tres paneles:
- A la izquierda, verás tus archivos.
- Al centro, el archivo que estás evaluando.
- A la derecha, las herramientas para evaluarlo.

### Breakpoints
Al hacer clic en un número de línea del archivo abierto, se crea un punto de interrupción (breakpoint), que indica que el código se ejecutará hasta esa línea y luego quedará en pausa. Esto te otorga el control sobre la ejecución y puedes avanzar o retroceder a voluntad.

### Control de ejecución
De izquierda a derecha, estos botones tienen las siguientes funciones:
1. Continuar el código normalmente (F8).
2. Saltar la función actual.
3. Entrar a la función actual.
4. Salir de la función actual.
5. Avanzar a la línea siguiente (F9).

### Inspección de variables
Es posible ver el valor actual de una variable posicionando el cursor encima de ella. El navegador ofrecerá esa información, lo que es útil para entender el estado actual del código.

### Debugger
La cláusula `debugger` en el código JS pausará la ejecución en el lugar donde se haya escrito. Luego, podremos controlar el código desde la misma barra de depuración. Es importante tener en cuenta que `debugger` solo funciona con las herramientas de desarrollador iniciadas.

## Revisión
- Aprendiste sobre el uso del depurador.
- Creaste puntos de interrupción.
- Utilizaste los controles para avanzar o continuar el flujo de ejecución.
- Utilizaste la inspección de variables para revisar el estado actual del código.

# Objeto Fecha: Clase Date

La clase Date es un objeto fundamental en JavaScript que permite manipular fechas y horas en los desarrollos. Es instanciable, lo que significa que puedes crear múltiples instancias de este objeto según las necesidades de la aplicación.

## Ejemplo

```javascript
// Instanciación de la clase Date con una fecha específica
const fecha = new Date(2024, 6, 14); // 14 de Julio de 2024
```
Cada instancia de la clase Date permite acceder a diferentes partes de la fecha utilizando varios métodos disponibles.

## Métodos

| Método         | Descripción                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `.getDate()`   | Retorna el día del mes (1-31) de la fecha.                                  |
| `.getDay()`    | Retorna el día de la semana (0-6), donde 0 es domingo y 6 es sábado.        |
| `.getMonth()`  | Retorna el mes (0-11), donde 0 es enero y 11 es diciembre.                  |
| `.getFullYear()` | Retorna el año completo de la fecha.                                       |

### Ejemplo: Método `getMonth()`

El método `getMonth()` retorna el número de mes de la fecha. Sin embargo, es importante recordar que los meses se representan del 0 al 11, donde 0 es enero y 11 es diciembre. Por lo tanto, si se necesita mostrar el número de mes en la aplicación, se debe sumar 1 al valor retornado por `getMonth()`.

### Ejemplo: Método `.toLocaleString()`

El método `.toLocaleString()` permite formatear la información de la fecha según la configuración regional específica y el tipo de datos deseado. Esto es útil para mostrar el mes en formato de nombre.

### Ejemplo: Método `.getTime()`

El método `.getTime()` retorna la fecha instanciada en milisegundos, lo que permite calcular períodos de tiempo entre fechas. Dividiendo la diferencia de tiempo en milisegundos por el número de milisegundos en un día, se puede obtener la diferencia en días. De manera similar, se pueden calcular diferencias en semanas, meses y años.

## Revisión

- Repasar el concepto de objeto en JavaScript.
- Implementar la clase Date con sus diferentes métodos.
- Combinar los métodos para extraer unidades de tiempo específicas.
- Realizar cálculos entre diferentes fechas para obtener el tiempo transcurrido.

