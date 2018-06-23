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




