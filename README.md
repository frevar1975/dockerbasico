# dockerbasico
Proyecto de ejemplo para la dockerizacion de una aplicacion java

Pasos para crear una imagen Docker 
1.	Crear el fichero Dockerfile
2.	Agregar en la carpeta del fichero los archivos necesarios para crear la imagen
3.	Agregar el contenido al fichero
4.	Construir la imagen mediante el comando “docker build”

Para construir la imagen Docker: docker build -t <nombre_contenedor> .
Observación: se debe estar posicionado en el mismo directorio donde se encuentra el fichero dockerfile.


Creación del proyecto Java con SprintBoot

Primero vamos a crear el proyecto Java simple para este ejercicio. Utilizaremos las herramientas de apoyo de Sprint para facilitar el avance hacia el objetivo principal. 

Programamos y desplegamos la aplicación para probar que funcione.
 
Ahora crearemos el fichero Dockerfile.
 
Creamos el JAR de la aplicación.
Ahora agregamos las propiedades en el archivo Dockerfile, en ARG se debe introducir el nombre del JAR.

Continuamos con el proceso de construcción de la imagen:
docker build -t dockerbasico .

Ahora verificamos que la imagen haya sido creada.
Procedemos a ejecutarla en Docker.
docker run -it -p 8080:8080 dockerbasico

