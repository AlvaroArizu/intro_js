# Modulo 4
- Intro a HTML
- Metodos de acceso a HTML
- Eventos
- Funciones 

### HTML DOM

HTML es el lenguaje de marcado más utilizado para la construcción de páginas web. La sigla HTML significa Hyper Text Markup Language (lenguaje de marcado de hipertexto). No es un lenguaje de programación, sino de marcas con sentido, a las que llamamos: etiquetas o Tags. Las etiquetas le indican al navegador qué es lo que debe mostrar en pantalla.

#### Inicios de HTML

HTML tuvo dos versiones iniciales en los 90's y en 2008 nació la especificación de HTML5. Esta versión simplificó la estructura de etiquetas y mejoró la velocidad de carga en los navegadores web.

#### Etiquetas (tags) HTML

Existen diversas etiquetas en HTML para definir la estructura y el contenido de una página web, como `<h1>` hasta `<h6>` para títulos, `<p>`, `<span>`, `<strong>`, `<em>`, `<code>` para texto, `<img>`, `<audio>`, `<video>` para multimedia, `<div>` como contenedor, `<input>` para cajas de texto, y `<button>` para botones.

#### ¿Qué es CSS?

CSS es el lenguaje de estilos gráficos que permite personalizar HTML en detalle, añadiendo estilos de diseño, color, transiciones, animaciones y adaptabilidad a diferentes dispositivos.

#### Entornos de trabajo

Existen frameworks y microframeworks CSS como Bootstrap, Bulma, Tailwind y Milligram, que permiten cambiar el diseño de una página web con facilidad.

#### JavaScript y el DOM HTML

JavaScript cuenta con un objeto llamado document, que proporciona herramientas para acceder, leer, modificar y generar elementos HTML. Para interactuar con el DOM, se debe configurar el archivo JS dentro del documento HTML con el atributo defer.

#### defer

El atributo defer en el tag `<script>` espera a que todo el documento HTML se cargue en el navegador web antes de interpretar el código JavaScript, lo que mejora el SEO y la estructura del documento.

#  Métodos de acceso a HTML

Los tres métodos convencionales para acceder a elementos HTML desde JavaScript son:

- `getElementById("id")`: Permite acceder a un elemento HTML por su ID.
- `getElementsByTagName("tag")`: Permite acceder a un conjunto de elementos HTML del mismo tipo.
- `getElementsByClassName("class")`: Permite acceder a un conjunto de elementos HTML que comparten una misma clase.

### Propiedades de acceso a HTML

Las tres propiedades más utilizadas para manipular el contenido de elementos HTML son:

- `innerText`: Permite acceder al texto dentro del elemento HTML.
- `textContent`: Proporciona el mismo resultado que `innerText`, pero es más claro en cuanto a su funcionalidad.
- `innerHTML`: Permite leer y escribir bloques de código HTML en un elemento.

### El método `querySelector`

CSS utiliza selectores para personalizar estilos gráficos. `querySelector` enlaza con elementos HTML a través de diferentes opciones, evitando la necesidad de agregar un ID único a cada elemento.

### Trabajar con múltiples elementos HTML desde JS

Los métodos `getElementsByTagName`, `getElementsByClassName` y `querySelectorAll` permiten enlazar con múltiples elementos HTML:

- `getElementsByTagName`: Genera una colección de elementos del mismo tipo.
- `getElementsByClassName`: Retorna una colección de elementos que comparten una clase.
- `querySelectorAll`: Ofrece la misma funcionalidad que los anteriores, pero con mayor precisión en la selección.

### Resumen: el DOM HTML desde JavaScript

- El DOM HTML es manipulable desde JavaScript para generar contenido dinámico.
- Los archivos JavaScript deben tener el atributo `defer` y ser referenciados dentro del `head` del documento HTML.
- Los métodos `getElementById` y `querySelector` permiten enlazar con elementos HTML.
- Las propiedades `innerText`, `textContent` e `innerHTML` permiten interactuar con el texto y el contenido HTML de los elementos.
- `getElementsByTagName`, `getElementsByClassName` y `querySelectorAll` permiten enlazar con múltiples elementos HTML.

### Eventos en Desarrollo Web

En una aplicación de software, los eventos se refieren a la interacción entre el usuario y el software. En desarrollo web, los eventos pueden incluir:

- Scroll del usuario por la página.
- Clic en botones y puntos de menú.
- Escribir datos en un formulario web.
- Subir o descargar archivos.
- Reproducir audio o video, entre otros.

### Categorías de Eventos

Los eventos en desarrollo web se pueden categorizar en:

- **Mouse**: Eventos asociados al puntero del mouse, incluyendo clic, doble clic, entre otros.
- **Teclado**: Eventos relacionados con la pulsación de teclas.
- **Formulario**: Eventos que ocurren en elementos de formularios web, como focus, blur, submit, etc.
- **Navegador**: Eventos que ocurren en el navegador, como scroll, resize, load, etc.

### Manejo de Eventos en JavaScript

Hay varias formas de manejar eventos en JavaScript:

1. **Atributos `on`**: Se definen dentro de los elementos HTML y se asocian con una función que se ejecuta cuando ocurre el evento.
2. **Eventos `on`**: Son una evolución de los atributos `on` y se manejan íntegramente desde JavaScript.
3. **`addEventListener`**: Método que permite agregar event listeners a elementos HTML y manejar los eventos de manera más efectiva y amplia.

### Funciones Anónimas

Las funciones anónimas son aquellas que no tienen nombre y se pueden asignar directamente a eventos. Son útiles para asociar una función a un evento específico sin definir un nombre para la función.

### Asignar Múltiples Eventos

Cuando se tienen múltiples elementos que requieren el mismo evento, se pueden asignar eventos múltiples a partir de un mismo código. Esto se puede lograr utilizando métodos como `getElementsByClassName` o `querySelectorAll` para seleccionar los elementos y luego asignar eventos de forma dinámica.

### Revisión

- Repasar el concepto de evento.
- Investigar todos los eventos posibles en desarrollo web.
- Combinar funciones con eventos para manejar interacciones.
- Integrar bucles para reutilizar funciones de manera eficiente.
- Trabajar en proyectos prácticos para aplicar los conocimientos adquiridos.

### Funciones en JavaScript

#### Concepto
Una función en JavaScript es un bloque de código reutilizable que realiza una tarea específica. Puede aceptar entradas, llamadas argumentos, y devuelve un resultado.

#### Definición
Para definir una función, se utiliza la palabra reservada `function`, seguida de un nombre, paréntesis para los parámetros, y llaves para el cuerpo de la función.

#### Características
- Debe expresar una acción.
- Debe comenzar con un verbo y en modo imperativo.
- Puede tener nombres simples o compuestos.
- Se ejecuta solo cuando es llamada.

#### Funciones con Parámetros
Las funciones pueden recibir uno o más parámetros, que son variables internas que contienen los valores que la función manipula.

#### Control de Valores No Definidos
Es importante establecer valores predeterminados para los parámetros de una función para evitar errores cuando no se les pasa un valor válido.

#### Funciones con Retorno
Las funciones con retorno permiten realizar operaciones y devolver un resultado mediante la palabra reservada `return`. Este valor puede ser utilizado en otras partes del código.

#### Ámbito de las Variables (Scope)
JS tiene variables globales y locales. Las variables locales solo pueden ser utilizadas dentro de su ámbito, como una función. Se pueden tener variables con el mismo nombre en diferentes ámbitos sin afectarse mutuamente.

#### Revisión
- Repasar el concepto de función.
- Estudiar cómo trabajar con parámetros desde una función.
- Entender cómo definir correctamente el ámbito de una variable.

```js
// Definición de una función sin parámetros y sin retorno
function saludar() {
  console.log("¡Hola!");
}

// Llamada a la función
saludar(); // Output: ¡Hola!

// Definición de una función con parámetros y sin retorno
function sumar(a, b) {
  console.log(a + b);
}

// Llamada a la función con argumentos
sumar(5, 3); // Output: 8

// Definición de una función con parámetros y retorno
function multiplicar(x, y) {
  return x * y;
}

// Llamada a la función con argumentos y almacenamiento del resultado
let resultado = multiplicar(4, 6);
console.log(resultado); // Output: 24

// Definición de una función con parámetros predeterminados
function saludarPersona(nombre = "amigo") {
  console.log("¡Hola, " + nombre + "!");
}

// Llamada a la función con y sin argumentos
saludarPersona(); // Output: ¡Hola, amigo!
saludarPersona("Juan"); // Output: ¡Hola, Juan!
```
Estos ejemplos ilustran diferentes aspectos de las funciones en JavaScript, como la definición con y sin parámetros, el uso de retorno de valores y la asignación de valores predeterminados para los parámetros.
