# Síntesis de sonido

1.-[Inicio ](README.md)

---


## Síntesis aditiva

se trata de generar sonido combinando dos o más señales, las señales se suman y modifican su timbre, generando sonidos más ricos

```supercollider
{SinOsc.ar(200)}.play
```

![image](https://user-images.githubusercontent.com/17996715/180320606-39ed032e-b661-4aae-abd2-ef32add4cb75.png)


```supercollider
{SinOsc.ar(800)}.play
```

![image](https://user-images.githubusercontent.com/17996715/180320704-2c5733dc-10dd-4487-8b8f-f282b8a05ff5.png)


```supercollider
{SinOsc.ar(800) + SinOsc.ar(200)}.play
```

![image](https://user-images.githubusercontent.com/17996715/180320766-9ad00253-9875-44da-a0ec-e87196e660ac.png)


En el caso de supercollider hay que cuidar de que el volúmen quede dentro de rangos de valores aceptables, ya que conforme se le sumen los valores más alto va a llegar la onda



## Síntesis Modulativa

Se trata de generar sonidos modulando alguna característica de la señal como lo puede ser la frecuencia, la fase, la amplitud, etcétera.

```supercollider
{SinOsc.ar(200 + (Pulse.ar(20)*100))}.play
```

![image](https://user-images.githubusercontent.com/17996715/180321001-bbe438e7-e984-4b25-ad76-e91333772bb4.png)

```supercollider
{SinOsc.ar(200 , SinOsc.ar(40)*2)}.play
```

![image](https://user-images.githubusercontent.com/17996715/180321196-380e213a-c4a1-43bf-8aeb-a65d36dfee73.png)


## síntesis sustractiva

Se trata de generar sonidos filtrando la misma, es decir removiendo frecuencias armónicas del sonido.

```supercollider
{ HPF.ar(PinkNoise.ar * SinOsc.ar(3000), 800)*2 }.play
```

![image](https://user-images.githubusercontent.com/17996715/180321537-b24db13e-505a-49f2-9199-bbb7a6c16c70.png)


Por supuesto que todos los tipos de síntesis pueden combinarse para encontrar texturas interesantes y modelos de sonidos nuevos.

