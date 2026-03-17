# comandos-instalacion-docker

DOCKER
¿Qué es?

Es un proyecto de código abierto con el que podremos crear "contenedores". Estos contenedores de Docker podríamos definirlos como máquinas virtuales ligeras, menos exigentes con los chips y memorias de los equipos donde se ejecutarán. Las características principales de estos contenedores son la portabilidad, la ligereza y la autosuficiencia.
- Portabilidad: El contenedor podremos desplegarlo en cualquier sistema con lo que nos ahorraremos el tener que instalar en este nuevo entorno todas aquellas aplicaciones que normalmente usemos.
- Ligereza: El peso de este sistema no tiene comparación con cualquier otro sistema de virtualización más convencional que estemos acostumbrados a usar. Por poner un ejemplo, una de las herramientas de virtualización más extendida es VirtualBox, y cualquier imagen de Ubuntu que queramos usar en otro equipo pesará entorno a 1Gb si contamos únicamente con la instalación limpia del sistema. En cambio, un Ubuntu con Apache y una aplicación web, pesa alrededor de 180Mb
- Autosuficiencia: Un contenedor Docker no contiene todo un sistema completo, sino únicamente aquellas librerías, archivos y configuraciones necesarias para desplegar las funcionalidades que contenga. Asimismo, Docker se encarga de la gestión del contenedor y de las aplicaciones que contenga.


3 elementos fundamentales:
- Contenedores: Son como un directorio, contienen todo lo necesario para que una aplicación pueda funcionar sin necesidad de acceder a un repositorio externo al contenedor. Cada uno de éstos es una plataforma de aplicaciones segura y aislada del resto que podamos encontrar o desplegar en la misma máquina host. El contenedor es un proceso de espacio aislado en su máquina que está aislado de todos los demás procesos en la máquina host.
- Imágenes: La imagen Docker podríamos entenderla como un SO con aplicaciones instaladas.
- Repositorios: contienen imágenes creadas por los usuarios y puestas a disposición del público. Podemos encontrar repositorios públicos y totalmente gratuitos o repositorios privados donde tendremos que comprar las imágenes que necesitemos.


¿Cómo funciona?

En un principio contamos con una imagen base , sobre la que realizaremos los diferentes cambios. Tras confirmar estos cambios mediante la aplicación Docker , crearemos la imagen que usaremos. Esta imagen contiene únicamente las diferencias que hemos añadido con respecto a la base. Cada vez que queramos ejecutar esta imagen necesitaremos la base y las 'capas' de la imagen. Docker se encargará de acoplar la base, la imagen y las diferentes capas con los cambios para darnos el entorno que queremos desplegar para empezar a trabajar.
Docker le proporciona una manera estándar de ejecutar su código. Docker es un sistema operativo para contenedores. De manera similar a cómo una máquina virtual virtualiza (elimina la necesidad de administrar directamente) el hardware del servidor, los contenedores virtualizan el sistema operativo de un servidor. Docker se instala en cada servidor y proporciona comandos sencillos que puede utilizar para crear, iniciar o detener contenedores.


CARACTERÍSTICAS DE DOCKER:
- Autogestión de los contenedores.
- Fiabilidad.
- Aplicaciones libres de las dependencias instaladas en el sistema anfitrión.
- Desplegar múltiples contenedores en un mismo equipo físico.
- Puesta en marcha de los servicios.
- Contenedores livianos que facilitan su almacenaje, transporte y despliegue.
- Capacidad para ejecutar una amplia gama de aplicaciones.
- Compatibilidad Multi-Sistema, desplegar nuestros contenedores en multitud de plataformas.
La aplicación base de Docker gestionará los recursos existentes para asignarlos responsablemente entre los contenedores desplegados.
Podremos establecer una base desde la que comenzar nuestros proyectos, lo que nos ahorrará el tiempo de preparar el entorno para cada uno de ellos.
Podremos compartir nuestros contenedores para aumentar los repositorios de Docker así como beneficiarnos de los que compartan los demás.


INSTALACIÓN DOCKER DESKTOP EN WINDOWS:
Si queremos instalar Docker debemos cumplir ciertos requisitos en Windows 10:
- Windows 10 versión Professional o Enterprise.
- Actualizado con Anniversary Edition o Creators Update.
- Updates críticos para Windows Containers.
- Compilación igual o superior a 14393.222.
- Virtualización activada en nuestro equipo.
https://docs.docker.com/desktop/install/windows-install/
Instalar Docker
BOTÓN DERECHO – ACCESO DIRECTO DE DOCKER – Destino – Escribimos –SwitchDaemon
Opciones avanzadas – Ejecutar como administrador
Escribimos en el cmd situados en la ruta de la carpeta docker –> DockerCli.exe -SwitchDaemon


COMANDOS BÁSICOS DE DOCKER:
- docker --help: Muestra la ayuda de todos los comandos.
- docker version: Muestra información y versión de docker.
- docker info: Muestra información sobre cliente y servidor.
- docker images: Ver la lista de imágenes descargadas.
- docker ps: Ver la lista de contenedores en ejecución.
- docker ps -a: Ver la lista de todos los contenedores ejecutados. Enumera todos los contenedores de Docker que se ejecutan / salieron / detuvieron con los detalles del contenedor.
- docker rm: Borra contenedores en nuestro equipo.
- docker rmi: Borra imagenes en nuestro equipo.
- docker search: Busca imágenes en el Docker Hub.
- docker pull: Descarga imágenes desde Docker Hub.
- docker restart: Reinicia el contenedor de la ventana acoplable con la identificación del contenedor mencionada en el comando.
- docker stop: Detiene un contenedor con el ID de contenedor mencionado en el comando.
- docker start: Inicia el contenedor de la ventana acoplable con la identificación del contenedor mencionada en el comando.
- docker kill: Detiene el contenedor Docker inmediatamente. El comando de detención de Docker detiene el contenedor con gracia, esa es la diferencia entre los comandos de detención y de detención.
- docker commit: Guarda una nueva imagen de Docker con el ID de contenedor mencionado en el comando en el sistema local.
- docker login: Inicia sesión en Docker Hub. Se le pedirán las credenciales de su Docker Hub para iniciar sesión.
- docker push: Carga una imagen de la ventana acoplable con el nombre de la imagen que se menciona en el comando en la ventana acoplable.
- docker network: Enumera los detalles de toda la red en el clúster.
- docker info: Obtiene información detallada sobre la ventana acoplable instalada en el sistema, incluida la versión del kernel, el número de contenedores e imágenes, etc.
- sudo docker cp: Copia un archivo de un contenedor de la ventana acoplable al sistema local.
- docker history: Muestra el historial de una imagen de la ventana acoplable con el nombre de la imagen mencionado en el comando.
- docker logs: Muestra los registros del contenedor de la ventana acoplable con la identificación contenida mencionada en el comando.
- docker search: Busca una imagen de docker en dockerhub con el nombre mencionado en el comando.
- docker update –help: Actualiza las configuraciones de contenedores. Esto muestra todas las opciones de actualización.
- docker volume create: Crea un volumen que el contenedor de la ventana acoplable utilizará para almacenar datos.
- docker volume ls: Ejecuta el comando si el volumen se ha creado.
- docker plugin install: Instala un complemento de docker vieux / sshfs con el entorno de depuración establecido en 1.
- docker logout: Cierra sesión en dockerhub.
- docker volume create <volume> : Crea un volumen.
- docker volume ls: Lista todos los volúmenes.
- docker-compose up –d: Para ejecutar el contenedor se necesita ejecutar el comando “docker-compose up” y se verá cómo crea el contenedor según Dockerfile y lo ejecuta con la definición del archivo docker-compose.yml y su servicio correspondiente situado en cualquier carpeta.
- docker ps –aq: Borra todos los contenedores de docker.
- docker run –it nombrecontenedor: Acceder a la terminal de un contenedor.
- docker-compose ps: Lista los containers corriendo en el contexto de este docker-compose.
- docker system df: Visualiza todo el estado del disco usado de docker.


Archivo de configuración docker:
El archivo de configuración se encuentra en C:\Program Files\Docker\Docker\resources\windows-daemon-options.json


## Autor
Alejandro Velaz

🎓 Formación: ASIR
