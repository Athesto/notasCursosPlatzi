# Introducción al curso

Profesor: Juan Pablo Roja

La app es 365 Desayunos hecho en Python con Django

# ¿Cómo funciona analytics?

Desde Google analytics tenemos un script en el cual debemos poner el id de nuestro usuario.

Significado de "isogram":
i -> Window
s -> DOM
o -> Variable 'script'
r -> Nombre global para llamar a 'google analytics ga'
a -> Script asícrono
m -> Script tag del elemento en el documento

con 'ga' podemos crear un traquer. Ejemplo

```
ga('create',{
    trackginId: 'UA-123123-4',
    cookieDomain: 'auto'
    });
ga('send'.{
      hitType: 'pageview',
    })
```

# Creando un tracker

Un tracker es la forma en que un código envía información a Google Analytics

Para crear un tracker:
`ga('create', 'UA-12312312-4', 'auto','MyTracker')` // crear, id, auto: la información de la cookie, con el dominio y el tiempo de expiración lo optenemos de forma automática. MyTracker: Nombre del tracker que es opcional.

> Google Analytics: https://analytics.google.com

Si vemos en consola podemos ver el Banner de Google Analytics

Cuando nosotros nombramos un tracker debemos especificarlo.

Ejemplo de: `ga('send', 'pageview')` a `ga('MyTracker.send', 'pageview')`

Cuando nombramos un tracker tenemos la posibilidad de crear más de uno.

# Obteniendo y enviando datos

Desde la consola:
```
zz=ko# Obteniendo y enviando datos

Desde la consola:
```
# Obteniendo y enviando datos

Desde la consola para ver la información del tracker creado.
```
ga(function(tracker){
    console.log(tracker);
    })
```

Otra forma es (especificando un nombre)
```
ga(function(){
    console.log(ga.getAll());
    })
```

Obtener el nombre del tracker:
```
ga(function(tracker){
    console.log(tracker.get('name'));
    })
```

LLamar a un tracker por su nombre
```
ga(function(){
    console.log(ga.getByName('t0'));
    })
```

// Obtener el nombre `tracker.get('name')`
// Conseguir el id cliente `tracker.get('clientId')`
// Determinar url de referencia `tracker.get('referrer')`

Para saber todas las cosas que podemos obtener de tracker `console.log(tracker)` -> pc -> b -> data (y aquí tenemo todas las keys)

Google Analytics tiene un código de google analytics para la mismas funciones. Ejemplo para un título `console.log(tracker.get('&dt'))`

Setear un valor 
```
ga('set', 'page', '/about');
```


