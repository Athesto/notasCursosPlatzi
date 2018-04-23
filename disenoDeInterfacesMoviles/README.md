# Notas de curso de Diseño de interfaces móviles

# Mobile hoy en día

Las interfaces son distintas en iOS y Android.

La navegacición en Android es superior y presencia de float button en la parte inferior.

El entorno de uso (carro,caminando, oficina).

> La atención del usuario no es mucha.

Tomar en cuenta que los usuarios usan el tlf con una mano y a la distancia normal con el teléfono.

# Diseñando de interfaces para móviles

Las dos plataformas más comunies son iOS y Android.

Vamos a diseñar un producto que con el tiempo va a ir creciendo, es decir escalable.

Entrar a la documentación para Material Design para Android, y el otro de iOS. Tomar en cuenta siempre el  flujo de las aplicaciones que usamos en nuestros dispositivos. Siempre pensando en secuencia de pasos.

Cuando estamos diseñando el producto debemos tener una uniformidad con los patrones de las plicaciones.

# Anatomía

Son propias de cada sistema. Que sería lo mismo para windows, Linux, iOS, etc.

En Twitter, la versión movil omite muchas cosas respecto a su versión Desktop.

Cuando estamos diseñando la versión móvil tratar de hacer lo más cercano a la versión Desktop.

> Pensar siempre en términos de componentes y pensar en lo que lo componen.

**Wireframe**: Pantallazos en boceto. Incluyendo la navegación. Tomar en cuenta las tarjetas (card) y cómo están compuestas. Con elementos no tan intrusivos.

# Interacciones

Esto son los gestos en iOS:
- Scroll
- Tap (pulsar)
- Force Touch (gesto al mantener pulsado)
- En fotos: 1 tap mira una foto, otro tap elimina el marco, 2 tap amplía la imagen.
- Zoom con dos dedos -> Pinch
- Swipe vertical hacia abajo o arriba, cierra la foto y más herramientas.
- Swipe horizontal cambia de foto

Gestos en Android:
- Swipe horizontal (en Android)
- Bar navigation de izquierda a derecha. Desde el borde izquiero o desde el home.
- Al hacer scroll hacia abajo solo deja visto las herramientas de los tap.
- Scroll hacia abajo para refresh. (Pull refresh)

# Bases

> Muchas veces vamos a recibir una App que viene desde desktop.

Dividir la pantalla en Desktop en 3 (segun sus funciones) y de ello tomar una pantalla. Éste será el telefóno.

Prioririzar las funciones en la aplicación, logrando un foco.

> No sirve tomar un texto en Desktop achicarlo para introducirlo en el telófono.

Vídeo se corta faltando 1 minuto.

# Cards

> Debemos definir cómo se va a mostrar las informaciones y una manera de mostrarlo es con cards (tarjetas).

Para representar bien la interfaz, debemos definir qué información presentar. Para ello debemos priorizar.

Un consejo para priorizar es clasificar. Definiendo las acciones que más interesan mostrar a los usuarios.

No hay una manera correcta de hacerlo, lo que debemos tener en cuenta son el usuario para que la estamos diseñando, casos de uso y las funcionalidades principales.

Debemos tener en cuenta una interfaz que va a escalar.

Las posibilidades son infinitas, solo debemos tener en cuenta cómo va a convivir con el resto.

# Presentar información

> Cuando definimos una card no necsariamente debemos usar un único diseño para el resto de las interfaces. Por ejemplo, en twitter, los trending topics.

La decisión de qué mostrar siempre va a establecerse según el usuario final.

Recursos:
- Carrusel: Es una menera de representar un trozo de una información más grande con swipe horizontal con unos indicadores en la parte inferior (como unos puntos) para representar la cantidad de información.
- Arcondeón: Son como las listas que se despliegan. Para mostrar más contenido, pero tener en cuenta que no debemos tapar otras funciones.
- Listados: Podemos usar también un listado como los Trending Topics con la opción de "Ver más". Debemos diseñar de tal forma que el usuario pueda consumir mucho mejor.

> Tomar en cuenta la estructura de las columnas, lo que dejamos a la derecha y en pequeño tiene menos importancia.

- Hero: Así se llama cuando desparace una parte de la barra de navegación al hacer Scroll.

Debemos buscar una manera para indicarle a usuario que el item es interactivo como una ícono para indicar una acción cliqueable.

# Acciones

> Una aplicación es un conjunto de pantallas conectadas entre sí de un punto A a un punto B.

- Estado de autocompletar: Si podemos anticiparnos a lo que va a ocurrir podemos dar un mejor resultado.
- El flujo de búsqueda no tiene por qué ser el fin, permitiendo entre los resultados de búsquedas filtrar por fecha, fotos, personas, vídeos, etc.
- Mostrar representar acciones, ejemplo cuando entramos en el perfil de alguien por la app movil de Twitter. Distribuyendo las acciones en un nivel vertial, para que el usuario no se pregunte "qué acción deberé estar usando?" 
- Debemos definir qué es lo importante. Para ello jugamos con los colores, opciones fijas (como el float button de publicar un tweet), tamaños. Al hacer Scroll, ocultar una información y mostrar otras como las barra de navegación.

Entender las acciones disponibles y las acciones que queramos de los usuarios. Diseñamos las interfaces.

# Onbording

Es cuando el usuario está entrando por primera vez y no tiene contenido.

Ejemplo:
- Contarnos una historia de screenshot en el uso de la App. Con slice, no más de 3 y lo más concretas.
- Tour virtual por algunas secciones específicias de la aplicación. Que no tienen sentido agregarlo el slide, debe ser simple, fácil de consumir y lo menos intrusivo.

> Tenemos que priorizar a que el usuario tenga la mejor experiencia posible.

# Otros lineamientos

Es importante que durante todos los procesos de diseño debemos estar en contacto con los desarrolladores, porque ellos van decir "esto se puede y esto no"

Lo van a decir si se puede o no en base al tiempo, posible es todo lo que limita es el tiempo disponible para el desarrollo.

Tener en cuenta las opciones nativas del sistema, como ejemplo alerts.

Si tenemos una interfaz de búsqueda y no haya resultado, en vez de solo mostrar el mensaje introducir un "Call to Action" para sacarlo de allí y pensar qué lo trajo allí para incorporar otras acciones.

Cada vez que estamos consultando información a servidores debemos mostrarle a los usuarios que es algo casi automático. Definir entonces qué mostrar al usuario mientras se espera. Facebook tiene el estado de "Wireframe" de "mira estoy cargando, espera un momento".

Es importante leer material design ya que allí tendremos los recursos para el desarrollo de interfaces.

# Platzitinerarie

> Un tip para nosotros: Nosotros no contamos como usuarios, debemos pensar siempre que va a ser para el resto. Entonces cómo saber si algo va a ser útil debemos utilizar encuestas.

Utilizar el mismo Research al momento de diseñar interfaces para Desktop.

Definimos el usuario, plasmar todos lo pasos que va a tomar para cumplir su objetivo.

Debemos diseñar en base a un MVP.

Debemos diseñar una secuencia de pasos lo más barata posible con sus respectivos wireframe, pero empezar en papel.

Luego del papel diseñarlo en digital.

Si empezamos primero la interfaz mobile, debemos seguir los pasos:
- Definir bien el producto con sus feature.
- Tener en cuenta los distintos usuarios del producto.
- Pensar en casos de uso
- Pensar en proto-persona
- Empezar por las secuencias de pasos
- Empezar por wireframe
- Terminar en la computadora

Pensar:
- Mobile web
- Android
- iOS

# Anatomía de web mobile

- Debemos tener en cuenta las proporciones de pantalla propio de cada sistema operativo
- Tomar en cuenta los gestos. No tenemos Hover (poner mouse encima).
- Hay sitios que nos van a permitir hacer zoom. Pero tomar en cuenta la perspectiva.
- Esta adaptación puede ser mecánica, preferiblemente. Haciendo adaptación sin tomar en cuenta los flujos. Pero sí tomar en cuenta la información a mostrar.
- Tomar en cuenta la velocidad de internet.

# Bocetos en papel para web mobile

- Tomar en cuenta los marcos.
- A diferencia de una aplicación nativa no vamos a usar navegación por swipe.
- Usar la menor cantidad de imágenes.
- Cuestionarse durante el diseño de la interfaz la incorporación de funciones para en caso necesario omitirlo o bien colocarlo en otra parte.
- Pensemos en cómo ahorrar pasos al usuario
- Tomar en cuenta el espacio del teclado que aparecerá al ingresar un texto.
- Para este tipo de interfaz el profesor seañala que debe ser lo más rápido.

---

# Anatomía en Android

Material Design no está destinado solo a Android.

Tiene una documentación muy extensiva. Leer esto lo más que pueda para el diseño de interfaces móviles.

Fijarse mucho en la parte de componentes, donde muestra cada elemento como lo que es.

El Floating Action Button -> Se usan para acciones muy importantes. Pero si no está bien diseñado puede pasar desapercibido

Permitir la navegación por gestos horizontales

También contamos con patrones de navegación.

El profesor prefiere usar a navegación arriba para dejar espacio al navigation de Android y al float action button

Hay diseño de listas.

> Roben, robar no es malo en este caso (patrones de diseño). Si ustedes creen que una aplicación está resolviendo en diseño un problema mucho mejor.

Leerse la mayor parte de la guía de material design.

# Bocetos en papel para Android

> El profesor usa como un sello de un teléfono para tomar en cuenta las proporciones.

En la sección de components es donde el profesor toma las guías para el diseño de la interfaz. Allí también tenemos los colores y proporciones.

Structure -> Estructuras.

> Todo lo que necesitamos en material design lo vamos a encontrar, debemos buscar bien.

Plantear la tendencia de que cuando queramos crear algo ubicarlo a la derecha.

En Android siempre poner el título de dónde estamos

Los detalles se van a sentir cuando respetemos detalles, formas, colores, posiciones, etc.

# Expandiendo sistema de diseño para Android

Uno de los objetivos debe ser un diseño lo más unificado que se pueda.

Mucho blanco = Mucho Aire

Si venimos de un Desktop se hacen más sencillo tomar algunas decisiones.

[Iconos de Material Design](https://material.io/icons)

En Sketch podemos iniciar un template de material design.

Con Crystal podemos ver pantallazos creados en Sketch

El onboart el profesor lo resolvión con un ícono de avión y un call to action "¿Con ganas de viajar?:Planificar tu viaje..."

En Android los márgenes se hacen en base a 8px, por los lados 16px y superior 8px.

En Material Design hay también los espaciados.

Jamás olvidar chequear material design.

# Funcionamiento

Notificaciones: Son el aspecto menos tenido en cuanto a diseñar una aplicación pero es una de las partes más importantes para crear engagement. ¡Cuidado! Puede resultar intrusivo. Deben hacerse en el momento justo.

Definir las acciones e interacciones con las notificaciones. Pero hacerlo muy limitado.

Ya las plataformas saben el momento correcto para mostrar notificaciones donde tendemos a cliclear sobre ellos.

# Notificación de nuestra app

Una forma de saber las notificaciones a crear es repasando todo el flujo de pasos en los wireframe.

Plantear las posibles notificaciones por wireframe.

Tomar en cuenta las notificaciones de acciones por personas y también las del sistema.

"Hace mucho que no agregas una ciudad" o "tal amigo tiene tiempo que no publica"

Invitar que un usuario motive a otro.

Definir también en las acciones por cada notificación.

> Cuando es bien tenido en cuenta hace que la experiencia sea mucho mejor. Hacerlo para todo lo que queramos desarrollar.

# Prototipos en Sketch

La última versión de Sketch permite a opción de crear prototipos muy reales. Con la conexiones entre las pantallas. Generando una interacción cercana a la realidad.

# UI kit

Es una especie de plantilla que agrupará todas las plantillas. Esto debe ser generado para cada plataforma por separado.
