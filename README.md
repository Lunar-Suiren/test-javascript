# test-javascript-platzi

## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?

Una variable es un espacio reservado en memoria que sirve para almacenar un valor, un objeto o una función, entre otros.

- ¿Cuál es la diferencia entre declarar e inicializar una variable?

Al declarar una variable se reserva el espacio en memoria de la misma y al inicializarla se le asigna un valor o información después de declarada. Una variable puede estar declarada pero no inicializada, en cuyo caso estará vacía.


- ¿Cuál es la diferencia entre sumar números y concatenar strings?

Sumar números corresponde a una operación matemática, mientras que concatenar strings es unir dos cadenas de texto.

- ¿Cuál operador me permite sumar o concatenar?

Se puede sumar o concatenar utilizando el signo más (+).


### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:
- Nombre = "String"
- Apellido = "String"
- Nombre de usuario en Platzi = "String"
- Edad = "Number"
- Correo electrónico = "String"
- Mayor de edad = "Boolean"
- Dinero ahorrado = "Number"
- Deudas = "Number"


### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```js
let nombre = "César";
let apellido = "Ceballos";
let username_platzi = "lunar_suiren";
let edad = 27;
let email = "jcceballosr92@gmail.com"
let adult = true;
let saved_money = 6000000;
let deudas = 100000;
```


### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:
- Nombre completo (nombre y apellido)

```js
let nombre = "César";
let apellido = "Ceballos"

console.log(`Mi nombre completo es ${nombre} ${apellido}`);
```

- Dinero real (dinero ahorrado menos deudas)

```js
let saved_money = 6000000;
let deudas = 100000;
let current_money = saved_money - deudas;

console.log(`Mi dinero real es $${current_money}`);
```

## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

-¿Qué es una función?

Son un conjunto de instrucciones, tareas y/o procedimientos, que permiten realizar ciertas acciones utilizando variables y parámetros. 

- ¿Cuándo me sirve usar una función en mi código?

Cuando se necesita utilizar una instrucción asociada a dicha función en específico.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?

Los parámetros los valores que se introducen en la función y los argumentos es el espacio interno que se asigna a cada uno de los parámetros que recibió la función.

### 2️⃣ Convierte el siguiente código en una función, pero, cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```js

function apodo(name, lastname, nickname) {
    console.log("Mi nombre es " + name + " " + lastname ", pero prefiero que me digas " + nickname + ".");
}
```

## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?

Es una restriccion para aplicar ciertos límites al código.

- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?

  - If...else 
  - switch

Sus diferencias radican en la forma de validar y ejecutar las expresiones presentadas según los diferentes casos. Mientras que en if...else se generan tantas condiciones como se quiera en switch se toma una sola expresión y se evaluan todos los casos.

- ¿Puedo combinar funciones y condicionales?

Sí, se puede por ejemplo hacer que una funcion se ejecute si se valida cierta expresión.

```js
if (true) {
  function miFuncion() {
    console.log ("Hola, soy una Función");
  }
}
```

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

```js
const tipoDeSuscripcion = "Basic";

if (tipoDeSuscripcion === "Free")
{
  console.log("Solo puedes tomar los cursos gratis");
} else if (tipoDeSuscripcion === "Basic") {
  console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
} else if (tipoDeSuscripcion === "Expert") {
  console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
} else if (tipoDeSuscripcion === "ExpertPlus") {
  console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays u objetos y un solo condicional. 😏

```js
 let tipoDeSuscripcion = ["Free", "Basic", "Expert", "ExpertPlus"];

 let info = [
"solo puedes tomar los cursos gratis", 
"puedes tomar casi todos los cursos de Platzi durante un mes", 
"puedes tomar casi todos los cursos de Platzi durante un año", 
"tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año"];

let suscripcion = "Basic";

 for (let i = 0, i < tipoDeSuscripción.lenght[i], i++) {
  if (suscripcion == tipoDeSuscripcion[i]) {
    console.log(`Con tu suscripcion al plan ${tipoDeSuscripcion[i]} ${info[i]}`);
  }
 }
```

## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?
Es recorrer una parte del código de forma repetitiva una cantidad de veces establecida o limitada previamente.

- ¿Qué tipos de ciclos existen en JavaScript?

    - For
    - While
    - For of

- ¿Qué es un ciclo infinito y por qué es un problema?

Es cuando un ciclo se ejecuta de forma indefinida, es decir, que no tiene límite, el código se repetira una y otra vez hasta el infinito. Esto es un problema dado que en cada iteración se asigna un nuevo espacio en memoria, y puesto que el hardware es límitado, no se puede calcular un ciclo de forma infinita, provocando que el codigo falle y se ralentiza la computadora.

- ¿Puedo mezclar ciclos y condicionales?

Sí, de hecho esta combinación se utiliza para resolver problemas más complejos o acortar código, tal como en el ejercicio bonus de la sección anterior.

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```js
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

//Solución
let i = 0
while (i < 5) {
  i++;
  console.log(`El valor de i es: ${i}`);
}
```

### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es 2 + 2. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.
>💡 Pista: puedes usar la función prompt de JavaScript.

```js
const result = 4

function quizz() {
  let user_answer = prompt("¿Cuánto es 2 + 2?");
  if (user_answer == result) {
    alert("Felicidades, tu respuesta es correcta!");
  } else {
    alert("Lo sentimos, tu respuesta es incorrecta, intentalo de nuevo");
  }
}

quizz();
```

## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?

Un conjunto o arreglo de valores que pueden ser de diferentes tipos.

- ¿Qué es un objeto?

Una estructura de datos para guardar información.

- ¿Cuándo es mejor usar objetos o arrays?

Es mejor usar arrays cuando se quiere tener un conjunto de valores al cual acceder de forma sencilla, en cambio un objeto es mejor cuando se necesita tener un identificador para cada tipo de valor.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

Si.

### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```js
let miArray = [1, 2, 3, 4, 5];

function miFuncion(array){
  console.log(`Mi primer elemento es` ${array[0]});
}

miFuncion(miArray);
```

### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```js
let miArray = [1, 2, 3, 4, 5];

function miFuncion(array){
  for (let i = 0; i < array.length; i++){
    console.log(`${array[i]}`);
  }
}

miFuncion(miArray);
```

### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```js
let miAuto = {
  marca: "Toyota",
  modelo: "Corolla",
  year: 2020,
};

function readObject(auto) {
  for (let key in auto) {
    console.log(auto[key]);
  }
}

readObject(miAuto);
```
