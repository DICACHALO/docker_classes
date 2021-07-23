**INSTALAR IMAGEN DOCKER NGINX**

1. Dirigirse a la siguiente página web para conocer detalles del proyecto:

https://hub.docker.com/_/nginx

2. Nos ubicamos en la terminal de ubuntu y escribimos los siguientes comandos:

```docker image build -t some-content-nginx .```

```docker-compose down```

```docker run --name some-nginx -d -p 8080:80 some-content-nginx```

```curl -k localhost:8080```

3. Creamos la carpeta donde vamos a almacenar la imagen Docker:

```mkdir mi-primer-dockerfile```

4. Una vez creada la carpeta nos ubicamos en ella:

```cd mi-primer-dockerfile/```

5. Creamos un archivo con el nombre Dockerfile:

```vim Dockerfile```

6. Se abrirá el editor, y dentro del archivo escribimos las siguientes lineas:

```FROM nginx```
```vCOPY static-html-directory /usr/share/nginx/html```

7. Guardamos con :wq

8. Creamos una nueva carpeta dentro de mi-primer-dockerfile:

```mkdir static-html-directory```

9. Nos ubicamos en esta nueva carpeta:

```cd static-html-directory/```

10. Creamos un nuevo archivo .html para visualizarlo en un navegador posteriormente:

```vim index.html```


11. Dentro de la terminal escribimos un mensaje de prueba y guardamos. Para asegurarnos de lo que escribimos:

```cat index.html```

12. Nos devolvemos a la carpeta principal mi-primer-dockerfile

```cd ..```

13. Ejecutamos el siguiente comando:

 sudo docker image build -t some-content-nginx .
 
 ![](https://drive.google.com/file/d/15k10wJlmmnRoinFOiDwNrxG58rPyu2Xb/view?usp=sharing)


```docker stop some-nginx```

```docker rm some-nginx```

Para borrar una imagen Docker:

```docker image rmi b3153cc68e1f```

COMMIT

https://docs.docker.com/engine/reference/commandline/commit/

```docker inspect nginx-final```

```docker stats nginx-final```


----

Poner en línea una imagen nuestra de Docker

1. Ingresar a https://hub.docker.com
2. Abrir una cuenta. El ID es un nombre de usuario.
3. En la terminal de ubuntu escribir:

```docker login```

4. Luego, el siguiente comando donde [tagname] es el ID

```docker tag local-image:tagname new-repo:tagname```


```docker push johnsebas94/fedesoft-web:tagname```

```image rm jsgiraldoh:fedesoft-web```

```image ls```

```tag some-content-nginx jsgiraldoh/fedesoft-web```

```push jsgiraldoh/fedesoft-web```

image rm jsgiraldoh:fedesoft-web

pull jsgiraldoh/fedesoft-web

run --name fedesoft-web -d -p 8081:80 jsgiraldoh/fedesoft-web


docker pull mxaxaxbx/fedesoft-web


----


Más información en:

https://issuu.com/johanse/docs/seccion-4-imagenes-y-contenedores.pptx

https://hub.docker.com/r/dicachalo/fedesoft-web