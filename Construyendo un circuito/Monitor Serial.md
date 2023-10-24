
El monitor serial es una herramienta esencial para el desarrollo en Arduino. Permite depurar el código, comunicarse en tiempo real con la tarjeta de Arduino ya sea mandarle información o visualizar lo que está escribiendo.

Se requiere tener instalado el [[Arduino IDE|IDE de Arduino]] y una tarjeta Arduino conectada a la computadora con sus respectivos controladores. En general, al instalar el IDE de Arduino se incluyen los controladores para las tarjetas de Arduino más populares.

Al inicio de un programa es necesario iniciar la comunicación serial estableciendo la cantidad máxima de bits por segundo que se puede transferir. Generalmente se trabaja con 9600 baudios.

Esto se declara en la función void setup(); con la sentencia Serial.begin(#cantidad de baudios);

Existen muchos métodos que permiten tener una comunicación serial con la tarjeta de Arduino. Alguna de las más populares son:
- begin
- println
- read
- write
- available

Existe más información sobre Serial en la [documentación de Arduino](https://www.arduino.cc/reference/en/language/functions/communication/serial/).

Ejemplo:

```
void setup() {
Serial.begin(9600);
}

void loop() {
Serial.println("Hello world!");
delay(1000); 
}
```


#### Referencias

_Using the Serial Monitor tool | Arduino Documentation_. (s.f..).  https://docs.arduino.cc/software/ide-v2/tutorials/ide-v2-serial-monitor