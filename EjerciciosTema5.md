
# Ejercicios Tema 5 #

### Ejercicio 1: Instalar los paquetes necesarios para usar KVM. Se pueden seguir estas instrucciones. Ya lo hicimos en el primer tema, pero volver a comprobar si nuestro sistema está preparado para ejecutarlo o hay que conformarse con la paravirtualización. ###

Vamos a probar a instalar kvm por si en este tiempo he formateado la máquina virtual donde tengo instalado Ubuntu. En primer lugar utilizamos el comando:

    sudo apt install -y qemu-kvm libvirt-bin

![](capturas/instalacionkvm.png)

A continuación podemos añadir usuarios al grupo de kvm para poder crear máquinas virtuales.

    sudo adduser antoniomfc90 kvm

![](capturas/aniadiruser.png)
