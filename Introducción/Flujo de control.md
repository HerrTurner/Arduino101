
Arduino tiene una ejecución de tipo mono hilo y secuencial. Mono hilo es que cada línea de código se ejecuta una a la vez o paso por paso y secuencial se refiere a que una línea se ejecuta una después de la otra, generalmente ordenadamente de arriba hacia abajo. A esto nos referimos con el "flujo del programa".

Existen ciertos eventos que alteran el flujo del programa, por ejemplo saltarse pasos o regresar a una línea de código anterior, sin embargo el flujo permanece lógico y sin errores. Para estos casos existen estructuras y sentencias que nos ayudan a controlar y manipular el flujo del programa y mantener un código lógico y libre de errores.

#### Ejemplo
Lo siguiente es un ejemplo de un programa y su flujo de control.
El programa consiste en un pin que va alternando entre prendido y apagado con una pausa entre cada cambio. 

Se puede observar en la Figura 1. (SparkFun Electronics, 2017) que el programa tiene un inicio y va avanzado paso a paso uno a la vez hasta que llega a un evento que regresa a un evento anterior generando un ciclo.


![Control Flow Example](Recursos/Control%20Flow%20Example.png)]
Figura 1. Diagrama de flujo de control de un programa

Más información sobre el flujo de control la puedes encontrar en la [documentación de Arduino](https://arduino.cl/flujo-de-control-estructura-y-sentencias-del-programa-arduino/).

#### Referencias
SparkFun Electronics. (2017, March 6). _Arduino Control Flow_ [Video]. YouTube.  https://www.youtube.com/watch?v=QpPGGuaGbCA