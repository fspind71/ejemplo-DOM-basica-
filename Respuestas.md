## Respuestas al Test de JavaScript

Recuerda que estas respuestas (o al  menos la mayoría) NO SON ABSOLUTAS. Es completamente válido (en la mayoría de casos) si tienes otras respuestas. Recuerda que podemos discutirlo en la sección de comentarios del curso. :D


## Variables y operaciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una variable y para qué sirve?

Cajtas (espacios en memoria) donde podemos guardar información (dependiendo de los tipos y estructuras de datos que soporte nuestro lenguaje).

- ¿Cuál es la diferencia entre declarar e inicializar una variable?

Declarar es cuando le decimos a JavaScript que vamos a crear una variable con el nombre tal. Mientras que inicializar (o reinicializar) es asignarle un valor a esa variable.

- ¿Cuál es la diferencia entre sumar números y concatenar strings?
- ¿Cuál operador me permite sumar o concatenar?

EL operador que nos permite sumar o concatenar es +. Este operador nos permite sumar números cuando lo usamos con números. Pero cuando los strings, lo que hace es unir (concatenar, así se dice) ambos strings.

### 2️⃣ Determina el nombre y tipo de dato para almacenar en variables la siguiente información:

- Nombre: string
- Apellido: string
- Nombre de usuario en Platzi: strig (@fulanito)
- Edad: number
- Correo electrónico: string (lala@gmail.com)
- Mayor de edad: boolean
- Dinero ahorrado: number
- Deudas: number

### 3️⃣ Traduce a código JavaScript las variables del ejemplo anterior y deja tu código en los comentarios.

```
let nombre = 'Juan David';
let apellido = 'Catro Gallego';
let username = 'juandc';
let edad = 19;
let mail = 'juanito@alcachofa.xyz';
let esMayorDeEdad = true;
let dineroAhorrado = 1000;
let deudas = 100;
```

### 4️⃣ Calcula e imprime las siguientes variables a partir de las variables del ejemplo anterior:

- Nombre completo (nombre y apellido)
- Dinero real (dinero ahorrado menos deudas)

```
let nombreCompleto = nombre + ' ' + apellido;
let dineroReal = dineroAhorrado - deudas;
```



## Funciones

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es una función?

Las funciones nos permiten encapsular (guardar) bloques de código para reutilizarlos y ejecutarlos en el futuro.

- ¿Cuándo me sirve usar una función en mi código?

Nos sirve cuando tenemos variables o bloques de código muy parecidos (con cambios que podrían ser parámetros y argumentos) que podemos encapsular para reutilizar más de una vez en el futuro.

También nos sirve para ordenar y mejorar la legibilidad de nuestro código.

- ¿Cuál es la diferencia entre parámetros y argumentos de una función?

las funciones reciben parámetros cuando las creamos. Y les enviamos argumentos cuando las ejecutamos.

### 2️⃣ Convierte el siguiente código en una función, pero cambiando cuando sea necesario las variables constantes por parámetros y argumentos en una función:

```
const name = "Juan David";
const lastname = "Castro Gallego";
const completeName = name + lastname;
const nickname = "juandc";

console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + nickname + ".");
```

```
function nombreCompleto(name, lastName) {
    return name + ' ' + lastName
}

function saludo(name, lastname, username) {
    const completeName = nombreCompleto(name, lastname);

    console.log("Mi nombre es " + completeName + ", pero prefiero que me digas " + username + ".");  
}
```


## Condicionales

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un condicional?
- ¿Qué tipos de condicionales existen en JavaScript y cuáles son sus diferencias?
- ¿Puedo combinar funciones y condicionales?

### 2️⃣ Replica el comportamiento del siguiente código que usa la sentencia switch utilizando if, else y else if:

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
}
```

### 3️⃣ Replica el comportamiento de tu condicional anterior con if, else y else if, pero ahora solo con if (sin else ni else if).

```
function conseguirTipoSuscripcion (suscripcion){
    if (suscripcion == 'Free') {
       console.log("Solo puedes tomar los cursos gratis");
        return
    }
    
    if (suscripcion == 'Basic'){
       console.log("Puedes tomar casi todos los cursos de Platzi durante un mes");
        return
    }
    
    if(suscripcion == 'Expert'){
        console.log("Puedes tomar casi todos los cursos de Platzi durante un año");
        return
    }
    
    if(suscripcion == 'ExpertDuo'){
       console.log("Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año");
        return
    }
    console.warn('Ese tipo de sucripcion no existe')
}
```



> 💡 Bonus: si ya eres una experta o experto en el lenguaje, te desafío a comentar cómo replicar este comportamiento con arrays y un solo condicional. 😏

```
const tiposDeSuscripciones ={
    free:'Solo puedes tomar los cursos gratis',
    basic: 'Puedes tomar casi todos los cursos de Platzi durante un mes',
    expert:'Puedes tomar casi todos los cursos de Platzi durante un año',
    expertduo:'Tú y alguien más pueden tomar TODOS los cursos de Platzi durante un año',
};

function conseguirTipoSuscripcion (suscripcion){
    if (tiposDeSuscripciones[suscripcion]) {
       console.log(tiposDeSuscripciones[suscripcion])
        return
    }

console.warn('Ese tipo de suscripcion no existe')
}


```
## Ciclos

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un ciclo?
- ¿Qué tipos de ciclos existen en JavaScript?
- ¿Qué es un ciclo infinito y por qué es un problema?
- ¿Puedo mezclar ciclos y condicionales?

### 2️⃣ Replica el comportamiento de los siguientes ciclos for utilizando ciclos while:

```
for (let i = 0; i < 5; i++) {
    console.log("El valor de i es: " + i);
}

while(i<5) {
     console.log ("el valor de i es:" +i);
    i++;
}

---------------------------------------------------------------

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

for (let i = 10; i >= 2; i--) {
    console.log("El valor de i es: " + i);
}

con for

El valor de i es: 10

El valor de i es: 9

El valor de i es: 8

El valor de i es: 7

El valor de i es: 6

El valor de i es: 5

El valor de i es: 4

El valor de i es: 3

con while

El valor de i es: 2

let i=10;

while (i>=2){
console.log ("El valor de i es:" +i)
i--;
}


El valor de i es:10

El valor de i es:9

El valor de i es:8

El valor de i es:7

El valor de i es:6

El valor de i es:5

El valor de i es:4

El valor de i es:3

El valor de i es:2





### 3️⃣ Escribe un código en JavaScript que le pregunte a los usuarios cuánto es `2 + 2`. Si responden bien, mostramos un mensaje de felicitaciones, pero si responden mal, volvemos a empezar.

> 💡 Pista: puedes usar la función prompt de JavaScript.

```
let respuesta;
undefined
while (respuesta !='4'){
let pregunta = prompt('¡Cuánto es 2+2?')
    respuesta = pregunta;
}
```


## Listas

### 1️⃣ Responde las siguientes preguntas en la sección de comentarios:

- ¿Qué es un array?
Es una lista de elementos
```
const array =[1, 'jaja', true, false, {nombre:Stella Artois, edad:23}]; 

````
- ¿Qué es un objeto?

Es una lista de elmentos PERO cada elemento tiene un nombre clave.

```
const obj ={
    nombre: "Fulanito",
    edad:3,
    comidas favoritas: ['pollo frito', 'vegetales'],
};
````
- ¿Cuándo es mejor usar objetos o arrays?

Arrays cuando lo que haremos en un elemento es lo mismo en todos los demas. Esta regla se puede incumplir. Mientras que un objeto cuando los nombres de cada elemento son importantes para nuestro algoritmo.

- ¿Puedo mezclar arrays con objetos o incluso objetos con arrays?

Si. Los arrays pueden guardar objetos. Y los objetos pueden guardar arrays entre sus propiedades.



### 2️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima su primer elemento.

```
function imprimirPrimerElementoArray(arr){
    console.log(arr[0])
}
undefined

imprimirPrimerElementoArray(['Santiago', 'Luciana', 'Martin', 'Vanina', 'Fabian'])
VM804:2 Santiago
undefined

function imprimirPrimerElementoArray(arr){
    console.log(arr[3])
}
undefined

imprimirPrimerElementoArray(['Santiago', 'Luciana', 'Martin', 'Vanina', 'Fabian'])
VM1041:2 Vanina
undefined

```
### 3️⃣ Crea una función que pueda recibir cualquier array como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el array completo).

```
function imprimirElementoPorElemento(arr) {
    for(i=0; i<arr.length; i++) {
        console.log(arr[i])
    }
}
undefined

imprimirElementoPorElemento(['Santiago', 'Luciana', 'Martin', 'Vanina', 'Fabian'])
Santiago
Luciana
Martin
Vanina
Fabian
undefined

```


### 4️⃣ Crea una función que pueda recibir cualquier objeto como parámetro e imprima todos sus elementos uno por uno (no se vale imprimir el objeto completo).

```
function imprimirElementoPorElemento(abj) {
    const arr = Object.values(obj);
    for(i=0; i<arr.length; i++) {
        console.log(arr[i])
    }
}
undefined

imprimirElementoPorElemento(obj)
Fulanito
3
(2) ['pollo frito', 'vegetales']
undefined


```
