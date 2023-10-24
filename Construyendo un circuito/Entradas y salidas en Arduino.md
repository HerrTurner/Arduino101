
Como mencionamos anteriormente en [[Microcontroladores |microcontroladores]],  existen entradas y salidas para permitir flujo de información. En Arduino podemos encontrar dos tipos de entradas y de salidas: analógicas y digitales.

Arduino tiene una serie de pines digitales y analógicos que pueden ser configurados para que sean pines de entrada o de salida. 
Para configurar los pines usamos la función *pinMode({pin},{modo})*

Es importante revisar la distribución de los pines de un Arduino, para esto podemos buscar el *Pinout* de la tarjeta Arduino que estemos utilizando.

En la Figura 1. (_UNO R3 | Arduino Documentation_, s.f.) podemos observar la distribución de un Arduino Uno R3. Podemos encontrar más información en la [documentación de Arduino](https://docs.arduino.cc/hardware/uno-rev3).

![[Arduino Uno Rev 3 Pinout.png]]
Figura 1. Diagrama de pines de un Arduino Uno R3

#### Digitales
Un pin digital espera una señal digital. Una señal digital es una onda cuadrada que contiene información codificada. Una onda cuadrada es una onda de corriente que alterna valores sin pasar por valores intermedios. Esto nos da un comportamiento binario, es decir 1 o 0, encendido o apagado. En Arduino vamos a encontrar frecuentemente los términos "HIGH" y "LOW", que se refieren a 5 V y 0 V respectivamente, o encendido y apagado.

Arduino tiene dos funciones integradas que nos permiten controlar los pines digitales:
- digitalWrite(): escribir información a un pin de salida.
- digitalRead(): leer la información que está recibiendo un pin de entrada.

Puedes leer más sobre los pines digitales en la [documentación de Arduino](https://docs.arduino.cc/learn/microcontrollers/digital-pins#properties-of-pins-configured-as-input)

##### Pines PWM (Pulse Width Modulation)
Es una técnica que nos permite tener un comportamiento analógico en una señal digital. 

Esto se logra al modificar el ancho de un pulso, o el tiempo "encendido" de la señal.

Una aplicación puede ser controlar un servomotor para determinar su posición.

>Es importante notar que no todos los pines de Arduino son compatibles con PWM. Generalmente van a estar indicados con un ~.

Puedes leer más sobre PWM en la [documentación de Arduino](https://docs.arduino.cc/tutorials/generic/secrets-of-arduino-pwm)

#### Analógicas
Una señal analógica  nos permite tener valores continuos en un intervalo. Por ejemplo, si estamos trabajando entre 0 V y 5 V inclusive, podría tener cualquier valor como 2.7 V.

Esto nos puede servir para leer las mediciones de sensores como lo puede ser temperatura o humedad, o la posición de un potenciómetro. En ocasiones los podemos identificar por Ax, donde la x es el número del pin.

Existen dos funciones que nos permiten manipular los pines digitales.
- analogWrite(): escribir información a un pin de salida.
- analogRead(): leer la información que está recibiendo un pin de entrada.


Referencias

Llamas, L. (2014, Mayo 31). _Entradas digitales en Arduino_. Luis Llamas.  https://www.luisllamas.es/entradas-digitales-en-arduino/

_Digital and Analog PINs | Arduino Documentation_. (s.f.).  https://docs.arduino.cc/micropython/basics/digital-analog-pins

_UNO R3 | Arduino Documentation_. (s.f.).  https://docs.arduino.cc/hardware/uno-rev3
