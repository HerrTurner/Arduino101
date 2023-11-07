
Arduino es un lenguaje de programación basado en C++, esto implica que es un lenguaje fuertemente tipado y estático. Esto es que al declarar variables y funciones se debe de establecer el tipo y este no se puede alterar. 

También es un lenguaje compilado, eso es que el código se convierte a código máquina en un archivo ejecutable que es lo que va a utilizar la tarjeta de Arduino.

Tanto Arduino como C++ utilizan el ";" como delimitador de sentencia. Un delimitador de sentencia se usa para indicar el fin de una sentencia. una sentencia es un conjunto de expresiones lógicas que permiten realizar una acción.

Otra entidad en Arduino son los bloques, estos son una serie de sentencias contenidas dentro de llaves "{  }".
Las sentencias y variables declaradas dentro de un bloque solo existen dentro de ese bloque, por lo que no se pueden acceder desde un bloque diferente.

Ahora bien, si un bloque se encuentra dentro de otro bloque, El bloque que está anidado puede acceder a las variables del bloque padre, pero el bloque padre no puede acceder a las variables del bloque anidado.

En Arduino se pueden escribir comentarios, los comentarios son líneas que no se van a compilar. 

Para escribir comentarios de una línea se usa "//"
Para comentarios de múltiples líneas se utiliza "/\*" en la primera línea y "\*/" al finalizar el comentario.

### Elementos mínimos para un Sketch de Arduino

- setup() Esta función se ejecuta al iniciar el programa. Aquí se inicializan las variables, se configuran los modos de los pines, se empiezan a usar las librerías, entre otras cosas. Este solo se ejecuta una vez
- loop() Esta función se ejecuta al concluir setup(). Como el nombre lo indica, esta función se ejecuta recurrentemente hasta que el programa se detenga, permitiendo al programa cambiar y responder. 

### Ejemplo mínimo de un sketch de Arduino

```
//Aquí incluimos las librerías que se van a utilizar

//Aquí declaramos los pines y variables que se van a usar

void setup() {
  // Este es un comentario de una línea
  //Aquí se inicializan las variables
}

void loop() {
  /*
  Este es un comentario
  de múltiples
  líneas
  */
  /*
  Aquí es dónde se encuentra la mayoría de la lógica y 
  acciones de un programa
  */
}

```

### Ejemplo de bloques o scopes

```
int num1; // num1 es una variable de tipo int y acaba con ;

void setup() {
	//Inicializar la variable
	num1 = 3;
  
	//Crear una nueva variable
	int num2 = 4;

}

void loop() {
	num1 += 1; 
	//Como num1 se declaró en un bloque mayor,
	//podemos acceder a ella y modificarla

	num2 += 5;
	//Si se compila el código va a marcar un error ya
	//que num2 se declaró en un scope del mismo nivel
	//y no se encuentra

	int num2 = 6; 
	//Es posible crear una variable con el mismo nombre
	//ya que la variable num2 se declaró en un scope diferente
	//y no existe en el scope actual

}
```

Se puede encontrar más información en la [Guía de referencia de Arduino](https://www.arduino.cc/reference/es/), sobre [sketches](https://docs.arduino.cc/learn/programming/sketches) y [los ejemplos incluidos](https://docs.arduino.cc/built-in-examples/)


