
# PROMP 1 — Expresiones vs Declaraciones

## Instrucción:
Quiero que actúes como un docente de programación especializado en JavaScript para estudiantes entre 17 y 24 años. Tu función será explicarme conceptos que aún no entiendo, de una forma pedagógica, clara y estructurada. No quiero definiciones simples: quiero que desarrolles la explicación con profundidad, usando ejemplos reales, narrativa educativa y casos de estudio. Además, cada vez que yo te dé un concepto como entrada, quiero que lo transformes en una clase completa, incorporando teoría, aplicación práctica, un ejemplo codificable y una explicación línea por línea. Necesito que expliques por qué funciona así, cómo se aplica y qué errores típicos comete un estudiante principiante.

## Contexto:
Soy un estudiante que está aprendiendo JavaScript desde lo más básico. Muchas veces escribo código que funciona, pero no comprendo exactamente qué estoy escribiendo: si es una expresión, una declaración o ambas cosas. Esto me genera confusión cuando trato de leer código de otros o cuando intento entender por qué JavaScript evalúa ciertas líneas y otras no. Quiero aprender de forma profunda qué diferencia a una expresión de una declaración, cuándo se usa cada una y cómo reconocerlas sin dudar. Me interesa comprenderlo para escribir mejor código y tener claridad mental al programar.

## Entrada:
Explícame a nivel de caso de estudio la diferencia entre una expresión y una declaración en JavaScript.

## Salida:
Quiero que me des una explicación pedagógica con teoría clara, un caso de estudio, un ejemplo codificable y una explicación línea por línea de ese ejemplo, además de advertencias típicas que un estudiante suele confundir.

## Ejemplo:
```js
let precioProducto = 20;
let cantidad = 3;
let total = precioProducto * cantidad;
console.log("El total a pagar es: " + total);
```

### Explicación del ejemplo

1. `let precioProducto = 20;`
   - Esta línea es una declaración: se crea la variable `precioProducto`.
   - El valor `20` es una expresión, porque produce un valor numérico.

2. `let cantidad = 3;`
   - De nuevo, la línea completa es una declaración.
   - El número `3` es una expresión.

3. `let total = precioProducto * cantidad;`
   - Toda la línea es una declaración, porque define la variable `total`.
   - La parte `precioProducto * cantidad` es una expresión aritmética que produce un valor.

4. `console.log("El total a pagar es: " + total);`
   - Esta línea es una expresión que llama a una función.
   - Dentro, `"El total a pagar es: " + total` es una expresión de concatenación.

---

# PROMP 2 — Precedencia de Operadores

Instrucción:

Actúa como docente experto explicando cómo JavaScript decide el orden de evaluación en una expresión. Usa ejemplos, teoría y análisis detallado.

Contexto:

A veces obtengo resultados inesperados en operaciones matemáticas, y me doy cuenta de que no entiendo cómo JavaScript decide qué resolver primero. Necesito claridad total en este tema.

Entrada:

Explícame cómo funciona la precedencia de operadores en JavaScript.

Salida:

Teoría extensa + ejemplo + análisis detallado + errores comunes.

Ejemplo:

## Ejemplo:
```js
let a = 6 + 2 * 5;
let b = (6 + 2) * 5;
let c = 20 / 2 ** 2;
console.log(a, b, c);

```

## Explicación:

2 * 5 se ejecuta primero → 6 + 10 = 16.

(6 + 2) se ejecuta primero → 8 * 5 = 40.

2 ** 2 = 4 y luego 20 / 4 = 5.


# PROMP 3 — Tipos de Datos Primitivos
------------------------------------------------------------
Instrucción

Quiero que actúes como un docente experto en programación, con una gran habilidad para enseñar conceptos desde cero a estudiantes jóvenes. Tu objetivo será explicar de manera profunda, técnica y altamente pedagógica el funcionamiento de los tipos de datos primitivos en JavaScript, incluyendo su importancia, su papel dentro del lenguaje, sus características fundamentales y sus comportamientos más complejos.
Necesito que seas claro pero a la vez profundo, conectando teoría con práctica, mostrando cómo estos tipos funcionan internamente en el motor de JavaScript, e ilustrando cada concepto con un ejemplo codificable.
Tu explicación deberá incluir: teoría extendida, análisis conceptual, ejemplos reales, explicaciones línea por línea, errores comunes que cometen los estudiantes y un caso aplicado que muestre por qué entender los tipos primitivos es esencial para cualquier desarrollador JavaScript.

Contexto

Soy un estudiante de JavaScript que está construyendo mis primeras bases en programación. Aunque ya sé escribir variables y usar números y textos, me he dado cuenta de que no entiendo realmente qué es un tipo primitivo. He visto palabras como string, number, boolean, undefined, null, symbol, bigint, pero sinceramente solo las memorizo sin comprenderlas.
Esto me genera problemas: comparaciones que no funcionan, operaciones matemáticas que se rompen, valores que no cambian como espero y errores que no sé interpretar. Por ejemplo, me confunde muchísimo que null sea un valor primitivo pero que typeof null diga "object". También me confunde que un string sea "inmutable", o por qué existen BigInt y Symbol en primer lugar.
Siento que mis bases no son sólidas, y no quiero avanzar sin realmente entender estos fundamentos. Necesito una explicación profunda, clara y técnica, como si un profesor experto me lo explicara pacientemente desde cero hasta un nivel profesional.

Entrada

Explícame qué son los tipos de datos primitivos en JavaScript a nivel técnico, pedagógico y con ejemplos detallados.

Salida

Quiero una explicación muy extensa que incluya:

Una definición profunda de qué es un tipo primitivo.

Una explicación completa de los 7 primitivos de JavaScript.

Razones técnicas por las que son inmutables.

Ejemplo codificable creado desde cero.

Explicación línea por línea del ejemplo.

Advertencias y errores típicos de estudiantes.

Un caso de estudio que demuestre por qué dominar los tipos primitivos es esencial.


```js
let nombre = "Sergio";
let edad = 22;
let registrado = true;
let telefono = null;
let direccion;
let claveUnica = Symbol("user_id");
let numeroGrande = 928374982374982374n;

console.log(typeof nombre);
console.log(typeof edad);
console.log(typeof registrado);
console.log(typeof telefono);
console.log(typeof direccion);
console.log(typeof claveUnica);
console.log(typeof numeroGrande);

```

Explicación Línea por Línea
let nombre = "Sergio";

Esto es un string, un tipo primitivo destinado a representar texto.

Los strings en JS son inmutables, lo que significa que no puedes modificar un carácter directamente.

Internamente, JavaScript gestiona los strings como valores fijos en memoria.

let edad = 22;

Esto es un number.

En JavaScript todos los números (enteros, decimales, negativos) comparten el mismo tipo.

No existe int, float, double: todo es number.

let registrado = true;

Esto es un boolean, utilizado para decisiones lógicas.

Solo existen dos valores: true y false.

let telefono = null;

Representa una ausencia INTENCIONAL de valor.

Aunque es primitivo, tiene un error histórico:
typeof null devuelve "object" por un bug del lenguaje.

let direccion;

Si no asignas un valor, JavaScript coloca automáticamente undefined.

Significa “ausencia NO intencional”.

let claveUnica = Symbol("user_id");

Cada Symbol es único, incluso si dos Symbols tienen la misma descripción.

Se utiliza para crear claves privadas o identificadores que no colisionan.

let numeroGrande = 928374982374982374n;

Este es un BigInt, un tipo diseñado para números gigantes que exceden el límite de seguridad de Number.

Se identifica por la letra n al final del número.

# PROMP 4 — Conversión de Tipos 
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript que explica de manera profunda cómo funcionan las conversiones de tipo en el lenguaje. Debes unir teoría, práctica, explicación técnica, ejemplos, casos reales y análisis de errores comunes.
Tu explicación debe cubrir:

Conversión implícita

Conversión explícita

ToString

ToNumber

ToBoolean

Coerción peligrosa

Comparaciones con == y ===

Ejemplos explicados paso a paso

Casos de uso reales en formularios, APIs y lógica de control
Quiero una explicación profesional pero entendible.


Contexto

Soy un estudiante de JS y constantemente me encuentro con resultados que no comprendo. Por ejemplo:

"10" + 5 devuelve "105"

"10" - 5 devuelve 5

Boolean("0") devuelve true

Number("hola") devuelve NaN

Y no sé por qué.
Esto me frustra porque me hace sentir que JS es impredecible, cuando realmente soy yo quien no entiende sus reglas internas.
Sé que la conversión de tipos es una de las partes más importantes del lenguaje, y si no la entiendo, voy a seguir cometiendo errores.

Entrada

Explícame de forma profunda cómo funciona la conversión de tipos en JavaScript con teoría, ejemplos y análisis detallado.

Salida

Quiero una explicación muy extensa que incluya:

Teoría

Conversión implícita vs explícita

Reglas internas de JS

Ejemplo claro

Explicación línea por línea

Advertencias

Errores típicos

Un caso de estudio real

```js
let valor = "25";
let valorNumerico = Number(valor);
let suma = valor + 10;
let resta = valor - 10;
let booleano = Boolean("0");
let invalido = Number("hola");

console.log(valorNumerico, suma, resta, booleano, invalido);

```

Explicación Línea por Línea
let valor = "25";

Literalmente un string, aunque representa un número.

let valorNumerico = Number(valor);

Conversión explícita.

Fuerza a JS a transformar "25" → 25.

let suma = valor + 10;

El operador + prioriza strings.

JS convierte 10 en "10" → "25" + "10" → "2510".

let resta = valor - 10;

El operador - solo funciona con números.

JS convierte "25" a 25 automáticamente.

Resultado: 15.

let booleano = Boolean("0");

"0" es un string NO vacío.

Resultado: true.

let invalido = Number("hola");

No puede convertirse a número

Resultado: NaN (Not a Number)

# PROMP 5 — typeof 
------------------------------------------------------------
Instrucción

Quiero que actúes como un docente experto en JavaScript, capaz de explicar profundamente cómo funciona el operador typeof, sus limitaciones, sus casos especiales y su importancia real dentro del lenguaje. Tu explicación debe incluir teoría detallada, ejemplo codificable, análisis línea por línea, errores comunes, advertencias importantes y un caso de estudio que muestre por qué typeof puede generar confusión incluso en programadores avanzados.
Debes explicar por qué a veces typeof devuelve resultados inesperados, por qué ciertos tipos primitivos son difíciles de detectar y cómo se debe usar correctamente en situaciones reales.

Contexto

Soy un estudiante de JavaScript y he usado typeof desde mis primeros ejercicios, pero muchas veces me encuentro con resultados que simplemente no entiendo. Por ejemplo, ¿por qué typeof null devuelve "object" si null es un tipo primitivo? ¿Por qué un array también devuelve "object" si claramente no es lo mismo que un objeto normal?
Todo esto me genera dudas fuertes sobre cómo JavaScript representa los datos por dentro y cómo funciona realmente su sistema de tipos. Siento que typeof debería ser una herramienta sencilla, pero en la práctica me doy cuenta de que tiene comportamientos extraños que necesito comprender de forma profunda.

Entrada

Explícame cómo funciona el operador typeof en JavaScript de forma extensa, profunda y pedagógica.


Salida

Quiero una explicación amplia que incluya:

Teoría clara

Por qué existen errores históricos

Ejemplo codificable

Análisis línea por línea

Limitaciones del operador

Qué detectar y qué NO detectar con typeof

Caso de estudio y errores comunes


 ```js
console.log(typeof 42);
console.log(typeof "Hola mundo");
console.log(typeof true);
console.log(typeof undefined);
console.log(typeof null);
console.log(typeof {});
console.log(typeof []);
console.log(typeof function saludar(){});
console.log(typeof 9007199254740991n);
console.log(typeof Symbol("clave"));

```

Explicación Línea por Línea
typeof 42

Devuelve "number".

Todos los números, enteros o decimales, son del tipo number.

typeof "Hola mundo"

Devuelve "string".

Cualquier texto, incluso vacío, es de tipo string.

typeof true

Devuelve "boolean".

typeof undefined

Devuelve "undefined".

Es el único valor cuyo typeof coincide 1:1 con su nombre.

typeof null

Devuelve "object".

Este es un error histórico que jamás fue corregido por compatibilidad.

null NO es un objeto, es un primitivo que representa ausencia intencional.

typeof {}

Devuelve "object".

Correcto: un objeto literal es un objeto.

typeof []

Devuelve "object".

typeof NO PUEDE detectar arrays.

Debemos usar:

 ```js

Array.isArray([])

```

typeof function saludar(){}

Devuelve "function".

Este es un caso especial: aunque técnicamente las funciones son objetos, typeof las reconoce con un subtipo único.

typeof 9007199254740991n

Devuelve "bigint".

typeof Symbol("clave")

Devuelve "symbol".

# PROMP 6 — Operadores Aritméticos  
------------------------------------------------------------
Instrucción

Actúa como un docente experto en programación y explícame profundamente cómo funcionan los operadores aritméticos en JavaScript.
Debes desarrollar la explicación con teoría detallada, ejemplos codificables, análisis línea por línea, advertencias, notas especiales y un caso real donde estos operadores afectan cálculos importantes como precios, porcentajes o totales.
Quiero que expliques cada operador aritmético: suma, resta, multiplicación, división, módulo y exponentes.

Contexto

Estoy aprendiendo JavaScript y aunque creo entender la suma y la resta, aún me cuesta visualizar cómo funcionan la división, el módulo y la exponenciación dentro del lenguaje.
He visto operaciones que dan resultados inesperados (como divisiones con decimales extraños), y a veces no sé por qué el operador % devuelve el residuo o por qué el operador ** es preferible a otros métodos.
Necesito entender estos operadores a profundidad, ya que son fundamentales en cálculos reales: precios finales, impuestos, porcentajes, conversiones, operaciones matemáticas básicas y lógicas de juegos o aplicaciones.

Entrada

Explícame detalladamente cómo funcionan los operadores aritméticos en JavaScript.

Salida

Quiero una explicación extensa que incluya:

Teoría detallada

Ejemplo codificable creado desde cero

Explicación línea por línea

Errores comunes

Notas especiales

Aplicaciones reales

 ```js
let suma = 12 + 8;
let resta = 20 - 6;
let multiplicacion = 7 * 4;
let division = 25 / 4;
let residuo = 25 % 4;
let potencia = 3 ** 4;

console.log(suma, resta, multiplicacion, division, residuo, potencia);


```


Explicación Línea por Línea
let suma = 12 + 8;

Operador + → suma.

Resultado → 20.

let resta = 20 - 6;

Operador - → resta.

Resultado → 14.

let multiplicacion = 7 * 4;

Operador * → multiplicación.

Resultado → 28.

let division = 25 / 4;

Operador / → división.

Resultado → 6.25.

JS siempre devuelve números flotantes si corresponde.

let residuo = 25 % 4;

Operador % → residuo o módulo.

25 / 4 = 6 con residuo 1.

let potencia = 3 ** 4;

3 ** 4 es 3 * 3 * 3 * 3.

Resultado → 81.


# PROMP 7 — Operadores Lógicos 
------------------------------------------------------------
Instrucción

Quiero que actúes como un docente experto en JavaScript, con dominio absoluto de la lógica booleana y de cómo funciona el sistema de truthy y falsy en el lenguaje. Debes explicarme profundamente los operadores lógicos: AND (&&), OR (||) y NOT (!), cubriendo teoría, aplicaciones reales, ejemplos codificables, análisis línea por línea, advertencias, errores comunes y situaciones en las que los operadores lógicos no funcionan como un principiante esperaría.
Tu explicación debe mostrar tanto el uso de estos operadores para evaluar condiciones como su comportamiento especial cuando se utilizan con valores no booleanos.

Contexto

Como estudiante de JavaScript, entiendo de manera superficial que los operadores lógicos sirven para trabajar con condiciones. Pero cuando empiezo a escribir código real, me doy cuenta de que no entiendo verdaderamente cómo funcionan.
Por ejemplo:

No sé por qué true && false es false.

No entiendo cómo "" || "Hola" devuelve "Hola".

Me confunde que 0 && "x" dé 0 en lugar de "x".

No entiendo por qué !"texto" da false.
Siento que estoy usando estos operadores de memoria, sin entenderlos. Necesito una explicación profunda que me dé seguridad para trabajar con condiciones, formularios, validaciones y lógica de aplicaciones.

Entrada

Explícame profundamente cómo funcionan los operadores lógicos en JavaScript, teoría y análisis detallado.

Salida

Quiero una explicación extensa que incluya:

Teoría completa

Valores truthy y falsy

Ejemplo creado desde cero

Explicación línea por línea

Advertencias clave

Errores comunes de estudiantes

Caso de estudio aplicado


 ```js
let resultadoAND = true && "JavaScript";
let resultadoOR = "" || "Valor alternativo";
let resultadoNOT = !0;
let mezcla = 5 && 0 && "Hola";
let cortoCircuito = null || false || "Activo";

console.log(resultadoAND, resultadoOR, resultadoNOT, mezcla, cortoCircuito);

```

Explicación Línea por Línea
let resultadoAND = true && "JavaScript";

El operador AND (&&) devuelve el primer valor falsy, o si todos son truthy, devuelve el último.

true es truthy → entonces devuelve "JavaScript".

Resultado: "JavaScript".

let resultadoOR = "" || "Valor alternativo";

El operador OR (||) devuelve el primer valor truthy.

"" es falsy → entonces se salta.

"Valor alternativo" es truthy → resultado final.

let resultadoNOT = !0;

0 es falsy.

!0 → true.

let mezcla = 5 && 0 && "Hola";

Se evalúa de izquierda a derecha.

5 es truthy → pasa.

0 es falsy → se detiene allí.

Resultado: 0.

let cortoCircuito = null || false || "Activo";

null → falsy

false → falsy

"Activo" → truthy → resultado "Activo"

Valores Truthy y Falsy
Falsy:

0

"" (cadena vacía)

null

undefined

false

Truthy:

Todo lo que NO sea falsy.

Ejemplo: "0" es truthy, "false" es truthy, {} es truthy.

# PROMP 8 — Operadores de Comparación 
------------------------------------------------------------
Instrucción

Quiero que actúes como un profesor de JavaScript con un dominio profundo de cómo funciona la comparación en el lenguaje. Debes explicarme la diferencia entre comparación débil (==) y comparación estricta (===), así como los operadores >, <, >=, <=, !=, !==, incluyendo casos especiales, conversión implícita, errores comunes y ejemplos claros.
Necesito una explicación extensa y pedagógica para comprender realmente cuándo usar cada operador y por qué la comparación estricta es más segura.

Contexto

Estoy aprendiendo JavaScript, pero constantemente me confundo con las comparaciones. No entiendo por qué:

5 == "5" es true

null == undefined también es true

false == 0 es true

pero luego false === 0 es false
Todo esto me parece muy extraño.
Me doy cuenta de que JavaScript hace conversiones internas cuando uso ==, y eso me causa resultados inesperados. Necesito entender qué pasa exactamente dentro del lenguaje y cómo comparar valores correctamente sin depender de la intuición.

Entrada

Explícame profundamente cómo funcionan los operadores de comparación en JavaScript, incluyendo la diferencia entre comparación débil y estricta.

Salida

Quiero una explicación completa con:

Teoría detallada

Comparación débil vs estricta

Tabla de conversión implícita

Ejemplo codificable

Explicación línea por línea

Advertencias y errores comunes

Casos especiales

Caso práctico

 ```js
let comparacion1 = 5 == "5";
let comparacion2 = 5 === "5";
let comparacion3 = null == undefined;
let comparacion4 = null === undefined;
let comparacion5 = false == 0;
let comparacion6 = false === 0;

console.log(comparacion1, comparacion2, comparacion3, comparacion4, comparacion5, comparacion6);


```

Explicación Línea por Línea
5 == "5"

El operador == convierte ambos valores al mismo tipo.

"5" se convierte a número.

Resultado: true.

5 === "5"

Compara tipo + valor.

Los tipos difieren → false.

null == undefined

Regla especial del lenguaje.

Son iguales solo con ==.

Resultado: true.

null === undefined

Tipos distintos → false.

false == 0

JS convierte false a número → 0

0 == 0 → true

false === 0

Tipos diferentes → false.

# PROMP 9 — Variables 
------------------------------------------------------------
Instrucción

Quiero que actúes como un docente experto en JavaScript y me expliques con absoluta profundidad, claridad y estructura la diferencia entre las tres formas de declarar variables: var, let y const. Tu explicación debe profundizar en temas como scope (alcance), hoisting, reasignación, redeclaración, temporal dead zone, características internas, casos de uso, buenas prácticas modernas y peligros comunes.
Necesito que desarrolles una explicación que no solo diga qué hace cada una, sino por qué existen, cómo funcionan internamente en el motor de JavaScript y cómo afectan el comportamiento del código en situaciones reales.

Contexto

Soy un estudiante aprendiendo JavaScript y todavía me confunde entender cuándo debo usar var, let o const. He visto que algunas personas dicen que var es “peligroso”, pero no sé por qué. También he escuchado términos como “hoisting”, “scope de función”, “scope de bloque”, “temporal dead zone”, pero no los comprendo.
Cuando intento escribir código, uso lo que sea que recuerdo sin saber realmente cuál es la opción correcta. Esto me genera errores, comportamientos inesperados y dudas al leer código de otros desarrolladores.
Quiero una explicación extensa, profunda y profesional que me deje claro cómo funcionan estas tres palabras clave.

Entrada

Explícame profundamente la diferencia entre var, let y const en JavaScript, con teoría, análisis detallado.

Salida

Quiero una explicación completa que incluya:

Teoría detallada

Scope de cada tipo de variable

Hoisting explicado profesionalmente

Reasignación y redeclaración

Ejemplo codificable

Explicación línea por línea

Advertencias

Errores típicos

Buenas prácticas recomendadas por la industria

 ```js
var nombre = "Luis";
let edad = 21;
const pais = "Colombia";

nombre = "Carlos";
edad = 22;

try {
  pais = "Argentina";
} catch(e) {
  console.log("Error al intentar modificar const:", e.message);
}

console.log(nombre, edad, pais);

```

Explicación Línea por Línea
var nombre = "Luis";

var tiene scope de función, no de bloque.

Puede redeclararse y reasignarse.

Se eleva al inicio del contexto (“hoisting”) con valor undefined.

let edad = 21;

Tiene scope de bloque.

No permite redeclaración en el mismo bloque.

Sí permite reasignación.

Existe en la temporal dead zone hasta que se ejecuta su línea.

const pais = "Colombia";

Scope de bloque.

NO permite reasignación.

NO permite redeclaración.

nombre = "Carlos";

Válido: var permite reasignar.

edad = 22;

Válido: let permite reasignar.

Bloque try modificando un const

pais = "Argentina"; produce un error porque const no permite reasignar.

Se captura en el catch.

console.log(nombre, edad, pais);

Muestra: "Carlos", 22, "Colombia".

Hoisting explicado profesionalmente

var se eleva → pero su valor es undefined hasta su asignación.

let y const también se elevan → pero NO son accesibles antes de su línea → temporal dead zone.

Acceder a una variable let antes de declararla produce error, no undefined.

# PROMP 10 — Template Strings 
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame profundamente qué son los Template Strings (template literals). Necesito que desarrolles teoría, sintaxis, características avanzadas, interpolación, saltos de línea, expresiones dentro de plantillas, beneficios, casos reales y diferencias con la concatenación tradicional.
Debe ser una explicación larga, completa, profesional y pedagógica, acompañada de ejemplos reales y análisis línea por línea.

Contexto

Soy un estudiante que viene de usar concatenación clásica con comillas " " y el operador +. Pero ya me di cuenta de que eso hace el código difícil de leer, especialmente cuando hay variables, textos largos o múltiples líneas.
He visto que existen template strings con comillas invertidas (` `), pero no entiendo completamente su potencial, ni cómo se usan correctamente.
Quiero aprenderlos a profundidad para mejorar la calidad y legibilidad de mi código.

Entrada

Explícame profundamente qué son los template strings en JavaScript con teoría,  análisis detallado.

Salida

Quiero una explicación completa que incluya:

Teoría avanzada

Sintaxis moderna

Interpolación

Expresiones dentro de la plantilla

Multi-líneas

Ejemplo codificable

Explicación línea por línea

Ventajas

Casos reales


 ```js
let nombre = "Sergio";
let edad = 22;
let mensaje = `Hola ${nombre}, tienes ${edad} años y en 2 años tendrás ${edad + 2}.`;

let descripcionLarga = `
Este es un texto
que ocupa varias
líneas gracias a los template strings.
`;

console.log(mensaje);
console.log(descripcionLarga);


```


Explicación Línea por Línea
let nombre = "Sergio";

Variable tradicional.

let edad = 22;

Otra variable que interpolaremos dentro del template.

let mensaje = \Hola ${nombre}, tienes ${edad} años y en 2 años tendrás ${edad + 2}.`;`

Uso de comillas invertidas.

${variable} permite insertar valores directamente sin concatenar.

${edad + 2} demuestra que se pueden ejecutar expresiones dentro del texto.

Template multilínea

No necesitas \n.

Basta con escribir el texto en varias líneas dentro de las comillas invertidas.

Ventajas Clave de los Template Strings

Mucho más legibles que concatenar con "texto" + variable.

Permiten expresiones dentro del texto.

Ideal para construir HTML, mensajes, logs y textos complejos.

Permiten texto en múltiples líneas.

Son estándar moderno del lenguaje.

# PROMP 11 — Operadores de Asignación 
------------------------------------------------------------
Instrucción

Quiero que actúes como un docente experto en JavaScript y me expliques a profundidad cómo funcionan los operadores de asignación del lenguaje. Debes cubrir el operador básico =, así como todas sus variantes: +=, -=, *=, /=, %= y **=. Tu explicación debe ser pedagógica, técnica y extensa, mostrando cómo cada uno transforma el valor de una variable.
Necesito teoría completa, ejemplos reales, casos prácticos, errores comunes, advertencias y un ejemplo codificable con análisis línea por línea.

Contexto

Soy un estudiante que ya sabe usar variables, pero todavía me confunde entender cómo funcionan los operadores de asignación combinada.
Por ejemplo:

No entiendo por qué x += 5 no es lo mismo que x = x + 5 en algunos casos.

Me confunde el operador **= porque no entiendo cómo funciona la potencia.

He visto que estos operadores hacen el código más corto, pero me da miedo usarlos mal.

También me cuesta entender qué pasa internamente cuando aplico varias operaciones a una misma variable.
Necesito una explicación extensa y que me deje claro cuándo usar estos operadores profesionalmente.

Entrada

Explícame profundamente cómo funcionan los operadores de asignación en JavaScript con teoría,  análisis técnico.

Salida

Quiero una explicación que incluya:

Teoría

Lista completa de operadores

Ejemplo creado desde cero

Explicación línea por línea

Notas técnicas

Errores comunes

Caso de estudio

 ```js
let puntos = 10;

puntos += 5;
puntos -= 3;
puntos *= 2;
puntos /= 4;
puntos %= 3;
puntos **= 3;

console.log(puntos);

```

Explicación Línea por Línea
let puntos = 10;

Inicializamos la variable con el valor 10.

puntos += 5;

Equivale a puntos = puntos + 5;

Resultado: 15.

puntos -= 3;

Equivale a puntos = puntos - 3;

Resultado: 12.

puntos *= 2;

Equivale a puntos = puntos * 2;

Resultado: 24.

puntos /= 4;

Equivale a puntos = puntos / 4;

Resultado: 6.

puntos %= 3;

Equivale a puntos = puntos % 3;

6 % 3 = 0.

puntos **= 3;

Equivale a puntos = puntos ** 3;

0 elevado a 3 → 0.

console.log(puntos);

Resultado final → 0.


# PROMP 12 — Objetos en JavaScript 
------------------------------------------------------------
Instrucción

Quiero que actúes como un docente experto y expliques de manera profunda qué son los objetos en JavaScript, incluyendo su estructura interna, cómo funcionan las propiedades, cómo se accede a ellas, cómo se modifican y cómo se eliminan.
Necesito teoría avanzada, ejemplos reales, casos modernos, explicación de notación de punto, notación de corchetes, mutabilidad, referencias en memoria y errores comunes.

Contexto

Como estudiante, entiendo que un objeto es “una estructura con claves y valores”, pero no entiendo realmente lo que significa que los objetos sean mutables, que se pasen por referencia o por qué a veces cuando copio un objeto y lo modifico, se modifica también el original.
También me confunde cuándo usar corchetes y cuándo usar el punto. Quiero entender los objetos a un nivel profundo, como un programador profesional.

Entrada

Explícame profundamente qué son los objetos en JavaScript y cómo funcionan con teoría, análisis detallado.

Salida

Quiero una explicación extensa que incluya:

Teoría completa

Mutabilidad

Propiedades

Formas de acceso

Ejemplo codificable

Explicación línea por línea

Advertencias

Errores comunes

Caso práctico real

 ```js
let usuario = {
  nombre: "Carlos",
  edad: 25,
  activo: true
};

usuario.edad = 26;
usuario["activo"] = false;

delete usuario.nombre;

console.log(usuario);


```

Explicación Línea por Línea
let usuario = { ... };

Crea un objeto literal con tres propiedades.

Los objetos almacenan valores organizados por claves.

Son mutables: su contenido puede cambiar.

usuario.edad = 26;

Notación de punto.

Cambia el valor de la propiedad edad.

usuario["activo"] = false;

Notación de corchetes.

Permite usar claves dinámicas o variables como nombre de propiedad.

delete usuario.nombre;

Elimina la propiedad nombre del objeto.

console.log(usuario);

Resultado: { edad: 26, activo: false }

# PROMP 13 — Métodos en Objetos
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame qué son los métodos dentro de un objeto. Necesito que desarrolles una explicación completa sobre cómo funcionan, qué papel tienen dentro de la programación orientada a objetos en JS, cómo utilizan el contexto this, y por qué son fundamentales para modelar comportamientos dentro de estructuras de datos.

Contexto

He visto objetos que tienen funciones dentro, pero no entiendo por qué esas funciones se llaman “métodos”. Tampoco comprendo por qué dentro de esas funciones se puede usar this para acceder a otras propiedades del objeto. Como estudiante, siento que me falta entender cómo darle “vida” a un objeto para que no solo almacene datos, sino que ejecute acciones.
Quiero entender esto de manera profunda, clara y práctica.

Entrada

Explícame qué son los métodos dentro de un objeto en JavaScript, cómo funcionan, cómo se invocan y cómo utilizan this.

Salida

Quiero una explicación completa que incluya teoría, un ejemplo codificable y un análisis línea por línea

 ```js
const persona = {
  nombre: "Daniel",
  edad: 28,
  saludar() {
    return `Hola, soy ${this.nombre}, tengo ${this.edad} años.`;
  },
  cumplirAnios() {
    this.edad += 1;
    return `Ahora tengo ${this.edad} años.`;
  }
};

console.log(persona.saludar());
console.log(persona.cumplirAnios());
console.log(persona.saludar());

```

Explicación Línea por Línea
const persona = { ... }

Creamos un objeto literal con propiedades (nombre, edad) y dos métodos (saludar, cumplirAnios).

saludar() { ... }

Es un método, no una función externa.
Representa un comportamiento asociado a la persona.

this.nombre

this apunta al objeto persona, por lo que accede correctamente a su propiedad nombre.

cumplirAnios()

Método que modifica el estado interno del objeto.
this.edad += 1 incrementa la edad.

Las llamadas a los métodos

persona.saludar() devuelve un mensaje con nombre y edad.

persona.cumplirAnios() aumenta la edad.

Volver a llamar persona.saludar() muestra el cambio aplicado.


# PROMP 14 — Arrays en JavaScript
------------------------------------------------------------
Instrucción

Actúa como docente experto y explícame qué son los arrays en JavaScript, cómo funcionan, cómo se manipulan y por qué son tan importantes en la programación moderna. Necesito teoría, ejemplos prácticos, métodos principales y una explicación línea por línea.

Contexto

Entiendo que un array es una lista de valores, pero no entiendo realmente cómo se almacenan, cómo acceder a ellos, por qué comienzan en índice 0, ni cómo funcionan métodos como push, pop, shift, indexOf, etc.
Quiero una explicación clara y completa.

Entrada

Explícame profundamente qué es un array, cómo se crea y cómo se manipula usando sus métodos básicos.

Salida

Quiero teoría, ejemplo largo, explicación línea por línea

 ```js
let frutas = ["Manzana", "Pera", "Banano"];

frutas.push("Uva");
frutas.unshift("Mango");

let primera = frutas.shift();
let ultima = frutas.pop();

let posicion = frutas.indexOf("Pera");

console.log(frutas, primera, ultima, posicion);


```

Explicación Línea por Línea
let frutas = ["Manzana", "Pera", "Banano"];

Creamos un array con tres elementos, posicionados en índices 0, 1 y 2.

frutas.push("Uva");

Agrega un elemento al final del array.

frutas.unshift("Mango");

Agrega un elemento al inicio del array.

let primera = frutas.shift();

Elimina y devuelve el primer elemento.

let ultima = frutas.pop();

Elimina y devuelve el último elemento.

let posicion = frutas.indexOf("Pera");

Busca la posición de "Pera".
Si no existe, devuelve -1.

console.log(...)

Muestra el array final y los valores removidos.


# PROMP 15 — Métodos de Arrays: map, filter, reduce
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame profundamente cómo funcionan los métodos map, filter y reduce. Quiero que detalles qué hace cada uno, para qué sirven, cómo transforman un array y cuál es su propósito real dentro de la programación funcional moderna.

Contexto

Como estudiante, me cuesta entender cuándo usar map, cuándo usar filter y por qué reduce parece tan complicado. Veo estos métodos en código profesional, pero todavía no logro comprender a fondo cómo funcionan internamente ni cómo escribirlos correctamente.

Entrada

Explícame map, filter y reduce con teoría, ejemplos y análisis línea por línea.

Salida

Teoría clara, ejemplo práctico, y análisis

 ```js
let numeros = [1, 2, 3, 4, 5];

let dobles = numeros.map(n => n * 2);
let pares = numeros.filter(n => n % 2 === 0);
let sumaTotal = numeros.reduce((acum, n) => acum + n, 0);

console.log(dobles, pares, sumaTotal);

```


Explicación Línea por Línea
let numeros = [1, 2, 3, 4, 5];

Array base sobre el cual aplicaremos los métodos.

let dobles = numeros.map(n => n * 2);

map crea un nuevo array transformando cada elemento.

No modifica el array original.

Para cada n, devuelve n * 2.

Resultado → [2, 4, 6, 8, 10].

let pares = numeros.filter(n => n % 2 === 0);

filter devuelve un nuevo array con los elementos que cumplen la condición.

Solo mantiene los números pares.

Resultado → [2, 4].

let sumaTotal = numeros.reduce((acum, n) => acum + n, 0);

reduce acumula todos los valores en un solo resultado.

acum empieza en 0.

Se suman uno a uno los valores del arreglo.

Resultado → 15.


# PROMP 16 — Bucles: for, while, for…of, for…in
------------------------------------------------------------
Instrucción

Explícame cómo funcionan los principales bucles de JavaScript: for, while, for…of y for…in.
Quiero teoría completa, ejemplos claros y análisis detallado.

Contexto

Sé que los bucles sirven para repetir código, pero no entiendo cuál usar en qué situación. También me confunde la diferencia entre for…of (valores) y for…in (propiedades). Quiero aprender esto bien.

Entrada

Explícame los distintos tipos de bucles y cómo funcionan.

Salida

Una explicación completa, con ejemplo codificable y análisis línea por línea.


 ```js
let numeros = [10, 20, 30];

for (let i = 0; i < numeros.length; i++) {
  console.log("For clásico:", numeros[i]);
}

let contador = 0;
while (contador < 3) {
  console.log("While:", contador);
  contador++;
}

for (let valor of numeros) {
  console.log("For...of:", valor);
}

let persona = { nombre: "Ana", edad: 25 };
for (let clave in persona) {
  console.log("For...in:", clave, persona[clave]);
}


```


Explicación Línea por Línea

For clásico

 ```js
for (let i = 0; i < numeros.length; i++) {
  console.log("For clásico:", numeros[i]);
}


```

Recorre con índice.

Ideal para controlar posiciones del array.

i++ incrementa el índice.

While
 ```js
let contador = 0;
while (contador < 3) {
  console.log("While:", contador);
  contador++;
}

```
Repite mientras la condición sea verdadera.

Riesgo: bucles infinitos si no se incrementa el contador.

For…of
 ```js
for (let valor of numeros) {
  console.log("For...of:", valor);
}


```


Recorre valores de arrays, strings y estructuras iterables.

No da acceso directo al índice.

For…in
 ```js
for (let clave in persona) {
  console.log("For...in:", clave, persona[clave]);
}


```
Recorre propiedades de objetos.

Útil para leer claves dinámicas.

# PROMP 17 — Funciones Declaradas vs Funciones Expresadas
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame la diferencia entre funciones declaradas y funciones expresadas, incluyendo cómo funcionan, cómo se ejecutan, qué diferencias internas tienen en cuanto al hoisting y por qué es importante entenderlas al desarrollar código limpio y profesional.

Contexto

Como estudiante, veo funciones que se escriben de formas distintas, y aunque ambas funcionan, no entiendo por qué elegir una sobre la otra.
Me confunde el tema del “hoisting”, y no sé por qué una función declarada se puede usar antes de su definición, mientras que una función expresada no.

Entrada

Explícame detalladamente la diferencia entre funciones declaradas y funciones expresadas con teoría, ejemplos y análisis línea por línea.

Salida

Quiero teoría, ejemplo real, análisis técnico, errores comunes y recomendaciones.


 ```js
// Función declarada
function sumar(a, b) {
  return a + b;
}

// Función expresada
const restar = function(a, b) {
  return a - b;
};

console.log(sumar(5, 3));
console.log(restar(5, 3));

```
Explicación Línea por Línea

 ```js
Función Declarada

function sumar(a, b) {
  return a + b;
}
Se “eleva” durante el hoisting.

Puede llamarse antes de que aparezca en el código.

Ideal para funciones reutilizables que deben estar disponibles globalmente en el archivo.


// Función expresada
const restar = function(a, b) {
  return a - b;
};

```

No se eleva como función, solo como variable.

No puede llamarse antes de ser definida.

Está ligada al comportamiento de const o let.

Es útil para funciones que deseas tratar como valores.


# PROMP 18 — Funciones Flecha (Arrow Functions)
------------------------------------------------------------
Instrucción

Actúa como docente experto y explícame profundamente cómo funcionan las arrow functions en JavaScript: sintaxis, reglas especiales, el comportamiento de this, cuándo usarlas y cuándo no.

Contexto

He visto arrow functions por todos lados en código moderno, pero no entiendo completamente por qué existen, ni su diferencia con las funciones tradicionales.
También he escuchado que tienen un this diferente y que no deben usarse como métodos de objetos.

Entrada

Explícame las arrow functions con teoría, ejemplo y análisis técnico.

Salida

Necesito teoría completa, explicación línea por línea

 ```js
const sumar = (a, b) => a + b;

const saludar = nombre => `Hola ${nombre}`;

const usuario = {
  nombre: "Laura",
  saludar: () => `Hola, soy ${this.nombre}`
};

console.log(sumar(3, 4));
console.log(saludar("Andrés"));
console.log(usuario.saludar());


```

Explicación Línea por Línea
const sumar = (a, b) => a + b;

Arrow function corta.

Retorno implícito cuando no se usan llaves {}.

Ideal para funciones simples.

const saludar = nombre => \Hola ${nombre}`;`

Un solo parámetro → no necesita paréntesis.

Retorna directamente una plantilla.

 ```js
const usuario = {
  nombre: "Laura",
  saludar: () => `Hola, soy ${this.nombre}`
};

```

Aquí NO funciona bien.

Arrow function no crea su propio this.

this.nombre será undefined porque no apunta al objeto.


# PROMP 19 — Parámetros y Argumentos en Funciones
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame claramente la diferencia entre parámetros y argumentos, cómo funcionan dentro de una función, cómo se pasan valores, qué ocurre si no se envían argumentos suficientes y por qué estos conceptos son esenciales para escribir funciones reutilizables.

Contexto

Como estudiante, me confunde mucho el tema de “parámetros vs argumentos”. A veces veo funciones con varios parámetros, pero cuando las llamo, si olvido enviar un valor, el resultado es undefined. También he visto que JavaScript permite más argumentos de los necesarios, y no sé cómo se manejan.
Necesito entender este concepto con ejemplos claros y aplicados.

Entrada

Explícame la diferencia entre parámetros y argumentos, y cómo funcionan dentro de una función.

Salida

Quiero teoría detallada, ejemplo práctico, explicación línea por línea


 ```js
function saludar(nombre, edad) {
  return `Hola ${nombre}, tienes ${edad} años.`;
}

let mensaje1 = saludar("Carolina", 27);
let mensaje2 = saludar("Luis");

console.log(mensaje1);
console.log(mensaje2);

```

Explicación Línea por Línea
function saludar(nombre, edad)

Parámetros: son las variables que la función espera recibir.

Aquí los parámetros son nombre y edad.

return \Hola ${nombre}, tienes ${edad} años.`;`

Usamos los parámetros para construir un mensaje.

Si un parámetro no recibe argumento, será undefined.

let mensaje1 = saludar("Carolina", 27);

"Carolina" y 27 son argumentos, valores enviados a la función.

Ambos parámetros reciben valor → funciona perfecto.

let mensaje2 = saludar("Luis");

Solo enviamos un argumento.

nombre = "Luis"

edad = undefined

Resultado: "Hola Luis, tienes undefined años."

Errores Comunes

Pensar que parámetros y argumentos son lo mismo (no lo son).

Olvidar enviar argumentos → produce valores undefined.

Enviar argumentos de más → JavaScript los ignora a menos que uses ...rest.

# PROMP 20 — Parámetros por Defecto
------------------------------------------------------------
Instrucción

Actúa como docente experto en JavaScript y explícame cómo funcionan los parámetros por defecto, cuándo usarlos, por qué existen y cómo ayudan a evitar valores undefined dentro de las funciones.

Contexto

Me pasa que cuando llamo a una función y olvido enviar un argumento, el valor se vuelve undefined. He visto que existe la sintaxis de “parámetros por defecto”, pero no la entiendo completamente ni sé cuándo usarla.

Entrada

Explícame cómo funcionan los parámetros por defecto con teoría y un ejemplo.

Salida

Quiero teoría clara, ejemplo codificable, explicación línea por línea 

 ```js
function registrarUsuario(nombre = "Invitado", pais = "Desconocido") {
  return `Usuario: ${nombre}, País: ${pais}`;
}

let a = registrarUsuario("Laura", "Colombia");
let b = registrarUsuario("Carlos");
let c = registrarUsuario();

console.log(a);
console.log(b);
console.log(c);

```
Explicación Línea por Línea
function registrarUsuario(nombre = "Invitado", pais = "Desconocido")

Si no se envía un argumento, se usa el valor definido por defecto.

Evita resultados inesperados como "undefined".

registrarUsuario("Laura", "Colombia")

Ambos argumentos se envían → la función usa esos valores.

registrarUsuario("Carlos")

Solo recibe el primer argumento.

pais no se envía → toma "Desconocido".

registrarUsuario()

Ningún argumento.

Ambos parámetros toman los valores por defecto.


# PROMP 21 — Operador Spread (...)
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame cómo funciona el operador spread (...), para qué sirve, qué problemas resuelve y cómo se usa tanto en arrays como en objetos. Incluye teoría, ejemplos claros y explicación línea por línea.

Contexto

Como estudiante, me confunde ver el operador ... en el código. A veces lo veo en arrays, otras en objetos, y no entiendo si copia, si expande, si mezcla o si convierte elementos. Necesito entender su propósito real y cómo usarlo correctamente.

Entrada

Explícame qué hace el operador spread y cómo se usa en arrays y objetos.

Salida

Una explicación completa, con teoría, ejemplos y advertencias.


 ```js
let numeros = [1, 2, 3];
let copia = [...numeros];
let mezcla = [...numeros, 4, 5];

let usuario = { nombre: "Laura", edad: 25 };
let copiaUsuario = { ...usuario, activo: true };

console.log(copia, mezcla, copiaUsuario);


```

Explicación Línea por Línea

Array Spread
let copia = [...numeros];

Crea una copia superficial del array.

NO modifica el original.

Cada elemento se expande dentro del nuevo array.

let mezcla = [...numeros, 4, 5];

Inserta cada elemento de numeros individualmente.

Luego agrega valores extra.

Object Spread
let copiaUsuario = { ...usuario, activo: true };

Copia todas las propiedades del objeto original.

Agrega (o reemplaza) propiedades nuevas.

El resultado es un objeto actualizado sin mutar el original.


# PROMP 22 — Rest Parameters (...args)
------------------------------------------------------------
Instrucción

Actúa como docente experto y explícame cómo funcionan los rest parameters, cuándo se usan, por qué existen y cómo permiten capturar múltiples argumentos en una función.

Contexto

Me confunde que el mismo símbolo ... del spread también se use para agrupar valores. No entiendo cómo diferencia JavaScript cuándo está expandiendo y cuándo está agrupando. Necesito entenderlo con claridad.

Entrada

Explícame cómo funcionan los parámetros rest con teoría y ejemplo.

Salida

Teoría, ejemplo extenso, análisis


 ```js
function sumar(...numeros) {
  return numeros.reduce((acc, n) => acc + n, 0);
}

let resultado = sumar(1, 2, 3, 4, 5);

console.log(resultado);

```

Explicación Línea por Línea

function sumar(...numeros)

...numeros agrupa todos los argumentos en un array real.

Sin importar cuántos argumentos envíes, quedan dentro del arreglo.

numeros.reduce((acc, n) => acc + n, 0)

Recorre todos los números acumulándolos.

0 es el valor inicial.

sumar(1, 2, 3, 4, 5)

Todos los valores ingresan dentro del parámetro rest.

Resultado final → 15.

# PROMP 23 — Desestructuración de Arrays (Array Destructuring)
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame cómo funciona la desestructuración de arrays, para qué sirve, cómo facilita el código, y cuáles son sus formas más comunes. Incluye teoría clara, un ejemplo práctico, explicación línea por línea, advertencias y un caso aplicado.

Contexto

He visto este tipo de sintaxis:


 ```js
const [a, b] = numeros;

```

Pero no entiendo completamente qué significa ni por qué es útil.
Quiero comprender cómo funciona, qué ventajas tiene y cómo usarla correctamente para extraer valores de arreglos.

Entrada

Explícame qué es la desestructuración de arrays en JavaScript y cómo utilizarla correctamente.

Salida

Teoría completa, ejemplo codificable, explicación paso a paso 

 ```js
let colores = ["Rojo", "Verde", "Azul"];

let [primero, segundo, tercero] = colores;

let [soloUno] = colores;

let [a, , c] = colores;

console.log(primero, segundo, tercero);
console.log(soloUno);
console.log(a, c);


```


Explicación Línea por Línea
let colores = ["Rojo", "Verde", "Azul"];

Tenemos un array con tres valores.

let [primero, segundo, tercero] = colores;

Extrae cada elemento del array en variables independientes.

primero = "Rojo"

segundo = "Verde"

tercero = "Azul"

let [soloUno] = colores;

Obtiene SOLO el primer valor.

Los demás no se almacenan.

let [a, , c] = colores;

“Saltamos” el índice 1.

a = "Rojo"

c = "Azul"

console.log(...)

Muestra los resultados de cada desestructuración.


# PROMP 24 — Desestructuración de Objetos (Object Destructuring)
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame cómo funciona la desestructuración de objetos, cómo se usa correctamente, cómo renombrar propiedades, cómo usar valores por defecto y por qué es una técnica fundamental en JavaScript moderno.

Contexto

He visto código así:

 ```js
const { nombre, edad } = persona;

```

Pero no entiendo completamente cómo funciona, ni qué pasa si el nombre de la propiedad no coincide, ni cómo asignarle un nombre diferente. Quiero dominar esta técnica porque la veo en todos los proyectos y documentación moderna.

Entrada

Explícame cómo funciona la desestructuración de objetos con teoría, ejemplo y análisis.

Salida

Una explicación clara, extensa y con ejemplo completo.

 ```js
let usuario = {
  nombre: "Carlos",
  edad: 29,
  pais: "México"
};

let { nombre, edad } = usuario;

let { pais: nacionalidad } = usuario;

let { profesion = "No especificado" } = usuario;

console.log(nombre, edad, nacionalidad, profesion);

```

Explicación Línea por Línea
let usuario = { ... };

Creamos un objeto con tres propiedades.

let { nombre, edad } = usuario;

Extraemos propiedades del objeto.

nombre = "Carlos"

edad = 29

Los nombres deben coincidir exactamente con las claves del objeto.

let { pais: nacionalidad } = usuario;

Desestructuración con renombramiento.

pais es la propiedad original.

nacionalidad es el nombre de la nueva variable.

let { profesion = "No especificado" } = usuario;

La propiedad no existe en el objeto.

Se asigna el valor por defecto "No especificado".

console.log(...)

Muestra todas las variables obtenidas.

# PROMP 25 — JSON: Qué es y cómo se usa en JavaScript
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame qué es JSON, cómo funciona, cuál es su estructura, cómo se convierte desde y hacia JavaScript, y para qué se utiliza en aplicaciones reales. Incluye teoría clara, ejemplo codificable, explicación línea por línea y advertencias importantes.

Contexto

Como estudiante, he escuchado mucho el término JSON, sobre todo cuando se habla de APIs, bases de datos, backend, peticiones HTTP, etc.
Pero todavía no entiendo del todo qué es, cómo está estructurado y por qué JavaScript lo maneja tan fácilmente.
También me confunde cuándo usar JSON.stringify y cuándo usar JSON.parse.

Entrada

Explícame qué es JSON, cómo se usa en JavaScript y cómo convertir objetos a JSON y JSON a objetos.

Salida

Teoría sólida, ejemplo, análisis línea por línea

 ```js
let usuario = {
  nombre: "Ana",
  edad: 30,
  activo: true
};

let json = JSON.stringify(usuario);
let objeto = JSON.parse(json);

console.log(json);
console.log(objeto);

```
Explicación Línea por Línea
let usuario = { ... }

Creamos un objeto de JavaScript con propiedades típicas.

let json = JSON.stringify(usuario);

Convierte el objeto a una cadena JSON.

JSON es TEXTO, no es un objeto real.

Útil para enviar datos por internet o almacenarlos.

Ejemplo del resultado:
"{"nombre":"Ana","edad":30,"activo":true}"

let objeto = JSON.parse(json);

Convierte el texto JSON nuevamente a un objeto JavaScript real.

console.log(json)

Imprime el texto JSON.

console.log(objeto)

Imprime el objeto convertido.


# PROMP 26 — Manejo de Errores con try…catch
------------------------------------------------------------
Instrucción

Actúa como docente experto en JavaScript y explícame cómo funciona el manejo de errores con try…catch, cuándo usarlo, cómo capturar errores, cómo manejar errores asincrónicos y cómo usar finally. Incluye teoría y ejemplo.

Contexto

Como estudiante, cuando el código falla la consola muestra errores rojos y no sé cómo controlarlos para que el programa no deje de funcionar.
He visto try…catch, pero no sé exactamente qué hace ni cómo se usa correctamente.

Entrada

Explícame profundamente cómo manejar errores usando try…catch.

Salida

Teoría clara, ejemplo codificable, análisis y advertencias.

 ```js
function dividir(a, b) {
  try {
    if (b === 0) {
      throw new Error("No se puede dividir entre cero");
    }
    return a / b;
  } catch (error) {
    console.log("Error capturado:", error.message);
  } finally {
    console.log("Operación finalizada");
  }
}

dividir(10, 2);
dividir(10, 0);

```

Explicación Línea por Línea
try { ... }

Aquí va el código que podría fallar.

Si ocurre un error, se salta automáticamente al catch.

if (b === 0) { throw new Error(...) }

Lanzamos un error manualmente para evitar operaciones inválidas.

catch (error) { ... }

Aquí capturamos el error.

error.message contiene la descripción del error.

finally { ... }

Este bloque SIEMPRE se ejecuta.

Útil para cerrar conexiones, limpiar recursos, mostrar mensajes finales, etc.

Llamadas a la función

dividir(10, 2) funciona normalmente.

dividir(10, 0) activa el error → pasa al catch.

# PROMP 27 — Asincronía en JavaScript (Concepto General)
------------------------------------------------------------
Instrucción

Actúa como docente experto en JavaScript y explícame profundamente qué es la asincronía, por qué existe en el lenguaje, cómo funciona el event loop, y cómo permite que JavaScript maneje múltiples tareas sin bloquear la ejecución.

Contexto

Como estudiante, me confunde totalmente el concepto de asincronía. He visto cosas como setTimeout, promesas, callbacks y async/await, pero no entiendo por qué funcionan de forma “diferida” ni por qué el código parece ejecutarse fuera de orden.
Necesito una explicación clara que me ayude a entender todo desde la base.

Entrada

Explícame qué es la asincronía en JavaScript con teoría y ejemplo.

Salida

Quiero teoría completa, ejemplo claro, explicación línea por línea 


 ```js
console.log("Inicio");

setTimeout(() => {
  console.log("Proceso asincrónico");
}, 2000);

console.log("Fin");

```

Explicación Línea por Línea

console.log("Inicio");

Se ejecuta inmediatamente.

setTimeout(() => { ... }, 2000);

Envía la función al Event Loop.

No se ejecuta de inmediato.

Se programa para ejecutarse después de 2 segundos.

JavaScript continúa sin esperar.

console.log("Fin");

Se imprime antes del mensaje asincrónico.

# PROMP 28 — Promesas (Promises)
------------------------------------------------------------
Instrucción

Actúa como docente experto en JavaScript y explícame qué es una Promise, para qué sirve, cómo funciona su ciclo interno y cuáles son sus estados: pending, fulfilled, rejected. Incluye teoría clara, ejemplo real y análisis completo.

Contexto

He oído mucho sobre Promesas, pero todavía me confunden.
No entiendo cómo funcionan, cuándo se resuelven, qué significa .then() y .catch(), o por qué son mejores que los callbacks anidados.

Entrada

Explícame profundamente qué son las promesas en JavaScript y cómo se utilizan.

Salida

Quiero teoría, ejemplo codificable, explicación línea por línea y errores comunes.


 ```js
function tareaAsincronica() {
  return new Promise((resolve, reject) => {
    let exito = true;

    setTimeout(() => {
      if (exito) resolve("Proceso completado");
      else reject("Ocurrió un error");
    }, 1500);
  });
}

tareaAsincronica()
  .then(mensaje => console.log("Éxito:", mensaje))
  .catch(error => console.log("Error:", error));

```

Explicación Línea por Línea

return new Promise((resolve, reject) => { ... })

Creamos una nueva promesa.

resolve → se ejecuta cuando la operación fue exitosa.

reject → se ejecuta cuando ocurrió un error.

setTimeout(() => { ... }, 1500);

Simula un proceso asincrónico.

if (exito) resolve("Proceso completado");

Cumple la promesa → estado: fulfilled.

else reject("Ocurrió un error");

Si algo sale mal, la promesa cambia a estado: rejected.

.then(mensaje => ...)

Se ejecuta cuando la promesa se cumple.

.catch(error => ...)

Captura cualquier error que ocurra.

Estados de una promesa

pending → aún no se ha completado

fulfilled → se resolvió exitosamente

rejected → ocurrió un error

# PROMP 29 — Async / Await
------------------------------------------------------------
Instrucción

Actúa como un docente experto en JavaScript y explícame cómo funcionan async y await, por qué existen, cómo simplifican el manejo de promesas, y por qué permiten escribir código asincrónico con una estructura más parecida al código síncrono.

Contexto

Como estudiante, entiendo que las promesas funcionan con .then() y .catch(), pero el código se ve muy encadenado. He visto que async/await hace que todo se vea más limpio, pero no entiendo cómo funciona internamente, ni por qué solo se puede usar await dentro de una función async.
Quiero entenderlo con claridad.

Entrada

Explícame async/await con teoría, ejemplo y explicación técnica.

Salida

Una explicación completa con teoría, ejemplo, análisis 

Ejemplo: 

 ```js
function procesoAsincronico() {
  return new Promise(resolve => {
    setTimeout(() => resolve("Datos cargados"), 2000);
  });
}

async function ejecutar() {
  console.log("Iniciando...");

  let resultado = await procesoAsincronico();

  console.log("Resultado:", resultado);
  console.log("Finalizado.");
}

ejecutar();

```

Explicación Línea por Línea
function procesoAsincronico() { ... }

Función que devuelve una promesa que se resuelve luego de 2 segundos.

async function ejecutar()

Declaramos una función async.

Solo dentro de funciones async se puede usar await.

let resultado = await procesoAsincronico();

Pausa la ejecución SOLO dentro de esta función.

Espera que la promesa se resuelva y guarda el resultado.

No bloquea todo el programa.

console.log("Resultado:", resultado);

Imprime el valor devuelto por la promesa.

ejecutar();

Llamamos la función asincrónica.

# PROMP 30 — Módulos en JavaScript (import / export)
------------------------------------------------------------
Instrucción

Actúa como un docente experto y explícame cómo funcionan los módulos en JavaScript, por qué existen, cómo usar import y export, qué son los módulos ES6, por qué ayudan a organizar proyectos y cuál es la diferencia entre exportaciones por defecto y exportaciones nombradas.

Contexto

Como estudiante, he visto import y export en proyectos modernos (Vite, React, Node, etc.), pero aún no entiendo completamente cómo funcionan los módulos ni por qué es obligatorio usar type="module" en HTML.
Quiero entender cómo dividir correctamente el código en archivos separados.

Entrada

Explícame cómo funcionan los módulos ES6 con teoría, ejemplos y análisis.

Salida

Una explicación clara y completa con ejemplo real.

Ejemplo (creado desde cero):
archivo: operaciones.js

 ```js
export function sumar(a, b) {
  return a + b;
}

export function restar(a, b) {
  return a - b;
}

export default function multiplicar(a, b) {
  return a * b;
}


```
Archivo App.js

 ```js

import multiplicar, { sumar, restar } from "./operaciones.js";

console.log(sumar(5, 3));
console.log(restar(10, 4));
console.log(multiplicar(6, 2));

```

Explicación Línea por Línea
En operaciones.js

export function sumar → exportación nombrada.

export function restar → otra exportación nombrada.

export default function multiplicar → exportación por defecto.

En app.js

import multiplicar, { sumar, restar }

multiplicar viene del export default.

{ sumar, restar } vienen de los exports nombrados.

console.log(...)

Probamos las funciones importadas desde otro archivo.