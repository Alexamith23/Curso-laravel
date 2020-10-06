# Vistas

Las vistas se encuentran en la carpeta

    resources/views

Puedo tener tantas vistas como yo quiera. También puedo tener mi vista dividida en muchas vistas.

## Ejemplo
Si tengo que agregar el mismo css a todas las vistas eso quiere decir que tendría que incluír la misma etiqueta en todas las vistas donde quiera usar ese css general.
Esto se resuelve así.

- Detro de esa carpeta agregamos un archivo llamado layout.blade.php
- Dentro de este archivo voy a crear la estructura básica de html y sólo le voy agregar las etiquetas de css.

    ![vagrant](layout.png "vagrant")
- En otro archivo llamado welcome.blade.php, ahí sólo voy agregar los divs y demás elementos para la contrucción de una página html, sin agregar la estructura básica de html porque esa estructura ya la agregué en el paso anterior.

    ![vagrant](div.png "vagrant")

- ¿Cómo enlazo estos 2 archivos?

    En el archivo welcome.blade en la primera linea agreo la línea de código 

        @extends('layout')
    Eso le indicará al archivo que pasará a obtener la estructura del archivo layout.blade

- Se debe indicar en el archivo `layout` todo lo que se va agregar queremos que esté dentro de la etiqueta `<body>`

    ![vagrant](body.png "vagrant")

Y de esta manera puedo tener dividida la vista en tantos pedazos de código como yo quiera.
<!-- ![vagrant](dbdefa.png "vagrant") -->

# Forms

En el controlador al menos al principio, recomendaría que sigas esta convención, así que comentemos muy rápidamente. cada uno de estos haría la acción de índice como se aprendió claramente. Debería generar una lista de un recurso. La acción de mostrar debería mostrar un solo recurso. La acción de crear muestra de usted para crear un nuevo recurso y así sucesivamente.

Las 7 acciones en el controlador

The Seven Restful Controller Actions

![vagrant](7.png "vagrant")

Del lado del controlador estatal, sin embargo, todavía tenemos que averiguar cuál es la convención para la escritura porque podría pensar que escribo esto es simple si voy a editar un artículo existente, entonces probablemente sea algo como esto y tenga razón, ¿qué pasa con las actualizaciones? ha editado un artículo existente, sabe que desea realizar esa acción de actualización para saber qué debería ser. Me veo así. ¿Es algo como esto? No, no, en cambio, podemos usar el tipo de solicitud o el verbo de solicitud para canalizar estas solicitudes entrantes.
Por ejemplo así

![vagrant](rutas.png "vagrant")

Y así sucesivamente con las rutas que quiera!