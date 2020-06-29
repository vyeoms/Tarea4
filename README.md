# Tarea 4: Modulación BPSK

Curso: IE0405-Modelos Probabilísticos de Señales y Sistemas  

Estudiante: Victor Manuel Yeom Song  

Carné: B78494  

<img src="https://render.githubusercontent.com/render/math?math=">

## Inciso 1: Creación del esquema BPSK  

Un esquema de modulación [BPSK](https://www.gaussianwaves.com/2010/04/bpsk-modulation-and-demodulation-2/) es aquel donde la modulación de una señal digital se realiza con señales sinusoidales, las cuales se modulan según su fase. La "codificación" utilizada en esta tarea es la siguiente:

<img src="https://render.githubusercontent.com/render/math?math=s_1(t) = \sen (2\pi f_c t)"> para un bit igual a 1;
<img src="https://render.githubusercontent.com/render/math?math=s_0(t) = -\sen (2\pi f_c t)"> para un bit igual a 0,

donde <img src="https://render.githubusercontent.com/render/math?math=f_c"> es la frecuencia de la señal portadora y t el tiempo. Así, se tiene que la señal portadora en cada periodo tiene la siguiente forma:  

![portadora](img/portadora.png)

Inicialmente, se leen los bits del [archivo proveído en el enunciado](bits10k.csv) con el método `genfromtext()` de la biblioteca `numpy`. Esto produce un objeto iterable cuyos elementos corresponden a los bits del enunciado. Para la modulación se utilizó una frecuencia de la onda portadora de 5000 Hz, con 50 puntos de muestra para graficar cada figura de esta tarea. Se utilizó una frecuencia de muestreo de 250 kHz para asegurar el cumplimiento de la *frecuencia de muestreo de Nyquist* y que se genere una representación fiel de la señal. Con los primeros 10 bits del archivo CSV, se obtiene la señal modulada con la siguiente forma:

![Tx](img/Tx.png)

