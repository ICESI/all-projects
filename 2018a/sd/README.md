## Miniproyecto Sistemas Distribuidos

**Universidad ICESI**  
**Curso:** Sistemas Distribuidos  
**Docente:** Daniel Barragán C.  
**Tema:**  Kubernetes  
**Correo:** daniel.barragan at correo.icesi.edu.co

### Objetivos
* Identificar los componentes de un cluster de kubernetes
* Desplegar un cluster de kubernetes
* Desplegar aplicaciones en un cluster de kubernetes empleando sus propiedades
de volumenes persistentes, balanceo de carga y descubrimiento de servicio
* Diagnosticar y ejecutar de forma autónoma las acciones necesarias para lograr infraestructuras estables

### Prerrequisitos
* Computador personal, Sala de computo

### Descripción
Debera realizar el despliegue de un cluster de kubernetes en al menos tres nodos independientes (un nodo maestro y al menos dos nodos de trabajo). Para ello realice la instalación y configuración de las dependencias necesarias (kubeadm, kubectl, kubelet), y el despliegue de los pods de red necesarios para la comunicación. Todo el proceso debera ser debidamente documentado

Para la prueba del funcionamiento del cluster deberá realizar el despliegue de un pod con al menos un servicio web que se ejecute en el framework de su preferencia. La especificación del deployment debe cumplir con los siguientes requerimientos:

* Cantidad de replicas: 3
* Asignar una etiqueta que identifique al pod

La especificación del servicio debe mapear un puerto de cada pod a un balanceador de carga, de esta manera la aplicación desplegada debe poder ser accedida a través de un navegador o cliente de consola (curl, wget)

**Opcional:**
* Plantee e implemente una estrategia para el monitoreo de los contenedores (Pods) puede emplear alguna de las siguientes tecnologías: kubernetes health checks, efk stack, cadvisor, otros.
* Plantee e implemente una estrategia para la automatización de la conexión a través de tokens

**Nota**
* No se requiere que incluya archivos de la automatización del cluster o infraestructura base.
* El empleo de tecnologías de automatización para la infraestructura base es a consideración del estudiante

### Actividades
1. Documento en formato PDF:  
  * Formato PDF (5%)
  * Nombre y código de los integrantes del grupo (5%)
  * Ortografía y redacción (5%)
2. Consigne la documentación que incluya los comandos de linux necesarios para el aprovisionamiento del cluster de kubernetes
  * Instalación y configuración de kubeadm, kubectl, kubelet (10%)
  * Instalación y configuración de un pod de red que interconecte los pods a desplegar en el cluster (20%)
  * Evidencias del despliegue del servicio solicitado ejecutandose correctamente en los nodos del cluster. Deberá demostrar que ante la caída de uno de los nodos que forman parte del cluster, los pods son reasignados automáticamente a un nodo saludable. Incluya los archivos: deployment.yml, service.yml empleados (15%)
4. El informe debe publicarse en un repositorio de github el cual debe ser un fork de https://github.com/ICESI-Training/sd-project y para la entrega deberá hacer un Pull Request (PR) respetando la estructura definida. El código fuente y la url de github deben incluirse en el informe (15%). Tenga en cuenta publicar los archivos para el aprovisionamiento
5. Incluya evidencias que muestran el funcionamiento de lo solicitado (15%)
6. Documente algunos de los problemas encontrados y las acciones efectuadas para su solución al aprovisionar la infraestructura y aplicaciones (10%)
