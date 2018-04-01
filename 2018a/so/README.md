## Miniproyecto Sistemas Operativos

**Universidad ICESI**  
**Curso:** Sistemas Operativos  
**Docente:** Daniel Barragán C.  
**Tema:**  LXC/LXD Containers  
**Correo:** daniel.barragan at correo.icesi.edu.co

## Objetivos
* Conocer las caracteristicas principales de la virtualización por medio de contenedores LXC/LXD
* Virtualizar servicios empleando contenedores LXC/LXD
* Realizar configuraciones sobre sistemas operativos para el acceso a servicios (network, load balancing)

## Descripción
Deberá realizar el despliegue de dos servidores web y un balanceador de carga por medio de contenedores LXC/LXD.
Puede elegir el sistema operativo a emplear para la máquina virtual y los contenedores, se sugiere Ubuntu 16.04.4 LTS (xenial).

![][1]  
**Figura 1.** Esquema básico para el despliegue

## Actividades
* Nombre y código de todos los integrantes del grupo (máximo 3) (5%)
* Ortografía y redacción (5%)
* Aproviosionamiento básico de máquina virtual: instalación de sistema operativo, configuración de interfaces de red, minimo 4 núcleos (10%)
* Instalación de LXC/LXD con permisos para el usuario operativos. (10%)
  * Indique los comandos empleados y su descripción
  * Indique que es un **storage pool** y cuales son las ventajas de emplear **ZFS** como sistema de archivos.
  * Explique los valores por defecto de la configuración de un puente LXD (LXD bridge configuration)
* Creación de contenedores con servicio web (tenga en cuenta que son dos contenedores web) (10%)
    * Instalación y configuración del servicio web
    * Validación de que el servicio web activo (usar systemctl)
    * Recuerde que puede diagnosticar errores en la carga de un servicio por medio del comando **journalctl -xe**
    * Página html que despliegue un mensaje que identifique el servicio web correspondiente
    * Asignar un procesador único para cada servicio web
* Creación de contenedor con servicio de balanceo de carga (10%)
    * Instalación y configuración del balanceador para redireccionar las peticiones entrantes hacia los servicios web
    * Configuración del balanceador para recibir conexiones remotas
    * Validación de que el servicio para conexion remota y el balanceador esten activos (usar systemctl)
    * Recuerde que puede diagnosticar errores en la carga de un servicio por medio del comando **journalctl -xe**
* Salida del comando lxc list con los contenedores creados y sus direcciones IP (10%)
* Pruebas del funcionamiento del balanceador (20%)
    * Muestre por medio del uso del comando curl la respuesta de cada uno de los servicios web a través del balanceador
    * Por medio de una herramienta de test de stress (siege, ab, otros) evalue el desempeño del sistema con las siguientes configuraciones:
      * Servidores web con 64Mb, 128Mb
      * Servidores web con 50%CPU, 100%CPU
* Configure el reenvio de puertos en la máquina virtual para permitir el acceso desde el sistema anfitrión hacia del contenedor con el servicio
para balanceo de carga (10%)
* El informe debe ser entregado en formato README.md y debe ser subido a un repositorio de github. El repositorio de github debe ser un fork de https://github.com/ICESI-Training/so-project y para la entrega deberá hacer un Pull Request (PR) respetando la estructura definida. El código fuente y la url de github deben incluirse en el informe (10%).

## Opcional
* Creación de contenedores por demanda: (?%)
  * Configure un adaptador nictype: macvlan, de tal modo que los contenedores reciban una ip de la red local
  * Por medio de pyxld cree una aplicación de consola que permita la creación y eliminación de contenedores, tenga en cuenta
realizar los cambios necesarios en los archivos de configuración de los contenedores para permitir el acceso remoto por ssh
* Preguntas ramdom: (?%)
  * Al reiniciar la máquina virtual en que estado quedan los contenedores?

## Recomendaciones
* Puede incluir como evidencias de lo realizado capturas de pantalla o la salida del comando en formato markdown
* Cuando realice los cambios sobre los recursos hardware asignados a cada servicio puede realizar la validación a través de algunos de los siguientes comandos:
  * watch free -h
  * top (presionando la tecla h obtendrá una ayuda con opciones)
* En lo posible use zsh/tmux

## Referencias
* https://www.digitalocean.com/community/tutorials/how-to-set-up-and-use-lxd-on-ubuntu-16-04
* https://linuxcontainers.org/lxd/
* https://github.com/lxc/lxd
* https://github.com/lxc/pylxd
* https://stgraber.org/2016/03/11/lxd-2-0-introduction-to-lxd-112/
* https://stgraber.org/2016/03/26/lxd-2-0-resource-control-412/
* https://www.digitalocean.com/community/tutorials/an-introduction-to-load-testing
* http://pylxd.readthedocs.io/en/latest/usage.html
* https://www.computersnyou.com/3047/forward-port-lxc-container-quick-tip/
* https://www.youtube.com/watch?v=3f57PovdY44
* https://www.digitalocean.com/community/tutorials/how-to-list-and-delete-iptables-firewall-rules
* https://stgraber.org/2016/04/18/lxd-api-direct-interaction/
* https://github.com/dobin/lxd-webgui

[1]: images/LXC_Project.png
