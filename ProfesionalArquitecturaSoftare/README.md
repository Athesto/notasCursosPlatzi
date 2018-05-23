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

# Conectores: Llamando asíncrono - sincrónico: Modelo Cliente Servidor

LLamado asincrónico -> Un emisor llama a un receptor pero no espera a que termine esa ejecución sino que simplemente sigue con su trabajo y en algún momento evaluará el resultado de esa ejecución.

Llamado sincróonico -> El emisor envía un mensaje al receptor y espera que éste le responda. Normalmente se utiliza hilos.

Cliente/Servidor -> Es la comunicación entre cliente servidor no trata tanto de asíncrono o síncrono sino de la forma en la que va a estar distribuido nuestros componentes que no necesariamente deben convivir en el mismo sistema.

# Conecores: Enrutador, difusor

Enrutador -> Facilita la conexión entre un componente que emite un mensaje y un set de componentes que le interese ese mensaje.

Difusión -> Dado un mensaje lo difunde a múltiples componentes interesados.

Ejemplo: Twitter -> Al escribir un tweet se publica en el TimeLine y notifica a usuarios interesados del mismo modo en el TimeLine que aparece en diversos perfiles.

Entonces el detalle es si el componente es inteligente para emitir un mensaje o bien si conector es inteligente para saber a quién enviar ese mensaje.

# Conectores: Pizarra, repositorio, colas, modelo PUBSUB

Cola -> Cuando un productor que tiene mucha más velocidad que un consumidor, entonces para conectarlo necesitamos compatibilizar esa conexión. Entonces el consumidor irá leyendo en la medida que su velocidad se lo permita. Ejemplo: Un fichero en memoria y luego tenemos que comunicar algo.

Repositorio/Pizarra -> Es un conector que está orientado a escribir o leer datos de un componente que funciona como bases de datos con su lectura y escritura. Un ejemplo de ello son los driver de las bases de datos relacionales garantizándonos que la transacción va a ser atómica.

Publicar/Suscribir -> Manda mensajes desde un componente que publica eventos en un bus a otro que se suscriba en un bus de eventos sin que necesariamente se comunican entre sí. Este conector es súper importante en aplicaciones o servicios distribuidos que no les interesan la fuente de los mismos.

# Escenarios y tácticas

Escenario: Atributo de calidad X

Estímulo -> Táctica para controlar la respuesta -> Respuesta

# Escenarios: Disponibilidad, detección, reparación, reintroducción y prevención.

Siguiendo el mismo esquema anterior

Falla (estímulo) -> Tácticas para controlar la disponibilidad -> Falla ocultada o sistema reparado.

Disponibilidad:
- Detección: Detectar si perdimos disponibilidad o detectar si hubo alguna actividad que está sucediendo en nuestro sistema que está comprometiendo nuestra disponibilidad.
  - Ping/Eco: Cómo un componente manda un mensaje genérico para saber si el componente está disponible o no.
  - Latido: Un componente emite un mensaje periódicamente para dar señales de que está disponible, por lo cual si no tenemos ese mensaje en una cierta cantidad de tiempo sabremos que no está disponible. Es muy típico en apps que no tiene interfáz gráfica como notificaiones push.
  - Excepciones: Nos ayuda a darnos cuenta de cúando estuvo comprometida la disponibilidad y por qué.

- Recuperación Preparar/Reparar: Cómo saber si estar listo para que cuando la falla ocurra repararla lo más rápido posible. Ya sea que el problema lo repare un operador o pueda repararse solo.
  - Votación: Tenemos múltiples componentes con la misma funcionalidad que podemos reemplazar uno u otro componente de forma arbitraria que no responda igual que el resto.
  - Redundancia activa: Garantiza que todos los mensajes de entrada llegue a todos los componentes del cluster. De tal forma que vuelva estar disponible en cuestión de milisegundos. Teniendo un componente líder que al caer vendrá otro que lo reemplace.
  - Redundancia pasiva: La comunicación se hace a un componente y éste se encarga de sincronizar a otros componentes que están de forma pasivas a estos cambios. Muy usada en una base de datos líder y otra seguidora.
  - Repuesto: Cuando algo falle, tendremos una arquitectura en el caso de que la principal se cae. Se requiere inicializar.

- Recuperación: Reintroducción -> Cómo hacer que con una falla de disponibilidad vuelva a estar disponible.
  - Modo sombra: Un component empieza a fallar lo quitamos del cluster productivo, lo reparamos y volvemos a introducir.
  - Sincronizaciónn de Estado: El componente no se comporta correctamente, entonces lo quitamos y lo reemplazamos.
  - Punto de control/Retroceso: Marcar estados de la aplicación en un estado en el que sabemos que esta en un estado consistente. Revisando los logs podemos saber qué correcciones aplicar para implementar la funcionalidad.  

- Prevención: Qué podemos hacer para prevenir la falla de disponibilidad.
  - Quitar de servicio: Quitar un componente que no estaremos reparando para prevenir que genere otro problema. Ejemplo cuando sabemos que la aplicació está consumiendo memoria.
  - Transacciones: Controlar el bloque de cambios para hacerlos todos juntos o quitarlos todos juntos para evitar que no sean inconsistentees.
  - Monitoreo de procesos: Pueden ser automáticos y nos ayudan a que nuestra app siga estando disponible por más que un proceso se siga comportando de forma anómala.

# Escenarios: Mantenibilidad, prevenir efectos dominó y diferir enlace

Período de cambio (nuevo requerimiento) -> Tácticas para controlar la mantenibilidad -> Cambio hecho, probado y desplegado.

Mantenibilidad:
- Confinar modificaciones: Las tácticas van a intentar trabajar sobre nuestros módulos para que cada cambio esté confinando al módulo. De esta forma, el cambio que nos proponen no afectan a muchas partes del sistema.
  - Coherencia semántica: Relación entre las responsabilidades de los módulos. Si logramos obtener cohesión (relación entre sí) podemos hacer que ese módulo sea más mantenible, de otra forma, si no es cohesivo (no tienen tanta relación entre sí). Entonces va a ser menos mantenibles.
    - Abstraer servicios comunes: Cuando tenemos login, etc. Podemos hacerlos un servicios externos en un componente separado.
  - Generalizar: Podemos separar lo específico de lo genérico. Nos permite tener eso ya más estable. Podemos tener un sistema más estable y la mantenibilidad del sistema va a mejorar.
  - Limitar opciones: Si un cambio requiere modificar una parte del sistema y hacer que se comporte de otra forma, quizás sea radicalmente diferente que la anterior. Por lo cual podemos limitar ciertos cambios para hacerlos más mantenibles. Ejemplo que las plataformas de pago, mantener el mismo API e interfaz.
  - Anticipar cambios: Si sabemos que en próximas iteraciones van a eexistir cambios, podemos preparnos para ello. No tanto el código sino ya tener una estructura pensada. Pudiendo usando el patrón estrategia.


- Prevenir efectos dominó: Trabaja con las dependencias. Para evitar que un cambio afecte a otros módulos. Haciendo que muchas otras partes necesiten cambiar.
  - Ocultar información: Cualquier módulo tenga la capacidad de ocultar cierta parte de la información sino que su método de acceso sea a través de una interfaz. De tal forma que si el componente cambión pero no la interfaz, no se verá afectado.
  - Mantener la interfaz: Si tengo un servicio hace algo, debemos establecer una interfaz. Si la semántica cambia también es necesario cambiar el módulo como agregar un nuevo paso, ejemplo que la autenticación ya no sea por usuario y contraseña sino con OAuth.
  - Restringir comunicación: Es una cadena de conocer variables y atributos de las dependencias de las dependencias de las dependecias. Por lo cual es importante restringir ciertos atributos de los objetos. 

> Ley de Dimiter, el principio de menor conocimiento. "Para generar sistemas que estén acoplados de forma ligera, en vez de conocer las dependencias de tus dependencias siempre te limites a hablar con tus dependencias directas. De esta forma, cualquier cambio en la que tus dependencias trabajan no afecte el módulo en el que estás trabajando".

  - Intermediarios: Es un punto donde se compatibilizan un módulo con otro y cuando ya no sean compatibles se utilizan un intermediario para generar compatibilidad como los adaptadores, Pub/sub, etc. De tal forma que si algo cambia, solo sea necesario cambiar el conector.

  

- Diferir enlaces: Cómo podemos hacer para que un cambio en nuesto código no implique desplegar todo el sistema.
 - Registro de ejecución: Cuando dos servicios depende de compilación podrían separarse.
  - Archivos de configuración: Sirve para en momentos de ejecución cómo conectar diversas partes. El ejemplo más claro es la arquitectura del tipo Plug-in.
  - Polimorfismo: Podemos postergar la forma en cómo se resuelve un problema. Donde dependiendo del estado actual del objeto va a recibir una instancia específica de ese estado que se va a encargar de todo su comportamiento.
  - Reemplazo de componentes: Capacidad desplegar un componente y luego una actualización que no afecte el resto de los componentes.
  - Adherir a protocolos: Tener un protocolo claro entre dos módulos como interfaces o esquemas, puede ser tipo JSON. Que estén adheridos al mismo protocolo que no cambió por más que ellos cambiaron.


# Escenarios: Eficiencia de ejecución

Eventos -> Tácticas para controar eficiencia -> Respuesta dentro del tiempo esperado.

Eficiencia de ejecución:
- Demanda de recursos: Cuando entra un evento cómo hacemos para que ese evento tenga los recursos disponibles y cuánto de esos recursos necesita.
  - Mejorar la eficiencia computacional: Analizar los algoritmos para encontrar los puntos donde no estamos eficiente. Se encuentran las eficiencias computacionales. Un ejemplo es que no tengamos que recorrer listas de listas.
  - Reducir sobrecarga: Cuántos pasos qué acciones estamos tomando para responder un mismo evento. Si podemos predecir podemos aliviar la carga del evento.
  - Manejar tasa de eventos: Cuántos eventos vamos a emitir a un componente específico y si es necesario qué tan fino o granular. Podríamos reducir la cantidad de eventos sumándolos en uno solo en vez de varias emisiones de eventos. Ejemplo un stream de varios datos. Podríamos usar un Buffer.
  - Frecuencia de muestreo: Tiene que ver con el componente que recibe. Debemos filtrar o agrupar los eventos para ejecutarlos a la vez cada cierta cantidad de tiempo en una tarea única. Procesando una vez varios eventos. Como los reportes cada 5 minutos.

- Gestión de recursos: Cómo ponemos más o menos recursos y cómo hacer para que esten disponibles en el momento que se necesiten.
  - Concurrencia: Cómo paralelizar recursos para particionar datos. Muy utilizado en DataScience.
  - Réplicas: Cómo podemos duplicar el procesamiento o los datos para hacer más accesible los recursos. Un ejemplo de esto es guardarlo en la caché en memoria del servidor.
  - Aumentar recursos: El poder medir y saber cuánto crecer en la medida que necesitamos como el disparo de nuevas instancias.

- Arbitraje de recursos: En caso de conflictos, donde diversos componentes quieran acceder a los mismos recursos cómo decidir quién tiene más prioridad.
  - Políticas de planificación de tareas: Podemos hacerlos asíncronos en el momento o colocarlos en una cola, decidir los pedidos y cuál es el más prioritario.

> Es muy importante creer en la ingeniería que la eficiencia de ejecución es muy prioritario siempre, sin embargo, hay que tener criterio porque hay muchos atributos que se van a ver afectados por priorizar la eficiencia.

# Escenarios: Seguridad

Ataque -> Tácticas para controlar la seguridad -> Detección, resistencia o recuperación (en caso de no poder resistirlo)

Seguridad:
- Detectar ataques: Verificar que en el estado actual de la app tiene un atacante de por medio como sensores o usos de la aplicación diferente a la habitual.
  - Detectores de intrusos: Diferentes implementaciones en la aplicación como tráficos de red, secuencia de acciones, etc. Para detectar que no se está usando nuestra App de forma correcta y crear alertas que nos permitan tomar acciones. Pueden ser complejas como automatizdas  o simples como redes que se pueden conectar a nuestra App. En la medida que avancemos iremos más profundo.

- Recuperación de ataques: Diferentes tácticas para volver a un estado consistentes y saber las acciones que el usuario tomó para poder evitarlas.
  - Restauración: Toda la estrategia de disponibilidad en un estado que sabemos que es consistente y volver a él.
  - Identificación: Saber qué fue lo que hizo el atacante. Para ello tener un log de todos los pasos que han hecho los usuarios e ignorar los del atacante para volver al estado estable.

- Resistencia al ataque: Es la más compleja, va a tratar de que el atacante no tenga éxito. Es muy común en apps web.
  - Autenticación: Para saber que los usuarios es quien dice ser. Como usuario contraseña, OAuth, datos biométricos.
  - Autorización: Saber quién es la persona y qué puede hacer esa persona. Esto definido por roles.
  - Confidencialidad de datos: Cómo garantizamos que el dato lo puede ver solo quien debe verlo. Para ello encriptamos la información.
  - Integridad de datos: Que el dato sea íntegramente igual al del emisor. Tiene encriptación y hash.
  - Limitar exposición: En el que si un atacante entra por algún medio no pueda acceder a información sensible. Esto se puede hacer separando la información sensible de aquella que no es tan importante.
  - Limitar acceso: Verificar todos los vectores de acceso y limitarlos a la menor cantidad posible. Los servidores web tienen múltiples puertos como 80 y 443. Sin embargo el puerto ssh no necesariamente debe estar disponible a todos los usuarios. Podríamos usar un servidor de acceso remoto. Recuerda que en el curso de Azure vimos cómo separar la instancia de la base de datos y que ésta no tenía conección a internet sino en una red privada.

Estos son ejemplos para mejorar la seguridad. Pero es importante consultar a un experto de seguridad informática o formarse en ella cuando la seguridad es muy importante.

# Escenario: Capacidad de pruebas

Funcionalidad -> Tácticas para controlar la capacidad de prueba -> Fallas detectadas

Capadidad de prueba:
- Entradas y salidas: Saber en cómo dadas unas entradas emitir una saida.
  - Captura y reproducción: En un escenario de comunicación capturarla y usarlo en un test de prueba. Se usa como librerías VCR.
  - Separar interfaz de implementación: Podemos hacer pruebas con una implementación contolada y saber si tiene las respuesta. Se le llama sprites o mock. Muchos frameworks tienen una facilidad para usar mocks.
  - Acceso exclusivo para pruebas: Cómo hacer cuando tenemos una funcionalidad que solo podemos probarla desde fuera de la aplicación. Por lo cual tenemos que usar código externo que debemos evitar que llegue al entorno de producción. Es muy usada en microservicios en APIs. Para ello creamos acceso específicos controlando las partes dependientes al servicio.

- Monitoreo interno: La ejecución de la aplicación y cómo probar que se está ejecutando correctamente.
  - Monitoreo incorporado: Monitorizar recursos de la aplicación.

Todo esto se ve afectado por la mantenibilidad. Una buena mantenibilidad de código va a ayudar a tener una mejor capadidad de prueba.

# Escenarios: Usabilidad

Pedido de un usuario -> Tácticas para controlar la usabilidad -> Información y asistena adecuada al usuario.

Usabilidad:
- Separar la interfaz de usuario: Cualquier módulo esté separado de la interfaz del usuario. Independientemente de la lógica del usuario. Mantenibilidad: Coherencia semántica.

- Iniciativas del usuario: Para que el usuario tenga mejor control de lo que está pasando o pueda mejorar en sus operaciones.
  - Cancelar: Dada una acción de usuario el poder arrepentirse, el poder decir "no hagas esto". Entonces cualquier proceso que tenga un tiempo determinado de ejecución pueda ser cancelado lo cual implica hacer que la interfaz soporte esta interacción. Hay procesos que al ser muy rápido no tienen la opción a cancelarse.
  - Deshacer: Para que el usuario pueda volver a un paso anterior cuando sucedió algo que no le parece al usuario. Es muy común en en Android y Desktop. En web es poco común pero algo sencillo de implementar en aplicaciones reactivas como React o VueJS que tienen cambios de estado.
  - Agregación: Entender cuando las funcionalidades debería estar agrupadas. Como repetir un grupo de acciones ya realizadas para implementar repetitividad y así agilizar su trabajo.
  - Múltiples vistas: Que el usuario tenga solo las vistas necesarias para que pueda ejecutar solo las acciones de la forma más eficiente posible. En cada cierto momento presentar la misma información pero de forma diferente, para que la vista esté optimizada en base a las accciones a ejecutar. 

- Iniciativas del sistema: La ideaes entender del lado del sistema el estado actual de la aplicación.
  - Modelado del usuario: Saber el estado actual del usuario para enviarle una notificación de acuerdo a su estado desde el lado del sistema para darle feedback en su estado actual como conocer que sigue viendo un formulario para dare feedback de cualquier eventualidad. El sistema necesita saber lo que está haciendo el usuario y saber si la información que le queremos dar es pertinente al momento.
  - Modelo del sistema: Qué sabemos de nosotros de lo que está pasando e nuestra App, para brindarle información de lo que está sucediendo. Muy usuado en carga de datos. Ejemplo si lo hacemos de forma asíncrona podemos notificarle al usuario lo que se ha cargado, errores en cciertas líneas, etc. El estado del sistema es que tiene un proceso de ejecución.
  - Modelo de la tarea: Es con cuánto entiende el sistema de la tarea que está queriendo resolver el usuario. Como por ejemplo el modelo de una compra para saber cómo ayudar al usuario para que sea exitoso en esa tarea específica.


# Validar las decisiones de diseño: Arquitectura en evelución

En tradicional se evalúa la arquitectura en momento del diseño mientras que en Agile se realizan en cada iteración.

Hay una metodología para el diseño de la arquitectura llamado ATAM.

Todas las decisiones que tomamos debemos usar métricas para saber qué está pasando y poder sabe cuán bien o mal estamos al respecto. Podemos implementar pruebas automatizadas para que se comunique con un umbral y pueda disparar una alerta.

En nuestro Backlog debemos saber qué priorizar y qué no. En cada iteración detectar qué se puede mejorar para un feedback con la ayuda de métricas y alertas automatizadas.

De esta forma podemos saber dónde nuestra arquitectura no está cumpliendo las expectativas y tomar acciones para mejorarla.

# Último análisis a PlatziServicios

Confiabilidad: Madurez, Disponibilidad
- Latido: Mensaje de un componente para avisar que está disponible.
- Excepciones: Saber un error.
- Transacciones: Atomicidad en bases de datos.
- Redundancia pasiva: Para asegurarnos la disponibilidad.

Seguridad: Autenticidad, confidencialidad
- Autenticación: Permitir al usuario otorgar información de usuarios.
- Confidenciaidad de datos: Encriptar y proteger información de los clientes para que solo le lleguen a los prestadores.
- Restauración: Podamos recuperarnos de ataques.

### Diseño de una arquitectura: En crecimiento

Eficiencia de ejcución: Uso de recursos, Capacidad
- Frecuencia de muestreo: Controlar el uso de recursos .
- Manejar la tasa de eventos: Limitar la entrada de eventos.
- Concurrencia: Servirá mucho para el cálculo de los reportes.
- Réplicas: Nos ayudará para la capacidad y poder soportar más pedidos en paraleo.

Compatibilidad: Interoperabilidad
- Separar interfaz de implementación: Para evitar que todo nuestro código esté acoplado a una interfaz. Y cualquier otra app externa pueda acceder a nuestra API común.
- Implementar estándares: Implementando estándares como APIRest o bien GraphQL.
- Documentar: Es importante.
- Ocultar información: Para no generar futuros acoplamientos.

Seguridad: Comprobación de hehos, traza de responsabilidad, confidencialidad.
- Traza de auditoría: Saber qué pasó y quién fue el que lo ejecutó.
- Limitar accesos: Ayuda a que estas cosas no pasen. 
- Autorización: De tal forma definir quién tiene acceso a qué.
- Detección de intrusos: Empezar a ser proactivos y desde nuestro lado cuándo alguien entró a nuestro sistema de forma no autorizada.

### Diseño de una arquitectura a gran escala

Usabilidad: Accesbilidad, reconocimiento de idoneidad, Operabilidad.
- Separar interfaz de usuario: Separa qué es lo que se ve con lo que se hace.
- Modelo de usuario: Nos ayudan con la accesbilidad.
- Modelo de tarea: Nos ayudan con la accesbilidad.
- Múltiples vistas: Para saber qué usuario está accediendo a la información y quén necesita ver.

Mantenibilidad: Modularidad, capacidad de prueba, capacidad de modificación.
- Abstraer servicios comunes: Detectar código común y abstraerlo a un servicio.
- Restringir la comunicación: Restringir qué parte se comunica con otra nos va a ayudar a crear en equipos más independientes ya sea en el software como en la organización del equipo.
- Intermediarios: Compatibilizar la comunicación entre dos módulos. 
- Adherir protocolos: Ayuda a la mantenibilidad del sistema.

Confiabilidad: Tolerancia a fallos, capacidad de recuperación. "Poder soportar errores que ya en esta etapa no están permitidos".
- Punto de controlo/retroceso
- Sincronización de estado
- Monitoreo de procesos

# Cómo comunicar la arquitectura: Vistas y puntos de vistas

"Esencialmente, todo modelo es incorrecto. Pero algunos son útiles" -> George Box

# Documentación vs implementación

Al momento de implementar la arquitectura al momento de código pueden existor diferencias.

La fuente de la verdad va a ser el código y no el documento de arquitectura.


Técnicas para solventar diferencias:
- Ignorar divergencias
- Modelo ad hoc
- Solo modelos de alto nivel
- Sincronización en hitos del ciclo de vida
- Sincronización en crisis (cuando las cosas no están funcionando)
- Sincronización constante (es lo menos eficiente)


# Adicional

# Pararse en hombros gigantes

La arquitectura la debemos diseñar en base a las necesidades.

Significa el aprovechar todo el conocimiento de la industria para empezar desde una mejor base.

Podemos:
- Usar productos "de la estantería" como librerías.
- Frameworks nos ayuda a proponer una arquitectura de diseño y luego nosotros podremos redefinir en base a las necesidades.
- Arquitecturas específicas del dominio: Las hay ya definidas para un dominio específico con el cual podemos aprovecharla.
- Patrones de arquitectura: Podemos definir gran parte del diseño y dejar ciertas partes por definir de manera restrictiva.

# Herramientas y partes de un diseño: Tipos de conectores.

En esta parte vamos a conectar los atributos de calidad con la solución que implemente dichos atributos. Viendo qué opciones tenemos para resolver esa operación  que al combinarla tendremos nuestra arquitectura.

Partes de una arquitectura:
- Componentes: Partes de nuestros sistemas que cumplen una función.
- Conectores: Es la conección entre componentes que no necesariamente está enlazado a un dominio (negocio).

Tipos de conectores:
- Llamada de procedimiento: Invocar de un componente a otro y esperar una respuesta.
- Enlace: Vinculan fuertemente un componente a otro incluso para poder compilarse.
- Evento: Permiten a un componente emitir que algo sucedió y a otro escuchar que algo sucedió y reaccionar con otra funcionalidad.
- Adaptador: Nos ayudan a compatibilizar la interfaz de un componente con otro y de esta forma podemos interconectar componentes que no estaban diseñados para comunicarse.
- Acceso a Datos: Nos ayudan a acceder a recursos compartidos, permitiendo compatibilizar la respuesta del recurso con lo que espera el componente.
- Flujo: La información está todo el tiempo pasando datos y un componente está interesado en ver esos datos.
- Arbitraje: Ver en cómo un componente y otro tienen acceso a un mismo recurso.
- Distribuidor: Dado un componente distribuir a muchos otros componentes, de esta forma podemos comunicar a través de un mismo mensaje y un mismo conector un mensaje a muchos componentes.
