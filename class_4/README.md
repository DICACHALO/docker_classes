# docker_classes
Training notes with FEDESOFT

docker-compose up --scale web=5 -d

docker-compose down

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
