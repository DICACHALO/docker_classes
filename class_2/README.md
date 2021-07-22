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

```sudo docker --version```

8. Instalar docker composer
9. Comprobar correcta instalación de docker composer

```docker-compose version```

10. Para correr un primer contenedor:

 ```sudo docker run hello-world```


**Para facilitar la comunicación entre Windows y una máquina virtual Linux en VirtualBox**

1. Descargar mobaxterm 

https://mobaxterm.mobatek.net/download-home-edition.html

2. En ubuntu instalar openssh-server

```sudo apt-get install openssh-server```

3. Investigar la ip de ubuntu

```Ip a s```

**Usar herramienta CodiMD**

```git clone https://github.com/jsgiraldoh/Codimd.git```

```sudo docker-compose up -d```

```sudo docker container ls```

Para visualizar la aplicación en un navegador usamos la ip y el puerto 3000. Por ejemplo: 192.168.1.104:3000

```Ip:3000```

```sudo docker-compose up -d```

```sudo systemctl enable docker```

```sudo systemctl status docker```

```sudo systemctl stop docker```

Ejemplo: sudo usermod -aG docker ubuntu

```sudo usermod -aG docker “usuario”```

```Systemctl reboot```


**ESTRUCTURA DE COMANDOS DOCKER**

docker --help

docker container ls

docker image ls

docker container stop codimd_codimd_1

docker container start 523811282c26

docker ps -a

docker container restart codimd_codimd_1

docker logs -f codimd_codimd_1

----

Más información en: 

https://docs.docker.com/engine/install/ubuntu/

https://docs.docker.com/compose/install/

https://jsgiraldoh.io/Blog/Instalar-Docker-Engine-en-Ubuntu/

https://www.youtube.com/watch?v=-4CkPurTCMU

https://jsgiraldoh.io/Blog/Estructura-de-comandos/