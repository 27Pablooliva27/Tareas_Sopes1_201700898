
##Actividad 3
#Utilizamos el comando sudo adduser usuario para la creacion de los usuarios
ablo@pablo-oliva:~$ sudo adduser usuario1
Añadiendo el usuario `usuario1' ...
Añadiendo el nuevo grupo `usuario1' (1001) ...
Añadiendo el nuevo usuario `usuario1' (1001) con grupo `usuario1' ...
Creando el directorio personal `/home/usuario1' ...
Copiando los ficheros desde `/etc/skel' ...
Nueva contraseña: 
Vuelva a escribir la nueva contraseña: 
passwd: contraseña actualizada correctamente
Cambiando la información de usuario para usuario1
Introduzca el nuevo valor, o presione INTRO para el predeterminado
	Nombre completo []: pablo
	Número de habitación []: 
	Teléfono del trabajo []: 
	Teléfono de casa []: 
	Otro []: 
¿Es correcta la información? [S/n] s
pablo@pablo-oliva:~$ sudo adduser usuario2
Añadiendo el usuario `usuario2' ...
Añadiendo el nuevo grupo `usuario2' (1002) ...
Añadiendo el nuevo usuario `usuario2' (1002) con grupo `usuario2' ...
Creando el directorio personal `/home/usuario2' ...
Copiando los ficheros desde `/etc/skel' ...
Nueva contraseña: 
Vuelva a escribir la nueva contraseña: 
passwd: contraseña actualizada correctamente
Cambiando la información de usuario para usuario2
Introduzca el nuevo valor, o presione INTRO para el predeterminado
	Nombre completo []: pablo
	Número de habitación []: 
	Teléfono del trabajo []: 
	Teléfono de casa []: 
	Otro []: 

¿Es correcta la información? [S/n] pablo@pablo-oliva:~$ 
pablo@pablo-oliva:~$ sudo adduser usuario3
Añadiendo el usuario `usuario3' ...
Añadiendo el nuevo grupo `usuario3' (1003) ...
Añadiendo el nuevo usuario `usuario3' (1003) con grupo `usuario3' ...
Creando el directorio personal `/home/usuario3' ...
Copiando los ficheros desde `/etc/skel' ...
Nueva contraseña: 
Vuelva a escribir la nueva contraseña: 
Las contraseñas no coinciden.
Nueva contraseña: 
Vuelva a escribir la nueva contraseña: 
Las contraseñas no coinciden.
Nueva contraseña: 
Vuelva a escribir la nueva contraseña: 
passwd: contraseña actualizada correctamente
Cambiando la información de usuario para usuario3
Introduzca el nuevo valor, o presione INTRO para el predeterminado
	Nombre completo []: pablo
	Número de habitación []: 
	Teléfono del trabajo []: 
	Teléfono de casa []: 
	Otro []: 
¿Es correcta la información? [S/n] s

#Utilizamos el comando sudo passwd usuario para colocarle una contrañe al usuario
pablo@pablo-oliva:~$ sudo passwd usuario1
Nueva contraseña: 
Vuelva a escribir la nueva contraseña: 
passwd: contraseña actualizada correctamente
pablo@pablo-oliva:~$ sudo passwd usuario2
Nueva contraseña: 
Vuelva a escribir la nueva contraseña: 
passwd: contraseña actualizada correctamente
pablo@pablo-oliva:~$ sudo passwd usuario3
Nueva contraseña: 
Vuelva a escribir la nueva contraseña: 
passwd: contraseña actualizada correctamente
#Utilizamos el comando id usuario para mostrar la información del usuario y a que grupom pertenece
pablo@pablo-oliva:~$ id usuario1
uid=1001(usuario1) gid=1001(usuario1) grupos=1001(usuario1)
pablo@pablo-oliva:~$ id usuario2
uid=1002(usuario2) gid=1002(usuario2) grupos=1002(usuario2)
pablo@pablo-oliva:~$ id usuario3
uid=1003(usuario3) gid=1003(usuario3) grupos=1003(usuario3)

#Utilizamos el comando sudo userdel usuario nos permitira eliminar el usuario seleccionado 
pablo@pablo-oliva:~$ sudo userdel usuario3
pablo@pablo-oliva:~$ sudo userdel usuario3
userdel: el usuario «usuario3» no existe

#Utilizamos el comando sudo groupadd grupo nos permitira crear un grupo nuevo para incluir usuarios 
pablo@pablo-oliva:~$ sudo groupadd grupo1
pablo@pablo-oliva:~$ sudo groupadd grupo2

#Utilizamos el comando sudo usermod -aG grupo usuario nos permite asignar usuarios a al grupo escrito
pablo@pablo-oliva:~$ sudo usermod -aG grupo1 usuario1
pablo@pablo-oliva:~$ sudo usermod -aG grupo2 usuario2

#Utilizamos el comando groups usuario nos permite visualizar a que grupos pertenece nuestru usuario
pablo@pablo-oliva:~$ groups usuario1
usuario1 : usuario1 grupo1
pablo@pablo-oliva:~$ groups usuario2
usuario2 : usuario2 grupo2

#Utilizamos el comando sudo groupdel grupo nos permite eliminar un grupo 
pablo@pablo-oliva:~$ sudo groupdel grupo2

#Utilizamos el comando su usuario para acceder al usuario creado y nos permita poder hacer configuraciones para ese usuario
pablo@pablo-oliva:~$ su usuario1
Contraseña: 

#Utilizamos el comando touch archivo1.txt nos permitira crear un archivo para el usuario que esta logueado
usuario1@pablo-oliva:~$ touch archivo1.txt

#Con el comando echo "Hola Mundo archivo 1" > archivo1.txt para escribir el contenido que tendra el archivo1.txt
usuario1@pablo-oliva:~$ echo "Hola Mundo archivo 1" > archivo1.txt

#Con el comando mkdir directorio1 crearemos el directorio donde almacenaremos los archivos que creemos
usuario1@pablo-oliva:~$ mkdir directorio1
usuario1@pablo-oliva:~$ touch directorio1/archivo2.txt

#Con el comando ls -l archivo1.txt visualizaremos los permisos que contiene el archivo
usuario1@pablo-oliva:~$ ls -l archivo1.txt
-rw-rw-r-- 1 usuario1 usuario1 21 ago  9 22:12 archivo1.txt

#Con el comando ls -ld directorio1 visualizaremos los permisos que contiene el directorio
usuario1@pablo-oliva:~$ ls -ld directorio1
drwxrwxr-x 2 usuario1 usuario1 4096 ago  9 22:12 directorio1

#Con el comando chmod 640 archivo1.txt realizaremos para configurar permisos en el archivo
usuario1@pablo-oliva:~$ chmod 640 archivo1.txt
usuario1@pablo-oliva:~$ chmod u+x directorio1/archivo2.txt

#Con el comando sudo chown :grupo1 directorio1/archivo2.txt cambiaremos el dueño del archivo 
usuario1@pablo-oliva:~$ sudo chown :grupo1 directorio1/archivo2.txt
drwxr-x--- 3 usuario1 usuario1 4096 ago  9 22:12 .
drwxr-xr-x 6 root     root     4096 ago  9 22:07 ..
-rw-r----- 1 usuario1 usuario1   21 ago  9 22:12 archivo1.txt
-rw-r--r-- 1 usuario1 usuario1  220 ago  9 22:06 .bash_logout
-rw-r--r-- 1 usuario1 usuario1 3771 ago  9 22:06 .bashrc
drwxrwxr-x 2 usuario1 usuario1 4096 ago  9 22:12 directorio1
-rw-r--r-- 1 usuario1 usuario1  807 ago  9 22:06 .profile
usuario1@pablo-oliva:~$ chmod 750 directorio1
usuario1@pablo-oliva:~$ ls -la
total 28
drwxr-x--- 3 usuario1 usuario1 4096 ago  9 22:12 .
drwxr-xr-x 6 root     root     4096 ago  9 22:07 ..
-rw-r----- 1 usuario1 usuario1   21 ago  9 22:12 archivo1.txt
-rw-r--r-- 1 usuario1 usuario1  220 ago  9 22:06 .bash_logout
-rw-r--r-- 1 usuario1 usuario1 3771 ago  9 22:06 .bashrc
drwxr-x--- 2 usuario1 usuario1 4096 ago  9 22:12 directorio1
-rw-r--r-- 1 usuario1 usuario1  807 ago  9 22:06 .profile

#Con el comando cat archivo1.txt mostraremos el contenido del archivo 
usuario1@pablo-oliva:~$ cat archivo1.txt
Hola Mundo archivo 1
usuario1@pablo-oliva:~$ cat directorio1/archivo2.txt 

#Con el comando ls -l visualizamos los permisos de los archivos y directorios que creamos antes y despues de los cambios de permisos y de dueños
usuario1@pablo-oliva:~$ ls -l
total 8
-rw-r----- 1 usuario1 usuario1   21 ago  9 22:12 archivo1.txt
drwxr-x--- 2 usuario1 usuario1 4096 ago  9 22:12 directorio1
usuario1@pablo-oliva:~$ ls -ld
drwxr-x--- 3 usuario1 usuario1 4096 ago  9 22:12 .
usuario1@pablo-oliva:~$ ls -l archivo1.txt
-rw-r----- 1 usuario1 usuario1 21 ago  9 22:12 archivo1.txt
usuario1@pablo-oliva:~$ ls -ld directorio1
drwxr-x--- 2 usuario1 usuario1 4096 ago  9 22:12 directorio1
