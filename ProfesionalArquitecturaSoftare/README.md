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

