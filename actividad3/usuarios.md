### Gestion de Usuarios
- - - - 

#### Creacion de Usuarios 

```
    sudo useradd usuario1
    sudo useradd usuario2
    sudo useradd usuario3

```
![Creacion de Usuarios](/actividad3/images/1.png)


#### Asignacion de Contrasenas

```
    sudo passwd usuario1
    sudo passwd usuario2
    sudo passwd usuario3

```

![Creacion de Usuarios](/actividad3/images/2.png)

#### Informacion de Usuarios

```
    id usuario1
```

![Creacion de Usuarios](/actividad3/images/3.png)

#### Gestion de Grupos

```
    sudo groupadd grupo1
    sudo groupadd grupo2

    sudo usermod -aG grupo1 usuario1
    sudo usermod -aG grupo2 usuario2

    groups usuario1
    groups usuario2

    sudo groupdel grupo2

```

![Creacion de Usuarios](/actividad3/images/4.png)

#### Gestion de Permisos

```
    su usuario1

    echo "Contenido de prueba" > archivo1.txt
    mkdir directorio1
    echo "Contenido del segundo archivo" > directorio1/archivo2.txt

    ls -l archivo1.txt
    ls -ld directorio1

    chmod 640 archivo1.txt

    chmod u+x directorio1/archivo2.txt

    sudo chown :grupo1 directorio1/archivo2.txt

    chmod 744 directorio1

    su usuario2

    cat /home/usuario1/archivo1.txt
    cat /home/usuario1/directorio1/archivo2.txt

    ls -l /home/usuario1/archivo1.txt
    ls -l /home/usuario1/directorio1/archivo2.txt
    ls -ld /home/usuario1/directorio1


```

![Creacion de Usuarios](/actividad3/images/5.png)

![Creacion de Usuarios](/actividad3/images/6.png)


##### ¿Por qué es importante gestionar correctamente los usuarios y permisos en un sistema operativo?
- - - -

Es crucial para garantizar la seguridad del sistema, mantener la privacidad de la información, y para asegurar que los usuarios tengan acceso solo a los recursos necesarios para cumplir con sus funciones.

##### ¿Qué otros comandos o técnicas conocen para gestionar permisos en Linux?
- - - -
(1) setfacl y getfacl: Para establecer y obtener listas de control de acceso en archivos y directorios.
(2) chown: Para cambiar el propietario de un archivo o directorio.
(3) chgrp: Para cambiar el grupo de un archivo o directorio.
(4) umask: Establece los permisos predeterminados para nuevos archivos y directorios.