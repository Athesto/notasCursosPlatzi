# Notas del curso de Java SE 2018

# El origen de Java

Java fue creado en 1991 creado por James Gosling, y en 2009 fue comprado por oracle.

Categorías:
JavaSE: Java Standard Edition, los fundamentos del lenguaje.
JavaEE: Java Enterprise Edition, aplicaciones web.
JavaME: Java MicroEdition, es la usada en teléfonos viejos. No está muy vigente.

# Creando un entorno de desarrollo

JDK: Java Development Kit, es un kit de desarrollo. Librerías, clases, y lo necesario.
JRE: Java Runtime Environment, para correr java. Es la máquina virtual de Java.

java -version : La versión de Java
javac : El conjunto de acciones de java

# Definiendo la versión de Java

Podemos usar por defecto la versión de Java.

# HolaMundo.java

Los archivos de Java siempre tienen que empezar por mayúsculas.

El nombre de la clase debe ser el mismo que el del archivo.

Compilamos con ***javac HolaMundo.hava***

Corremos con ***java HolaMundo***

# Método Main

Es el punto de entrada de una aplicación Java.

# Tipos de datos primitivos enteros

Tenemos los tipos objetos y los primitivos.

Se escriben con letras minúsculas, entre los datos primitivos están:

- byte: 1 byte 
- short: 2 bytes
- int: 4 bytes
- long: 8 bytes

Para especificar un long, ***Agregar L*** al final del número. De lo contrario el compilador lo tomará como entero.

# Punto flotante

Son aquellos que permiten agregar puntos decimales.

- float: 4 bytes. Agregar ***F*** al final del número, porque el compilador lo tomaría como double.
- double: 8 bytes. 

- char: 2 bytes. Es único, solo tendrá un dato. Una letra en comillas simples siempre.

- boolean: 2 bytes. True o False.

# Naming en Java

Nombres en Java

Reglas:
- Java es sensible a mayúsculas y minúsculas
- Pueden comenzar con _ o $
- No pueden comenzar con números
- Las constantes se escriben en Mayúsculas
- LowerCamelCase para funciones y UpperCamelCase para clases.

# Cast de variables

Esto es para convertir un tipo de dato a otro.

Podemos castear datos primitivos y objetos.

Este es un cast:

```
double d = 86.45;
int i = (int) d;
```

El casteo es de menor a mayor es automático, en sentido inverso requiere un casteo.

# Arrays

Son objetos en los que podemos guardar más de una variable.

# Ejemplos de Arrays

Los arrays son inmutables, las maneras de declararlos son:

```
int[] arregloInt = new int[3];
double arregloDouble[];
char[][] days = {{'M', 'T', 'W'}, {'M', 'T', 'W'}};
```

> Arreglos de más de 4 dimesiones ya no es una buena práctica en la proogramación. Para estos casos lo mejor es utilizar bases de datos.

# Búsqueda de elementos en Arrays e índices

char[] names = new char[3];
names[0]='h';
names[1]='o';
names[2]='l';

Ejemplo del chango
char[][][][] mokey = new char[2][3][2][2];
mokey[1][0][0][1] = 'm';

# Tipos de operaciones en Java

Con + podemos concatenar textos

double x = 2.56;
int y = 9;
float w = (float)x + y;

Operadores de asignación:

+=, -=, *=, /=, %=


// Esto es aplicable en las operaciones como por ejemplo System.out.println
++i -> Primero incrementa el valor y luego lo asigna a la variable
i++ -> Primero asigna valor a l y luego incrementa el valor

==, !=

# Operadores relacionales y lógicos

>, <, >=, <=

# If, else y switch

switch(mes){
  case 1:
    System.out.println("Enero");
    break;
  case 2:
    System.out.println("Febrero");
    break
  default:
    break
}

# Ciclo while

while (condición){
  // Código
}

do {
  // Código  

}(condición)

> "do-while es muy común utilizarlo cuando trabajamos con menús"

Ejemplo:
```
package com.osmandi;

public class Main {

	public static void main(String[] args) {
		// TODO Auto-generated method stub
		
		
		int exit = 0;
		do {
			System.out.println("Bienvenidos Amazon Viwer\n");
			System.out.println("Selecciona el número de la opción desdeada");
			System.out.println("1. Movies");
			System.out.println("2. Series");
			System.out.println("3. Books");
			System.out.println("4. Megazine");
			System.out.println("0. Exit");			

		}while(exit !=0);
	}
}
```

# Ciclo for y foreach

**For**

for(inicializacion, condicion, incremento){
  // Comandos
}

**foreach**

Nota: Números es el arreglo y j es el valor de la variable.

for (int j:numeros){
  // Código
}

A nivel de performance foreach es más rápido pero en for sí tenemos acceso al índice. Pero en foreach no tenemos acceso al índice.

Para un foreach anidado

```
public class ForEachAninado {
 
    public static void main(String[] args) {
 
        //Definimos un array de 3 filas x 5 columnas
        int array[][]={{1,2,3,4,5}, {6,7,8,9,10}, {11,12,13,14,15}};
 
        //Recorremos el array multidimensional
        for (int[] arrayInterno : array){
            for(int numero: arrayInterno){
                System.out.println(numero);
            }
        }
    }
 
}
```

break -> Sale de todo el bucle de la sentencia.
continue -> Retorna al comienzo de la sentencia.
return -> Retorna un valor del ciclo o función termiando la misma.

# Programación orientada a objetos

Se trata de descomponer un problema en subproblemas y más subproblemas.

**"Divide y vencerás"**

Para ello ver un problema como un escenario del problema y tratar de simularlo con objetos. No pensar directamente en la solución, podría no ser la mejor solución.

Los atributos deben ser sustantivos y los métodos deben ser verbos.

# Análisis de un objeto y qué es una clase

Una clase es la forma en cómo defines tu objeto, para generar objetos.

Primeros colocamos los atributos y luego los métodos.

# Analizando nuestro proyecto

Ann primero plantea todas las posibles clases

|Movie | Chapter | Serie |
|------|---------|-------|
|id    | id      | id    |
|title | title   | title | 
|genre | duration | genre |
|creator | year  | creator          |
|duration | viewed  | duration      |
| year | timeViewed | year          |
| viewed | sessionNumber | viewed   |
| timeViewed |      | sessionQuanty |
|        |          | charpters     |


# Creando nuestro proyecto

- Movie: id, title, genre, creator, duration, ear, viewed, timeViewed +see(), getters, setters.
- Serie: id, title, genre, creator, duration, year, viewed, sessionQuality, chapters +getters, setters.
- Chapter: id, title, duration, year, viewed, timeViewd, sessionNumber +see(), getters(), setters.
- Books: id, title, editionDate, editorial, autores, isbn, readed, timeReaded +Getters,setters,read
- Megazime: id, title, editionDate, autories +getters, setters

Ann usa Drow.io para hacer los diagramas con sus librerías y dependencias.

# Métodos y método constructor en Java

Auto miAuto = new Auto();
miAuto.marca = "Ferrari";

El método constructor nunca va a regresar un valor.
