# Introducción

Profesora: Marce Velenzuela

# Conceptos básicos de Probabilidad y estadística

### Lo que debes recordar
- La probabilidad de que un evento ocurra puede ser un número entre 0 y 1. Jamás negativo.
- La probabilidad puede escribirse en forma de fracción, decimal o porcentaje.
- La probabilidad del evento A suele escribirse como P(A).
- Si P(A) > P(B), el evento A tiene una mayor probabilidad de ocurrir que el evento B.
- Si P(A) = P(B), significa que ambos tienen la misma probabilidad 

### Experimento

Es un proceso que nos va a aportar los datos estadísticos que nos van ayudar a estudiar.

- Numérico: Los resultados son numéricos.
- No numérico: Son cualitativos como colores.

Experimento: Tomar un caramelo al azar con los ojos cerrados. Rosa o azul.

(Se trata de un experimiento no numérico)

Espacio muestral: Es todo el conjunto de valores que vamos a obtener en determinados experimentos = {azul, rosa} se simboliza con omega

Suceso elemental: Cada resultado que obtenemos de nuestro experimento se encuentra dentro de nuestro espacio muestral.

Pueden ser:
- Posible: Tiene probabilidad.
- Seguro: Sin posibilidad a fallo.
- Imposible: Sin posibilidad de éxito.

# Cálculo de probabilidades

Regla de Laplace: En experimentos equiprobables

P(A)=Casos favorlables de A/Casos posibles

# Probabilidad compuesta y Diagramas de árbol

Otro nombre es probabilidad condicionada.

> Es aquella donde intervienen más de un experimento aleatorio.

Ejemplo de ir un lugar o no y contar con el permiso o no.

Otro ejemplo es haciendo un diagrama de árbol de tres lanzamientos de una moneda y la probabilidad de que salgan dos cruces.

El espacio muestral (omega) es equivalente a 8 sucesos elementales.

Como es un suceso equiprobable:

P(Cada rama completa) = 1/2 * 1/2 * 1/2 = 1/8

Las ramas que cumplen la condición de dos cruces son: C++, +C+, ++C, +++

Cada una de estas ramas tienen una probabilidad de 1/8 que al sumarlas:

p(A) = 1/8+1/8+1/8+1/8 = 4/8 = 1/2

Entonces la probabilidad de que ocurra el suceso A, es de 50%.

# Probabilidad compuesta: Union

Ejemplo: Lanzando un dado.

El espacio muestral de 1,2,3,4,5,6
Si tenemos los sucesos A=[6,1], B=[1,3,2], C=[4], D=[4,5,6] y sacamos un 1:

- Compatibles A y B: El 1 se encuentra en ambos subconjuntos; es decir, **suceden al mismo tiempo**.
- Incompatibles A y C: **Ambos sucesos no se pueden dar al mismo tiempo**. No comparten algún suceso elemental.
- Complementarios B y D: Al unir todos los sucesos elementales en un solo grupo, **al unirlos conforman todo el espacio muestral**

### Unión

Suceso formado por todos los resultados que cumplen A o cumplen B.

Si A = [2,4,6] y B=[4,5,6], la unión de A y B sería igual a: AUB={2,3,6}U{4,5,6}={2,4,5,6}

Para calcular la probabilidad de una unión se utiliza la siguiente regla elemental:
- P(AUB)=P(A)+P(B)
- P(AUB)= P(A)+P(B)-P(ANB) // N es una U invertida, quitando la intersección que hay entre ellos como por ejemplo dos veces el 4.

Ejemplo: Un 15% de los pacientes atendidos en un hospital son hipertensos, un 10% son obesos y un 3% son hipertensos y obesos. ¿Qué probabilidad hay de que elegido un paciente al azaar sea obeso o hipertenso?

A={Hipertenso} P(A)=15%=0.15
B={Obeso} P(B)=10%=0.10
ANB={Hipertenso y obeso} P(ANB)=3%=0.03
P(AUB) = P(A)+P(B)-P(ANB)
AUB = {Hipertenso u obeso} = P(AUB) = 0.15+0.1-0.03=0.22

La probabilidad de que al elegir un paciente al azar y sea obeso o hipertenso es del 22%.

# Probabilidad compuesta: Intersección

Susceso formado por todos los resultados que cumplen A y cumplen B.

Si A={2,4,6} y B={4,5,6}, la intersección de A y B es igual a ANB={2,4,6}N{4,5,6} = {4,6}

Para calcular la probabilidad de una intersección:
- P(ANB) = P(A)*P(B)
- P(ANB) = P(A/B)*P(B), donde
P(B/A) = P(ANB)/P(A) si P(A) != 0

Ejemplo: Determine el valor de la probabilidad de obtener 2, sabiendo que ha salido un número par al lanzar un dado al aire.

Solución:
Primero se definen los sucesos:
- P(A) = P(Al lanzar el dado, el resultado es par) A={2,4,6}
- P(B) = P(Que salga el número 2) B={2}
- P(ANB) = P(Que al lanzar un dado, el resultado sea pa y sea el 2) ANB={2}

Se calculan las probabilidades:
- P(A) = 3/6 = 1/2
- P(ANB) = 1/6

Finalmente se calcula la probabilidad condicionada
P(A/B) = P(ANB)/P(A) = (1/6)/(1/2) = 2/6 = 1/3

> Recordar: Sucesos favorables sobre sucesos posibles.

1/3 es la probabilidad de que ocurra dicha intersección.


# Variaciones, permutaciones y combinaciones: Ejercicios

### Variaciones

Ejemplo: ¿De cuántas maneras pueden sentarse 10 personas en un banco y solo hay 4 sitios disponibles?

v|10,4 = n!/(n-r)! = 10!/(10-4)! = 10!/6! = (10*9*8*7*6!)/6! = 10*9*8*7 = 5040 maneras

### Combinación

Ejemplo: En una clase de 10 alumnos van a distribuirse 3 premios, suponiendo que los alumnos no pueden recibir más de un premio, cuántas maneras posibles hay de repartir los premios si:

- Los premios son diferentes:

V|10,3 = n!/(n-r)! = 10!/(10-3)! = 10!/7! = 10*9*8*7!/7! = 720 manerasposibles de repartir.

- Los premios son iguales

C|10,3 = n!/r!(n-r)! = 10!/3!(10-3)! = 10!/3!7! = 10*9*8*7!/3*2*1*7! = 720/6 = 120 maneras de repartir los premios

### Permutaciones

Hay que colocar a 5 hombres y 4 mujeres en una fila de modo que las mujeres ocupen los lugares pares. ¿De cuántas maneras puede hacerse?

Como la fila es de 9 personas en total, hay 4 posiciones pares (que deben ser ocupadas por las 4 mujeres) y 5 posiciones imparse (para los 5 hombres)

HMHMHMHMH

P4! = 4*3*2*1 = 24 // Esto es la permutación de mujeres
P5! = 5*4*3*2*1 = 120 // Permutaicones de hombres

24*120 -> 2880 maneras de distribuir esta fila con hombres y mujeres

# Variaaciones, permutaaciones y combinaciones

Combinatoria: Ciencia que estudia las agrupaciones partiendo de un conjunto teniendo en cuenta el orden y el número de esos elementos.

> Factorial: El factorial de un número natural n es el resultado del producto de este número por todos los números naturales que lo anteceden, excluyendo al cero y se representa por el número !

**Variaciones**: Son subgrupos que ocurren cuando tenemos que agrupar cierto número de elementos en una cantidad específica dentro del grupo. Es necesario tener n elementos y agruparlos en grupos de r elementos (dos en dos, tres en tres, ect)

V|n,r = n!/(n-r)!

Ejemplo1: ¿Cuántas variaciones existen entre los elementos A,B,C y D tomados de dos en dos?

> En la variación si va a ser tomado de dos en dos, quiere decir que por cada una de las cuatro letras vamos hacer una pareja, AB, AC, AD, BA, BC, BD, CA, CB, CD, DA, DB, DC. Aquí sí importa el número de elementos pero no las repeticiones (AB y BA) se cuentan ambas.

V4,2 = 4!/(4-2)! = (4*3*2*1)/2*1 = 4 * 3 = 12

**Permutaciones**: Son variaciones de n elementos tomados en grupos de r, donde n = r.

Cada agrupación difiere de las restantes solo en el orden de colocación de los elementos, y en cada grupo intervienen todos los elementos del conjunto.

El número de permutaaciones ordinarias formadas de n elementos viene dado por:

Pn = n (n-1)*(n-2)...(1) = n!

Ejemplo: ¿Cuántas permutaciones ordinarias (sin repetición) se pueden formar con elementos A, B y C?

Combinando -> ABC, ACB, BAC, BCA, CAB, CBA

P|3 = 3! = 3*2*1=6

> Aquí se cambian lugares

**Combinaciones**: Se obtienen al seleccionar de un conjunto de n elementos grupos de r, de tal forma que sin importar el orden de sus elementos, estos no se repiten.

El nḿero de combinaciones ordinarias (sin repetición) que se pueden formar con n elementos tomados de r en r se calcula a partir de la sigiente fórmua:

C|n,r = n!/r!(n-r)! = (n|r) = C|n,r = Vn,r/P|r

Ejemplo: ¿Cuál es el número de combinaciones que pueden formarse con los elementos A, B, C y D tomados de dos en dos?

Combinaciones -> AB, AC, AD, BC, BD, CD

C|4,2 = 4!/(2!(4-2)!) = 6

> Aquí no se permiten repeticiones.

# Tablas de frecuencia

**Distribución de datos**: Es esencial para elejir le método estadístico correcto según las necesidades.

Los datos analizados se representan en tres formar:
- Gráficas
- Texto
- Cuadros estadísticos

¿Cómo organizar los datos? -> Para ello utiliza una tabla de frecuencia según el muestreo.

> Hay muchos ejercicios en el curso.

Ejercicio: Una profesora tiene la lista de las calificaciones en matemáticas de 30 alumnos de su clase.

Se dicta una tabla de notas de 30 alumnos

Ki -> Notas
Frecuencia absoluta (n) -> Cantidad de alumnos que tuvieron esa nota
Frecuencia absoluta acumulada (N) -> Frecuencia absoluta + Frecuencia absoluta anterior (la primera so toma la misma frecuencia absoluta). Debe dar igual a la cantidad de alumnos (30).
Frecuencia relativa ( fi -> n/n° total de alumnos) La suma de esta frecuencia debe ser unitario.
Frecuencia relativa acumulada (N/n° Total de alumnos)
- Dos columnas de frecuencias absolutas y relativa acumulada multiplicada 100%

# Tablas de frecuencia en distribución de datos: Ejercicios

Ejercicio: Lista de goles de Messi de la temporada 2011-2012 de la liga, hacer una tabla de frecuencia (sa -> Que estuvo sancionado)

Datos: 3,2,0,3,0,3,0,2,0,0,3,1,1,0,1,0,1,0,2,3,0,1,0,4,1,0,2,1,3,1,1,2,1,2,0,2,4,0


| Xi | ni| Ni| fi(ni/N) | Fi(Ni/N) | Fr(%) | Fra(%) |
|---|---|----|----------|----------|-------|--------|
|0 |  13|  13 | 0.342   | 0.342    |  32.2 |  34.2  |
|1|  10 |  23 | 0.363   | 0.605    |  26.3 |  60.5  |
|2|   7 |  30 | 0.184   | 0.789    |  18.4 |  68.9  |
|3|   6 |  36 | 0.157   | 0.947    |  15.7 |  94.7  |
|4|   2 |  38 | 0.052   | 1        |  5.2  |  100   |
|Total |  38 |     | 0.998   |          |  99.8 |        |

N = 38

# Tablas de frecuencia gráficas

Distribución de datos y gráficas más utilizadas.

> La **Distribución de datos es esencial para elegir el método estadístico correcto

Gráficas: Existen diversos tipos de gráficas. Pueden proveer instantáneamente sobre la distribución de un conjunto de datos.

Diagrama de sectores: Es un diagra de tortas. Se utilizan y agregan dos tablas

|Goles por partido (Xi)| Frecuencia absoluta (ni) | Arco de grados (0=(ni*360°)/N)|Porcentaje de la gráfica(Fr en %)|
|----------------------|--------------------------|-------------------------------|---------------------------------|
| 0 | 13 | 123.15 | 34.2 |
| 1 | 10 | 94.73  | 26.3 |
| 2 | 7  | 66.31  | 18.4 |
| 3 | 6  | 56.84  | 15.7 |
| 4 | 2  | 18.94  |  5.2 |
| Total | N=38 | 359.97 | 99.8 |

En el gráfico se usa la columna de Frecuencia relativa

Polígono de frecuencia: Se utilizan trazando los puntos que representan las frecuencias (nativas o absolutas según el caso) y uniéndolos mediante segmentos. En el Eje X: Cantidad de goles, en el Eje Y: Frecuencias.

Gráfica de barras: La altura se toma igual a la frecuencia absoluta o relativa (según la distribución de frecuencias que estemos representando), consiguiendo de esta manera rectángulos con áreas proporcionales que se quiren representar.

# Parámetros estadísticos centralización

Medidas de tendencia central: Son los representantes de  los datos donde la mayoría se considera los mejores (michael jackson, ect).

Parámetros estadísticos:
1. Centralización: Son los valores centrales del conjunto de valores qrecogidos que representan, de forma global, a toda la población o la muestra. Aunque no sepamos del tema sabemos que es un representante del sector.
1.1. Media: Es el valor característico de la serie de datos resultado de la suma de todas las observaciones dividido por el número total de datos.
x⁻ = (x1+x2+x3+xn)/N

La línea de arriba se llama testada.

1.2. Mediana: Es el valor de posición central en un conjunto de datos ordenados. Dependiendo de si el número de datos es impar o par, se utilizan las siguientes fórmuas, en ese orden:
Mediana(X) = X|(N+1)/2
Mediana(X) = [X|N/2 + X|(N/2 +1)]/2

> Es el dato de justo del medio. De una cantidad impar, como el siete sería el cuarto número. Si es par, se ordenan y se aplica la segunda fórmula con los dos valores del medio.

1.3. Moda: Es el valor repetido del conjunto de datos. Puede haber más de una moda. Es el número que más se repite de un conjunto de datos.

# Parámetros estadísticos centralización: Ejercicio

Datos: 3,2,0,3,0,3,0,2,0,0,3,1,1,0,1,0,1,0,2,3,0,1,0,4,1,0,2,1,3,1,1,2,1,2,0,2,4,0

Datos ordenados: 0 0 0 0 0 0 0 0 0 0 0 0 0 1 1 1 1 1 1 1 1 1 1 2 2 2 2 2 2 2 3 3 3 3 3 3 4 4

**Media(X⁻)** = 50(goles)/38(partidos) = 1.31

**Mediana**
Posición de la mediana = 38/2 = 19 (se marca el 19avo de atrás para adelante y de adelante para atrás de la secuencia numérica ordenada)

Mediana = (1+1)/2 = 2/2 = 1

**Moda** = 0

> Notas: Media es el promedio, mediana es el valor del medio del set de datos y moda es el número que más se repite.

# Gráficas de dispersión

Relacionan los datos de estudio: Estas gráficas las representamos en un diagrama matemático mediante coordenadas cartesisanas que generan puntos dispersos alrededor del plano.

También llamado nube de puntos.

Analiza la relación entro dos variables estadísticas bidimensionales, conociendo qué tanto se afectan entre sí o qué tan independientes son una de al otra.

Una es una variable dependiente y la otra es independiente.

Estas son las estadísticas de los goles anotados por de Lionel Messi en cada temporda jugada con el Club Barcelona

| Temporada | Goles |
|-----------|-------|
| 2004-2005 | 1 |
| 2005-2006 | 8 |
| 2006-2007 | 17 |
| 2007-2008 | 16 |
| 2008-2009 | 38 |
| 2009-2010 | 47 |
| 2010-2011 | 53 |
| 2011-2012 | 73 |
| 2012-2013 | 60 |
| 2013-2014 | 41 |
| 2014-2015 | 58 |
| 2015-2016 | 41 |
| 2016-2017 | 54 |
| 2011-2012 | 73 |
| 2012-2013 | 60 |
| 2013-2014 | 41 |
| 2014-2015 | 58 |
| 2015-2016 | 41 |
| 2016-2017 | 54 |


Se grafica un gráfico de dispersión en el Eje X -> Temporada y Eje Y -> Goles

# Tipos de correlación y covarianza

Tipos de correlación: Según el comportamiento de las variables de estudio. Podemos encontrar tres tipos de correlación: Directa, inversa y nula.

Covarianza: (S|xy o O|xy):
- Es la media aritmética de los productos de las desviaciones de cada una de las variables respecto a sus medias respectivas.
- Al determinar el valor de la covarianza, nos ayudará a comprender el tio de correlación lineal.

> Nos va a dar pauta para saber de cómo están relacionadas estas variables.

Correlación directa  (Covarianza +): Se representa cuando una variable aumenta o disminuye y a otra también, respectivamente. Ha una relación proporcional. Es una distribución de datos con tendencia lineal. Por ejemplo: En una fábrica mientras más ventas, más ingresos.

> Si la covarianca es positiva la correlación va a ser directa. Es una pendiente en crecimiento de izquierda a derecha.

Correlación inversa (covarianza -): Se presenta cuando una variable se comporta de forma contraria a la otra; si una variable aumenta, la otra disminuye. hay una relacion inversa proporcional.

> Es una pendiente negativa. Inclinado de forma descendente de izquierda a derecha.

Correlación nula: Se da cuando no se encuentra un comportamiento entre las variables. Son puntos dispersos completo por todo el plano.

Correlación fuerte: Los puntos están cercanos a la línea de regresión.

Correlación débil: Cuando los puntos tienden a formar una línea pero no están muy cercanos a una de regresión.

# Rango

Dispersión de distribuciones.

**Parámetros estadísticos**

2. Dispersión: Son una serie de valores que indican lo dispersos o agrupados están los datos entre sí y respecto a la media. Es decir qué tan juntos o separados están nuestros datos.

2.1. Rango: Es el recorrido de la distribución estadística. Dada una serie de valores X1, X2, ..., Xn. Su recorrido es la diferencia aritmética entre el máximo y el mínimo de estos valores:

Esto es para datos no agrupados.

Re = Xi(max) - Xi(min)

Siendo i = 1,2,...,n.

Ejemplo: Sea el siguiente conjunto de datos: 12, 15, 17, 23, 25, 28. Hallar el rango.

Xmáx = 28
Xmin = 12

Rango = 28 - 12 = 16

Rango para datos agrupados: Si los datos están agrupados en una tabla de frecuencias, el recorrido es la diferencia entre el límite real superior del último intervalo y el límite real inferior del primer intervalo.

R = Lmáx - Lmin

Ejemplo: Según los datos de la tabla, hallar el rango:

|Peso (Kg) | fi |
|----------|----|
|55.0 - 63.0 | 5 |
| 63.1- 71-1 | 15|
| 71.2 - 79.2 | 12 |
| 79.3 - 87.3 | 5 |
| 87.4 - 95.4 | 3 |
| Total | 40 |

Lmin = 55
Lmáx =95.4
R = 40.4

El rango mide **"la dispersión total"** del conjunto de datos. Aunqu el rango es una medida de dispersión simple y que se calcula con facilidad, su debilidad preponderante es que no toma en consideraación la forma en que se distribuyen los datos entre los valores más pequeños y los más grandes.

> No podemos tomarlo como parámetro principial porque nos generaliza qué tan dispersos están todos nuestros conjunto de datos porque no toma las dispersión de los datos. Solo nos sirve para tenerlo la dispersión de los datos de manera general.

# Desviación media

2.2. Desviación media: Es la media aritmética de los valores absolutos de las desviaciones de todos los datos respecto  la media aritmética.

> Es un número que nos indica la diferencia o el promedio de la diferencia que nos vamos a encontrar entre los valores absolutos de cada uno de nuestros elementos con la media aritmética.

Ejemplo: Obtener la desviación media para los datos 4, 7, 8, 10 y 16

X⁻ = (4+7+8+10+16)/5 = 45/5 = 9

DM = (|4-9|+|7-9|+|8-9|+|10-9|+|16-9|)/5 = 16/5 = 3.2

**Desviación media para datos agrupados**: Si los datos vienen agrupados en una tabla de frecuencias, la expresión es:

DM = [sumatoria(|Xi - X⁻|)*fi;n,i=1]/N

Con i = 1, 2, ..., n

Obtener la desviación media de la siguiente distribución

|   |xi  | fi  | xi*fi | xi-x⁻ | (xi-x⁻)*fi |
|---|----|-----|-------|-------|------------|
| [10,15] | 12.5 | 3 | 37.5 | 27.858 |
| [15,20] | 17.5 | 5 | 87.5 | 21.43 |
| [20,25] | 22.5 | 7 | 157.5 | 4.998 |
| [25,30] | 27.5 | 4 | 110  | 22.856 |
| [30,35] | 32.5 | 2 | 65   | 21.428 |
|         |      | 21| 457.5| 98.57

X⁻ = 457.5/21 = 21.786
Dx = 98.57/21 = 4.69

# Varianza y desviación estándar

2.3. Desviación estándar: Es qué tan separados están nuestros datos.
2.4. Varianza: Es la raíz cuadrada de la desviación estándar.

Ejemplo calcualar la varianza y desviación estándar de los siguientes números.

Datos: 1, 2, 5, 7 y 9

X⁻ = (1+2+5+7+9)/5 = 24/5 = 4.8

Luego restar lo siguiente:

4.8-1=3.8 Se elevan al 2 -> 14.44
4.8-2=2.8  -> 7.84
4.8-5=-0.2 -> 0.04
4-8-7=-2.2 -> 4.84
4.8-9= -4.2 -> 17.64
        Total: 44.8

Vaianza = 44.8/5 = 8.96
Desviación estándar = sqrt(8.99) = 2.99

Con la desviación se utiliza el margen de más o menos. Es decir, tenemos el límite.

Peso normal= 4.8
Extra alto de peso= 7.8
Extra bajo de peso= 1.8

# Coeficiente de correlación

2.4. Coeficiente de correlación: Nos describe cómo es la relación existente entre dos variables. 

Enunciados:

- Es un valor cuantitativo de la relación entre dos o más variables.
- La correlación de proporcionalidad directa o positiva se establece con los valores +1.00 y de proporcionaldad inversa o negativa, con -1.00.
- No existe relación entre las variables cuando el coeficiente es de 0.00

A través del valor del coeficiente de correlación podemos tener una referencia de la gráfica y viceversa.

> Las gráficas de los coeficientes de relación de 0 tienen formas muy intersantes.

Ejercicio: En una empresa de transporte trabajan 4 conductores. Los años de antigüedad de sus permisos de conducir y el número de infracciones cometidas en el último año por cada uno de ellos son los siguientes:

|X: Años de antigüedad | Y: Infracciones |
|----------------------|-----------------|
|3 | 4 |
|4 | 3 |
|5 | 2 |
|6 | 1 |

a. Representar gráficamente los datos anteriores. Razonar si los datos muestran una correlación positiva o negativa.
b. Calcular el coeficiente de correlación e interpretarlo en términos de la situación real.

**Nota** No se termina de cargar el vídeo.

# Cuartiles, deciles y percentiles

3. Parámetros estadísticos de posición: Tienen como funcion ubicar la distribución a lo largo de los valores de la misma. Se suelen utilizar una serie de valores ue dividen la muestra en tramos iguales.

3.1. Cuartiles (son 3): Son los tres valores de la variable que dividen a un conjunto de datos ordenados en cuatro partes iguales. Q1,Q2,Q3 determinan los valores correspondientes al 25%, 50% y al 75% de los datos. Q2 coincide con la mediana.

3.2. Deciles (son 9): Son los nueve valores que dividen la serie de datos en diez partes iguales. Dan los valores correspondientes al 10%, 20%... y al 90% de los datos. D5 coincide con la mediana.

3.3. Percentiles (son 99): Son los 99 valores que dividen la serie de datos en 100 partes iguales. Dan los valores correspondientes al 1%, 2%... y al 99% de los datos. P50 coincide con la mediana y D5.

# Cuartiles

Son los tres valores de la variable que dividen a un conjunto de datos ordenados en cuatro partes iguales.

Pasos:
- Ordenar los datos de menor a mayor
- Buscamos el lugar que ocupa cada cuartil mediante la expresión

Datos: 2,3(Q1),4,5(Q2),6,7(Q3),9

# Deciles

Son los nueve valores que dividen la seride de datos en diez partes iguales

|  |fi | Fi |
|--|---|----|
|[50,60] | 8 | 8 |
|[60,70] | 10 | 18 |
|[70,80] | 16 | 34 |
|[80,90] | 14 | 48
|[90,100] | 10 | 58 |
|[100,110] | 5 | 63 |
|[110,120] | 2 | 65 |
|          | 65|    |

1er Decil
65*1/10 = 6.5
D1=50+(6.5-0)/8*10 = 58.12
  
2do Decil
65*2/10=13
D2=60*(13-8)/10 *10 = 65

3er Decil
65*3/10=19.95
D3=70+(19.5-18)/16 * 10 = 70.94

4to Decil
65*4/10 = 26
D4 = 70+(26-18)/16 * 10 = 75

5to Decil
65.5*5/10 = 32.5
D5 = 70+(32.5-18)/16 * 10 = 79.06

6to Decil
65*6/10 =39
D6=80+(39-34)/14 * 10 = 83.57

7mo Decil
65*7/10 = 45.5
D7 = 80+(45.5-34)/14 * 10 = 88.21

8vo Decil
65*8/10 = 52
D8=90+(52-48)/10 * 10 = 94

9no decil
65*9/10 = 58.5
D9=100*(58.5-58)/5 * 10 = 101

# Percentiles

Son los 99 valores que dividen la serie de datos en 100 partes iguales

Con la misma tabla de datos

Percentil 35
65*35/100 22.75

> 22.75 sobrepasa la frecuencia 16 y antecede a 34

P35=70+(22.75-18)/16 * 10 = 72.97

Percentil 60
65*60/100 = 39

> 39 está entre 14 y 48 de frecuencia

P60 = 80+(39-34)/14 * 10 = 83.57

# ¿Qué es y para qué sirve la regresión lineal?

# Ejemplo de regresión lineal (tipo de correlación)


