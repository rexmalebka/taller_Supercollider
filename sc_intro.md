# Introducción a Supercollider

1.-[Inicio ](README.md)

---

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

