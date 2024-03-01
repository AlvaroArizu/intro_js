# Modulo 5
- ECMAScript 6
- CSS y JS
- Template String y Literals
- Arrow functios
- ES Moderno

# Declaración de variables en JavaScript

## Introducción
JavaScript se organiza en elementos del lenguaje, interfaces de intérprete, librerías y frameworks.

## ECMAScript 6
- Definición del lenguaje que aporta mejoras a JavaScript, como la integridad de datos y la gestión avanzada del ámbito.
- Introduce `const` y `let` para la declaración de variables.

## Declaración de variables
- En versiones anteriores, se usaba solo `var`, permitiendo reasignación y redefinición.
- Variables representan un espacio en memoria y pueden tener un dato actualmente guardado y un espacio reservado.
- `const` crea variables que no pueden ser reasignadas ni redefinidas.
- `let` permite reasignar variables, pero no redefinirlas.

## Promoción de la integridad de los datos
- `const` y `let` promueven la integridad de los datos al hacer el código más predecible.
- Ejemplo de la analogía con una orden en una oficina: Juan da una orden poco específica (como `var`), mientras que Santiago da una orden precisa (`const` y `let`).

## Tabla comparativa de las palabras reservadas
| Palabra reservada | Reasignar (cambiar valor) | Redefinir (cambiar posición) |
|--------------------|----------------------------|-------------------------------|
| const              | NO                         | NO                            |
| let                | SI                         | NO                            |
| var                | SI                         | SI                            |

Se recomienda utilizar `const` siempre que sea posible, `let` si se necesita reasignación y evitar `var` en ECMAScript 6.

```js
// Declaración de variables con const
const PI = 3.14159;
console.log(PI); // Output: 3.14159

// Intento de reasignación de variable constante (generará un error)
// PI = 3.14; // Error: Assignment to constant variable.

// Declaración de variables con let
let nombre = 'Juan';
console.log(nombre); // Output: Juan

// Reasignación de variable let
nombre = 'Santiago';
console.log(nombre); // Output: Santiago

// Declaración de variables con var
var edad = 30;
console.log(edad); // Output: 30

// Redefinición de variable var
var edad = 35;
console.log(edad); // Output: 35
```

# Introducción CSS y JS

Cuando se trabaja con elementos HTML desde JavaScript, no solo se puede leer y especificar su contenido, sino que también se puede manipular los estilos CSS de estos elementos. JavaScript proporciona dos opciones para manipular los estilos CSS fácilmente. Sin embargo, es importante tener en cuenta que cualquier manipulación de estilos CSS debe manejarse siempre desde CSS, y la intervención de JavaScript se limita a cambios pequeños que no pueden lograrse con CSS puro.

## La propiedad style

El objeto `HTMLElement Style` es un mecanismo técnico utilizado por los motores web para referenciar al DOM desde JavaScript. Este objeto básico, denominado Style, representa los estilos definidos para el DOM a través del mecanismo de interfaces. Aunque trabajar directamente sobre cada uno de los estilos definidos en los documentos CSS integrados a un sitio web puede ser un poco complejo, el objeto Style también forma parte del objeto document, lo que nos permite manipular los estilos de los elementos HTML una vez enlazados a ellos desde JavaScript.

### Objeto style

El objeto `style` permite acceder a los estilos de un elemento HTML con el documento como intermediario. Se pueden obtener los estilos de un elemento o sobreescribirlos. Es importante tener en cuenta que solo se sobreescribe la propiedad especificada y no las demás propiedades que pueda tener ese elemento. Además, estos estilos se agregan en línea y no de manera externa, ya que no se puede modificar una hoja externa de CSS con JavaScript.

- Cada propiedad CSS se trabaja desde JavaScript con el mismo nombre, pero las propiedades CSS con nombre combinado, separado por un guion (kebab-case), se transforman en propiedades (camelCase).
- Los valores asignados a cada propiedad CSS desde JavaScript deben encerrarse entre comillas.

# Acceso a Clases CSS

Prácticamente todos los elementos HTML dependen del uso de clases CSS para adquirir estilos, como colores, espacios, bordes y ubicación en pantalla, entre otros. JavaScript proporciona una serie de métodos dedicados que facilitan la interacción con estas clases.

## Acceso mediante className

La propiedad `className` permite acceder a las clases CSS de un elemento HTML. Se puede leer las clases CSS definidas, vaciar todas las clases de un elemento HTML o agregar una nueva a las existentes. Es importante dejar un espacio al agregar una nueva clase CSS para evitar que se pegue a la clase existente.

## Acceso mediante classList

La propiedad `classList` permite manejar las clases CSS de un elemento HTML como un array. A diferencia de `className`, que devuelve una cadena de texto con todas las clases, `classList` devuelve un array con cada una de las clases integradas en el elemento HTML. Esto facilita el acceso a las clases individuales y su manipulación.

### Métodos de classList

Existen varios métodos que facilitan realizar operaciones básicas sobre las clases CSS:

- `.add("nombre-clase")`: Agrega una clase CSS al elemento HTML.
- `.remove("nombre-clase")`: Remueve la clase CSS indicada del elemento HTML.
- `.toggle("nombre-clase")`: Si la clase CSS no se encuentra listada en el elemento HTML, la agrega; si se encuentra, la quita.
- `.replace("clase-vieja", "clase-nueva")`: Permite reemplazar una clase CSS por otra en el elemento HTML.

En todos los casos, el nombre de la clase CSS se define entre los paréntesis del método a utilizar, y se evita anteponer el punto (.).

Los beneficios de utilizar `classList` y sus métodos asociados incluyen un control más preciso sobre el CSS y la capacidad de aplicar pequeños cambios que no pueden ser controlados directamente por CSS, ya que forman parte de la lógica de una aplicación web.


# Template String + Literals

## Introducción al uso de template String + Literals

Hasta ahora, cuando se necesitaba intercalar contenido estático con contenido dinámico en JavaScript (JS), se utilizaba el operador `+` para concatenar texto y variables. Esta tarea puede volverse compleja, especialmente al trabajar con estructuras complejas como cards HTML, donde se necesita escribir varios elementos y manipular atributos.

El template String + Literals es una herramienta que simplifica esta tarea. Veamos cómo se utiliza.

### Ejemplo simple

Supongamos que tenemos un elemento HTML `<ul>` que queremos llenar con elementos dinámicos de un array en JS. Tradicionalmente, esto se haría con concatenación de strings, pero con template String + Literals se simplifica.

```javascript
const paises = ['Argentina', 'Brasil', 'Chile'];

const ul = document.querySelector('ul');
ul.innerHTML = '';
for (const pais of paises) {
    ul.innerHTML += `<li>${pais}</li>`;
}
```
En este ejemplo, vemos cómo se utiliza template String + Literals para intercalar contenido HTML con valores dinámicos de JS.

### Uso de template String + Literals en estructuras complejas

Cuando trabajamos con estructuras HTML más complejas, como cards de productos, la concatenación de strings puede volverse muy engorrosa. Aquí es donde template String + Literals brilla.
```JS
const productos = [
    { 
        titulo: 'Producto 1',
        descripcion: 'Descripción del producto 1',
        precio: 10.99,
        id: 'producto-1'
    },
    { 
        titulo: 'Producto 2',
        descripcion: 'Descripción del producto 2',
        precio: 15.99,
        id: 'producto-2'
    },
    // Más productos...
];

function generarCard(producto) {
    return `
        <div class="card">
            <h2>${producto.titulo}</h2>
            <p>${producto.descripcion}</p>
            <span>Precio: $${producto.precio}</span>
            <button id="${producto.id}">Agregar al carrito</button>
        </div>
    `;
}

const contenedor = document.querySelector('.contenedor');
productos.forEach(producto => {
    contenedor.innerHTML += generarCard(producto);
});
```

En este ejemplo, la función `generarCard` utiliza template String + Literals para crear dinámicamente una card HTML para cada producto en el array. Esto simplifica enormemente la generación de HTML dinámico y permite una mejor legibilidad del código.

### Ventajas obtenidas con Template String + Literals:
- Reutilización de propiedades/valores.
- Simplificación de código complejo, evitando concatenación de strings y facilitando la inserción de datos dinámicos.
- Generación de atributos HTML id dinámicos.

### Consideraciones
Es fundamental comprender que, en el desarrollo web, los datos son dinámicos y son manejados por JS. Por lo tanto, el HTML que los muestre debe ser dinámico, y para eso se utiliza Template String + Literals. Además, comprender esta técnica es crucial para entender conceptos como componentes en librerías y frameworks JS como React, Angular, Vue, Svelte, entre otros.

# Arrow functions
Las funciones flecha, o arrow functions, ofrecen una estructura moderna y ligeramente diferente, respecto a las funciones convencionales JavaScript. Además de aportar una estructura distinta a las funciones convencionales, integra algunas características de JavaScript moderno que simplifican su elaboración. Veremos a continuación cómo estructurarlas.

### Declaración
Las funciones flecha requieren ser declaradas con la palabra reservada `const`, para cumplimentar el mismo cuidado que debemos tener al declarar objetos, enlaces a elementos HTML, constantes, y toda aquella declaración de funcionalidades JS que necesitamos que no puedan ser sobreescritas, con otros valores.

### Arrow functions con parámetros
Cuando se deben utilizar parámetros, se definen tal como en una función convencional: dentro de sus paréntesis. Internamente los utilizamos de igual forma que con las funciones convencionales. En el ejemplo se observa también el uso de Template String + Literals sobre el valor resultante de la operación aritmética.

### Arrow functions con retorno
Y si debemos retornar valores o resultados con una arrow function, podemos aplicar también el mismo mecanismo que utilizamos con las funciones convencionales. Aunque también, estas nos ofrecen simplificar aún más su estructura. En el ejemplo se puede simplificar el retorno del resultado de la operación aritmética a una sola línea de código, y suprimir la creación innecesaria de una variable. Esto resume nuestra función, a una sola línea de código.

### Retorno implícito
Cuando una arrow function puede resolver una tarea con una sola línea de código, nos da la capacidad de suprimir las llaves de bloque que encierran su lógica, y de evitar utilizar la palabra reservada `return`. No es necesario aplicar arrow functions con retorno implícito que utilicen parámetros. También lo podemos hacer con funcionalidades que no requieren parámetros, tal como muestra el ejemplo.

Incluso las funciones flecha con retorno implícito son aplicables también en los Callbacks de los eventos, en lugar de tener que definir una función anónima.

```js
// Ejemplo de función convencional
function sumar(a, b) {
  return a + b;
}

// Ejemplo de arrow function con parámetros
const sumarArrow = (a, b) => {
  return a + b;
};

// Ejemplo de arrow function con retorno implícito
const sumarArrowImplicito = (a, b) => a + b;

// Llamadas a las funciones
console.log(sumar(2, 3)); // Output: 5
console.log(sumarArrow(2, 3)); // Output: 5
console.log(sumarArrowImplicito(2, 3)); // Output: 5
```

# La evolución de ECMAScript y JavaScript moderno
JavaScript nació en 1996 de la mano de Netscape Inc., creadora del navegador web Netscape. Posteriormente, se convirtió en un estándar regulado por ECMA International, lo que llevó a una evolución constante del lenguaje para adaptarse a las necesidades modernas.

### Evolución de ECMAScript

#### ES1
En 1997, ECMAScript versión 1 se estandarizó, lo que requirió que todos los navegadores web que admitieran JavaScript cumplieran con el estándar establecido por Ecma International.

#### Evolución y siguientes versiones

La evolución de ECMAScript ha sido continua, con importantes hitos como:
- ES5: Introducción de cambios funcionales dentro del lenguaje.
- ES6: Cambios significativos en el lenguaje, lanzado en 2015.
- Desde 2015, ECMAScript evoluciona a una nueva versión cada año.

### JavaScript moderno

Dentro de la revolución causada por ES6, algunas funcionalidades destacadas incluyen:
- `querySelector` y `querySelectorAll`.
- Manejo de eventos con `addEventListener`.
- Template String y el uso de backticks (\`\`).

Otras funcionalidades importantes son:
- Operador ternario.
- Operador lógico AND (`&&`).
- Operador lógico OR (`||`).
- Operador nullish coalescing (`??`).

### Operador ternario

El operador ternario simplifica la estructura de un `if - else` convencional en una sola línea de código.

### Operador lógico AND

Se utiliza para confirmar la evaluación positiva de dos condiciones dentro de un bloque `if`.

### Operador lógico OR

Permite evaluar el cumplimiento de una condición u otra, simplificando estructuras de asignación de valores.

### Operador nullish coalescing

Similar al operador lógico AND, pero acepta solo valores `null` o `undefined`.

### Conclusión

Estos operadores modernos fueron introducidos desde ES6 en 2015 y son ampliamente utilizados en el mercado laboral actual y en los frameworks JS modernos.

Es importante familiarizarse con ellos y estar al tanto de la evolución continua de JavaScript.

```js
// Ejemplo de operador ternario
const edad = 20;
const mensaje = edad >= 18 ? "Eres mayor de edad" : "Eres menor de edad";
console.log(mensaje);

// Ejemplo de operador lógico AND
const tieneDinero = true;
const tieneTarjeta = true;
if (tieneDinero && tieneTarjeta) {
  console.log("Puedes comprar ese artículo");
} else {
  console.log("No puedes comprar ese artículo");
}

// Ejemplo de operador lógico OR
const nombre = "";
const nombreUsuario = nombre || "Usuario Anónimo";
console.log(nombreUsuario);

// Ejemplo de operador nullish coalescing
const valor = null;
const valorPorDefecto = valor ?? "Valor por defecto";
console.log(valorPorDefecto);
```
Estos ejemplos ilustran el uso de los operadores ternario, lógico AND, lógico OR y nullish coalescing en JavaScript. Puedes copiar y pegar este código en un archivo .js y ejecutarlo en un entorno de desarrollo para ver los resultados.
