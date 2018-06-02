# Bienvenida al curso

Con esto entenderemos y saber qué es lo que hacemos cuando derivamos, aplicamos integrales, etc.

La profe Marce es Ing. Mecatrónica

# Función, dominio y contradominio

**¿Qué es una función?**: Una función es la relación que hay entre dos conjuntos, a través de la cual a cada elemento del primer conjnto se la asigna un único elemento del segundo conjunto o ninguno.

> Tener un buen desempeño está en función de si estamos lleno, estar lleno está en función del dinero que tenenmos en el bolsillo, tener diero en el bolsillo está en función del dinero que ganamos en el trabajo.

> "No es solo tener una fórmula sino comprender la misma".

Dominio: Conjunto iniciao de partida.
Codominio: Conjunto final o de llegada.

Ejemplo: Para f(x)=x^2; Dominio (-infinito,+infinito); Contradominio(0,+infinito)

# Representación gráfica de la función

R^2: 2 dimensiones (x, y)

# Introducción al cálculo diferencial

Podemos saber qué es y cómo resolver una derivada. Pero ¿qué es lo que realmente sucede?

Imagina montaña de escalones donde entre peldaño ascendente aumenta de no en uno.

> "La derivada nos muestra la evolución de la inclinaciń de los tablones a lo largo del proyecto".

Los cambios de los coeficientes directores de los ángulos están definidos por nuestra derivada.

Las derivadas tienen muchas aplicaciones en medicina, arquitectura, cambios en fenómenos físicos.

Ejemplo: "Si tenemos una función de movimiento de una mosca que dibuja una trayectoria, esa trayectoria será un función en un tiempo T. Al tenerla y la derivamos obtenemos la función tenemos la velocidad, al derivarla nuevamente obtendremos aceleración".

# Fórmulas básicas de derivación

- Una variable es un elemento que puede llegar a tomar cualquier valor.
- Constante es un elemento que permanece constante.

La tendencia es que variables son las últimas letras y las constantes las primeras del alfabeto.

Funciones:
- (d/dx)C = 0
- (d/dx)X = 1
- (d/dx)CX = C
- (d/dx)X^n = nX^(n-1)
- (d/dx)CX^n = nCX^(n-1)

# Derivada de funciones algebraicas suma y resta

- Suma: Es equivalente a la suma de la derivada de cada término.
- Resta: Es equivalente a la resta de la derivada de cada término.

# Derivada de funciones algebraicas multiplicación I

- d/dx(uv)= u(d/dx)V+V(d/dx)u; Donde u y V son dos polinomios.

# Derivada de funciones algebraicas Multiplicación II

Es un ejemplo con raíces.

# Derivada de funciones algebraicas Muliplicación III

Aquí se usa producto común.

# Derivadas de funciones algebraicas de División I

d/dx (u/v) = [v(d/dx)(u)-u(d/dx)(v)]/[v^2] @v!=0

# Derivadas de funciones algebraicas de División II

> "El cálculo no solo está hecho para resolverlo y ya"

Si no simplificamos nuestras funciones en cualquier campo de estudio ser hará más complicado implementarla. Como el crecimiento de las bacterias, etc.

# Derivadas de funciones algebraicas de División III

El ejercicio es `y=2x/sqrt(x+1)` sqrt: Raíz cuadrada

# Derivadas de funciones Potencia-Exponenciales

- d/dx(v^n) = nv^(n-1)d/dx(v)

Ejercicio: y=(3x+6)^3 Resultado: y'=9(3x+6)^2

# Derivada de funciones trigonométricas (transcendentales)

- d/dx Sen(v) = Cos(v) dv/dx

> Aquí encontramos el formulario.

- d/dx tg(v) = Sec^2(v) dv/dx

- d/dx ln(v) = [dv/dx]/v

> "Un arco (arc) de una función tigonométrica es la función inversa"

- d/dx(arctg(v)) = [dv/dx]/(1+v^2)

# Derivada de funciones exponenciales

- d/dx(a^v) = a^v ln a (dv/dx) 
- d/dx(e^v) = (dv/dx)e^v

Ejemplo: y = a ^(-10x³) 

Ejemplo: y = e ^(9x²+7)

# Optimización

"Tenemos el dinero suficiente dinero en área rectangular para construir cuatro estanques para un cultivo"

Necesitamos saber cuánto es el área que podemos usar para construir los estantes.

Entre cada estanque hay 2 metros de separación. Por lo cual necesitamos saber la base y altura de cada tanque.

"Son cuatro tanques dentro de un rectángulo separado por dos metros incluyendo entre las paredes"

ÁreaTotal = 500 m = b(base)*h(altura)
b1 = (b- 10)/4 => 10 metros en la sumatoia entre todos los tanques
h1 = h - 4 => 4 metros son los dos metros de cada lado (arriba y abajo)
A1 = b1*h1 = [(b-10)/4]*(h-4)
h = 500/b

A1 = [(b-10)/4]*(500-4b/b1) = (b-10)(500-4b)/4b = -b + 133 - 1250/b

Derivamos

dA1/db = d/db(-b+135-1250/b)
       = -1 + 1250b⁻²

Igualamos a cero para desejar b.

b = +- 35.355m => Como en distancias no existe negativo, usamos el positivo.

Aplicamos la segunda derivada

d²A1/db² = d/db(-1+1250/b²) = -2500B⁻³

> Con la primera derivada obtenemos el máximo y con la segunda tenemos el mínimo. (valor de la base).

Reemplazamos:
h = 500m²/b= 500m²/35.55m = 14.14 m

La capacidad máxima para insertar 4 tanques en un área de 500m² es que éstos tengan una base de 35.55 m y una altura de 14.14m

> **Las derivadas son usadas para optimizar ecuaciones y problemas**.

# Introducción al cálculo integral

Es una sumatorio de diferentes áreas a través de una función que la va a trazar.

Es una porción debajo de la curva.

Las integrales se utiliza para calcular áreas y volumen debajo de una función. En figuras definidas es un poco más complicada.

> Con las derivadas obtenemos los cambios de una función.

# Integrales fórmualas básicas I

- |e^x dx = e^x
- | a^x dx = a^x/lna => a>0

> Cuando en vez de x sea 2x -> Reemplazar a u=2x y du=2dx

# Integrales fórmulas básicas II

- |x^n = x^(n+1)/n+1

# Integrales Fórmulas básicas III

Hay formulario y ejercicios en la sección de archivos.

# Integrales fórmulas básicas IV

- |Sen x dx = -Cos x + C

Se utiliza u=4x y du=4dx y 4/4 en la integral para no alterala.

# Integrales fórmulas básicas V

Vamos a usar integrales definidas para calcular un área bajo la curva.

Ejercicio: y=x²

|x²dx = x³/3 (evaluado en 2 a 0)

- @x=2,0 => (2)³/3 - (0)³/3 = 8/3 (Área)

# Introducción al cálculo multivariable - Derivadas parciales

Ejemplo: f(x,y) = x²y

> Considereamos a la variable que no está involucrada como una constante (como un número)

&f/&x = 2xy
&f/&y = x²

En funciones multivariables, hacemos derivadas parciales en cada una de ellas.

# Gradientes

El gradiente almacena toda la información de la derivada parcial de una función multivariable.

Es un vector.

Opeardor gradiente (triángulo invertido -> nabla)

\/f(x0,y0,...) = [&f/&x, &f/&y, ...]

f(x,y) = x² - xy

\/f = [2x-y, -x]
