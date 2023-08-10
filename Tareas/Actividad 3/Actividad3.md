# Actividad 3

## Creación de Usuarios


### Descripción de comandos
```
Utilizamos el comando `sudo adduser usuario` para la creación de los usuarios:
pablo@pablo-oliva:~$ sudo adduser usuario1
...
pablo@pablo-oliva:~$ sudo adduser usuario2
...
Asignación de Contraseñas
Utilizamos el comando sudo passwd usuario para colocarle una contraseña al usuario:

bash
Copy code
pablo@pablo-oliva:~$ sudo passwd usuario1
...
pablo@pablo-oliva:~$ sudo passwd usuario2
...
Información del Usuario y Grupos
Utilizamos el comando id usuario para mostrar la información del usuario y a qué grupo pertenece:

bash
Copy code
pablo@pablo-oliva:~$ id usuario1
...
pablo@pablo-oliva:~$ id usuario2
...
Eliminación de Usuarios
Utilizamos el comando sudo userdel usuario para eliminar el usuario seleccionado:

bash
Copy code
pablo@pablo-oliva:~$ sudo userdel usuario3
...
Creación de Grupos
Utilizamos el comando sudo groupadd grupo para crear un grupo nuevo:

bash
Copy code
pablo@pablo-oliva:~$ sudo groupadd grupo1
...
pablo@pablo-oliva:~$ sudo groupadd grupo2
...
Asignación de Usuarios a Grupos
Utilizamos el comando sudo usermod -aG grupo usuario para asignar usuarios a un grupo:

bash
Copy code
pablo@pablo-oliva:~$ sudo usermod -aG grupo1 usuario1
...
pablo@pablo-oliva:~$ sudo usermod -aG grupo2 usuario2
...
Visualización de Grupos de Usuarios
Utilizamos el comando groups usuario para visualizar a qué grupos pertenece nuestro usuario:

bash
Copy code
pablo@pablo-oliva:~$ groups usuario1
...
pablo@pablo-oliva:~$ groups usuario2
...
Eliminación de Grupos
Utilizamos el comando sudo groupdel grupo para eliminar un grupo:

bash
Copy code
pablo@pablo-oliva:~$ sudo groupdel grupo2
...
Acceso al Usuario y Configuraciones
Utilizamos el comando su usuario para acceder al usuario creado y hacer configuraciones:

bash
Copy code
pablo@pablo-oliva:~$ su usuario1
...
Creación y Manipulación de Archivos y Directorios
Utilizamos comandos como touch, echo, mkdir, ls, chmod, chown, y cat para crear, modificar y visualizar archivos y directorios.

bash
Copy code
usuario1@pablo-oliva:~$ touch archivo1.txt
usuario1@pablo-oliva:~$ echo "Hola Mundo archivo 1" > archivo1.txt
usuario1@pablo-oliva:~$ mkdir directorio1
usuario1@pablo-oliva:~$ touch directorio1/archivo2.txt
...
