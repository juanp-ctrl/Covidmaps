# Descripcion Covidmaps
Nuestra app es creada para ayudar a la población de Medellín a mantenerse informada con respecto al número de contagiados y sus ubicaciones, de esta manera el usuario se puede mantener informado acerca de que lugar de medellín se encuentran los casos apartir de un mapa en nuestra aplicación con el fin de mostrar cual es el nivel de seguridad para salir en la determinada zona en la que el usuario vive.
# Arquitectura
·Servidor y Firewall
Es un servidor de AWS montado con una imagen de ubuntu 18.04, en este correra Docker y el servicio HTTP que utilizara nuestra aplicación, este servidor fue montado en un grupo de seguridad de AWS que permite los puertos 22, 80 y 443 e internamente en el servidor por medio de UFW se permitieron los protocolos SSH, HTTP, HTTPS y Apache Full.
·Contenedor
Para los contenedores usaremos Docker montado en el servidor, su función sera mantener la información de cada usuario en un contenedor unico y para esto montamos la configuración basica.
·Dockerfile
En este archivo estan las instrucciones para manejar los contenedores, para los servicios y elementos necesarios para el funcionamiento de la aplicación.
·Flask
Usaremos flask y python para la programación del sitio web en el servidor y este recibira los datos de la app y se encarga de el control y uso de lo recibido para la contruccion del mapa y riesgo del usuario, usando una base de datos mysqli.
·Kodular
En este desarrollamos la aplicación movil, su interfaz gráfica con 3 pantallas, la primera es el menu de inicio que da la opción de Registrar Información, Ver mapa, y Riesgo de contagio.
La segunda pantalla es donde el usuario registra su información y envia los datos a la base de datos, y tiene el boton de enviar información y volver al menu.
y la tercera pantalla es donde se visualiza el mapa con los puntos en donde se encuentran usuario infectados, boton para ver el riesgo y un boton para volver al menu.
# Arbol de carpetas del sitio
·/Templates
En este archivo estan los documentos html que son los diseños y visual del archivo, index.html, registro.html, mapa.html
·/Database
En esta carpeta los archivos de la base de datos
·site.py
Este es el visor principal del sitio por medio de este se puede acceder a las otras funcionalidades del sitio.
y los archivos .py de la aplicación.
# Autor
Juan Pablo Jiménez Heredia
Id 000131834
