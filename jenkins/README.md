# Jenkis 
El pipeline automatiza el proceso de construcción y despliegue de la aplicación, desde la descarga del código fuente hasta la actualización de los manifiesto de Kubernetes. 

El pipeline está definido en el archivo ‘jenkinsfile’ y consta de varias etapas, cada una de las cuales realiza un paso específico en el proceso de  CI/CD. 

**Etapa 1.** clonar el repositorio de github donde se encuentra el código fuente de proyecto. 

**Etapa 2.** Construir la imagen Docker para la aplicación. 

**Etapa 3.** Subir la imagenes Docker a Docker Hub.

**Etapa 4.** Aplicar los manifiesto de kubernetes para desplegar la aplicación
