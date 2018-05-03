# Bienvenida al curso de Java 2018 Avanzado

En este curso veremos aspectos avanzados de Java, entre ellos interfaces, lambdas y Java 9.

Crearemos JDBC en Java para almacenamiento en base de datos.

Profesora Anahí Salgado.

# Clases Abstractas

Es algo que ayuda a crear programas mucho más mantenibles y robustos a futuro.

Ayuda a integrar nuevos módulos sin necesidad de realizar muchos cambios.

En el curso anterior implementamos poliformismo en Herencia e interfaces.

> Recuerda que en las interfaces debemos implementar todos los métodos.

Hay una forma más profunda de implementar poliformismo.

- A veces no necesitamos todas las implementaciones de una interfaz.
- A veces no necesitamos usar todos los métodos de la herencia.
- A veces no necestamos crear instancias de la clase padre.

Quien viene a solucionar estos detalles son las clases Abstractas combina a la herencia con interfaces.

Clase abstracta:
- No imlementaremos todos los métodos: Definimos cuáles son los métodos obligatorios a implementar y cuáles no.
- No crearemos instancias: Es un tipo de resticción.

Ejemplo:

```
public abstract class Figura {
  abstract void dibujate();
}
```

> Un método que sea obligatorio implementar debe llevar la palabra clave **abstract**. El cual no contendrá implementación, así como las interfaces.

Uso:
```
class Triangulo extends Figura {
  abstract void dibujate();
}
```

# Implementando clases abstractas al proyecto

# Imlementando métodos abstractos en Java

# Qué es JavaDocs

Generar documentación en HTML desde el código Java.

Esto es para explicar la documentación en Java. Es la ayuda que aparece en Crtl+barra-espaciadora.

Es la misma documentación de Android y de Spring.

JavaDoc se autodocumenta a los comentarios.

La documentación es `/** Documentacion */`

Ejemplo: Dando Ctrl+clic a un objeto, seremos enviados al código.

Los comentarios de documentación son de color azul.

Dentro del código podemos crear etiquetas HTML para dar mejor estructura.

```
/**
* <p>
* [Descripción larga]
*
* [author, version, params,
returns, throws, see, other tags]
* [see also]
*/
```

