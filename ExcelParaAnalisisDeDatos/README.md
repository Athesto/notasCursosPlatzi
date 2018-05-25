# Bienvenida al curso

Prof: Felipe Guzmán

Pasos:
1. Conocer Excel.
2. Recolectar información.
3. Preparar la información.
4. Construir modelos para analizarla.

# Siéntete cómodo con la barra de menu

Excel se distribuye en filas, columnas y como tal coordandas.

Con los estilos de celda, encontraremos diferentes opciones para personalizar la celdas.

- Insertar: Tablas, tablas dinámicas, gráficos...
- Diseño de página: Configuración para impresión, organización de objetos.
- Fórmulas: Diferentes tipos de fórmulas, administrar nombres a ciertas columnas, encontrar erroes dentro de las fórmulas.
- Datos: Ver dónde están las conexiones de archivos internos o externos, filtrar la información, herramienta de texto en columnas para bajar información en texto plano de archivos de internet, se puede quitar duplicados.
- Revisar: Proteger archivos, hojas, celdas, insertar comentarios, atatajos de teclados, inserción de comentarios.
- Vistas: Personalizar la hoga, inmovilizar filas y crear y grabar macros.

# Conoce la estructura de un libro de excel

Podemos usar etiquetas de color en el nombre de las hojas.

Podemos mover, dupliarla, mover al final, etc. Estas copias las podemos hacer en un libro nuevo o bien en un libro que tengamos abierto.

Para moverse entre hojas con teclado: Ctrl+RePág y Crtl+AvPág.

# Protegiendo información en Excel

Podemos progteger información y más:
- Protege archivos, libros, celdas.
- Insertar, cortar y pegar columnas o filas.

> La razón por la que protegemos los archivos es cuando tenemos que compartir información y queremos que sea parcial.

Por defecto, todas las celdas quedan bloqueadas cuando bloqueamos el archivo.

> Nota: Para seleccionar todas las hojas damos clic en la esquina superior izquierda.

Luego en la pestaña de inicio damos clic a número y allí a proteger.

Vamos a revisar y luego a proteger la hoja, nos preguntará una contraseña y definimos las acciones permitidas. Si bloqueamos toda la hoja podemos desbloquear una celta entrando en formato de celdas y luego en Proteger y quitamos la opción de proteger. Esto será muy útil para que ingrese la cantidad de elementos que utilizaron pero no deben modificar el costo, número de asistentes,etc.

En proteger libro, bloqueamos la estructura. Es decir a insertar hojas, hacerlas visibles, ocultarlas, etc. Las hojas las ocultamos para no mostrar información que no queramos que sean públicas, siendo ésta del origen de los datos.

En vistas, quitamos las líneas de cuadrícula. Muchas personas sienten que trabajan mejor así porque sienten que trabajan en una hoja en blanco.

Atajos de teclado
- shift+barra espaciadora: Seleccionar toda una fila.
- Ctrl+barra espaciadora: Seleccionar columna.
- Ctrl+shift++: Insertar una celda. O una columna manteniendo el formato.
- Ctrl+- : Eliminar una celda.

# Listas desplegables

**Proyecto**: Evento de emprendimiento: Habrá un evento donde varios proyectos de emprendimiento serán expuestos. Debemos diseñar el formato que diligenciarán los asistentes.

Las opciones de valores monetarios podemos colocarlo con "contabilida" para que separe en unidades de miles.

Para crear una lista:
- Creamos los item de una lista.
- Vamos a datos -> validación de datos -> Configuración:Lista -> Seleccionamos el origen  luego en aceptar.

> Atajo de teclado para listas desplegables: Alt+flecha hacia abajo.

Es importante saber cómo recolectar información y a su vez, cómo analizarlas.

Ctrl+Inicio: Volver al comienzo de la hoja.

# Listas desplegables dependientes

Son aquellas que dependen de las opciones seleccionadas de una lista desplegable anterior. Ejemplo si en la celda de arriba pone trabajo en la lista desplegable inferior aparezcan si buscando trabajo u otra cosa.

> Podemos darle nombre a un grupo de celdas desde la parte superior izquierda de la hoja. Por donde está el margen. Es importante usar el mismo nombre de la columna y de título del nivel 1.

Ejemplo:

Nivel 1: Trabajo, inversión y conocimiento.
Nivel 2: Trabajo(opción 1 y opción 2), Inversión (Opción 1 y opción 2)...

Para crear la lista desplegable dependiente, para ello creamos como cualquier lista y luego en origen `= indirecto(celdaListaDeLaCualDepend)`.

# ¿Imprimir en Excel? No será un problema nunca más

Hay una opción para imprimir una selcción. También se puede cambiar la orientacion de vertical a horizontal. De igual forma tenemos la opción de ajustar los márgenes.

Dentro de la impresión, en la opción de configurar página podemos especificar el orden de impresión de las hojas.

En la pestaña vistas: Tenemos la opción de "Ver salto de página" para ver la delimitación de la impresión. Podemos en esta vista mover la línea de impresión.

# Reforcemos juntos varios conceptos

- Combinar celdas y ajustar texto para que se combinen varias celdas y se ajuste.

- Entrando en una celda larga, donde queramos que ocurra un salto de línea presionamos Alt+Enter.

En la estaña de inicio, tenemos la opción de "estilos de celda" para que tengan un color representativo. Rojo:mal, amaillo:normal, verde:bien.

Alto de la fila por defecto es 16.5.

Desde la opción de bordes podemos configurar el estilo del borde en una selección.

# Bases de datos

- Para inmovilizar -> En vista inmovilizar -> Inmovilizar paneles y tomará la fila superior y columna izquierda a donde tenemos el cursor.

- Para filtrar en Inicio -> Filtro.

> Ctrl+Flecha -> Nos ayuda a movilizarnos entre extremos de la tabla.

Alt+Flecha -> Para desplegar el filtro.

Ctrl+shift+l -> Quitar todos los filtros.

Ctrl+Shift+flecha -> Seleccionamos el rango de celdas llegas. (Para saber cantidad).

Desde la opción de filtros podemos ordenar. Con el orden personalizado podemos agregar niveles para aplicar orden.

# Separa texto y después júntalo

Esto para transformar la información respecto a cómo nos llega para 
 usarlo en lo que nos interesa.

> Para insertar una fórmula puede ser con **=** o con **+**.

Para juntar el texto de dos celdas: **=C1&C2** Para insertar espacions: **=C1&" "&C2**. Otra opción es **+CONCATENAR(C1;" ";C3)**.

Separar texto en columnas fija:
- Seleccionar el rango: Ctrl+Shift+teclaAbajo -> Datos -> Texto en Columnas -> Ancho Fijo (Definir en qué punto se separan las palabras)

> Elimnar toda una columna: Ctrl+BarraEspaciadora Ctrl+- Para seleccionar y eliminar la columna.

Separar texto en columna delimiata:
- Misma ruta de columna fija y especificar el caracter en el que se va a separar.

# Fórmulas básicas

- SUMA -> Suma un rango.
- PROMEDIO -> Obtiene un promedio de un rango.
- REDONDEAR(celda;cantidadDecimales) -> Redondea un número.

Podemos buscar y reemplazar con las opciones de Buscar.

# Fórmulas de texto

+MAYUSC(celda) -> Convierte a mayúscula
+MiNUSC(celda) -> Convierte a minúscula

> Excel reconoce la fecha como por ejemplo "24 dic"

+HOY() -> Imprime la fecha de hoy

> Si restamos dos fechas optenemos la diferencia en días.

# Sumar.si y Promedio.si

Esto es aplicando una condición.

"Encontrar una fórmula que sume toda la inversión hecha en el sector tecnología en el 2018"
+sumar.si(rangoCelda;criterioItem;rangoCelda) -> Ejemplo +sumar.si(RangoDeCeldaSector;sectorTecnología;rangoCeldaInversion2018)

> Presionando F4 podemos fijar celdas.

"Contar pesonas de las diferentes modalidades y porcentaje de cada uno"
+contar.si(rango;Criterio) Ejemplo -> +contar.si(RangoIntenciónProyectos;trabajo)

+contar -> Cuenta el número de celdas que contienen números en un rango determinado.
+contarA -> Cuenta el número de celdas no vacía en un rango determinado.

+promedio(celda1,celda2,celda3...)

"¿Cuál es la calificación promedio de los proyectos de acuerdo a cada uno de los sectores?"
+promedio.si(rango;criterio;rango) -> Ejemplo +promedio.si(rangoSector;tecnología;rangoProyectos)

# Nombra rangos y haz operaciones 

En el ejemplo restamos dos sumar.si la primera inversión esperada y la otra inversión realmente invertida. En una misma celda
+sumar.si(rango;criterio;rango) -> Ejemplo +sumar.si(sector;tecnología;rangoExpectativa2018)

> Recuerda que el nombre de un rango se colocan en la esquina superior izquierda.

Si le damos un nombre a un rango podemos colocar dentro de la fórmula. Que será constante.

# Promedio ponderado y fijación de datos

Promedio ponderado son porcentajes dentro de los porcentajes como las calificaciones.

"¿Cuál es la calificación promedio? Teniendo en cuenta que la feria tiene una ponderación del 70% y la del proyecto un 30%"
+(feria*70%)+(proyectos*70%)

Podemos hacer lo mismo con la función sumaproducto(rangoPesoPorcentual,rangoCantidad)

F4 (1 vez)  -> Fija el rango
F4 (3 veces, pesos antes de las letras) -> Fijamos las columnas
F4 (2 veces, pesos antes de los números) -> Fijamos las filas

Podemos crear un hipervínculo colocando un contenido en una celda, clic contrario en hipervínculo y especificar una celda.


# Pegado especial

La opción aparace en Pegar -> Pegado especial

Podemos definir si queremos pegar el valor, fórmula, estilo de la celda, etc.

Atajo -> Ctrl+Alt+v

> Si cortamos, las fórmulas que están dentro de la celda también se corta.

Transponer: Las filas pasan a ser las columnas y las columnas pasan a ser filas.

# ¿Qué es BuscarV?

# BuscarV aplicado

Permite traer información de otras hojas o bien en archivos externos.

> Es una especie de una celda inteligente donde busca información según un dato de entrada.

Es importante que el valor buscado esté dentro de la primera columna de la matriz.

Fórmula -> BUSCARV(valorBuscado, matrizValorBuscadoYResultado,indicadorDeColumnaDeValor,FALSO(coincidenciaExacta))

|Gerente | Ventas|
|-----|-----|
|Juan     |+BUSCARV(celdaIzquierda,rangoTabla,columnaValor,falso)|

De tal forma si cambia el nombre del gerente se muestra el valor.

SI.ERROR -> Forma de mostrar un error -> +SI.ERROR(valorOK,valorError)

+SI.ERROR(fórmulaBuscarV,"") // Las comillas dejarán la celda vacía.

# Ahora ¿qué es BuscarH?

BuscarV es buscar vertical y BuscarH es buscar horizontal.

BuscarV -> Indicador es columnans.
BuscarH -> Indicador es filas.

# Practica el BuscarH

Se utiliza de forma similar a BuscarV pero diferenciando en que se usan filas en vez de columnas.

Combinamos BuscarV con BuscarH para poder modificar dos indicadores. El BuscarV se utiliza para el obtener el indicador.

|   |Enero|Febrero|Marzo|  |
|---|-----|--------|----|--|
|Ventas  |#|#|#|2|
|Costos  |#|#|#|3|
|Utilidad|#|#|#|4|

|Gerente|Item(Ventas, Costos, Utilidad)|
|-------|------|
|Mes    |celdaBuscar|

+BUSCARH(celdaMes,rangoMesesYValores,BUSCARV(item,rangoGerenteANumerosSinMeses,columnaNumeros,falso),falso)


Enlazando el BuscarV con el BuscarH podemos tener una fórmula muy interesante para buscar en toda la matriz.

# Fórmulas condicionales ¿qué son?

Es lo mismo que una sentencia condicional if/else

+SI(condición,Si-Si,Si-No)

+SI(C5="J","Platzi","Rojo")

Excel va a leer las fórmulas de izquierda a derecha.

+SI(C18=2,"Platzi",SI(C18="K","Platzi", "Rojo"))

Se pueden manejar ">" en Excel.

# Fórmulas condicionales indispensables

> Para expandir varias columnas cuyo contenido sobresale de la celda. Seleccionar todas y dar doble clic en el límite de cada una de ellas. 

> Para excel el != es <>

# Formatos condicionales

Esto es para darle color a las celdas en base a una condición.

En inicio -> formato condicional -> Resaltar reglas que... // Aparecen múltiples opciones.

También hay la opción de barras.

Para hacer una regla en todo un rango para un valor límite, usar -> Reglas superiores e inferiores.

# Semáforos, celdas de colores y formulación

Detrás de la celda de un semáforo hay un valor, lo que hacemos es condicionar la celda para que muestre un color tipo semáforo.

Las celdas con comentarios aparecen un triángulo rojo en la esquina superior derecha.

> Crecimiento porcentual=(valorFinal-valorInicial)/valorInicial

Para agregar una flecha al lado del número.

Formato condicional -> Nueva Regla -> Aplicar formato a todas la celdas según sus valores -> Íconos // Seleccionamos el ícono y configuramos los parámetros.

Con la opción "Utilice una fórmula que determine las celdas para aplicar formato" se puede especificar la fórmula dentro de cuadrante.

# Tablas dinámicas

- Permite agilizar movimientos
- Ayuda a manejar grandes volúmenes de datos
- Utiliza información general a datos que interesan utilizar

Debemos tener seleccionada toda la tabla, incluyendo los items.

Insertar -> Tabla dinámica 

Arrastaramos los títulos según correspondan. Ya sea que si queramos filas, columnas, valores o filtros.

Para modificar la forma como se procesan los valores (por defecto es sumar) -> Configuración de campo de valor -> Allí seleccionamos el campo de valor.

> En las tablas dinámicas no es tan sencillo formular, de ser necesario, copimos y pegamos solo los datos.

# Tipos de gráficas y sus diferentes usos

Podemos cambiar la orientación de los ejes, en el botón "Cambiar entre filas y columnas".

En la gráficas de torta se utiliza los porcentajes.

En las gráficas de líneas, podemos deschecar ciertos items y modificar otros para que en vez de que aparezcan números se indique el valor del item.

# Gráficas sencillas

> Este más fácil y sencillo muestre las gráficas mejor es. En gráficas las personas se fijarán más en aquello que es más grande y con color que resalta.

# Gráficas dinámicas

- Permite agilizar procedimientos
- Iterar posibiliades para encontrar patrones

Se hace como las tablas dinámicas con la diferencia que se actualizará un gráfico.

Seleccionamos toda la tabla -> Insertar -> Gráfico dinámico

Cuando agregamos más filas, para configurar la prioridad de uno de los ejes de la gráfica dinámica (si/no) sencillamente modificamos el orden de las filas.

# Formulación con tablas dinámicas

Es posible formular con tablas dinámicas.

Lo que hacemos es crear celdas inteligentes con listas desplegables reemplazando la fórmula de la tabla dinámica por el de una celda. Ejeplo "Colombia", "Sector construcción".

En pocas palabras, editamos la fórmula de la tabla dinámica.

# Buscar objetivo

En inglés es Goal Seek.

Es un proceso iterativo.

Datos -> Análisis de hipótesis -> Buscar objetivo

Definimos la celda resultado, el valor objetivo, la celda que se va a cambiar.

Hay un truco para resolver problemas con números grandes.

Aquí hay un reto interesante.

# Macros: Escribiendo y entendiendo código

Las Macros se pueden hacer de dos formas:
- Escribiendo código
- Grabando la macro y modificando código

En windows presionar **Alt+F11** para abrir Visual Basic.

Sub nombreMacro() // Abre macro
End Sub // Finaliza Macro

F8 permite ejecutar la Macro paso por paso, con Play las lee toda.

Para setear una celda -> ActiveCell.value = 2

Workseets("Hoja2").Activate // Entrar en la "Hoja2"
ActivateSheet.Range("d5").Value = "Hoja que tal?" // En la hoja activa, en la celda "d5" ingrese un valor igual a "Hola qu tal?"
ActivateSheet.Range("d5").Font.Bold = True // En la hoja que está activa, en la celda "d5" usar negritas.
ActivateSheet.Range("d5").Font.Color = RGB(255,0,0) // En la celda "d5" utilizar el color RGB asignado

// Otra forma de escribir el código
With ActivateSheet.Range("a7")
.Value = "Pepe"
.Font.Bold = True
.Font.Color = RGB(0,255,0)
End With

# Macros: Grabando macros

Si no está habilitada la pestaña de desarrollador -> Clic derecho en la barra -> Personalizar la cinta de opciones -> Check opción de desarrollador

Para grabar una macro -> Desarrollador -> Grabar una macro // A partir de aquí va a ser grabado

La grabación se detiene en un botón que está en la parte inferior izquierda.

> Es buena idea grabar una macro y luego modificarla.

Para insertar botones -> Desarrollador -> Insertar -> Botón -> Asignar a una macro.

También podemos insertar formas al que le podemos asignar una macro.

Haciendo clic contrario a botones podemos asignar una macro.

Con un botón con Scroll horizontal podemos modificar un valor y con una macro asignada se puede utilizar buscar objetivo cada vez que se mueva el botón.

# Conclusiones

Equivocarse, encontrando errores, corregirlos y practicando mucho es la única forma de aprender.
