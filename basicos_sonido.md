# Información Básica de sonido


1.-[Inicio ](README.md)

---

## Características importantes del sonido

El sonido es una señal de energía que viaja através del aire, y como señal mantiene ciertos parámetros que le dan sus características especiales.

- Amplitud: que tan fuerte o bajito suena
- Frecuencia: que tan agudo o grave suena
- Timbre: que tipo de sonido escuchamos 

## señales básicas de audio

Existen ciertos tipos de señales básicas que permiten generar casi todo tipo de sonidos


- Onda sinuidal
 
![image](https://user-images.githubusercontent.com/17996715/180099363-c96e8241-01bb-4011-87ed-952b87dd29be.png)

se crea con el UGen

```supercollider
{SinOsc.ar}.play
```

- onda cuadrada

![image](https://user-images.githubusercontent.com/17996715/180099592-634fcbd1-8c54-44d0-a292-9964e1815e3e.png)

se crea con el UGen

```supercollider
{Pulse.ar}.play
```

- onda Triangular

![image](https://user-images.githubusercontent.com/17996715/180099552-10ef8ab7-1b7f-4785-87c0-955d555120e5.png)


se crea con el UGen

```supercollider
{LFTri.ar}.play
```

- onda diente de sierra

![image](https://user-images.githubusercontent.com/17996715/180099847-275dfc76-ed81-41bf-9851-64ce3a2075b6.png)

se crea con el UGen

```supercollider
{Saw.ar}.play
```

- ruido blanco

![image](https://user-images.githubusercontent.com/17996715/180099627-7cff8405-7098-472c-9fde-210d0658a940.png)

se crea con el UGen

```supercollider
{WhiteNoise.ar}.play
```

- ruido rosa

![image](https://user-images.githubusercontent.com/17996715/180099679-c41878d8-eb6c-48a6-96f4-d63474e532c3.png)

se crea con el UGen

```supercollider
{PinkNoise.ar}.play
```

- impulsos

![image](https://user-images.githubusercontent.com/17996715/180100124-4d546ec4-044b-4511-af51-ef48ca1c0770.png)

se crea con el UGen

```supercollider
{Impulse.ar}.play
```


Existen Ugens para todo tipo de sonidos, es necesario explorar códigos o la documentación para ver la existencia de otros tipos de Ugens y ver ccomo podrían usarse para generar sonido


Todos Los Ugens reciben dos tipos de inicializaciones, como audiorate o como control rate

```supercollider
SinOsc.ar
SinOsc.kr
```

y además cada función recibe sus parámetros únicos, es decir que características van a definir la onda, por ejemplo

SinOsc recibe estos parámetros que le permiten modificar su frecuencia y su fase de inicio


![image](https://user-images.githubusercontent.com/17996715/180100364-e73ac89b-a3a4-407d-975a-eff4c58792a1.png)


```supercollider
{SinOsc.ar(20)}.play
```

![image](https://user-images.githubusercontent.com/17996715/180100461-da3f4512-784d-4506-a035-18bbaaace0d9.png)


```supercollider
{SinOsc.ar(600)}.play
```

![image](https://user-images.githubusercontent.com/17996715/180100523-d1b4f9d9-237d-4b04-9cdd-9030c2b91bc4.png)


---

https://doc.sccode.org/Classes/UGen.html



