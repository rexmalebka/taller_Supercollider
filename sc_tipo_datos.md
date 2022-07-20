# Tipo de datos Supercollider

1.-[Inicio ](README.md) 

---

## Tipos de Datos Supercollider

```supercollider
// Números
// números enteros (no tienen punto decimal)
2

// números flotantes (tienen punto decimal)
2.0

// números con notación científica 
2e3


// texto
// llevan comillas dobles (importante) y siempre abren y cierran
"hola"

// booleanos
// representa solo verdadero o falso

true 
false

// nil
// Representa ningún valor o nada
nil

// si se quiere usar comilla dentro del string, se us \" para evitar que falle
"comilla: \" "

// listas 
// pueden contener cualquier tipo de valor, abre con [ y cierra con ], los elementos van separados por coma
[1, 3, 4]
[5.5, 6.7, 7.7]
["hola", "que onda"]

// podemos acceder a los elementos de la lista indicando entre [x] la posición del valor que queremos extraer, desde el 0 en adelante

[3,6,3,4][0] // 3
[3,6,3,4][1] // 3
[3,6,3,4][6] // nil no existe valor en esta posición



// Events
// Iguales que las listas pero el índice no es un número
(a:1, b:2)

// accedemos a los valors con un punto
(a:2).a

(a:3).f // nil

// Symbols
// Sirven para etiquetar, se escriben sin separar por espacios iniciando con \, o también con comilla simple
\hola
\amp
'freq'


// Ante la duda, siempre podemos saber el tipo de un valor con .class

2.class
3.4.class
"Hola".class
[6,3,4].class
(a:4,b:3).class
nil.class
[3,5.6, "hola"][2].class
\simbolo.class
'Simbolo'.class
true.class

```

## Variables

Son los contenedores donde podemos almacenar datos que serán consumidos más tarde, esto permite no escribir dos veces el mismo código y tener referencia de cosas con nombres más humanos.


```supercollider

// Variables globales, llevan el signo ~ al inicio
~sonido = {SinOsc.ar(200)!2}
~sonido.play

~sonido2 = {LFPar.ar(300)!2}
~sonido2.play

// tambien pueden definirse variables globales usando una sola letra
a=2
b=3

a+b

// podemos definir bloques de código usando paréntesis
// cada linea separada debe terminar con ;
// para variables locales, es decir que solo existen en el bloque de código, se usa la palabra var nombre;
// para ejecutar un bloque de código, puede presionarse Control + Enter
(
var numeros=[1,2,3,5];
numeros[3].postln
)

