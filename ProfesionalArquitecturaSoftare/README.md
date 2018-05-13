# Notas del curso profesional de arquitectura de software

# Defición

**Atributos de calidad**
"Los atributos de calidad son expectativas de usuario, en general implícitas, de cuán bien funcionará un producto". Por ejemplo, rendimiento y seguridad de la aplicación.

# Atributos: Idoneidad funcional

Es lo que conecta al usuario de las necesidades del usuario con las funcionabilidades de la aplicación.

- Completitud funcional: De cuán está completa las funciones respecto a lo que se espera del sistema. Requerimietos funcionales vs funcionales implementadas.
  - Por ejemplo que necesitemos implementar login de redes sociales, podríamos hacerlo incrementalmente.
- Exactitud funcional: Lo preciso de la implementación funcional. Resultado esperado vs resultado obtenido.
  - De esto saber si se ha tenido un éxito o un fracaso.
- Pertinencia funcional: Cuán alineado está lo que se implementó con lo que se necesita. Objetivos cumplidos vs objetivos esperados.
  - Las aplicaciones suelen ser muy buenas al principio. Pero en la medida que avance la aplicación esto será segmentado.

# Atributos: Eficiencia de ejecución

Trata de cuán bueno es la aplicación al momento de responder lo que el usuario necesita. Y saber cómo aprovecha los recursos disponibles.

- Tiempo a comportamiento: Tiempo transcurrido entre pedido y respuesta vs tiempo esperado o tiempo máximo tolerado.
- Uso de recursos: Consumo de recursos vs consumo esperado o tolerado de recursos. Ejemplo: RAM, CPU.
- Capacidad: Límite de tolerancia detectado y límite de tolerancia esperado. Esto es la cantidad de tiempo en responder. En esto se utilizan las métricas! Debemos estar preparado para esos momentos en que el sistema va a estar exigido.

# Atributos: Compatibilidad

Trata de cuán el sistema es compatible con otro. Es decir en vivir en un contexto más grande.

- Interoperabilidad: Cuán fácil es comunicarse con este sistema.
  - Implementación de estándares y disponibilidad de esquemmas: HATEOAS (analizar una API de un sistema), SOAP, Open API, JSON Schema. Todo esto trata de cómo comunicarse con el sistema de forma programática.
- Coexistencia: Cuánto el sistema soporta o no estar en un contexto con otro sistema. Es decir en otro servidor.
  - Cantidad de fallos por razones externas en un tiempo dado. En un contexto dado, que una aplicación externa hace que falle nuestra aplicación. Ejemplo API públicas. Ejemplo transacciones.

# Atributos: Usabilidad

- Reconocimiento de idoneidad: Cuánto nos damos cuenta es lo que nosostros necesitamos usar para resolveer un problema. Relación entre conceptos de dominio y acciones de sistema. Ejemplo: Compra, carrito de compra para asociar la acción a una compra.
- Curva de aprendizaje: Cuán fácil o difícil es aprender a usar el sistema. Cuanto más intuitivo  sea el sistema más fácil será usarlo.
- Operabilidad: Cantidad de pasos hasta lograr los objetivos. Métricas de conversión.
- Protección a errores: Cantidad de intentos fallidos e intentos totales de interacción: Esto viene del feedback de los usuarios.
- Estética de interfaz: Es muy abstracto, podemos hacer encuesta de apreciación de estética de nuestros usuarios.
- Accesibilidad: Adhesión a estándares, para ser usado por personas con discapacidades.

Ejemplos:
- Reconocimiento de idoneidad: Cuando estamos haciendo uso de un sistema que no está hecho para tal. Ejemplo los CM como WordPress que está hecho para hacer blogs pero tiende a ser complicado agregar funcionabilidades para que haga lo que queramos que haga. El dominio de la aplicación originalmente se distanción mucho del uso actual.
- Curva de aprendizaje: Aprovechar diseños ya establecidos para que intuitivamente el usuario tenga una curva de aprendizaje ligera.
- Operabilidad: Intentar ahorrar pasos.
- Protección a errores: Maneras rápidas de decirle a usuario que se equivocó y cómo corregirlo. Como por ejemplo que no se haya ejecutado un pago. De la forma más amable posible porque nos interesa que complete ese paso. Ejemplo: Que haya ingresado mal su tajeta.
- Estética de la interfaz: Esto trata de UX y UI. Todo dependerá del usuario final. Aprovechar gestos ya definidos. Para que el usuario no necesite buscar documentación ni el botón de ayuda.
- Accesibilidad: Por ejemplo imágenes con texto, para ello usar **alt** de las imágenes. Puede ser con los usuarios con discapacidades visuales, o bien no usar html semántico.
- Estética de interfaz: Esto es cuando hablamos de UI/UX. Más que otorgar una experiencia de usuario, definir la interfaz para el cliente ideal. Y entender la relación de UI y UX.

# Atributos: Confiabilidad

Saber cuánto tiempo el sistema nos permite usarlo de forma normal.

- Madurez: Errores del sistema. Cuanto menos falle más maduro. Se mide con el tiempo medio entre averías. "Cuanto más tiempo pase más maduro es el sistema".
- Disponibilidad: Es la cantidad de tiempo que el sistema está fuera de servicio en su ciclo normal. Medimos el tiempo fuera de servicio en forma de porcentaje. En un mes o semana. Hay contratos entre empresas que garantizan un porcentaje de disponibilidad alto.
- Tolerancia a fallos o resiliencia: Es por cuánto un sistema puede seguir sirviendo el servicio a pesar del fallo. Para medirlos generamos el fallos y vemos cómo se comporta el sistema. Netflix crearon **Chaos testing**.
- Capacidad de recuperación: Cuánto el sistema puede estar disponible luego de un fallo. Es importante medirlo cuando detectamos un fallo y cuando lo quitamos intencionalmente.

> Los sistemas más maduros, normalmente son los sistemas bancarios. En el caso de la tolerancia a fallo, el ejemplo más claro son las aplicaciones móviles que tienen que poder funcionar en offline. La capacidad de recuperación, el mejor ejemplo son las aplicaciones distribuidas en el que se utiliza docker y orquestación de contenedores.

# Atributos: Seguridad

De cuánto el sistema protege, identifica y valida al usuario. Esto trata de conectar al usuario con la información.

- Confidencialidad: Trata en conectar al usuario con lo que puede o no acceder. Es decir en cómo el sistema autoriza a ciertos usuarios a acceder a cierto tipo de información.
- Integridad: Cuánto el sistema toma recaudos para proteger esa información de atacantes o usuarios que no deberían tener accesos a ellos.
- Comprobación de hechos: Trata en la parte legal. En qué pasos siguió el usuario para llegar a ese estado.
- Traza de responsabilidad: Conectar a lo que hizo el usuario con el sistema que lo hizo, es decir, conectar la acción con su responsable.
- Autenticidad: En cómo el sistema logra identificar al usuario. Qué pasos toma para que la persona que está usando el sistema es quien dice ser.

Confidencialidad: Redes sociales.
Integridad: Bancos y hospitales.
Comprobación de hechos: Firmas digitales. En cómo fue lo que pasó.
Traza de responsabilidad: Los logs de auditorías. Saber qué pasó y quién lo hizo.
Autenticidad: Aplicaciones web y móviles. Como Email, contraseña, biométricos, etc.

Confidencialidad: Redes sociales.
Integridad: Bancos y hospitales.
Comprobación de hechos: Firmas digitales. En cómo fue lo que pasó.
Traza de responsabilidad: Los logs de auditorías. Saber qué pasó y quién lo hizo.
Autenticidad: Aplicaciones web y móviles. Como Email, contraseña, biométricos, etc.

La técnica para medir la seguridad de aplicaciones es con Penetration testing.

# Atributos: Mantenibilidad

Todas las cosas del sistemas que puedan cambiar, ser reparados, etc.

- Modularidad: Capacidad de un sistema en ser separado en partes. Donde cada una de esas partes es independiente de las otras. Muy importante para un sistema mantenible y en diferentes equipos.
- Reusabilidad: Cuánto podemos aprovechar el esfuerzo de un módulo en otra parte. Ejemplo open source usables en diferentes contextos.
- Capadidad de análisis: De cuánto podemos entender el problema que estamos resolviendo y resolver ese problema a la implementación del código. Cuánto una funcionalidad afecta a uno o más módulos. Conexión entre código y requerimientos. Ejemplo: Jetkins.
- Capacidad de modificación: Cuán fácil o difícil es ir al código y cmbiar el comportamiento. Cómo saber si una modificación afecta una funconalidad. Para ello usamos test automatizados.
- Capacidad de prueba: Cuán fácil o difícil es crear estos test para que el sistema haga lo que queremos que haga. Tenemos que darle más importancia a nuestra estructura de código y cuán independientes unas de otras. Diseñar funciones que solo se afecten a sí mismas y a nadie más.

> Un error muy común es usar la fecha actual como test de pruebas, ya que es más difícil la mantenibilidad.

Es muy importante dar espacio a los test. Cuando hacemos mucho código sin test la mantenibilidad se ve afectada.

Una herramienta son análisis estático de código -> No lo ejecutan sino que leen el código.

# Atributos: Portabilidad

- Adaptabilidad: Cantidad de dependencias a entornos específicos. Ejemplo del tipo de sistema operativo destinado.
- Capacidad de instalación: Cuán fuertemente tenemos los requerimientos del entorno en el despliegue, es decir, cuando tenemos que poner el servicio de nuestra aplicación cuántos pasos tenemos que hacer. ¿Se puede reproducir en otro contexto? Ejemplo los App Store.
- Capacidad de reemplazo: Cuántos son los requerimientos que cumplen con los sistemas actuales y cómo éstos pueden ser reemplazados en un futuro. Ejemplo: Un sistema muy grande para un monolítico es más difícil hacer cambios que aplicaciones distribuidas.

# Tensiones entre atributos

Sistemas cliente-servidor en tres capas.

Clientes (Movil, web y android)
\/
Sistema: Backend
\/
Base de datos


El problema vendrá cuando implementemos seguridad en el sistema ya que hará más complicada la comunicación con los clientes y la base de datos.

Cuando se tienen aplicaciones modularizadas es más complicado levantar el servicio que una ya completa.

Implementar tolerancia a fallos, implica un aumento en el tiempo de respuesta y resilencia.

Una linterna que parece una cámara -> Perdió reconocimiento de la funcionalidad: Esto demuestras que algunos sistemas se preocupan tanto por la estética y perder la idioneidad funcional (cuánto se puede reconocer lo que hace el sistema en la medida que estamos utilizando).

En el software afecta el darle una prioridad a un producto que a otro.

# Analizando PlatziServicios

Proyecto: Arquitectura y la máquina del tiempo.

Atributos de calidad de stand-up:

- Confiabilidad (madureez, disponibilidad): Como cliente necesito contactar un profesional en el momento para reparar un problema en mi hogar. **Un sistema estable que no tenga una tasa de error muy alta**.
- Seguridad (Autenticidad, confiabilidad): Un profesional llegó a la puerta de mi casa y no puedo confirmar que sea quien dice que es. **Reconocer las credenciales del profesional y que nadie va a tener la credencial de su casa**.
- Compatibilidad (Interoperabilidad): Como profesional necesito cobrar mi trabajo realizado para continuar prestando el servicio. Registr de impuests del profesional. Garantía de profesionales sin antecedentes penales. **Es cómo nuestro sistema se comunicará con otros tales como pasarelas de pago, sistema de policía o fiscal**

> Atributos de calidad en crecimiento. Podemos agregar atributos de calidad sin perder la compatibilidad con otros.

- Eficiencia de ejecución (Uso de recursos, capacidad, reportes): Como empresa cliente necesito reportes de gastos en servicios para controlar y entnder mis finanzas. Como empresa prestadora necesito medir el rendimiento de mis profesionales para comprender mi propio crecimiento.
- Compatibilidad (interoperabilidad): Las empresas cliente no pueden extraer la información del sistema para integrar en sus aplicaciones **Que otros sistemas ahora se comuniquen con nosotros**.
- Seguridad (Comprobación de hechos, traza responsabilidad, confidencialidad): El proyecto podría recibir juicios de fraude por cobros injustificados. Garantizar la privacidad de los datos de consumo.

> Atributos de calidad a **Gran escala** -> Internacionalización del sistema.

- Usabilidad (Accesibilidad, Reconocimiento de idoneidad, Operabilidad): Como cliente necesito entender el sistema en mi idioma para poder garantizar el buen uso del mismo. Evitar procesos acoplados a un huso horario específicos. Al ampliar las funcionalidades del sistema siempre tenemos que mostrar lo que hace el sistema de forma coherente.
- Mantenibilidad (Modularidad, Capacidad de prueba, Capacidad de modificación): El crecimiento de la compañía hace difícil la transmisión de conocimiento y a productividad de nuestros equipos de desarrollo. **Cuanto más seamos, más tenemos que tener capacidad de prueba para garantizar de que ningún cambio rompa funcionalidades anteriores**
- Confiabilidad (Tolerancia a fallos, Capacidad de recuperación): Pérdida parcial o total de datos por fallas no previstas. **Demostrar que no perdemos ni parcial ni totalmente los datos de nuestros clientes**

# Patrones: Monolíticos vs Distribuidos

Los monolíticos se despiegan con una misma unidad.
Distribuidos -> Cada módulo se despliega de forma independiente. Donde cada uno es uno monolítico.

**Gran Bola de Lodo/Big Ball of Mud** -> Cuando no hay una arquitectura definitiva, cuando no se toma los criterios de arquitectura y es todo un caos. Para solucionarlo, hay que modularizar.

Cuando las empresas triunfan teniendo una bola de nieve, tienen que ivertir mucho dinero en modularizar para ofrecer un mejor servicio.

# Patrones: Modelo Vista Controlador

Separa a nuestra aplicación en la vista, el modelo y el controlador (acciones del usuario). Tenemos que hacer que la vista cambie sin que el modelo lo haga y que el usuario tenga la misma vista.

Lo importante de esto es separar, estas tres responsabilidades.

El punto es separar la vista del modelo y las acciones del usuario.

- Modelo vista modelo-de-vista / Model View ViewModel -> Se ve mucho en aplicaciones C# y .Net.
- Modelo Vista Presentador / Model View Presenter -> Hay un coordinador de la vista.
- Flux / Flux -> Es una separación entre las acciones del usuario, el modelo y las vistas representadas por el componente de react.

Ejemplo modelo vista controlador en web:
- El usuario accede con una url al router.
- El router toma la acción del usuario y lo pasa al controler.
- El controler lo entrega al modelo quien tiene acceso a una base de datos y le responde al controlador y éste le responde a la vista.

Hay variaciones del modelo MVC tiene muchas variantes entre las comunicaciones.

# Patrones: Capas

Nos plantea una separación en capas donde cada una va a ser responsable de cierto concepto de la aplicación.

Ejemplo:
Aplicación -> Controler 
Dominio -> Service -> Entity
Datos -> Repository

De esta forma, el repository no necesita saber del usuario que está consumiendo el controler ni del dominio mismo. Sino que va a encargarse del acceso a datos.

La comunicación debe ir de arriba hacia abajo.

Con esta arquitectura tiene muchas facilidades de mantenibilidad.

# Patrones: Orientado a eventos / Event-Driven

Trata de conectar entre componentes a través de eventos con su bus de eventos.

Todos los eventos están suscritos a un bus de eventos que reacciona al evento dentro del bus de eventos.

Se utiliza en aplicaciones orientados a servicios.

Ejemplo:
- API de ingreso de eventos: Consumidora y productora de eventos. Cada vez que le hagan un pedido de lectura va a publicar un evento de que algo se quiere escribir como un ingreso de datos que luego un módulo de ventas o clientes podría consumir.
- Procesos de importación: Está leyendo un archivo muy largo podría estar publicando en ese archivo a modo de eventos y que cada uno de los servicios vaya consumiéndolo si es que está suscrito a ese evento.
- Módulo de ventas.
- Módulo de reportes.
- Módulo de clientes.

El problema con esta arquitectura es que es un poco complejo de testear ya que debemos tener en funcionamiento todos los componentes involucrados en el bus de eventos.

Provisión de Eventos / EventSourcing: Guardar los eventos de forma secuencial en el log y de esta forma podemos saber el estado del evento. Muy bueno para encontrar fallas y secuencias de ataques. Tiene como desafíos que a medida que acumulamos eventos la lectura del log va a ser más difícil. Una solución a ello es crear vistas del estado actual, reportes, ect. Un ejemplo de ello es una secuencia de transacciones bancarias.

> Tener en cuenta que todos los patrones de arquitectura tienen ventajas y desventajas. Si conocemos los patrones podemos escoger el que mejor se adapte.

# Patrones: Microkernel - Plug-ins

Trata de tener un kernel/Core y puntos de conección llamados Plug-in. Puede verse monolítico al deplegar con todos sus plug-in o bien cambiarlos en tiempo de ejecución y verse como un tipo de aplicación distribuido.

Ejemplo son los IDE y sus Plug-in.

# Patrones: Comparte-nada / Shared-Nothing

Compartir recursos entre componentes agrega complejidad a la hora de decidir qué componente tiene disponibilidad de ese recurso.

Esta arquitectura se utiliza para no compartir nada, sin un punto de unión entre componentes. De tal forma que cada componente tenga sus datos privados o bien su propia base de datos para su funcionamiento.

Un ejemplo es el proceso de MapReduce. En el cual trabajamos con un volumen muy grande de datos y para ello lo particionamos en partes (A-I, J-O, P-Z) de forma que decidamos cómo atacar esos datos en forma agrupada y secuencial. De esta forma no necesita compartir datos entre componentes.

Es un patrón muy puntual.

# Patrones: CQRS

Separación de Responsabilidades entre Consultas y Comandos / CQRS

Separa las consultas de los comandos para diferenciar el momento en el que estamos escribiendo con el que estamos leyendo.

Con esta arquitectura podemos separar modelos de escritura y lectura con sus respectivas bases de datos.

Un caso de uso muy común es el de los reportes. Este patrón fue invitado para reportes. Otro caso de es el de los eventos.

Tienen un costo alto al tener dos modelos y dos bases de datos. Usarlo cuando estemos en un caso en el que van a brillar.

# Patrones: Hexagonal - Puertos y adaptadores

Se utiliza en una aplicación en el que ya tenga claras sus depndencias externas. Esto lo hace definiendo puertos que se comunican con la función y un adaptador http que se comunica con la vista. Es uno de los patrones usados en RestAPI, bases de datos, vistas.

Un ejemplo de ello es una app web. Este tipo de arquitectura es muy poderosa al diseñar un sistema pero a la vez muy compleja porque tenemos que tener bien claros los puntos y no salirnos de ellos.

Un error de diseño es cuando tenemos que leer un archivo de reporte y destruirlo para responderlo en JSON. Por lo que hacen muy complejos y tenemos que ser muy estricto ya que debemos saber qué hacer en cada lugar.

Es recomendable empezar usando una arquitectura simple y luego evolucionarla a una hexagonal.

# Patrones: Diseño orientado al dominio / Domain-driven design

> Lo que hacemos es guiar nuestra aplicación y diseño a través del uso del lenguaje común dentro del negocio.

Centrarse en el concepto de una venta, de un servicio, de un producto. Va más allá de una sola aplicación modularizando la app en contexto limitados que es dónde el lenguaje cambia de sentido.

Se concentra mucho en trabajar con el negocio y el lenguaje que usa. Hay mucho valor en la semántica y la manera en cómo diseñamos a la manera de cómo el negocio piensa.

Cada contexto se comunica entre sí.

Ejemplo en un eCommerce: Ventas - Usuarios - Inventario. 

# Combinando patrones de arquitectura

El cliente con arquitectura en Flux el cual se conecta con el balanceador de carga y éste se conecta a otras con un RestAPI o GraphQL que no se cumican entre sí y están conectadas aun bus de eventos.

Es una arquitectura muy usada en aplicaciones empresariales y aquellas que necesitan escalar.

Otro ejemplo, tenemos un MVC el cual se comunica a una base de datos y ésta  se conecta a otras apps monolíticas de bases de datos y modelo el cual se conecta a otra base de datos para generar lectura de ellos y hacer reportes. Aquí tenemos CQRS.

Otro ejemplo, tenemos un MVC el cual se comunica a una base de datos y ésta  se conecta a otras apps monolíticas de bases de datos y modelo el cual se conecta a otra base de datos para generar lectura de ellos y hacer reportes. Aquí tenemos CQRS.

Ejemplo de una bola de lodo. En vez de ensuciarnos en ella creamos una arquitectura hexagonal con una base de datos compartida que se comunica con la bola de lodo. Entonces el hexagono tiene para entrega en el JSON, luego con un bus de eventos persistentes nos conectamos con la bola de lodo que respalde el log en una base de datos. De esta forma podemos saber qué está pasando en la bola de lodo con el hexagono. En la bola de lodo solo creamos una conexión con el bus de eventos y la base de datos compartidas y de esta forma no nos metemos a modificar tanto el código en la bola de lodo.

# Analizando nuevamente PlatziServicios

Proyecto: Arquitectura y la máquina del tiempo

Etapa Startup:
- Empezamos con la estructura cliente servidor con el patrón MVC. Monolítico, fácil de desplegar.
- Otra opción es en capas: Monolítico, fácil de desplegar, buena abstracción del dominio (capa del negocio).

En crecimiento:
- Se tuvo la necesidad de crear reportes los cuales eran costosos. Se usa arquitectura comparte-nada para el proceso de reportes con sus bases de datos independientes. Distribuído. Buen uso de recursos. Capacidad de procesamiento paralelo. Es muy útil cuando el volumen de datos es muy grandes.
- Otra opción es basada en eventos. Donde leemos esos eventos y lo pasamos al reporte. Distribuído, buen uso de recursos, capacidad de procesamiento paralelo. 
- Otra es por microservicios: Sería ambicioso y más complejo. Si somos pocos (menos de 20 programadores) quizás mantener el monolito tiene sus ventajas. Podríamos usar microservicios de prestadores y otro de reportes.

Gran escala: Empresa global con traducciones, husos horarios, etc.
- Microservicio: En el estado anterior era ambiciosa pero ahora cobra sentido. Servicios de reportes, servicios locales y servicios globales.
- Otro provisión de eventos: Para provisión interna de reportes. Si se basa en eventos podemos tener una base de datos con los pasos por usuarios.
- Separación de consultas y comandos: Es una buena utilidad para un sistemas que necesitan servicios. Separamos la escritura y la lectura con eventos separados. Es muy buena para múltiples servicios combinadas entre sí con el bus de eventos. Monolítico, mejora la modularidad y se integra bien con la provisión de eventos.



