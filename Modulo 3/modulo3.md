# Modulo 3
- Vectores
- Vectores y objetos
- Bucles While y for

# Arreglos (arrays)

Los arrays, (también llamados arreglos o colecciones) permiten definir, bajo una misma estructura, una serie de valores útiles dentro de nuestra aplicación. En JS, se utilizan dos tipos de arrays:

- Arrays de elementos.
- Arrays de objetos.

Si bien es posible crear arrays que almacenan diferentes tipos de datos, no es una práctica común, dado que le agrega complejidad a la aplicación, al momento de validar a qué tipo de dato corresponde cada valor almacenado.

## Ejemplo: array de objetos

Ante la necesidad de crear un array que almacene diferentes valores, en cada uno de sus índices, lo más apropiado será estructurar un array de objetos, que aporte orden y entendimiento.

Cada valor almacenado en un array, obtiene una posición numérica, denominada índice. Esta posición numérica inicia siempre a partir del valor 0 (cero), y se incrementa en un dígito por cada nuevo valor contenido en el array.

Para leer algún valor que esté almacenado en el array, simplemente se define el nombre del array, y se encierra entre corchetes el valor numérico de la posición que se desea leer.

## Ver contenido del array y depurarlo

Cuando trabajamos con arrays, la forma más efectiva de ver su contenido y depurarlo, es utilizar el objeto console, y su método `.table()`. Este método representa un array en DevTools > Console, que muestra en formato tabular, y representa sus índices en una segunda columna.

## Contabilizar el total de elementos almacenados

Si se necesita contabilizar el total de elementos almacenados, se puede recurrir a la propiedad `.length`, la cual retornará un valor numérico correspondiente al total de elementos almacenados en el array.

## Métodos de arrays

Además de la propiedad `.length`, los arreglos cuentan con una serie de métodos que permiten operar con sus valores. A través de ellos, es posible:

- Agregar o quitar elementos.
- Modificar elementos existentes.
- Cambiar elementos del arreglo.
- Ordenar de forma ascendente o descendente.
- Fusionar arreglos.
- Buscar, filtrar, reestructurar, calcular, validar.
- Crear nuevos arreglos a partir de uno existente.

# Métodos de arrays
| Método  | Descripción                                                                                     | Ejemplos                    |
|---------|-------------------------------------------------------------------------------------------------|-----------------------------|
| push    | Agrega un nuevo elemento al final del array.                                                     | array.push('nuevoElemento')|
| unshift | Agrega un nuevo elemento al principio del array.                                                 | array.unshift('nuevoElemento') |
| pop     | Quita el último elemento del array.                                                              | array.pop()                 |
| shift   | Quita el primer elemento del array.                                                              | array.shift()               |
| slice   | Crea un nuevo array con elementos de otro array, de forma parcial o total.                       | array.slice(1, 3)          |
| splice  | Quita uno o más elementos del array de cualquier posición. También reemplaza uno o más elementos de un array. | array.splice(2, 1)   |
| indexOf | Permite identificar si un elemento existe o no dentro del array. Retorna true o false según el resultado. | array.indexOf('elemento') |
| includes| Permite identificar si existe o no un elemento dentro de un array.                                | array.includes('elemento') |
| concat  | Agrega un nuevo elemento al final del array.                                                     | array1.concat(array2)      |
| join    | Agrega un nuevo elemento al principio del array.                                                 | array.join('-')             |
| sort    | Ordena de forma ascendente los elementos de un array.                                             | array.sort()                |
| reverse | Revierte el orden de los elementos de un array.                                                   | array.reverse()             |



## Encadenamiento de métodos

JavaScript permite utilizar encadenamiento de métodos en los arrays, lo que facilita aplicar transformaciones y acciones sobre los datos en una sola línea de código. Por ejemplo, se puede combinar el método `sort()` con `reverse()` para obtener un ordenamiento descendente de los elementos del array.

Es importante tener en cuenta que casi todos estos métodos son aplicables tanto en arrays de elementos como en arrays de objetos. Sin embargo, en los arrays de objetos pueden existir métodos alternativos para realizar ciertas operaciones debido a su mayor complejidad.

## Revisión

- Repasar el concepto de arreglo en JavaScript.
- Mostrar una lista de empleados.
- Practicar la combinación de los diferentes métodos de arrays.
- Trabajar en el Proyecto integrador.
- Realizar las preguntas necesarias al docente antes de continuar.

## Objetos y su definición

En el mundo de la programación existe, desde hace poco más de treinta años, una rama denominada Programación Orientada a Objetos (P.O.O.). A través de esta, se busca desarrollar aplicaciones de software basadas en el paradigma de objetos. Cuando hablamos de objetos, nos referimos a entidades que representan conceptos reales o abstractos en un formato digital. Si bien el paradigma de la P.O.O. nació entre los 50’s y 60’s, recién comenzó a verse reflejado en lenguajes de programación hacia fines de los 70’s.

Cada objeto tiene un estado y un comportamiento:
- el estado es definido por sus atributos.
- el comportamiento se define por sus métodos.

Los objetos se relacionan entre sí a través de sus mensajes y sus métodos, y su uso en el desarrollo de software permite clarificar de forma efectiva aquellas tareas que definimos en cada línea de código que le da vida a nuestra aplicación.

### Atributos y métodos

Cada objeto tiene un estado y un comportamiento:
- el estado es definido por sus atributos.
- el comportamiento se define por sus métodos.

Los objetos se relacionan entre sí a través de sus mensajes y sus métodos, y su uso en el desarrollo de software permite clarificar de forma efectiva aquellas tareas que definimos en cada línea de código que le da vida a nuestra aplicación.

### Propiedades y métodos

Entonces:
- Cada característica (o atributo) que representa a estos objetos dentro del ecosistema de software suele llamarse propiedad.
- Cada comportamiento de estos objetos es representado por un método.

### Entidad abstracta

Se puede pensar en, por ejemplo, una computadora. Si bien es algo físico, suele tratarse como una entidad abstracta por sus limitaciones o nicho específico. Sus características pueden ser:
- Marca.
- Modelo.
- Posee display.
- Posee teclado.
- Posee mouse pad o puntero.
- Sistema operativo.
- Batería.

## El objeto literal

JS es un lenguaje que evoluciona año tras año, desde 2015 hasta la actualidad. Previo a esto, su evolución se daba en períodos más espaciados (entre 3 y 5 años para que saliera una nueva versión). Y durante el período que lleva este lenguaje de programación, el mismo tuvo una evolución importante en la forma de trabajar con objetos. Pero de toda su evolución, nos concentraremos solamente en el objeto literal, dado que necesitamos entender su base para luego poder hablar de array de objetos. El objeto literal en JS es el más simple de todos, dado que lo declaramos y comenzamos a utilizarlo inmediatamente. Además, su estructura de datos fácil de entender y leer inspiró la creación del formato de transporte de datos conocido como JSON, y utilizado desde hace más de una década para intercambiar información entre aplicaciones de servidor y aplicaciones frontend (web, nativas, móviles).

Cuando se define un objeto literal, éste se debe crear a través de la palabra reservada const. El nombre que le asignamos suele definirse con su primera inicial en mayúsculas, y debe ser una palabra (sustantivo), expresado en singular. Su estructura de datos se debe encerrar entre las llaves de bloque.

### Ejemplos
```js
// Definición del objeto literal Persona
const persona = {
    nombre: "Juan",
    edad: 30,
    casado: false,
    hobbies: ["fútbol", "lectura", "viajes"],
    direccion: {
        calle: "Calle 123",
        ciudad: "Ciudad A",
        codigoPostal: "12345"
    }
};

// Acceder al valor de la propiedad nombre
console.log(persona.nombre); // Salida: Juan

// Cambiar el valor de la propiedad edad
persona.edad = 35;

// Acceder al valor del hobby en la posición 0
console.log(persona.hobbies[0]); // Salida: fútbol

// Acceder al valor de la propiedad ciudad dentro del objeto direccion
console.log(persona.direccion.ciudad); // Salida: Ciudad A
```

### Arreglos de objetos
- En JavaScript, es posible crear arrays de objetos literales.
- Estas estructuras son las más apropiadas para representar un conjunto de objetos usualmente del mismo tipo, y poder trabajar con ellos de forma efectiva.
- Este orden permitirá trabajar con los datos de forma prolija, aprovechando métodos de búsqueda y transformación.
```js
// Creación de un array de objetos literales
const objetos = [
    { atributo1: valor1, atributo2: valor2 },
    { atributo1: valor3, atributo2: valor4 },
    { atributo1: valor5, atributo2: valor6 }
];

// Ejemplo de uso de console.table() para visualizar el array de objetos
console.table(objetos);
```

### Operaciones básicas con arreglos de objetos

Para acceder a un objeto específico del array, se utilizan corchetes ([ ]) junto al índice que le corresponde al objeto, para poder acceder al mismo y a sus propiedades.

Partiendo de un array de productos existente, se define una función para cargar nuevos productos. Esta función recibe los valores del nuevo producto por parámetro.

- Arma un objeto literal con los valores recibidos.
- Llama al método .push() y le envía como parámetro el nuevo producto a agregar.

### Objetos, arrays de elementos, arrays de objetos

En JavaScript, es recomendable declarar tanto objetos como arrays utilizando la palabra reservada `const`, en lugar de `let`. Esta práctica ayuda a prevenir la sobreescritura accidental del contenido del objeto o array en otras partes de la aplicación, asegurando la integridad de los datos. Además, sigue la buena práctica de programación que sugiere que cualquier valor que no deba cambiar su valor inicialmente asignado debe declararse como constante.

```js
// Ejemplo de array de productos existente
const productos = [
    { nombre: 'Producto 1', precio: 20 },
    { nombre: 'Producto 2', precio: 30 },
    { nombre: 'Producto 3', precio: 25 }
];

// Función para cargar nuevos productos al array
function cargarProducto(nombre, precio) {
    // Objeto literal con los valores recibidos
    const nuevoProducto = { nombre, precio };
    
    // Llama al método .push() para agregar el nuevo producto al array
    productos.push(nuevoProducto);
}

// Ejemplo de llamada a la función cargarProducto
cargarProducto('Producto 4', 35);
console.log(productos); // Verificar que el nuevo producto se agregó correctamente al array
```

# Ciclos de Iteración (Bucles)

En JavaScript, los ciclos de iteración son cláusulas que permiten realizar tareas repetitivas según la necesidad del programador. Estos ciclos se dividen en dos tipos:

1. **Ciclos de Iteración por Conteo**
2. **Ciclos de Iteración por Repetición**

#### Ciclos de Iteración por Conteo (for y for...of)

##### Ciclo for

El ciclo `for` es ideal para recorrer arreglos y realizar operaciones sobre sus elementos. Su estructura consta de tres parámetros configurables entre paréntesis:
1. Valor inicial
2. Condición
3. Incremento
```javascript
for (let i = 0; i < array.length; i++) {
    // Código a ejecutar en cada iteración
}
```

##### Ciclo for...of

El ciclo `for...of` proporciona una forma más simple de iterar sobre los elementos de un arreglo.

```js
for (const element of array) {
    // Código a ejecutar en cada iteración
}
```

#### Interrupción del Ciclo

- **Cláusula `break`**: Interrumpe el ciclo de iteración.
- **Cláusula `continue`**: Saltea una iteración en el ciclo.

#### Ciclos de Iteración por Repetición (while y do-while)

##### Ciclo while

El ciclo `while` repite un bloque de código mientras una condición sea verdadera.

```js
while (condición) {
    // Código a ejecutar mientras se cumpla la condición
}
```

##### Ciclo do-while

El ciclo `do-while` repite un bloque de código al menos una vez y luego evalúa la condición.
```js
do {
    // Código a ejecutar al menos una vez
} while (condición);
```
#### Diferencia entre while y do-while

La diferencia principal entre `while` y `do-while` radica en que el primero puede no ejecutarse si la condición inicialmente es falsa, mientras que el segundo se ejecuta al menos una vez antes de evaluar la condición.

#### Atención

Aunque los ciclos `while` y `do-while` pueden utilizarse para recorrer arreglos, es más efectivo utilizar las alternativas del ciclo `for`, especialmente `forEach()`, optimizada para este propósito.

#### Revisión

- Repasar el concepto de bucle.
- Mostrar datos de un arreglo con `for`.
- Mostrar datos de un arreglo con `while`.
- Mostrar datos de un arreglo con objetos que contengan propiedades.
- Trabajar en el Proyecto Integrador.
- Realizar las preguntas necesarias al docente antes de continuar.
