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
