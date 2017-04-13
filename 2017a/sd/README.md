## Miniproyecto Sistemas Distribuidos

**Universidad ICESI**  
**Curso:** Sistemas Operativos  
**Docente:** Daniel Barragán C.  
**Tema:**  Despliegue automático de un espejo  
**Correo:** daniel.barragan at correo.icesi.edu.co

## Objetivos
* Emplear herramientas de aprovisionamiento automático para la realización de tareas en infraestructura
* Instalar y configurar espejos de sistemas operativos en forma automática para el soporte al aprovisionamiento de máquinas virtuales en clústers de computo
* Especificar y desplegar ambientes conformados por contenedores virtuales para la realización de tareas específicas

### Nota Importante
El parcial podrá realizarse en grupos de tres personas máximo, en caso de encontrar copia a otros compañeros se anulará su proyecto. Podrá usar cualquier material de clase o realizar consultas en Internet. Una vez termine su proyecto se le pedirá que realice la respectiva sustentación de su solución, esta sustentación tendrá un factor de 0 a 1 sobre el valor de cada ítem de evaluación.

## Descripción
En ambientes conformados por cantidades considerables de nodos como es el caso de clústers de computo, se requiere contar con mecanismos eficientes para la actualización y despliegue de nueva infraestructura.

Para este proyecto deberá realizar el aprovisionamiento automático de un espejo por medio de las herramientas vistas en clase. Debe cumplir con los siguientes requerimientos:

* El espejo debe ser del sistema operativo ubuntu-xenial
* Debe especificar por medio de un arreglo los paquetes a instalar
* No es necesario que genere llaves nuevas cada vez que despliegue el espejo, puede crearlas previamente y precargarlas en la solución de aprovisionamiento automático a emplear
* Probar por medio del despliegue de uno o varios contenedores que el mirror ha sido correctamente desplegado

### Actividades
En un documento en formato PDF cuyo nombre de
archivo debe ser proyecto_codigoestudiante.pdf debe incluir lo siguiente:

1. Documento en formato PDF:  
  * Formato PDF (5%)
  * Nombre y código de los integrantes del grupo (5%)
  * Ortografía y redacción (5%)
2. Consigne los comandos de linux necesarios para el aprovisionamiento de los servicios solicitados. En este punto no debe incluir archivos Vagrantfile, Dockerfile u otro tipo de fuentes, solo se requiere que usted identifique los comandos o acciones que debe automatizar (15%)
3. Consigne los archivos empleados para el aprovisionamiento automático del espejo, tenga en cuenta agregar comentarios al código con una breve descripción de cada paso (Vagrantfile, Dockerfile y demás fuentes) (20%)
4. Consigne los archivos empleados para la prueba del espejo (Vagrantfile, Dockerfile y demás fuentes) (10%)
5. Publicar en un repositorio de github los archivos para el aprovisionamiento junto con un archivo de extensión .md donde explique brevemente como verificar que su solución cumple con lo solicitado (15%)
6. Incluya evidencias que demuestren que su solución cumple con lo solicitado (15%)
7. Documente algunos de los problemas encontrados y las acciones efectuadas para su solución al aprovisionar la infraestructura y aplicaciones (10%)

## Referencias
https://atlas.hashicorp.com/boxesio/boxes/xenial64-chef  
https://serverfault.com/questions/478268/how-do-you-execute-a-command-in-the-background-with-a-chef-recipe-on-windows  
http://stackoverflow.com/questions/16975299/override-the-chef-bash-return-code  
https://www.aptly.info/tutorial/mirror/
