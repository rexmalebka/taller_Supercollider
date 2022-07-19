# Taller SC

[![Cápsula Marianne Teixido](https://img.youtube.com/vi/sxRY371BC8k/0.jpg)](https://www.youtube.com/watch?v=sxRY371BC8k)


## Que es un algoritmo ? 

Un algoritmo es una serie de pasos lógicos o reglas que hay que seguir para llegar a un objetivo o realizar algo concreto.
En la vida cotidiana, se emplean algoritmos frecuentemente para resolver problemas determinados, cambiar una llanta, conducir, etc; Pudiendo ser muy sencillos o muy complejos, con datos cuantitativos o datos cualitativos.

Las recetas de cocina pueden ser un ejemplo de algoritmos, creados con la finalidad de obtener un platillo o postre, tienen pasos explicando las cantidades, los tiempos, tipos de corte, etc; que si los seguimos masomenos al pie de la letra, terminaremos con un platillo específico.


![ejemplo algoritmo](https://upload.wikimedia.org/wikipedia/commons/thumb/b/bd/LampFlowchart-es.svg/220px-LampFlowchart-es.svg.png)


## Qué es un lenguaje de programación ? 

Un lenguaje de programación es un idioma con sus propias palabras, reglas y lógica que permiten a las personas describir algoritmos que pueden más tarde ser entendidos por una computadora.

Mayoritariamente los lenguajes de programación están basados en el idioma inglés y tienen maneras de describir operaciones matemáticas y lógicas condicionales.

Todos los programas creados por un lenguaje de programación, deben someterse a un proceso donde, después del procesamiento de un "intérprete" la computadora puede entender los pasos que escribimos, llegando entonces a un lenguaje de unos y ceros llamado lenguaje máquina.

Hay muchos tipos de lenguajes de programación y para todas las finalidades, muy complejos, muy sencillos, de rápido procesamiento y de bajo procesamiento, para internet, para bases de datos, o como es nuestro caso para hacer música.

## Qué es programar ? 

Programar es redactar algoritmos usando lenguajes de programación, tienen que ser escritos en lenguajes de programación para que la computadora pueda entender estos pasos.

Programar también significa explicar el flujo de datos que tendrá el algoritmo, donde va a entrar información y como va a salir al exterior mediante pantallas, impresoras, teléfonos, etc;


## Entonces qué es el livecoding ? 

Es la práctica artística de generar música, imagen, coreografía y texto a través de dar instrucciones a computadoras en forma de algoritmos.
El término comenzó a usarse en el 2003, para referirse a la improvisación musical con computadoras y desde el 2004 con la creación de TOPLAP se fue popularizando el término, en  México, el término fue acuñado en el 2008.

El livecoding implica además, improvisación en vivo, sonorización de datos, instalación de piezas sonoras, etc;

A diferencia de la programación habitual, en la práctica del livecoding no hay un problema técnico a resolver, y por lo tanto hay muchas maneras de resolver lo mismo, inclusive el error aporta dinamism a lo sonoro

La improvisación como técnica estética además convierte al artista-máquina en  un cyborg, pero también hace a la máquina parte de la obra, de la instalación como instrumento y como objeto de valor.

Además, la práctica del livecoding permite generar comunidad, ya que es una práctica habitual compartir el código y proyectar en vivo la pantalla, que permite a otras personas aprender nuevas técnicas.

existen múltiples lenguajes que permiten generar sonido en vivo, algunos son:

- supercollider
- tidalcycles
- sonic-pi
- FoxDot
- processing
- puredata
- Orca




[![M4l4ndr0n3](https://img.youtube.com/vi/0kBxq0rdTBg/0.jpg)](https://www.youtube.com/watch?v=0kBxq0rdTBg)

[![Marianne Teixido](https://img.youtube.com/vi/XsfMo5EuRaI/0.jpg)](https://www.youtube.com/watch?v=XsfMo5EuRaI)

[![Tacacocoding](https://img.youtube.com/vi/NsRhS4HIu8o/0.jpg)](https://www.youtube.com/watch?v=NsRhS4HIu8o)



## Supercollider

Supercollider es un programa creado en los años 90's pensado principalmente para la investigación académica, síntesis audio en tiempo real y composición algorítmica.

Es la base de muchos otros lenguajes de programación del tipo livecoding, está compuesto principalmente por 3 partes:

- **sclang**: es el lenguaje de programación de supercollider, con sus propias reglas y anotaciones.
- **scsynth**: es el motor de audio encargado de calcular a nivel hardware el sonido
- **scide**: se refiere a la ventana o parte gráfica del programa, que permite leer la documentación, leer logs y redactar el código.

Supercollider además cuenta con una suite de Funciones que nos permiten usar MIDI, mandar mensajes OSC e interactuar con el serial de la máquina.

![Logo Supercollider](https://upload.wikimedia.org/wikipedia/commons/thumb/6/60/SuperCollider_logo.svg/250px-SuperCollider_logo.svg.png)


## Instalación

Para todos los casos Supercollide es libre y gratuito, puede encontrarse en este link https://supercollider.github.io/downloads
En el caso de GNU/Linux, opcionalmente instalar qjackctl para tener un mejor control de las conexiones de salida y entrada

## Entorno

![image](https://user-images.githubusercontent.com/17996715/179660376-bb052b65-7649-47a8-aa86-96b47f4ca2ae.png)

Supercollider tiene al menos 3 partes

- Editor

Aqui es donde vamos a escribir el cuerpo de nuestra composición, definiremos el algoritmo de nuestro sonido 

- Buscador de ayuda

Aqui vemos un mini navegador en el que podemos buscar datos rápidos sobre funciones y sintáxis

- Ventana de logs

Aqui veremos la bitácora de lo que estemos ejecutando, así como logs de errores que puedan ocurrir 

---
## Haciendo sonido



```supercollider
// recuerda antes de ejecutar el código estar usuando audífonos para evitar dañar las bocinas de tu computadora.
// inicia el servidor y se conecta con el motor de audio
// para ejecutar código, seleccionas un pedazo de código y presionas Shift + Enter 
s.boot  

// inisia el meter para ver volúmenes, así como ver un scope de la señal
s.meter
s.scope


// Corre este snippet y ve lo que sucede
{SinOsc.ar(300)}.play

// para detener todo los sonidos, presionar Control + "."
// que pasa si le cambiamos los datos ?
{SinOsc.ar(500)}.play

// y ahora?
{[ SinOsc.ar(500), SinOsc.ar(200)]}.play

// probamos con otro tipo de onda ? 
{[ Saw.ar(500), Saw.ar(200)]}.play

// prueba con combinaciones de Pulse LFTri Saw LFPulse LFPar SinOsc etc;
```

Al estar ejecutando código, nuestros logs se llenaran con información valiosa en caso de que nos equivoquemos

![image](https://user-images.githubusercontent.com/17996715/179662697-22ad0185-2b07-4609-b7a9-4a409cc54b1f.png)


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

```




### más información 

- https://es.wikipedia.org/wiki/Live_coding
- https://toplap.org/
- https://algorave.com/
- https://github.com/toplap/awesome-livecoding
- https://docs.google.com/spreadsheets/d/1tLWnX_Dyha0toGC-DQQaS2ICJ-U2U9bmuJOBvXOv59c/edit#gid=0

