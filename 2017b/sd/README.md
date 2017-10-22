### Proyecto
**Universidad ICESI**  
**Curso:** Sistemas Distribuidos  
**Docente:** Daniel Barragán C.  
**Tema:** Introducción a Kubernetes  
**Correo:** daniel.barragan at correo.icesi.edu.co

### Objetivos
* Relacionar conceptos aprendidos sobre balanceo de carga y
descubrimiento de servicio con tecnologías para la orquestación
de contenedores virtuales
* Diagnosticar y ejecutar de forma autónoma las acciones necesarias para lograr infraestructuras estables

### Prerrequisitos
* Cluster de Kubernetes

### Descripción
Deberá realizar el despliegue de un Pod con al menos un servicio web que se ejecute en el framework de su preferencia. La especificación del deployment debe cumplir con los siguientes requerimientos:

* Cantidad de replicas: 3
* Asignar una etiqueta que identifique al Pod

La especificación del servicio debe mapear un puerto de cada Pod a un balanceador de carga, de esta manera la aplicación desplegada debe poder ser accedida a través de un navegador o cliente de consola (curl, wget)

**Nota:**
Deberá demostrar que ante la caída de uno de los nodos que forman parte del cluster, los Pods son reasignados automáticamente a un nodo saludable

**Opcional:**
Plantee e implemente una estrategia para el monitoreo de los contenedores (Pods) puede emplear alguna de las siguientes tecnologías: kubernetes health checks, efk stack, cadvisor, otros.

### Actividades
1. Documento en formato PDF:  
  * Formato PDF (5%)
  * Nombre y código de los integrantes del grupo (5%)
  * Ortografía y redacción (5%)
2. Consigne los comandos de linux necesarios para el aprovisionamiento de los servicios empleados. En este punto no debe incluir archivos tipo Dockerfile solo se requiere que usted identifique los comandos o acciones que debe automatizar (15%)
3. Escriba los archivos Dockerfile para los servicios empleados junto con los archivos fuente necesarios, en el caso de emplear una imagen de docker hub debe incluir una explicación de lo realizado en el Dockerfile del repositorio de github. Tenga en cuenta consultar buenas prácticas para la elaboración de archivos Dockerfile. (20%)
4. Escriba los archivos de configuración necesarios deployment.yml, service.yml para el despliegue de la infraestructura (10%). Incluya un diagrama general de los componentes empleados.
5. El informe debe publicarse en un repositorio de github el cual debe ser un fork de https://github.com/ICESI-Training/sd-project y para la entrega deberá hacer un Pull Request (PR) respetando la estructura definida. El código fuente y la url de github deben incluirse en el informe (15%). Tenga en cuenta publicar los archivos para el aprovisionamiento
6. Incluya evidencias que muestran el funcionamiento de lo solicitado (15%)
7. Documente algunos de los problemas encontrados y las acciones efectuadas para su solución al aprovisionar la infraestructura y aplicaciones (10%)

### Referencias
http://labs.play-with-k8s.com/  
https://kubernetes.io/docs/setup/independent/install-kubeadm/  
https://kubernetes.io/docs/user-guide/walkthrough/k8s201/  
https://kubernetes.io/docs/concepts/workloads/controllers/deployment/  
https://kubernetes.io/docs/tasks/access-application-cluster/list-all-running-container-images/  
https://kubernetes.io/docs/user-guide/kubectl-cheatsheet/  
https://kubernetes.io/docs/tutorials/kubernetes-basics/explore-intro/  
https://kubernetes.io/docs/user-guide/walkthrough/  
https://kubernetes.io/docs/tutorials/stateless-application/hello-minikube/  
https://github.com/kubernetes/kops  
https://github.com/kubernetes/minikube/releases  
https://github.com/kubernetes/community/blob/master/contributors/design-proposals/README.md  
https://github.com/kubernetes/kubeadm/issues/42  
https://damyanon.net/post/flask-series-logging/
