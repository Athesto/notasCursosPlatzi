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

# Miembtros estáticos y final

- Static: Se pueden usar en toda la clase. Todos los métodos de la clase main deben ser estático. Puede ser invocado en una clase que no tiene instancia de la clase. Los métodos estáticos ayudan a ahorrar memoria. -> **Calculadora.suma(a,b)**. E incluso editar los valores de la variable.

# Sobrecargas de métodos

A veces necesitamos que dos métodos tengan el mismo nombre pero con diferentes argumentos que devuelvan diferentes valores. Ejemplo la suma dos valores enteros y otra con valores flotantes.

Puede ocurrir en los métodos y también en los constructores.

# Modificadores de acceso

Ann genera los campos con el IDE en la clase. el id debe generarse automáticamente.

Generamos el constructor Movie con title, genre y year.

- Public: Clase, Package, Subclase, otros.
- Portected: Clase, Package, Subclase, Otros.
- Default: Clase, Package.
- private: Clase.

Subclase es Herencia.

Encapsular: Esconder con default o private.

A todos los atributos le ponemos private del resto de las clases.

# Getters y Setters

Ello no permite acceder a nuestros atributos y métodos.

> Es una buena práctica encapsular los atributos de las clases.

Con Getter obtenemos el valor y Setter ingresamos el valor.

La diferencia de usar o no Getter y Setter es que podemos usar un trozo de código de validación para aceptar los valores.

Lo mejor es tener marcados todos los getters y setters.

Las variables se guardan en el stack y los objetos en el heap.

> Nota: Cuando se usan variables con short, se debe castear: **(short)2017**

# Que es la herencia

> Una de las filosofías de Java es reutilizar la mayor cantidad de código.

Ann está reciclando los atributos repetidos entre las clases.

Quedando de esta manera:
- Film: id, title, genre, creator, duration, year, viewed +see()+getters+setters.
- Movie: Hereda de Film -> id, timeViewed +see()+getters+setters().
- Serie: Hereeda de Film -> id, sessionQuatility, chapters +getters+setters.
- Chapter: Hereda de movie -> id, sessionNumber +see()+getters+setters.

- Publication: title, editionDate, editorial, autores +getters+setters.
- Book: Hereda de Publication -> id, isbn, readed, timeReaded +getters+setters.
- Magazine: Hereda de Publication -> id +getters+stters.

> La herencia es crear clases a partir de las ya existentes para reciclar código.

# Super y this

- Super: Se refiere a la clas padre.
- this: Se refiere a la clase hija.

Una subclase hereda todos los miembros de su súper clase que están declarados como public o protected.

# Implementando herencia en el proyecto

> Lo mejor es modularizar la mayor parte del código. Aplicamos las herencias que mencionamos anteriormente.

Con la herencia nos ahorramos mucho código, implementamos buenas prácticas en Java y modularizamos.


# Poliformismo

> Implícitamente todos los objetos que yo cree de una clase, estarán heredando de la clase Object (extedns Objects). Por eso es que cuando ponemos **super.** vemos los métodos y atributos de la clase Object.

Entre los métodos de la clase Object está el método **toString()**. El cual podemos editarlo. Para ello debemos coloar la anotación **@Override**. Dicho método imprime de dónde proviene la clase y el puntero de memoria.

Ejemplo de poliformismo:

```
@Override
public String toString(){
  return "Hola, este es el objetoMovie"
}

// Incovar con
Movie movie = new Movie("Coco", "Animation", "", 120, (short)2017);
System.out.println(movie.toString());

// Nota: la impresión de movie retorna como si fuera movie.toString().
```

Sobreescritura: Cuando una clase hereda de otra, y en esta clase hija se redefine un método con distinto de la clase padre.

**Los métodos marcados como final  o static no se pueden sobreescribor**

También podemos reescribir constructores.

Poliformismo: Posibilidad de construir varios métodos con el mismo nombre, pero con relación a la clase a la que pertenece cada uno, con comportamientos diferentes.

En la clase Chapter, en vez de devolver getId() padre, devolvemos el del hijo.

# Interfaces

Es un tipo de referencia similar a una clase que podría contener solo constantes y definiciones de métodos, métodos con modificador de acceso default.

Solo definiremos el método mas no el código. Es decir no bloques de código.

> Ayuda mucho el diagrama de Ann con los métodos.

Definir las entidades que pueden ser vializados: Movie, Chapter  Book.

> Las interfaces permite relacionar métodos de diferentes familias (diferentes clases Padre).

Se define la interfaz **IVisualible** en Movie y Book. Cuando implementemos los métodos de la interfaz en Movie, éstos por herencia heredarán a Chapter.

> Nota: Interfaces para reutilizar métodos en diferentes familias (diferentes clases Padre) y la herencia para reutilizar métodos de la misma familia.

Interfaz:
```
public interface IVisualizable{
  Date startToSee(Date dateI);
  void stopToSee(Date dateI, Date dateF);
}
```

Implementación:
```
public class Movie extends Film implements IVisualizable {
  // Code
}
```

En las interfaces nombraremos los métodos y en las clases los definimos.

# Implementando interfaces al proyecto

Después de haber aplicado herencia (clase Film y Publication) y poliformismo (editar el método toString() que es el encargado de devolver información a invocar el método). Creamos la interface en el paquete models.

Es buena práctica que las interfaces empiecen por I.

> Las herencias no son múltiples pero las interfaces sí.

En el caso de las interfaces es necesario editar los métodos.

# Interfaz List, ArrayList y Vector

Colecciones de datos: Se diferencian de los arrays en que su tamaño no es fijo. Se pueden realizar operaciones de añadir, eliminar, obtener, encontrar, encontrar o recorrer una colección.

Las más comunes son: 
- Set:
  - HashSet:
    - LinkedHashSet.
  - SortedSet:
    - NavigableSet
    - TreeSet
- List:
  - ArrayList
  - Vector
- Queue(ésta ya no es muy utilizada):
  - LinkedList
  - PriorityQueue


### List

Se utiliza para almacenar colecciones de objetos, proviene del paquete java.util. No colecciones de datos primitivos.

Las colecciones pueden estar ordenadas y con elementos repetidos.

Métodos:
- add(Object o): Añadir un objeto al final de la lista.
- add(int indice, Object o): Añade un objeto a la lista en la posición indicada.
- get(int indice): Devuelve el objeto de la lista de la posición indicada.
- remove(int indice): Elimina el objeto en el índice indicado.
- clear(): Elimina todos los elementos de la lista.
- indexOf(Object o): Devuelve la posición de la primera vez que un elemento coincida con el objeto pasado por parámetro. Si el elemento no se encuentra devuelve -1.
- lastIndexOf(Object o): Devuelve la posición de la última vez que un elemento coincida con el objeto pasado por parámetro. Si el elemento no se encuentra devuelve -1.
- size(): Devuelve el número de elementos de la lista.
- contains(Object o): Devuelve verdadero o falso si el objeto pasado en la lista coincide. Utiliza intrísicamente equals().

> En java movie == movie2 -> Lo que compara es la dirección de memoria. Para comparar usar el método equals.

### Set

Puede estar o no ordenada pero o tiene elementos repetidos.

- ArratList: Almacena un arreglo de objetos que puede cambiar de tamaño, tiene una capacidad que crece automáticamente.

```
// Lo que va entre los diamantes es el objeto
ArrayList<String> androids = ArrayList<String>();

androids.add("Jelly Bean");
android.add("Kit Kat");
android.add("Lollipod");
```

- Vector: Es muy similar a un array, la diferencia estriba en que un vector usa hilos y está sincronizado y un ArrayList no.

# Creando e imprimiendo colecciones de datos

Vamos a Implementar ArrayList en el proyecto.

Está mejor visto "Sí" o "No". Cuando se pregunta si ha sido visto en vez de true o falae. Recuerda **No creamos aplicaciones para nosotros**.

# Como leer datos desde la consola en Java

Desde Java 5 tenemos la clase Scanner:

```
// TODO -> Se debe validar que sea un entero
Scanner sc = new Scanner(System.in);
int response = Integer.valueOf(sc.nextLine());
```

# Solución del reto de mostrar series y películas

Aquí se termina la clase series y películas.

# Escribir archivos File

Aquí creamos un nuevo proyecto para dar ejemplo.

```
public class Report{
  private String nameFile;
  private String title;
  private String content;
  private String extension;

  // Creamos getters y Setters

  public void makeReport(){
    
    if ((getNameFile() != null) && (getTitle() != null) && (getContent() != null)){

      // Crear el archivo, del paquete io
      File file = new File(getNameFile()+"."+getExtension());
      FileOutputStream fos = new FileOutputStream(file); // Va a recibir el archivo y prepararlo para escribir.
      OutoutStreamWriter osw = new OutputStreamWriter(fos); // Convertir el stream de de bytes a caracteres.
      BufferedWriter bw = new BufferedWriter(ows); // Es mucho más rápido
      bw.write(getContent());
      bw.close(); // Cada vez que usamos un buffer es bueno cerrarlo.

    } else{
      System.out.println("Ingresa los datos del archivo");
    }
  }
}
```

Creamos la clase main
```
Report report = new Report();
report.setNameFile("Reporte");
report.setExtension("txt");
report.setTittle(":: REPORTE ::");
String content = report.getTittle();
for (int i =0;i<=5; i++){
  content += "\nReporte: " +i;
}
report.setContent(content);
report.makeReport();

```

# Cómo crear e integrar un archivo jar de java

En eclipse, clic derecho en el proyecto y export.

- JAR file: Se exporta como una librería. (sin el main).
- Runnable JAR file: Un archivo ejecutable  desde consola.

Para agregar la librería a un proyecto, damos clic contrario a la carpeta del mismo, luego en **Bluid path** y seguido en **Add External Archives...**. Buscamos el JAR y listo. Pero de esta forma toma la ruta original del archivo.

Ann crea una carpeta llamada libs donde guardar las librerías que creamos. Para que eclipse lo reconozca realizamos el mismo procedimiento pero con la nueva ruta.

> "Es lindo utilizar tus propias librerías".

Todo en Java deben ser por Getters y Setters.

Implementaremos la librería para escribir y leer en el archivo de reporte. Uno por clase. Se reporta las movies vistas.

Crear validaciones para hacer un reporte solo si se ha visto algo.

Se agrega como ReportToDay.

Para generar las fechas en Java

```
public static void makeReport(Date date){
  SimpleDateFormat df = new SimpleDateFormat("yyyy-MM-dd");
  String dateString = df.format(date);
  Report report = new Report();
  report.setNameFile("reporte"+ dateString);

  // Colocar aquí el llenado de todos.

}
```
