# Routing
## ¿Qué pasa exactamente cuando hacemos una petición?

    Antes de profundizar en los aspectos prácticos de laravel, veamos primero qué sucede exactamente cuando llega una solicitud.
    Imaginemos que administra un restaurante de entrega de pizzas.

    Cuando una persona visita URL de la página del restaurante antes de que se muestren las páginas, primero llegamos al servidor y cargamos su laravel.
    Inmediatamente, su aplicación se da cuenta de que, esta es una solicitud para la página de inicio.
    Ahora en laravel, es realmente fácil asociar cualquier URI con una respuesta

    Para notar en este caso si el usuario realiza una solicitud para la página de inicio, cargaremos un controlador y un controlador es la siguiente pieza del rompecabezas.

    El controlador recibe una solicitud y proporciona una respuesta, por lo que en este caso, la solicitud es cargar la página de inicio de Larry's Pizza.

    Cómo el controlador genera esa respuesta puede tomar muchas formas y hablaremos un poco sobre esto, pero por ahora digamos que el controlador debe delegar para obtener la información necesaria de su base de datos puede ser todas las pizzas, todos los especiales, todos los temas que podemos utilizar, lo que se conoce como un modelo elocuente.Para esto ahora, no solo el modelo  proporciona una buena API para realizar cualquier cantidad de consultas SQL en su base de datos, sino que también es una ubicación para almacenar cualquier lógica de dominio o lógica de negocios específica.

    Una vez que el controlador ha delegado en el modelo, el siguiente paso es cargar la vista.

    Son las hojas del usuario en última instancia. Es la parte HTML de su código base, define la estructura, carga un archivo CSS, las referencias de JavaScript ahora lo más importante si recibió los datos del controlador.

    Ahora lo más importante es que la vista recibe los datos del controlador y luego los procesa para el usuario.

## Resumen

    El controlador delega y carga toda la información necesaria para proporcionar una respuesta que  recibe los datos del controlador y luego genera la estructura HTML para el usuario.

# Setup a Database Connection