Taller de Nivelación Curso Desarrollo Web Frontend

El presente taller tiene el propósito de evaluar la comprensión y aplicación de conceptos fundamentales del desarrollo web Frontend desde los conceptos de lógica de programación, HTML, CSS, JavaScript, React Js, los diferentes tipos de Hooks, su uso adecuado y cómo utilizar React Router DOM v6 para la navegación en una aplicación React. Se busca nivelar y asegurar la apropiación de los conceptos vistos hasta el momento en el curso de desarrollo web frontend, la implementación de ReactJS y sus tecnologías asociadas.

MÓDULO SOBRE LÓGICA, LÓGICA DE PROGRAMACIÓN Y PROGRAMACIÓN CON JAVASCRIPT

Preguntas teóricas

1.	¿Qué es la lógica en el contexto de la programación? Y explicar por qué es importante en el desarrollo web Frontend.

La lógica se refiere al modo en que un programa toma decisiones y realiza acciones basándose en reglas lógicas. En el desarrollo web front-end, es importante en la interacción con el usuario, la manipulación de datos, la validación de entradas, la gestión de eventos, el enrutamiento y la optimización de las páginas.

2.	Definir el concepto de “algoritmo” y proporcionar un ejemplo sencillo de un algoritmo relacionado con la lógica de programación.

	Un algoritmo es un conjunto finito y ordenado de pasos que describen cómo resolver un problema o realizar una tarea concreta. Los algoritmos son una parte fundamental de la lógica de programación y se utilizan para diseñar soluciones eficaces en informática.
Ejemplo: Hacer un algoritmo que me determine si un numero es par o impar:
•	Inicio
•	Ingresa un numero entero
•	Divide el número entre 2
•	Si el residuo de la división es igual a 0, muestra "El número es par".
•	Si el residuo de la división no es igual a 0, muestra "El número es impar".
•	Fin.


	
3.	¿Qué son estructuras de control en la programación?, ¿Cuáles son los tipos de estructuras de control y las estructuras más comunes de cada tipo?, Describir al menos dos tipos de estructura de control, explicar por qué son importantes y proporcionar ejemplos de cada uno de cómo se utilizan en el desarrollo web Frontend.

Una estructura de control es un bloque de código que permite al programador determinar y controlar el flujo de ejecución de un programa. Los tipos más comunes son:
	Estructuras de control condicionales:

•	if: Permite ejecutar un bloque de código si una condición es verdadera.
Ejemplo:
if (edad >= 18) {
    console.log("Eres mayor de edad");
} else {
    console.log("Eres menor de edad");
	}

•	switch: Permite elegir entre múltiples casos basados en una expresión.
	Ejemplo:
	switch (díaDeLaSemana) {
   	 	case "Lunes":
        			console.log("Hoy es lunes");
        			break;
    		case "Martes":
       			 console.log("Hoy es martes");
       			 break;
    		default:
       			console.log("No sé qué día es.");
	}

Estructuras de control de bucle:

•	for: Se utiliza para repetir un bloque de código un número específico de veces.

Ejemplo de for:
for (let i = 0; i < 5; i++) {
    console.log("Iteración " + i);
}

•	while: Permite repetir un bloque de código mientras se cumple una condición.
	
	let contador = 0;
	while (contador < 3) {
   		 console.log("Contador: " + contador);
   		 contador++;
	}

	


4.	Describir cómo se declaraban variables y constantes en JavaScript antes de la introducción de ECMAScript 6 (ES6). Explicar cómo ES6 mejoró la declaración de variables y constantes, y mencionar los problemas que esta mejora resuelve en el desarrollo web Frontend.

	Antes de ES6, JavaScript utilizaba var para variables con problemas de ámbito y const para restricciones de objeto; ES6 introdujo let para el ámbito de bloque, mejoró const, resolvió los problemas de ámbito y permitió constantes más seguras. más seguras. Estas mejoras hacen que el código sea más claro y fácil de mantener para el desarrollo web front-end.
	
5.	¿Cómo se declaran las funciones en JavaScript y cuál es la diferencia entre una declaración de función, una expresión de función y una función de flecha (arrow function)? Proporcionar ejemplos de cada una.

Declaración de función:
function suma(a, b) {
  return a + b;
	}

	Expresión de función:
	const suma = function(a, b) {
 		return a + b;
	};

	Función flecha:
	const suma = (a, b) => a + b;

Sus diferencias radican en su sintaxis, ya que cada tipo es diferente en su escritura, en su contexto ya que Declaración de función y expresión de función tienen su propio   this y la función flecha no tiene su propio this; toma el this del contexto en el que se encuentra.
	
6.	¿Por qué es necesario el uso de funciones en el desarrollo web Frontend? Enumerar al menos tres razones fundamentales y proporcionar ejemplos de situaciones en las que las funciones son esenciales. Además, mencionar la ventaja de las funciones flecha en el contexto de estas razones.

Reutilización de código: Las funciones permiten definir bloques de código que pueden ser llamados y ejecutados varias veces. Ejemplo: una función que valida formularios en distintas partes de un sitio web.
Organización del código: Facilitan la estructuración y mantenimiento del código al dividirlo en funciones específicas para realizar tareas particulares. Ejemplo: funciones para manejar la lógica de presentación, como cambiar estilos o manipular el DOM.
Abstracción y encapsulamiento: Las funciones permiten ocultar detalles de implementación y exponer solo la interfaz necesaria, mejorando la modularidad. Ejemplo: una función que realiza peticiones AJAX para obtener datos, abstracta los detalles de la implementación.

Funciones flecha:
•	Sintaxis concisa: Ayudan a reducir la cantidad de código y a hacerlo más legible.
•	Contexto léxico: Mantienen el valor de this del ámbito circundante, evitando problemas comunes. Ejemplo: en funciones de callback dentro de eventos.


7.	¿Cuál es la diferencia entre parámetro y argumento?
	Parámetro: Es una variable en la declaración de una función. Representa un valor que la función espera recibir cuando se llama. Los parámetros son nombres de variables dentro de la definición de la función. En el siguiente ejemplo a y b son parámetros

function sumar(a, b) {
    return a + b;
}

Argumento: Es el valor real que se pasa a la función cuando se la invoca. Son los valores concretos que se asignan a los parámetros durante la llamada a la función. En el siguiente ejemplo 3 y 5 son argumentos que se pasan a la función sumar

var resultado = sumar(3, 5);
	
8.	Definir el concepto de Callback y proporcionar un ejemplo práctico.

	Un callback es una función que se pasa como argumento a otra función y que se ejecutará después de que algún evento o tarea específica haya ocurrido. Es comúnmente utilizado en situaciones asincrónicas, como operaciones de entrada/salida, para manejar la finalización de una tarea.

function hacerPeticionAsync(callback) {
    setTimeout(function() {
        console.log("La operación asíncrona ha terminado");
        callback(); // Llamada al callback después de la operación
    }, 2000); // Simulando un retardo de 2 segundos
}
	hacerPeticionAsync(function() {
    console.log("El callback ha sido ejecutado");
});
En este ejemplo, hacerPeticionAsync simula una operación asíncrona y recibe una función como argumento (callback). Después de que la operación asíncrona (simulada mediante setTimeout) se completa, se ejecuta la función de callback proporcionada. Esto es útil para manejar tareas después de que una operación asíncrona haya finalizado.

9.	¿Qué es el hoisting en JavaScript y cómo afecta a las variables y funciones? Proporcionar ejemplos de hoisting en declaraciones de variables y funciones.
Hoisting en JavaScript: El hoisting es un comportamiento en JavaScript donde las declaraciones de variables y funciones son elevadas (movidas) al inicio de su contexto de ejecución durante la fase de compilación, antes de que el código se ejecute. Sin embargo, es importante destacar que solo la declaración es elevada, no la inicialización.
Ejemplo en Variables:
console.log(x); // Salida: undefined
var x = 5;
console.log(x); // Salida: 5

Ejemplo en Funciones:
saludar(); // Salida: "Hola, Mundo!"

function saludar() {
    console.log("Hola, Mundo!");
}

10.	Definir brevemente el concepto de objeto en JavaScript y cuál es la visión general sobre este concepto. Indicar, también cómo se declaran estas estructuras de datos.
	
	En JavaScript, un objeto es una estructura de datos que permite almacenar y organizar información mediante pares clave-valor. Las claves son cadenas o símbolos, y los valores pueden ser cualquier tipo de dato, incluyendo otros objetos.

// Declaración de objeto vacío
var persona = {};

// Declaración de objeto con propiedades
var estudiante = {
    nombre: 'Juan',
    edad: 20,
    estudiar: function() {
        console.log('Estudiando...');
    }
};

// Acceso a propiedades y método
console.log(estudiante.nombre); // Salida: 'Juan'
estudiante.estudiar(); // Salida: 'Estudiando...'


11.	¿Qué son propiedades?, y ¿Cuál es la diferencia entre una propiedad y un método en un objeto?
Las propiedades en un objeto son pares clave-valor que almacenan datos asociados con el objeto. La clave (también llamada nombre de la propiedad) es una cadena o un símbolo, y el valor puede ser cualquier tipo de dato, incluyendo otros objetos. Las propiedades permiten almacenar información de manera estructurada dentro de un objeto.
Propiedad: Representa un valor asociado con una clave en un objeto. Es esencialmente una variable que pertenece al objeto. Se accede a las propiedades utilizando notación de punto (objeto.propiedad) o notación de corchetes (objeto['propiedad']). Ejemplo:
var persona = {
    nombre: 'Ana',
    edad: 25
};


	Método: Es una función asociada a un objeto. Mientras que una propiedad almacena datos, un método realiza acciones específicas o lleva a cabo operaciones en el objeto. Se accede a los métodos utilizando notación de punto. Ejemplo:
var calculadora = {
    sumar: function(a, b) {
        return a + b;
    }
};


12.	Explicar las dos formas de acceder a una propiedad de objetos e indicar las situaciones en que conviene usar una manera sobre la otra.
	Notación de punto (objeto.propiedad):

	var persona = {
    nombre: 'Carlos',
    edad: 30
};

	console.log(persona.nombre); // Salida: 'Carlos'

	Notación de corchetes (objeto['propiedad']):

	var persona = {
    nombre: 'Ana',
    edad: 25
};

var propiedad = 'nombre';
console.log(persona[propiedad]); // Salida: 'Ana'
	
13.	¿Existe alguna forma de recorrer las propiedades de un objeto? En caso negativo, explicar por qué no es posible y en caso positivo proporcionar un ejemplo. Mencionar una situación en la cual sea muy útil recorrer las propiedades de un objeto.

	Sí, es posible recorrer las propiedades de un objeto en JavaScript. Una manera común de hacerlo es utilizando bucles, como el bucle for...in. Este bucle itera sobre todas las propiedades enumerables de un objeto, incluyendo aquellas heredadas de su prototipo. Ejemplo:

	var persona = {
    nombre: 'Juan',
    edad: 25,
    ciudad: 'Barcelona'
};

for (var propiedad in persona) {
    console.log(propiedad + ': ' + persona[propiedad]);
}
En este ejemplo, el bucle for...in recorre todas las propiedades del objeto persona, y en cada iteración, imprime el nombre de la propiedad y su valor.

14.	¿Por qué son útiles los objetos en la programación web y qué tipos de datos pueden almacenar?

1.	Organización de datos: Los objetos permiten organizar y estructurar datos de manera más clara y comprensible. Puedes agrupar información relacionada bajo un solo nombre de objeto, facilitando la gestión y manipulación de datos complejos.
2.	Flexibilidad: Los objetos en JavaScript son dinámicos y pueden ser modificados fácilmente. Puedes agregar, modificar o eliminar propiedades en cualquier momento, lo que proporciona flexibilidad en la manipulación de datos a medida que evoluciona la aplicación.
3.	Modelado de entidades: En el desarrollo web, los objetos son ideales para modelar entidades del mundo real

Tipos de datos que pueden almacenar: Los objetos en JavaScript pueden almacenar una variedad de tipos de datos, incluyendo:
•	Cadenas (Strings): Para representar texto.
•	Números (Numbers): Para almacenar valores numéricos.
•	Booleanos: Para representar valores de verdadero o falso.
•	Arrays: Pueden ser utilizados como valores de propiedad para almacenar listas de datos.
•	Funciones: Pueden ser asignadas como propiedades, permitiendo la creación de métodos dentro del objeto.

15.	¿Qué es un array en JavaScript y por qué son esenciales?

Un array en JavaScript es una estructura que almacena elementos bajo un solo nombre, permitiendo acceso por índices. Son esenciales por su capacidad para organizar datos, facilitar el acceso y manipulación eficiente, admitir operaciones iterativas, proporcionar flexibilidad dinámica y permitir estructuras de datos complejas. Ejemplo:

	var miArray = [1, 2, 3, 4];
console.log(miArray[2]); // Salida: 3

16.	¿Cómo acceder a un elemento dentro de un array? Explicar con un ejemplo.

Puedes acceder a un elemento dentro de un array mediante su índice. El índice representa la posición del elemento en el array, comenzando desde 0. Ejemplo:

var colores = ['rojo', 'verde', 'azul'];
var segundoColor = colores[1];
console.log(segundoColor); // Salida: 'verde'
	
17.	Mencionar al menos tres funciones de arrays y describir su utilidad en la programación web.

	map():
Crea un nuevo array con los resultados de llamar a una función proporcionada en cada elemento del array original.

var numeros = [1, 2, 3];
var duplicados = numeros.map(function(numero) {
    return numero * 2;
});
// Resultado: [2, 4, 6]

	filter():
Crea un nuevo array con todos los elementos que cumplan cierta condición proporcionada por una función.

var edades = [18, 25, 16, 30, 22];
var mayoresDeEdad = edades.filter(function(edad) {
    return edad >= 18;
});
// Resultado: [18, 25, 30, 22]

	reduce():
Aplica una función acumuladora a cada elemento del array (de izquierda a derecha) para reducirlo a un único valor.

var numeros = [1, 2, 3, 4];
var suma = numeros.reduce(function(acumulador, numero) {
    return acumulador + numero;
}, 0);
// Resultado: 10
	
18.	Proporcionar un ejemplo de cómo se utiliza una función de array para transformar y filtrar datos en un array.
var libros = [
    { titulo: 'Cien años de soledad', año: 1967 },
    { titulo: 'El señor de los anillos', año: 1954 },
    { titulo: 'Código Da Vinci', año: 2003 },
    { titulo: 'Sapiens', año: 2014 },
    { titulo: '1984', año: 1949 }
];

// Filtrar libros publicados después de 2010 y extraer sus títulos
var librosRecientes = libros
    .filter(function(libro) {
        return libro.año > 2010;
    })
    .map(function(libro) {
        return libro.titulo;
    });

console.log(librosRecientes);
// Resultado: ['Sapiens']

Preguntas prácticas

1.	Escribir un programa con JavaScript que resuelva el siguiente problema: Dada una lista (o array) de números enteros, encontrar el número más grande de la lista y mostrarlo en consola. No se debe usar la función Math.max(), ni .forEach().


	function encontrarNumeroMasGrande(lista) {
    // Verificar si la lista no está vacía
    if (lista.length === 0) {
        console.log("La lista está vacía.");
        return;
    }

    // Inicializar la variable para almacenar el número más grande
    var numeroMasGrande = lista[0];

    // Iterar a través de la lista para encontrar el número más grande
    for (var i = 1; i < lista.length; i++) {
        if (lista[i] > numeroMasGrande) {
            numeroMasGrande = lista[i];
        }
    }

    // Mostrar el resultado en consola
    console.log("El número más grande es: " + numeroMasGrande);
}

// Ejemplo de uso
var numeros = [15, 3, 7, 22, 11, 8];
encontrarNumeroMasGrande(numeros);

2.	Escribir una función en JavaScript que tome dos números como argumentos y devuelva su suma. Luego, escribir la misma función utilizando una función flecha (arrow function) y comparar ambas declaraciones. Llamar a ambas funciones con valores de ejemplo y mostrar los resultados en la consola del navegador.

Función Tradicional:
function sumarNumeros(a, b) {
    return a + b;
}

// Llamada de ejemplo
var resultadoTradicional = sumarNumeros(5, 7);
console.log("Resultado (tradicional): " + resultadoTradicional);

Función Flecha:
const sumarNumerosFlecha = (a, b) => a + b;

// Llamada de ejemplo
var resultadoFlecha = sumarNumerosFlecha(5, 7);
console.log("Resultado (flecha): " + resultadoFlecha);

3.	Escribir una función en JavaScript que reciba un array de números como argumento y utilizar la función de array para calcular la suma de todos los números pares en el array. Luego, llamar a la función con un array de ejemplo y mostrar el resultado en la consola del navegador.


function sumarNumerosPares(array) {
    var sumaPares = array.reduce(function (acumulador, numero) {
        if (numero % 2 === 0) {
            return acumulador + numero;
        } else {
            return acumulador;
        }
    }, 0);
    console.log("La suma de los números pares es: " + sumaPares);
}

var numerosEjemplo = [1, 2, 3, 4, 5, 6, 7, 8, 9, 10];
sumarNumerosPares(numerosEjemplo);


MÓDULO SOBRE HTML, CSS Y RESPONSIVE DESIGN

Preguntas teóricas

1.	¿Qué significa HTML y cuál es su función en el desarrollo web?
HTML significa "Hypertext Markup Language" (Lenguaje de Marcado de Hipertexto). Su función principal en el desarrollo web es estructurar el contenido de una página. Define elementos y etiquetas que indican la función de cada parte del contenido, como encabezados, párrafos, enlaces y más. HTML actúa como el esqueleto de una página web, proporcionando la base para la presentación y organización del contenido.
	
2.	¿Cuál es la estructura básica de un documento HTML? Describir las etiquetas esenciales.

•	<!DOCTYPE html>: Declaración que define la versión de HTML que se está utilizando.
•	<html>: Contenedor principal que engloba todo el contenido de la página.
•	<head>: Sección que contiene información sobre el documento, como metadatos, enlaces a hojas de estilo y scripts.
•	<meta charset="utf-8">: Define la codificación de caracteres (UTF-8) para admitir caracteres especiales.
•	<title>: Define el título de la página, visible en la barra de título del navegador.
•	<body>: Contenedor que alberga el contenido visible de la página, como texto, imágenes, enlaces, etc.

3.	¿Qué es CSS y cuál es su propósito en el desarrollo web?

	CSS significa "Cascading Style Sheets" (Hojas de Estilo en Cascada). Su propósito en el desarrollo web es definir y controlar el aspecto visual de las páginas HTML. CSS separa la presentación del contenido, permitiendo el diseño consistente y la adaptabilidad a diferentes dispositivos. Con CSS, se pueden aplicar estilos como colores, fuentes, márgenes y diseños, mejorando la estética y la usabilidad de una página web.






4.	¿Qué son selectores CSS, cuáles son los principales tipos de selectores y porqué es importante entender la especificidad en el contexto de las hojas de estilo en cascada (CSS)? Describir al menos tres tipos de selectores CSS y cómo la especificidad afecta a la aplicación de estilos en un proyecto de desarrollo web Frontend. Proporcionar ejemplos de situaciones en las que se utiliza la especificidad de selectores para resolver conflictos de estilos.

	Selectores CSS: Los selectores CSS son patrones que seleccionan elementos HTML a los que se les aplicarán estilos.
Principales tipos de selectores:
1.	Selectores de tipo: Seleccionan elementos por su nombre (ej. p selecciona todos los párrafos).
2.	Selectores de clase: Seleccionan elementos por su clase (ej. .clase selecciona elementos con esa clase).
3.	Selectores de id: Seleccionan elementos por su id (ej. #identificador selecciona un elemento con ese id).
Especificidad en CSS: Especificidad determina qué estilo se aplica cuando hay conflictos. Se mide en términos de selecciones y reglas.

Resolución de conflictos:
•	Regla general: Mayor especificidad gana.
•	Importancia: !important anula otras reglas.
•	Orden: La última regla se aplica en caso de igualdad de especificidad.

	p { color: blue; }
.clase { color: red !important; }
#identificador { color: green; }

5.	Explicar las diferencias entre los estilos en línea (inline), estilos internos (embedded) y estilos externos (external) en CSS. Indicar cuál de los tres estilos es el recomendado usar y por qué.
	Estilos en línea (Inline):
•	Definidos directamente en la etiqueta HTML mediante el atributo style.
•	Se aplican solo a ese elemento específico.
•	Ejemplo: <p style="color: blue;">Texto</p>.
Estilos internos (Embedded):
•	Definidos dentro del documento HTML, en la sección <style> del elemento <head>.
•	Se aplican a elementos específicos o a toda la página.
•	Ejemplo:
<head>
    <style>
        p { color: red; }
    </style>
</head>
	Estilos externos (External):
•	Definidos en archivos CSS separados.
•	Se aplican a múltiples páginas y facilitan el mantenimiento.
•	Se enlazan al documento HTML mediante la etiqueta <link>.
•	Ejemplo:
<head>
    <link rel="stylesheet" href="estilos.css">
</head>

	Recomendación:
Estilos externos: Son recomendados debido a su capacidad de reutilización, mantenimiento simplificado y la posibilidad de aplicar estilos consistentes en múltiples páginas. Favorecen la separación de preocupaciones (CSS separado del HTML), mejorando la legibilidad y escalabilidad del código.

6.	¿Qué es flexbox y cómo se utiliza para el diseño de páginas web?

	Flexbox es un modelo de diseño en CSS que facilita la creación de diseños más eficientes y flexibles en una página web. Permite distribuir espacio entre elementos de manera dinámica y alinea los elementos de manera automática.

Contenedor Flex:
•	Aplicar display: flex; o display: inline-flex; al contenedor padre.

	Propiedades del Contenedor:
•	flex-direction: Define la dirección de los elementos (fila o columna).
•	justify-content: Alinea los elementos en el eje principal.
•	align-items: Alinea los elementos en el eje secundario.
	
7.	Explicar cómo se emplean las propiedades flexbox y explicar la función de las principales propiedades en la creación de diseños flexibles.

	
Propiedades de Flexbox:
1.	display:
•	Uso: display: flex; o display: inline-flex; en el contenedor.
•	Función: Define el contexto flex para los elementos hijos directos.
2.	flex-direction:
•	Uso: flex-direction: row | row-reverse | column | column-reverse;
•	Función: Establece la dirección de los elementos en el contenedor (fila o columna).
3.	justify-content:
•	Uso: justify-content: flex-start | flex-end | center | space-between | space-around | space-evenly;
•	Función: Alinea los elementos en el eje principal del contenedor.
4.	align-items:
•	Uso: align-items: stretch | flex-start | flex-end | center | baseline;
•	Función: Alinea los elementos en el eje secundario del contenedor.
5.	align-self:
•	Uso: align-self: auto | flex-start | flex-end | center | baseline | stretch;
•	Función: Permite que un elemento anule la alineación establecida por align-items.

6.	flex:
•	Uso: flex: grow shrink basis; (p. ej., flex: 1 0 auto;).
•	Función: Define la capacidad de crecimiento, contracción y tamaño inicial del elemento.

8.	¿Qué es CSS Grid Layout y en qué se diferencia de flexbox?

	CSS Grid Layout es un sistema de diseño bidimensional en CSS que permite organizar elementos en filas y columnas, creando estructuras de diseño más complejas. Proporciona un control preciso sobre el diseño de la página y facilita la creación de diseños de tipo cuadrícula.
Diferencias con Flexbox:
1.	Orientación:
•	Flexbox: Diseño unidimensional, ya sea en fila o columna.
•	Grid Layout: Diseño bidimensional, con filas y columnas.
2.	Estructura:
•	Flexbox: Centrado en la distribución del espacio a lo largo de un solo eje.
•	Grid Layout: Ofrece control tanto en el eje de las filas como en el de las columnas simultáneamente.
3.	Control de Espacio:
•	Flexbox: Ideal para distribuir espacio a lo largo de un eje.
•	Grid Layout: Permite distribuir espacio en ambas direcciones, proporcionando mayor control sobre el diseño general de la página.
4.	Aplicación:
•	Flexbox: Útil para estructuras más simples o para alinear elementos en un solo eje.
•	Grid Layout: Más adecuado para estructuras de diseño complejas, como cuadrículas y disposiciones bidimensionales.

9.	Proporcionar un ejemplo de cómo crear una cuadrícula sencilla con CSS Grid.

.contenedor-grid {
    display: grid;
    grid-template-rows: 100px 100px;
    grid-template-columns: 1fr 2fr; 
    gap: 10px; 
}

.elemento-grid {
    background-color: #3498db; 
    color: #fff; 
    padding: 20px; 
    text-align: center; 
}

.elemento-grid-especial {
    grid-row: 1 / 3; 
    grid-column: 2; 
}

<!-- Estructura HTML -->
<div class="contenedor-grid">
    <div class="elemento-grid">1</div>
    <div class="elemento-grid">2</div>
    <div class="elemento-grid elemento-grid-especial">3</div>
    <div class="elemento-grid">4</div>
</div>


10.	¿Qué significa el diseño responsivo en el contexto del desarrollo web?
Diseño responsivo en desarrollo web implica crear sitios web que se adapten y respondan de manera óptima a diferentes tamaños de pantalla y dispositivos, como computadoras de escritorio, tablets y teléfonos móviles. La meta es proporcionar una experiencia de usuario consistente y agradable independientemente del dispositivo utilizado.
	
11.	Enumerar al menos tres técnicas o estrategias utilizadas para lograr el diseño responsivo en una página web.

	Media Queries:
•	Utilizar @media queries en las hojas de estilo CSS para aplicar estilos específicos según características del dispositivo, como el ancho de la pantalla.
	
Unidades Relativas:
•	Emplear unidades relativas como porcentajes, ems o vws en lugar de unidades fijas para permitir que los elementos se escalen proporcionalmente al tamaño de la pantalla.
Imágenes Flexibles:
•	Utilizar imágenes con anchos y alturas configurados como porcentajes o unidades relativas. También se puede emplear la propiedad max-width: 100% para evitar que las imágenes desborden sus contenedores. 


Preguntas prácticas

1.	Crear un documento HTML llamado index.html que incluya encabezados, párrafos, enlaces y una lista no ordenada. Aplicar la práctica recomendada de estilo CSS para cambiar el color y la fuente de los elementos.
2.	Diseñar una sección de la página web en index.html que contenga tres elementos (por ejemplo, tarjetas). Utilizar flexbox para alinearlos horizontalmente y distribuir el espacio de manera uniforme.
3.	Crear una cuadrícula de imágenes (o galería de imágenes) utilizando CSS Grid. Asegurarse de que las imágenes se ajusten automáticamente a diferentes tamaños de pantalla.
4.	Modificar la página web para que sea responsiva. Asegurarse de que los elementos se reorganicen y se ajusten correctamente cuando el tamaño de pantalla del navegador cambie.
5.	Agregar media queries a la página para personalizar el diseño en dispositivos móviles. Lograr que los estilos cambien cuando la pantalla sea más estrecha.




MÓDULO SOBRE DOM E INTERACCIÓN CON EL DOM

Preguntas teóricas

1.	¿Qué es el DOM (Modelo de Objeto de Documento) en el contexto de la programación web?

	El DOM (Modelo de Objeto de Documento) en programación web es una representación jerárquica y estructurada de un documento HTML o XML. Es una interfaz de programación que permite a los scripts o programas manipular dinámicamente la estructura, contenido y estilo de un documento web.

2.	¿Cuál es la diferencia entre el DOM y el HTML en una página web?

HTML es Estático: HTML proporciona la estructura estática de la página web.
DOM es Dinámico: El DOM representa esa estructura de manera dinámica, permitiendo cambios en tiempo real mediante programación.

3.	¿Por qué es importante entender y manipular el DOM en el desarrollo web Frontend?

•	Permite crear páginas web interactivas y dinámicas al modificar el contenido y la estructura del documento en respuesta a eventos del usuario o cambios en la aplicación.
•	Facilita la actualización del contenido de la página sin necesidad de recargarla.
•	Permite responder a eventos del usuario, como clics, teclas presionadas o cambios en formularios
•	Permite realizar solicitudes asíncronas a servidores, cargar datos de manera dinámica y actualizar la interfaz sin recargar la página
•	Posibilita la modificación dinámica de estilos y clases, facilitando la implementación de animaciones, cambios visuales y adaptación a diferentes dispositivos.

4.	¿Qué son los eventos del DOM y cuál es su función en una página web?
	
Los eventos del DOM son acciones o sucesos que ocurren en una página web y que pueden ser detectados y manejados mediante programación. Estos eventos pueden ser desencadenados por la interacción del usuario, el navegador, o incluso por el propio documento. La función principal de los eventos es permitir la creación de páginas web interactivas y dinámicas.
	
5.	Proporcionar ejemplos de eventos prácticos y comunes, como “click”, “submit” y “load o DOMContentLoad”.

CLICK:
document.getElementById('miBoton').addEventListener('click', function() {
    alert('¡Botón clickeado!');
});

SUBMIT:
document.getElementById('miFormulario').addEventListener('submit', function(event) {
    event.preventDefault(); // Evita la recarga de la página
    alert('Formulario enviado'); 
});
LOAD O DOMContentLoaded:
window.addEventListener('load', function() {
    alert('Página completamente cargada');
});

// O para detectar la disponibilidad del DOM sin esperar a los recursos externos
document.addEventListener('DOMContentLoaded', function() {
    alert('DOM listo para ser manipulado');
});

6.	¿Por qué es importante manejar eventos en la interacción usuario-web y cómo se añaden controladores de eventos a los elementos del DOM?

	Permite que las páginas web respondan a las acciones del usuario, mejorando la experiencia y haciéndola más dinámica y además, facilita la retroalimentación inmediata al usuario, como mensajes, animaciones o cambios visuales, en respuesta a sus acciones.

Para el ejemplo utilizare el método addEventListener el cual va cumplir la función de controlador del evento:

// Obtener el elemento por su id
var miBoton = document.getElementById('miBoton');

// Añadir un controlador de evento para el clic
miBoton.addEventListener('click', function() {
    alert('¡Botón clickeado!');
});

7.	Describir al menos tres métodos para seleccionar elementos del DOM en JavaScript.
getElementById: Selecciona un elemento del DOM por su identificador único (ID)

var miElemento = document.getElementById('miId');

getElementsByClassName: Selecciona elementos por su nombre de clase y devuelve una colección de elementos

var elementosClase = document.getElementsByClassName('miClase');

querySelector: Selecciona el primer elemento que coincida con un selector CSS

var primerElemento = document.querySelector('#miId'); // Por ID
var primerParrafo = document.querySelector('p'); // Por etiqueta

getElementsByTagName: Selecciona elementos por su nombre de etiqueta y devuelve una colección de elementos

var elementosEtiqueta = document.getElementsByTagName('p');



	
8.	¿Cómo se crea un nuevo elemento HTML y se agrega al DOM utilizando JavaScript?

	var nuevoElemento = document.createElement('div');
	nuevoElemento.id = 'nuevoId';
    	nuevoElemento.innerHTML = 'Contenido del nuevo elemento';
	var contenedorExistente = document.getElementById('miContenedor');
	contenedorExistente.appendChild(nuevoElemento);

	// Opción 2: Insertar antes de otro elemento existente
    	var elementoExistente = document.getElementById('otroElemento');
    	contenedorExistente.insertBefore(nuevoElemento, elementoExistente);
	
9.	¿Cuál es la importancia de la manipulación del DOM en la creación de aplicaciones web dinámicas e interactivas?

•	Permite responder a las acciones del usuario, como clics, teclas presionadas, movimientos del ratón, entre otros, creando una experiencia interactiva.
•	Facilita la actualización dinámica del contenido de la página sin necesidad de recargarla
•	Permite cambiar el estado de la aplicación en respuesta a eventos específicos, como cambios en formularios, actualización de datos, o interacción con elementos de la interfaz
•	Facilita la carga asincrónica de datos y contenido adicional
•	Facilita la comunicación asíncrona con servidores

10.	Explicar brevemente los conceptos “event bubbling” y “event delegation” en el contexto de eventos del DOM.

	El "event bubbling" se refiere a la propagación ascendente de eventos desde el elemento objetivo hasta el ancestro más externo, mientras que la "event delegation" es una estrategia que aprovecha este proceso para asignar manejadores de eventos de manera eficiente en estructuras dinámicas del DOM.
11.	¿Por qué son relevantes los conceptos “event bubbling” y “event delegation” en la gestión de eventos en páginas web con múltiples elementos interactivos?

Son relevantes ya que permiten una asignación eficiente de eventos, adaptándose a páginas dinámicas y facilitando la escalabilidad del código. "Event bubbling" propaga eventos desde el elemento objetivo hasta el ancestro, mientras que "event delegation" asigna un solo manejador a un ancestro común en lugar de a cada elemento individual.

Preguntas prácticas

1.	Escribir una función en JavaScript que tome un botón en el DOM y, al hacer click en él, cambie el color de fondo de un elemento específico en la página. Luego, agregar el botón y el elemento objetivo en el DOM y asociar la función al evento “click”.
2.	Crear una lista no ordenada de elementos (por ejemplo, elementos de lista) en el DOM. Implementar la delegación de eventos (event delegation) para que, al hacer clic en cualquier elemento de la lista, se muestre un mensaje en la consola que indique qué elemento de la lista se ha hecho clic.
3.	Agregar un formulario a tu página web con un campo de entrada y un botón "Enviar". Implementar una función que sea llamada al enviar el formulario y que valide el campo de entrada (por ejemplo, si está vacío), muestre un mensaje de error accesible si es necesario y en caso de que el formulario esté correctamente diligenciado muestre en consola un objeto con el dato que ha ingresado el usuario en el campo de entrada y un alert con el siguiente mensaje: “Formulario correctamente diligenciado”.

MÓDULO SOBRE COMUNICACIÓN CON EL SERVIDOR (STORAGE, PROMESAS, ASINCRONÍAS Y PETICIONES HTTPS)

Preguntas teóricas

1.	Definir brevemente el concepto de localStorage y sessionStorage.

LocalStorage: Este es un mecanismo de almacenamiento de datos en el navegador, que así se cierre el navegador, este sigue persistiendo con los datos

SessionStorage: Tiene similitus al localstorage, pero este tiene una duración limitada, por lo que se borra cuadno se cierre la pestaña o ventana del naveagdor
	
2.	Describir las diferencias claves entre localStorage y sessionStorage.

Duración de los datos: En el LocalStorage, los datos persisten así se cierre el navegador, con el sessioStorage tiene una duración limitada y se borran automáticamente apenas se cierre el navegador.

Capacidad de Almacenamiento: LocalStorage Tiene una capacidad mayor de almacenamiento en comparación con sessionStorage. Puede almacenar más datos, pero la cantidad específica varía según el navegador y la configuración del usuario.
sessionStorage: Tiene una capacidad de almacenamiento más limitada en comparación con localStorage.

3.	¿Por qué son útiles para almacenar datos en el navegador y cuál es su límite de capacidad?

Persistencia de Datos: Permiten almacenar datos en el lado del cliente, lo que es útil para recordar preferencias del usuario, configuraciones, o cualquier información que deba persistir entre sesiones o visitas al sitio web.

Mejora la Experiencia del Usuario: Almacenar datos localmente evita la pérdida de información cuando se recarga la página o se cierra el navegador.

Eficiencia en el Acceso a Datos: Reduce la necesidad de hacer solicitudes al servidor para recuperar datos que raramente cambian, optimizando la velocidad de carga de la aplicación.

Limites:
	localStorage: Puede almacenar entre 5 MB y 10 MB de datos por dominio, aunque algunos navegadores permiten configuraciones específicas del usuario que pueden aumentar o disminuir este límite.

sessionStorage: Tiene una capacidad más limitada en comparación con localStorage. Generalmente, se permite almacenar alrededor de 5 MB de datos por dominio.
4.	¿Qué son las promesas en JavaScript y para qué se utilizan en el desarrollo web?
	Las promesas son objetos que representan la eventual finalización o falla de una operación asincrónica y su resultado. Son un patrón de manejo de operaciones asíncronas que brinda una forma más limpia y estructurada de trabajar con código asíncrono en comparación con los callbacks.
	
5.	Explica el concepto de asincronía en programación y cómo las promesas ayudan a manejar operaciones asincrónicas.

	La asincronía en programación se refiere a la ejecución de operaciones de manera no secuencial, donde una tarea puede iniciarse antes de que otra se complete. Lo que quiere decir que las operaciones no bloquean la ejecución del programa, permitiendo que otras tareas continúen mientras se espera la finalización de una operación.
Y las promesas ayudan para la gestión de las operaciones asíncronas, permitiendo que se manejen con una mejor estructura y legibilidad

6.	Proporciona un ejemplo de cómo se utiliza una promesa para realizar una operación asincrónica, como una solicitud de red. 

	function operacionAsincronica() {
    return new Promise((resolve, reject) => {
        
        setTimeout(() => {
            const exito = true; 

            if (exito) {
                resolve('Operación exitosa');
            } else {
                reject('Fallo en la operación');
            }
        }, 1000); 
    });
}

operacionAsincronica()
    .then(resultado => {
        console.log(resultado);
    })
    .catch(error => {
        console.error(error);
    });


operacionAsincronica devuelve una promesa que simula una operación asincrónica que tarda un tiempo.
La promesa se resuelve con un mensaje de éxito si la operación es exitosa.
La promesa se rechaza con un mensaje de error si la operación falla.




7.	¿Qué es JSON Server y cómo se utiliza en el desarrollo web?

Es una herramienta que proporciona una API REST, que simula un archivo JSON, esta se comporta como una base de datos para hacer puerbas de aplicaciones que interactúan con una API, lo que permite la simulación de un servidor y endpoints.

8.	¿Por qué es útil simular una API REST falsa con JSON Server en el desarrollo frontend?

•	Permite a los desarrolladores avanzar en el desarrollo sin depender de la disponibilidad de la API backend
•	Facilita la realización de pruebas 
•	Permite evaluar rápidamente las funcionalidades del frontend

9.	¿Cuáles son las diferencias claves entre los métodos del objeto promesa .then().catch()
y las palabras claves async/await?

•	El .then()  y .catch()  se utilizan para el manejo de resultados exitosos y los errores de una promesa y async se utiliza para declarar una función asíncrona y await para esperar la resolución de una promesa dentro de la función
•	.then().catch(): Permite encadenar múltiples operaciones asíncronas utilizando varios bloques .then().  
•	async/await: Facilita el encadenamiento de operaciones asíncronas de manera más estructurada y legible. 


10.	Proporciona un ejemplo de cómo configurar una API falsa con JSON Server y realizar solicitudes (GET, POST, PUT, PATCH y DELETE) a través de ella.


•	El primer paso es la instalación y se realiza con el siguiente comando:
			npm install -g json-server

•	Creamos el Archivo Json, generalmente se maneja con el nombre db.json
	{
  "usuarios": [
    { "id": 1, "nombre": "Usuario 1" },
    { "id": 2, "nombre": "Usuario 2" }
  ]
}
•	Iniciamos el Json Server
	json-server --watch db.json

•	GET(obtener los usuarios)
		curl http://localhost:3000/usuarios
		
•	POST(Agregar un nuevo usuario)
curl -X POST -H "Content-Type: application/json" -d '{"nombre": "Nuevo Usuario"}' http://localhost:3000/usuarios

•	PUT( Actualizar un usuario por ID)
curl -X PUT -H "Content-Type: application/json" -d '{"nombre": "Usuario Modificado"}' http://localhost:3000/usuarios/1

•	PATCH( Actualizar parcialmente un usuario por ID)
curl -X PATCH -H "Content-Type: application/json" -d '{"nombre": "Usuario Modificado"}' http://localhost:3000/usuarios/1	

•	DELETE( Eliminar un usuario por ID)
curl -X DELETE http://localhost:3000/usuarios/1

11.	Describe las diferencias entre Fetch y Axios como métodos para realizar solicitudes HTTP en JavaScript.

•	Fetct utiliza la interfaz nativa de JavaScript y sigue un enfoque basado en promesas, requiere varias llamadas para realizar operaciones comunes como verificar el estado de la respuesta y convertir datos JSON y Axios proporciona una interfaz más simple y limpia. Retorna una promesa que se resuelve directamente con los datos de la respuesta, evitando la necesidad de múltiples llamadas para tareas comunes.
•	Fetch requiere verificación manual del estado de la respuesta y del flag ok. Puede ser menos intuitivo para manejar errores y Axios manejo más claro de errores. Detecta automáticamente códigos de estado de error y rechaza la promesa en consecuencia.
•	Fetch requiere llamadas adicionales (response.json()) para convertir datos JSON y Axios realiza automáticamente la conversión de datos JSON. Simplifica la tarea de trabajar con respuestas JSON.
	
12.	¿Por qué es importante considerar las peticiones HTTP en aplicaciones web modernas?

	Las peticiones HTTP son fundamentales en aplicaciones web modernas. Facilitan la interactividad en tiempo real, permiten la integración eficiente con servidores y APIs, posibilitan la carga dinámica de contenido, y permiten actualizaciones incrementales sin recarga de página.
	
13.	Proporciona ejemplos de cómo se utilizan Fetch y Axios para realizar solicitudes GET y POST.

FETCH:

•	GET:
fetch('https://jsonplaceholder.typicode.com/posts/1')
    .then(response => response.json())
    .then(data => console.log(data))
		.catch(error => console.error(error));

•	POST:
		fetch('https://jsonplaceholder.typicode.com/posts', {
    method: 'POST',
    headers: {
        'Content-Type': 'application/json',
    },
    body: JSON.stringify({
        title: 'Nuevo Post',
        body: 'Contenido del nuevo post.',
        userId: 1,
    }),
})
    .then(response => response.json())
    .then(data => console.log(data))
    .catch(error => console.error(error));


AXIOS:

•	GET:
const axios = require('axios');

axios.get('https://jsonplaceholder.typicode.com/posts/1')
    .then(response => console.log(response.data))
		.catch(error => console.error(error));

•	POST:
		const axios = require('axios');

axios.post('https://jsonplaceholder.typicode.com/posts', {
    title: 'Nuevo Post',
    body: 'Contenido del nuevo post.',
    userId: 1,
})
    .then(response => console.log(response.data))
    .catch(error => console.error(error));

14.	Explica la importancia del manejo de errores al trabajar con promesas en el desarrollo web.

El manejo de errores en el desarrollo web al trabajar con promesas es crucial para evitar comportamientos inesperados, mejorar la experiencia del usuario, facilitar la identificación y resolución de problemas, prevenir fugas de promesas, y garantizar un mantenimiento sencillo y centralizado del código asíncrono.
	
15.	Describe cómo se manejan los errores en las promesas, incluyendo el uso de catch.

	En las promesas, el manejo de errores se realiza principalmente mediante el método .catch(). Este bloque captura cualquier error que ocurra durante la ejecución de la promesa, permitiendo un manejo centralizado de errores. Además, cuando se utiliza async/await, se puede emplear el bloque try-catch para gestionar errores de manera más estructurada.
	
16.	¿Cuáles son las diferencias claves entre los métodos del objeto promesa .then().catch()
y la estructura try/catch?

La forma .then().catch() utiliza métodos encadenados para manejar el resultado exitoso y los errores de una promesa, permitiendo un flujo de control más específico para promesas encadenadas. Por otro lado, la estructura try/catch ofrece mayor flexibilidad, ya que no está limitada solo al manejo de promesas; puede adaptarse tanto a código síncrono como asíncrono, proporcionando un enfoque más general para gestionar excepciones.
17.	Proporciona un ejemplo de cómo se puede manejar un error en una promesa al realizar una solicitud de red.

function simularSolicitudDeRed() {
    return new Promise((resolve, reject) => {
        setTimeout(() => {
            const exito = Math.random() < 0.8; 

            if (exito) {
                resolve("Datos recibidos con éxito");
            } else {
                reject(new Error("Error al recibir los datos"));
            }
        }, 2000); 
    });
}

	simularSolicitudDeRed()
    .then(resultado => {
        console.log(resultado);
    })
    .catch(error => {
        console.error("Error de solicitud:", error.message);
    });

Preguntas prácticas

1.	En una sección de la página web construida en los módulos anteriores, permitir a un usuario almacenar y recuperar datos utilizando localStorage y sessionStorage. Demostrar cómo se puede guardar y recuperar datos de estas áreas de almacenamiento del navegador.
2.	Escribir una función que utilice una promesa para simular una operación asincrónica, como, por ejemplo, una solicitud de datos. Luego, mostrar los resultados de la promesa en una sección en la página web.
3.	Crear una API falsa con JSON Server y realizar una solicitud GET y POST con Fetch o Axios y mostrar los resultados en una sección de la página web.
4.	Crear un repositorio remoto en GitHub con la estructura de carpetas y archivos de la página web creada para darle respuesta a las preguntas anteriores.
5.	La respuesta a las preguntas teóricas debe estar resueltas en un archivo README.md en el repositorio creado en el ítem anterior.
6.	Desplegar la página web en GitHub pages.

