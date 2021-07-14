# Proyecto 4

Este proyecto es del curso de Modelos probablísticos de señales y sistemas (IE-0405) de la
Universidad de Costa Rica.

## Autores

- [@Edson0121](https://www.github.com/Edson0121)

  
## Documentación

### Modulación 16-QAM

El proyecto consiste en un trabajo de modulación de señales para simular el proceso de
enviar una imagen. Para ello, se efectuaron diversas funciones que se encargaban de obtener
los píxeles de la imagen, modularlos, agregarles ruido, demodularlos y pasar nuevamente los
píxeles a imágenes.

Para la función modulador_16QAM, se basó primeramente en la función modulador brindada
por el profesor. A continuación, se procede a realizar dos portadoras: Portadora I y portadora Q.
En este caso, la modulación 16-QAM se trabaja con 4 bits que contienen la información. Por
lo tanto, se leen de de 4 en 4 los bits, repartiéndolos entre ambas portadoras y obteniendo
una fórmula que describe la amplitud de ambas, para así obtener una señal modulada que sea 
la suma de ambas.

Seguidamente, se trabajó con la demodulación de la señal luego de que se le agregara ruido
a esta. La función demodulador_16QAM se encarga de leer la señal y pasarla nuevamente a 
los bits. Para ello, se crean dos productos para cada portadora, que consiste en la señal recibida
por la portadora para sumarlas y obtener la señal demodulada. Luego, los bits se asignan
según un análisis de la señal recibida y observando las condiciones para cada uno 
de ellos correspondiente a su signo y magnitud.

Finalmente, se asignan los valores de frecuencia de la señal que sería 5 kHz, la cantidad
de muestras por período que sería de 20 y la relación señal-a-ruido que es de 5 dB. Se obtienen
las imágen transmitida y recuperada, donde se presentan 70579 errores y un BER = 0.1669.

#### Resultados de la modulación 16-QAM

![App Screenshot](https://github.com/Edson0121/Proyecto4/blob/main/modulada.png)

#### Señales obtenidas
La primera señal es la señal cuadrada modulada, la segunda es la señal modulada con el método
16-QAM, la tercera es la señl recibida que contiene el ruido y la cuarta la señal demodulada.

![App Screenshot](https://github.com/Edson0121/Proyecto4/blob/main/senales.png)

### Estacionaridad y Ergocidad

En esta sección se pretendía realizar las pruebas correspondientes para analizar la estacionaridad
y ergocidad, pero no se pudo completar el código. Con esto se esperaba obtener la autocorrelación
entre las N funciones de la señal.

### Densidad espectral de potencia

Para la densidad espectral se puede observar que los valores se reúnen cerca de 5 kHz, que
es la frecuencia de las dos portadoras. Los demás valores representan las otras frecuencias
asociadas a la moduladora.

![App Screenshot](https://github.com/Edson0121/Proyecto4/blob/main/potencia.png)
