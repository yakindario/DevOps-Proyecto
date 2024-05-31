# Docker 
En este punto, realice los siguiente punto: 
- Utilicé contenedores Docker para empaquetar y distribuir la aplicación backend y frontend, junto con todas sus dependencias.
- Definí Dockerfiles para construir imágenes de contenedor optimizadas y 
- Utilicé Docker Compose para orquestar contenedores en entornos locales de desarrollo y pruebas.
- Subí las imágenes al registro de Docker Hub.

En nuestra configuración está compuesta con la siguientes  componentes:  
- Frontend: Desarrollado en React y ejecutado en Node. js. 
- Backend: API desarrollado en flask  usando Python. 

![Docker](/doc/Docker.png)

Como se muestra en la imagen, utilizamos Nginx como un proxy inverso para manejar eficientemente las peticiones de los usuarios.
- Nginx redirige las peticiones para la interfaz de usuario (desarrollada en React) al servidor que corre en el puerto 5173. 
- Nginx redirige las peticiones para la API (desarrollada en Flask) al servidor que corre en el puerto 5000.

Para cada aplicación de  flask y react de node, tiene su propio archivo en dockerfile, lo puedes encontrar en la carpeta de api, y web. 

Para poder ejecutar el docker composer  utiliza el siguiente comando:

    docker compose up -d --build 

Para visualizar la web ingrese al siguiente sitio: 

http://localhost/ [](http://localhost/)

--- 
## Imagen Docker hub
Cada imagen de Docker ya ha sido construida y subida a Docker Hub. Puedes ejecutarlas desde el directorio de Docker en tu máquina local.

Para iniciar los contenedores, ingrese en la carpeta de Docker y utiliza el siguiente comando:

    docker compose up -d --build 

Para visualizar la web ingrese al siguiente sitio:

http://localhost/ [](http://localhost/)
