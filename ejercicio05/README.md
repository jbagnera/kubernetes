* HEALTHCHECK
  Dockerfile Healthcheck es una opción del sistema que se encarga de indicarle al daemon de Docker cómo comprobar que el contenedor se encuentre funcionando, es decir, le dice cómo probar un determinado container de Docker para verificar si aún se encuentra realizando sus labores.

Esta instrucción permite que el sistema sea capaz de detectar casos de errores, como, por ejemplo, un servidor web que esté atascado en un bucle infinito y que no pueda controlar las conexiones nuevas, incluso si el proceso de este servidor sigue ejecutándose dentro de la plataforma.

Cuando un contenedor cuenta con una verificación de health especificada, tiene un estado de salud o health status, además de su estado normal, que, de manera inicial, es el estado de starting. En cada ocasión en la que la herramienta Dockerfile Healtcheck realiza una verificación de estado, el contenedor pasa a estar en healty status, independientemente del estado en el que se encontrara anteriormente. Después de darse una determinada cantidad de fallos consecutivos dentro del container, este actualiza su estado a unhealthy.

* ONBUILD
ONBUILD es una declaración que escribe en sus Dockerfiles. Es único porque acepta otro la educación como argumento. Puede especificar cualquier operación de Dockerfile, por ejemplo COPY o RUNy hacer que se ejecute al compilar una imagen posterior.

ONBUILD no afecta el sistema de archivos del contenedor base, pero Docker aún sabe que los desencadenantes están presentes cuando crea una imagen posterior. El proceso de construcción realiza un seguimiento ONBUILD las instrucciones las encuentran y las registran en los metadatos de la imagen.

Docker inspecciona los metadatos de las imágenes a las que se hace referencia en un FROM instrucción. Si la imagen nombrada incluye desencadenantes en sus metadatos, esas declaraciones desencadenantes se pegan en la parte superior del Dockerfile descendente antes de que comience la compilación.

Los activadores se ejecutan realmente como parte de la compilación FROM escenario. Se ejecutarán en el orden en que se escribieron en el Dockerfile ascendente. Si uno ONBUILD la declaración falla, Docker deshará la compilación y se verá como el FROM el escenario fue la causa.


* VOLUME
  Se utiliza el comando en un archivo Docker para crear un espacio de almacenamiento compartido en el contenedor.
  A diferencia de cuando se ejecuta el comando sin Dockerfile, no se asigna una carpeta host ni se puede dar nombre a el volume
