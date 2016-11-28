# Ejercicios hito 4 #

### Ejercicio 1: Instala LXC en tu versión de Linux favorita. Normalmente la versión en desarrollo, disponible tanto en GitHub como en el sitio web está bastante más avanzada; para evitar problemas sobre todo con las herramientas que vamos a ver más adelante, conviene que te instales la última versión y si es posible una igual o mayor a la 1.0. ###

He instalado la versión 2.0.5 de **LXC**
![](capturas/lxcversion.png)

### Ejercicio 2: Comprobar qué interfaces puente se han creado y explicarlos. ###

Para comprobar las interfaces primero arrancamos la máquina y accedemos a ella.

![](capturas/comienzoprimercaja.png)

Para ver las interfaces usamos el comando:

    ifconfig -a

![](capturas/comprobacioninterfaces.png)

eth0 (Ethernet) es la interfaz de red. Es utilizada para tener acceso a internet.

La segunda interfaz es lo (loopack) y sirve para comunicarse con nuestro sistema y los demás contenedores.
