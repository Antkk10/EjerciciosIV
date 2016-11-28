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

### Ejercicio 3: ###

#### 1. Crear y ejecutar un contenedor basado en Debian. ####

Para instalar debian en el contenedor:

    sudo lxc-create -t debian -n tercera-caja-debian
    
#### 2. Crear y ejecutar un contenedor basado en otra distribución, tal como Fedora. Nota En general, crear un contenedor basado en tu distribución y otro basado en otra que no sea la tuya. Fedora, al parecer, tiene problemas si estás en Ubuntu 13.04 o superior, así que en tal caso usa cualquier otra distro. Por ejemplo, Óscar Zafra ha logrado instalar Gentoo usando un script descargado desde su sitio, como indica en este comentario en el issue. ####

He instalado centos, para ello primeros instalamos **yum**

    sudo apt-get install -y yum

Creamos el contenedor:

    sudo lxc-create -t centos -n segunda-caja-centos

Para establecer la contraseña debemos de introducir este comando:

    sudo chroot /var/lib/lxc/caja_centos/rootfs passwd

Por último iniciamos el contenedor y accedemos a el:

    sudo lxc-start -n segunda-caja-centos
    sudo lxc-console -n segunda-caja-centos


![](capturas/conectamoscentos.png)
