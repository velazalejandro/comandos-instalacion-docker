# comandos-instalacion-docker

DOCKER
¿Qué es?
Es un proyecto de código abierto con el que fácilmente podremos crear "contenedores". Estos contenedores de Docker podríamos definirlos como máquinas virtuales ligeras, menos exigentes con los chips y memorias de los equipos donde se ejecutarán. Las características principales de estos contenedores son la portabilidad, la ligereza y la autosuficiencia.
Portabilidad: El contenedor podremos desplegarlo en cualquier sistema con lo que nos ahorraremos el tener que instalar en este nuevo entorno todas aquellas aplicaciones que normalmente usemos.
Ligereza: El peso de este sistema no tiene comparación con cualquier otro sistema de virtualización más convencional que estemos acostumbrados a usar. Por poner un ejemplo, una de las herramientas de virtualización más extendida es VirtualBox, y cualquier imagen de Ubuntu que queramos usar en otro equipo pesará entorno a 1Gb si contamos únicamente con la instalación limpia del sistema. En cambio, un Ubuntu con Apache y una aplicación web, pesa alrededor de 180Mb
Autosuficiencia: Un contenedor Docker no contiene todo un sistema completo, sino únicamente aquellas librerías, archivos y configuraciones necesarias para desplegar las funcionalidades que contenga. Asimismo, Docker se encarga de la gestión del contenedor y de las aplicaciones que contenga.

3 elementos fundamentales:
Contenedores: Son como un directorio, contienen todo lo necesario para que una aplicación pueda funcionar sin necesidad de acceder a un repositorio externo al contenedor. Cada uno de éstos es una plataforma de aplicaciones segura y aislada del resto que podamos encontrar o desplegar en la misma máquina host.
El contenedor es un proceso de espacio aislado en su máquina que está aislado de todos los demás procesos en la máquina host
Imágenes: La imagen Docker podríamos entenderla como un SO con aplicaciones instaladas.
Repositorios: contienen imágenes creadas por los usuarios y puestas a disposición del público. Podemos encontrar repositorios públicos y totalmente gratuitos o repositorios privados donde tendremos que comprar las imágenes que necesitemos.
¿Cómo funciona?
En un principio contamos con una imagen base , sobre la que realizaremos los diferentes cambios. Tras confirmar estos cambios mediante la aplicación Docker , crearemos la imagen que usaremos. Esta imagen contiene únicamente las diferencias que hemos añadido con respecto a la base. Cada vez que queramos ejecutar esta imagen necesitaremos la base y las 'capas' de la imagen. Docker se encargará de acoplar la base, la imagen y las diferentes capas con los cambios para darnos el entorno que queremos desplegar para empezar a trabajar.
Docker le proporciona una manera estándar de ejecutar su código. Docker es un sistema operativo para contenedores. De manera similar a cómo una máquina virtual virtualiza (elimina la necesidad de administrar directamente) el hardware del servidor, los contenedores virtualizan el sistema operativo de un servidor. Docker se instala en cada servidor y proporciona comandos sencillos que puede utilizar para crear, iniciar o detener contenedores.

Características:
Autogestión de los contenedores
Fiabilidad
Aplicaciones libres de las dependencias instaladas en el sistema anfitrión
Desplegar múltiples contenedores en un mismo equipo físico
Puesta en marcha de los servicios
Contenedores livianos que facilitan su almacenaje, transporte y despliegue.
Capacidad para ejecutar una amplia gama de aplicaciones
Compatibilidad Multi-Sistema, desplegar nuestros contenedores en multitud de plataformas
La aplicación base de Docker gestionará los recursos existentes para asignarlos responsablemente entre los contenedores desplegados.
Podremos establecer una base desde la que comenzar nuestros proyectos, lo que nos ahorrará el tiempo de preparar el entorno para cada uno de ellos.
Podremos compartir nuestros contenedores para aumentar los repositorios de Docker así como beneficiarnos de los que compartan los demás.

Instalación Docker Desktop en Windows 10:
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
Docker --help: Muestra la ayuda de todos los comandos.
Docker version: Muestra información y versión de docker.
Docker info: Muestra información sobre cliente y servidor.
Docker images: para ver la lista de imágenes descargadas.
Docker ps: para ver la lista de contenedores en ejecución.
Docker ps -a: para ver la lista de todos los contenedores ejecutados. Enumera todos los contenedores de Docker que se ejecutan / salieron / detuvieron con los detalles del contenedor.
Docker rm: para borrar contenedores en nuestro equipo.
Docker rmi: para borrar imagenes en nuestro equipo.
Docker search: para buscar imágenes en el Docker Hub.
Docker pull: para descargar imágenes desde Docker Hub.
docker restart: Reinicia el contenedor de la ventana acoplable con la identificación del contenedor mencionada en el comando.
Docker stop: Detiene un contenedor con el ID de contenedor mencionado en el comando.
Docker start: inicia el contenedor de la ventana acoplable con la identificación del contenedor mencionada en el comando.
Docker kill: Detiene el contenedor Docker inmediatamente. El comando de detención de Docker detiene el contenedor con gracia, esa es la diferencia entre los comandos de detención y de detención.
Docker commit: Guarda una nueva imagen de Docker con el ID de contenedor mencionado en el comando en el sistema local.
Docker login: inicia sesión en Docker Hub. Se le pedirán las credenciales de su Docker Hub para iniciar sesión.
Docker push: Carga una imagen de la ventana acoplable con el nombre de la imagen que se menciona en el comando en la ventana acoplable.
Docker network: enumera los detalles de toda la red en el clúster.
Docker info: Obtiene información detallada sobre la ventana acoplable instalada en el sistema, incluida la versión del kernel, el número de contenedores e imágenes, etc.
sudo docker cp: Copia un archivo de un contenedor de la ventana acoplable al sistema local.
Docker history: Muestra el historial de una imagen de la ventana acoplable con el nombre de la imagen mencionado en el comando.
Docker logs: Muestra los registros del contenedor de la ventana acoplable con la identificación contenida mencionada en el comando.
Docker search: Busca una imagen de docker en dockerhub con el nombre mencionado en el comando.
Docker update –help: Actualiza las configuraciones de contenedores. Esto muestra todas las opciones de actualización.
Docker volume create: Crea un volumen que el contenedor de la ventana acoplable utilizará para almacenar datos.
Docker volume ls: Ejecuta el comando si el volumen se ha creado.
Docker plugin install: Instala un complemento de docker vieux / sshfs con el entorno de depuración establecido en 1.
Docker logout: cierra sesión en dockerhub.
Docker volume create <volume> : crea un volumen.
Docker volume ls: lista todos los volúmenes.
Docker-compose up –d: Para ejecutar el contenedor se necesita ejecutar el comando “docker-compose up” y se verá cómo crea el contenedor según Dockerfile y lo ejecuta con la definición del archivo docker-compose.yml y su servicio correspondiente situado en cualquier carpeta.
Docker ps –aq: Borra todos los contenedores de docker.
Docker run –it nombrecontenedor: acceder a la terminal de un contenedor.
Docker-compose ps: Lista los containers corriendo en el contexto de este docker-compose.
Docker system df: Visualiza todo el estado del disco usado de docker.

Archivo de configuración docker:
El archivo de configuración se encuentra en C:\Program Files\Docker\Docker\resources\windows-daemon-options.json


Integrar Jenkins en docker:
Si nos vamos al Docker Hub veremos que tenemos multitud de tags para la imagen de jenkins/jenkins
https://hub.docker.com/_/jenkins
Descargar la imagen jenkins al Docker Host:
PRIMERO TENEMOS QUE REGISTRARNOS CON UNA CUENTA DE DOCKERHUB PARA PODER DESCARGAR LA IMAGEN DE JENKINS O CUALQUIER OTRA.
1. Correr la plataforma Docker de manera local.
En Docker Desktop – settings – docker engine – experimental: true
Escribimos experimental: true y lo hacemos para que nos funcionen las descargas de las imágenes en el cmd (consola de comandos).
2. Dirigirse a https://hub.docker.com/ y buscar la imagen oficial de la herramienta Jenkins para ejecutar dentro de un contenedor Docker.
3. Para descargar nuestra imagen jenkins/jenkins que hayamos elegido lo haremos con el comando docker pull tal que así:
Docker pull jenkins/jenkins
Docker pull jenkins/jenkins:lts-jdk11
Docker pull jenkins/jenkins:lts
Hemos descargado 3 imágenes de jenkins:
- jenkins/jenkins
- jenkins/jenkins:lts-jdk11
- jenkins/jenkins:lts --> versión más estable y me funciona bien la imagen y sus contenedores
4. Verificamos que la imagen se haya descargado correctamente:
Docker images
5. Ahora ejecuta jenkins como contenedor Docker exponiéndolo en el puerto 8080 de tu ordenador local.
docker run -p 32769 -p 50000:50000 -v /var/jenkins_home jenkins/jenkins:lts
docker run -p 8080:8080 -p 50000:50000 -v /var/jenkins_home jenkins/jenkins:lts
El comando con el que funciona y arranca jenkins con docker:
Docker run –it –p 8080:8080 jenkins/jenkins:lts
Copiamos la contraseña del administrador para acceder a jenkins.
6. Verifica que puedas ingresar al contenedor a través del navegador web de tu preferencia.
La imagen jenkins lts funciona perfectamente – In Use
El ultimo contenedor seleccionado está funcionando – abrimos 8080:8080
En la web nos funciona.
Copiamos la clave de administrador.
7. Cancela la ejecución actual y ahora hazlo asignando un volumen dentro de tu ordenador local para guardar las configuraciones que hagas en la herramienta y no se pierdan a medida que ejecutas el contenedor. Comando: docker run -p 8080:8080 -p 50000:50000 -v /var/jenkins_home jenkins/jenkins
docker run -p 32769 -p 50000:50000 -v /var/jenkins_home jenkins/jenkins
8. Para ingresar a Jenkins por primera vez es necesario tener a la mano la contraseña de administrador que se muestra en la consola de comandos que se muestra a medida que el contenedor se inicia. También la podrán encontrar posteriormente en el archivo que se crea en el volumen llamado /your/home/secrets/initialAdminPassword.
Ejecutamos el comando docker exec keen_herschel cat /var/jenkins_home/secrets/initialAdminPassword
Keen_herschel es el nombre del contenedor que se ha creado en la imagen jenkins/jenkins:lts
/var/jenkins_home/secrets/initialAdminPassword es el fichero donde se encuentra el password inicial para jenkins.
De esta forma puedes guardar el password en una variable de entorno y usarlo en un script, para acceder desde otra aplicación usando la API, etc.
JENKINS_InitialPassword=$(docker exec keen_herschel /var/jenkins_home/secrets/initialAdminPassword)


Integrar SonarQube en docker:
Vamos a necesitar dos imágenes Docker: una para el servidor SonarQube y otra para la base de datos, en este caso PostgreSQL. Concretamente, las imágenes que vamos a utilizar son la imagen oficial de SonarQube (sonarqube) y la imagen oficial de PostgreSQL (postgres).
https://hub.docker.com/_/sonarqube/ -> enlace a la imagen de sonarqube
https://hub.docker.com/_/postgres/ -> enlace a la imagen de postgres
Instalamos las imágenes:
docker pull sonarqube -> comando para instalar imágenes, que se encuentran en la página oficial de docker.
docker pull postgres
Instalación de SonarQube utilizando docker-compose:
Para facilitar la instalación de SonarQube en contenedores Docker vamos a utilizar el comando docker-compose up -d.
Se puede ver el fichero docker-compose.yaml que describe cómo se van a ejecutar los contenedores, pero primero hay que crearlo
Creamos el fichero docker-compose.yaml en una carpeta que creamos en C: llamada opt – Docker – sonar
En el cmd nos situamos en la carpeta del fichero docker-compose.yaml y ejecutamos el comando docker-compose up –d y nos instala sonar.

Integrar Nexus en docker:
https://hub.docker.com/r/sonatype/nexus/
docker pull sonatype/nexus
Para ejecutar (si el puerto 8081 está abierto en su host):
docker run –d –p 8081:8081 --name nexus sonatype/nexus:oss
Usando docker-compose:
Con docker-compose, vamos a poder configurar con más facilidad el Nexus, como por ejemplo, separar los datos del repositorio y llevarlo fuera del contenedor, de manera tal que si en algún momento se quiere actualizar a la última versión no se pierda la información. A continuación, el archivo de configuración de docker-compose que debe crearse.
Creamos en la carpeta opt – docker , una carpeta llamada nexus:
Creamos y añadimos el archivo docker-compose.yaml
Dentro de la carpeta nexus situada en opt – docker, ejecutamos el comando docker-compose up –d
