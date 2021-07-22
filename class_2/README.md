**Instalar Docker Engine en Ubuntu**
----


1. Una vez ubicados en la terminal, actualizar los paquetes

```sudo apt-get update```

2. Instalar los paquetes para permitir el uso de un repositorio sobre HTTPS

sudo apt-get install \ 
apt-transport-https \ 
ca-certificates \ 
curl \ 
gnupg-agent \ 
software-properties-common


3. Agregar la clave GPG oficial de Docker

```curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -```

4. Agregar los repositorios estables de Docker

echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null


5. Actualizar los paquetes relacionados con los repositorios del sistema

 ```sudo apt-get update```
 
6. Instalar la versión para la comunidad, conocido como Docker CE.
 
 ```sudo apt-get install docker-ce docker-ce-cli containerd.io```

7. Verificar la correcta instalación de Docker

```docker --version```

8. Para correr un primer contenedor:

 ```sudo docker run hello-world```


Más información en: 

https://docs.docker.com/engine/install/ubuntu/

https://jsgiraldoh.io/Blog/Instalar-Docker-Engine-en-Ubuntu/