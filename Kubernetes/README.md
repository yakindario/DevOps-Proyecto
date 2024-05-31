# Kubernetes

En este punto pude realizar lo siguiente:

- Implementé Kubernetes para orquestar y administrar los contenedores en un entorno de producción.
- Definí y desplegué manifiestos de Kubernetes (archivos YAML) para desplegar y escalar la aplicación en clústeres de Kubernetes.

![kubernetes](/doc/Kuberntes.jpg)

Como se muestra en la imagen, este es el diseño de Kubernetes utilizado para la implementación en producción de la aplicación:

- **Ingreso (ing):** El componente de ingreso se encarga de gestionar el tráfico de red que llega desde el exterior del clúster Kubernetes. Redirige el tráfico a los servicios adecuados dentro del nodo.
- **Service api:** Este servicio expone y administra el tráfico dirigido a la API de la aplicación.
- **Deployment:** Gestiona y asegura que un número especificado de instancias de la API (contenedores) se estén ejecutando en el clúster. Facilita la actualización y el escalado de la aplicación.

Para poder ejecutar la aplicación de kubernetes utilice el siguiente comando:

    kubectl apply -f Deployment-flask.yml
    kubectl apply -f Service-flask.yml
    kubectl apply -f Deployment-react.yml
    kubectl apply -f Service-react.yml
    kubectl apply -f Ingress.yml

Para mejorar la seguridad se creó los pods para tener el certificado de SSL para https, la configuración se encuentra en YAML,para la ejecución de kubernetes.

Con el archivo yaml ejecuta el siguiente comando:

    kubectl apply -f letsencrypt-issuer.yml 
    kubectl apply -f yakindario-tls-certificate.yml 

Para poder verificar los pods, utilice el siguiente comando:
 
    kubectl get all

Para ver los servicios 

    kubectl get svc 

**NOTA:** para poder utilizar ingress se tiene que activar el ingress de kubernetes.


