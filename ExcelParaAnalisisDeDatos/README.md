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

Podemos buscar y reemplazar.
