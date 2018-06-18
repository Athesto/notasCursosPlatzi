# Introducción

Prof: Estefania Zmaragdis (Epi)

¿Qué es Watson?

E la platafoma te inteligencia artificial de IBM. Los aquellos sistemas que aprenden, rezonan y entienden.

Es un sistema en redes neuronales estructurado en Machine Learning.

Los servicios de Watson son como legos, separados no significan mucho pero al combinar servicios podemos crear soluciones de alto impacto. 
> "Solo debemos tener un objetivo en mente y pensar a construir. Al igual que con los bloques el único impedimento es nuestra creatividad y las ganas de crear algo."

# Introducción a Watson Assistant

Keyword recognition no es IA. Lo primero es reconocer las palabras para entregar una respuesta.

Con este servicio va entender el lenguaje natural.

Recibe un input -> Procesa y entinde -> Entrega una respuest(según lo hayamos entrenado)

Entrenamiento:
- Intenciones: Los motivos de la pregunta. Propuesta de mucha fomas.
- Entidades: Definir diferencias, ejemplo entre televisor y computadora.
- Flujo de diálogo: Para armar el árbol de decisiones para que sepa qué contestar en cada caso.

Hay herramientas para crear y mejorar el algoritmo.

# Watson Assistant Tool

Creamos una App para Watson Assistant y luego entramos en la Tool.

> Esto cambia bastante seguido.

Creamos un nuevo Workspace.

Antes de crear nada debemos pensar qué es lo que va hacer el asistente, qué va a contestar y qué no va a contestar.

Luego de ello bajamos las intenciones que son las preguntas frecuentes.

Colocamos un intent name como #horarios.

Una vez creadas colocamos los ejemplos de cómo serían las preguntas.

> Cuanto más general sean los ejemplos, mejor se adaptarán. Ejemplo: Qué horarios -> horarios. Es decir, lo más general posible y lo más específico posible para un asistente robusto que sepa contestar bien.

Notar que entre las preguntas de entrada no se usan signos.

Entramos en la parte de Dialog.

Sus nodos iniciales son:
- Bienvenido: Mensaje de bienvenida.
- En otras cosas: Se va a usar cuando el asistente no esté seguro de lo que se hace. La IA trabaja con confianza, cuando llega un punto que la confianza no alcanza límites mínimos entra en esta parte.

> El orden de los nodos equivale a un if/else. Entrará en el primer nodo que haga Match.

Para insertar el nodo horario debajo del nodo de bienvenida. Colocamos un nombre y tiene que reconocer el intent #horario.

> Para indicar que es un intent se usa #, con @ es para entidades y con $ es para variables de contexto.

Luego de ello, indicar la respuesta, luego podemos especificar de qué hacer luego de entregar una respuesta. Tales como finalizar, saltar  a un nodo, finalizar o esperar un input del usuario.

Podemos probar el servicio en un botón Try out.

Luego de terminado, no llevarlo a producción. Sino entrenarlo con terceros para mejorar el entrenamiento. Cuanto más ejemplos le demos y de personas distitntas mejor va a ser.

Durante el flujo de dialogo podemos especificar la intención correcta según la pregunta.

# Watson Natural Language Understanding

Podemos decir una misma frase para enojo, alegría, tristeza, etc.

Este servicio reconoce de lo que decimos: Categorías, conceptos, emociones, entidades, keywords, metadata, relaciones, roles semánticos, sentimientos.

Las escalas van entre -1 y 1.

Un ejemplo de uso con el módulo anterior, podemos conocer el sentimiento del usuario para darle una atención más certera.


