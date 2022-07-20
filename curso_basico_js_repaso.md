# Javascript Repaso De Platzi 💚

## Variables y operaciones
### Responde las siguientes preguntas
- #### ¿Qué es una variable y para qué sirve?
Una variable es un espacio en memoria donde podemos guardar información. Strings, numbers, booleans, funciones, etc.  
- ####  ¿Cuál es la diferencia entre declarar e inicializar una variable?
Cuando declaramos una variable, simplemente nombramos la variable, sin indicarle que tipo de información o dato almacenara. En cambio, cuando inicializamos una variable indicamos el tipo de dato e información que va a almacenar.
- #### ¿Cuál es la diferencia entre sumar números y concatenar strings?
Al momento sumar números estamos realizando una operación matemática con dos tipos de datos (Numbers) mientras que al concatenar estamos sumando dos tipos de datos (String) que son cadena de textos.
- #### ¿Cuál operador me permite sumar o concatenar?
El operador utilizado es el signo +.

## #Determina el nombre y tipo de dato para almacenar en variables la siguiente información:
- Nombre: string
- Apellido: string
- Nombre de usuario en Platzi: string
- Edad: numer
- Correo electrónico: string
- Mayor de edad: boolean
- Dinero ahorrado: number
- Deudas: number 

###Traduce a código JavaScript las variables del ejemplo anterior 

    let nombre = 'Roger';
    let apellido = 'Montes';
    let nombreUsuario = 'rmthirty';
    let edad = 23;
    let correo = 'rogerxmontes@gmail.com';
    let mayorEdad = true;
    let dineroAhorrado = 15000;
    let deudas = 2800;

### Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:
#### Nombre completo (nombre y apellido)
```
let nombreCompleto = nombre + ' ' + apellido;

console.log(`Mi nombre completo es ${nombreCompleto}`);
// Mi nombre completo es Roger Montes 
```
#### Dinero real (dinero ahorrado menos deudas)
```
let dineroReal = dineroAhorrado - deudas; 
console.log(`El dinero que tengo en total es ${dineroReal}`);
// El dinero que tengo en total es 12200
```
##Funciones

### Responde las siguientes preguntas:
- #### ¿Qué es una función?
Es un conjunto de acciones que nos permitirá reutilizar en nuestro código y siempre deben devolver un resultado. Podemos crear diferentes funciones con parámetros distintos y luego utilizar la información para realizar un evento o acción dentro de nuestro código.
- ####¿Cuándo me sirve usar una función en mi código?
Cuando necesitamos repetir una acción en nuestro código, en vez de escribir una suma, por ejemplo en cada línea, podemos crear una función que nos permita sumar elementos cada vez que lo necesitemos y solo cambiamos sus parámetros.
- ####¿Cuál es la diferencia entre parámetros y argumentos de una función?
Los parámetros son las variables declaras y solicitadas en nuestra función, al momento de realizar el llamado de nuestra funciones nos exigirá declarar nuestras variables que vendrían a ser nuestros argumentos de la función.

### Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:
```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```
//Solución 
```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

let informacion = function (name, lastName, completeName, nickname) {
	return console.log(`Mi nombre completo es ${completeName}, pero prefiero que me digas ${nickname}`);
};
informacion('Roger','Montes','Roger Montes', 'rmrhirty');
//Mi nombre completo es Roger Montes, pero prefiero que me digas rmrhirty
```
## Condicionales
### Responde las siguientes preguntas:
- #### ¿Qué es un condicional?
Es una expresión que nos permite evaluar si es True o False.
- ####¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
If…else
Switch

Con el condicional If…Else podemos tener diferentes expresiones para evaluar dependiente del caso, y generar tantos If o else como sea necesario. Mientras que Switch case toma una sola expresión de entrada pero puede evaluar todos los casos como sea necesario de una forma más ordenada.
- ####¿Puedo combinar funciones y condicionales?
Podemos encadenar una respusta desde un condional a otro pero no podemos combinarlo dentro de una misma expresión. Si podemos ocuparlos de forma separada y luego encadenar una acción dependiendo del resultado.

### Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:
```
const tipoDeSuscripcion = "Basic";

switch (tipoDeSuscripcion) {
   case "Free":
       console.log("Solo puedes tomar los cursos gratis");
       break;
   case "Basic":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
       break;
   case "Expert":
       console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
       break;
   case "ExpertPlus":
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
       break;

//Solucion
const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion === 'Free') {
    console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion === 'Basic') {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion === 'Expert') {
    console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else {
    console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
};

```
###Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).
```
const tiposDeSuscripciones = {
    free: 'Solo puedes tomar los cursos gratis',
    basic: 'Puedes tomar casi todos los cursos de Platzi durante un mes',
    expert: 'Puedes tomar casi todos los cursos de Platzi durante un año',
    expertduo: 'Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año',
};

function conseguirTipoSuscripcion(suscripcion) {
    if (tiposDeSuscripciones[suscripcion]) {
        console.log(tiposDeSuscripciones[suscripcion]);
        return;
    }

    console.warn('Ese tipo de suscripción no existe')
}
```

## Ciclos
### Responde las siguientes preguntas:
- ####¿Qué es un ciclo?
Un ciclo es un bucle que se repite hasta que se cumpla una condición.
- ####¿Qué tipos de ciclos existen en JavaScript?
Ciclo For, While, etc.
- ####¿Qué es un ciclo infinito y por qué es un problema?
Un ciclo infinito es cuando la condición es infinita, nunca se cumple y, por lo tanto, no existe termino al proceso, por consecuencia nuestro código puede fallar y ralentizar nuestras computadoras.
- ####¿Puedo mezclar ciclos y condicionales?
Sí, podemos condicionar un ciclo para que se repita todas las veces hasta que se cumplan una condición que internamente puede tener otra condición para su evaluación.

### Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:
```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

// Solucion

while ( i < 5) {
    i++;
    console.log("El valor de i es: " + i);
}

while ( i >= 2) {
    i--;
    console.log("El valor de i es: " + i);
}

```
### Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

```
let n1 = 2;
let n2 = 2;
const resultado = n1 + n2;

let quiz = {
    q1: `Cuanto es ${n1} + ${n2}`
}

function quizzer () {
    let respuesta = prompt(quiz.q1);

    if (respuesta == resultado) {
        alert("Felicitaciones! Tu respuesta es correcta 😎");
    } else {
        alert("Ups!, parece que tu respuesta no es correcta. Vuelve a intentarlo 😁");
    }
}

quizzer();
```

## Listas
- ### Responde las siguientes preguntas en la sección de comentarios:
- ####¿Qué es un array?
Un array es una colecciones de elementos con valores de una sola variable. Se escriben dentro de [ … ], separado por una coma.
- ####¿Qué es un objeto?
Es una colección de datos relacionados con múltiples variables con sus valores.
- ####¿Cuándo es mejor usar objetos o arrays?
Ocupamos objetos cuando el conjunto de elementos es muy grande y de distintos tipos de valores.
- ####¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

### Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```
let array = ['Kobe','LeBron','Steph','Michael'];

function imprimeArray(arreglo) {
    console.log(arreglo[0]);
}

imprimeArray(array);
```

### Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```
let nba = ['Doncic','Curry','Jordan','Bryant','Thompson'];


function readArray(jugadores) {
    for (let i = 0; i < jugadores.length; i++) {
        console.log(`${jugadores[i]}`)
    } 
}
readArray(nba);
```
###Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).
 ```
let basket = {
    nombre: 'Luka',
    apellido: 'Doncic',
    posicion: 'Base',
    equipo: 'Dallas Mavericks',
}

const basketArray = Object.values(basket);

function nba(jugadores) {
    for ( let i = 0; i <= jugadores.length; i++) {
        console.log(`${jugadores}`);
    }
}

nba(basketArray);

```