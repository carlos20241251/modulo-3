# modulo-3
practica I
sudo nano /etc/default/grub

grub_timeout=5 cambiarlo a 20

despues ctrl + x para guardar y despues

despues el comando: sudo update-grub

Esto hará que el menú de GRUB se muestre
durante 20 segundos antes de arrancar
automáticamente el sistema operativo
predeterminado.

reinicia el sistema sudo reboot
selecciona la opcion avance options
o edita a entrada con la tecla e

despues  al final del codigo que empieza
con  Linux agrega  init=/bin/bash
despues presio na ctrl + x

una vez dentro : mount -n -o remount,rw /
cambia la contraseña de usuario con
passwd root

despues de cambiar la contraseña
exec /sbin/init
despues su - para confirmar contraseña

PRACTICA II

nano ip_save.sh

#!/bin/bash

# Preguntar nombre del archivo
echo "Ingrese el nombre que desea para el archivo:"
read NOMBRE

# Definir ruta al escritorio del usuario actual
ESCRITORIO="/home/$(whoami)/Escritorio"

# Guardar salida de ip addr en el archivo
ip addr > "$ESCRITORIO/$NOMBRE.txt"

# Confirmación
echo "Archivo creado en: $ESCRITORIO/$NOMBRE.txt"
 ctrl + o enter y ctrl +x 
permisos de ejecucion 
chmod +x ip_save.sh

./ip_save.sh
cuando pida nombre escribe red 
verificar  contenido
cat /home/lavoe/Escritorio/red.txt
