# docker_classes
Training notes with FEDESOFT

***Archivo docker-compose***

1. Crear carpeta proxy

mkdir proxy

2. Crear archivo docker-compose.yml 
3. Agreagar dentro de ese archivo lo siguiente:

version: '3'
services:
  web:
    image: dockercloud/hello-world
  lb:
    image: dockercloud/haproxy
    links:
      - web
    volumes:
      - /var/run/docker.sock:/var/run/docker.sock
    ports:
      - 80:80

4. Levantar el contenedor

`docker-composer up -d`

5. Listar contenedores

`docker-composer ps`

6. Ver información de los contenedores

`docker info`

7. Bajar el contenedor

`docker-composer down`

Dar escalabilidad creando varios contenedores que responden las peticiones.

`docker-compose up --scale "servicio"=#contenedores -d`

`docker-compose up --scale web=5 -d`


*** INSTALAR JENKINS ***

1. Clonar el proyecto 

git clone https://github.com/jsgiraldoh/Jenkins

2. cd Jenkins
3. Realizar los siguientes comandos

docker-compose -f docker-compose-jenkins.yml up -d

sudo chown ubuntu:ubuntu jenkins_home/

sudo chmod 2777 jenkins_home/

4. Abrir el navegador con la ip y el puerto 8090
5. Digitar la contraseña
6. Instalar plugins sugeridos
7. El correo solicitado debe ser con gmail
