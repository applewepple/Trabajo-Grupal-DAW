---
author: Diego, Velasco y Frisuelos
title: redes
---

# Almacenamiento

[TOC]

### Ejercicio 1

Pantallazos donde se vean los contenedores creados y en ejecución 

```bash
docker run -d --name mariaDB --network redbd -e MYSQL_ROOT_PASSWORD=root -v /home/applewepple/Escritorio/almacen;/var/lib/mysql -p 3306:3306 mariadb
docker run --network redbd --link mariaDB:mari -p 8080:8080 adminer
docker ps -a
```

![1.-mariaBD](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Redes\imágenes\1.-mariaBD.JPG)

![2.-adminer](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Redes\imágenes\2.-adminer.JPG)

![3.-contenedores en ejecucion](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Redes\imágenes\3.-contenedores en ejecucion.PNG)

### Ejercicio 2

Pantallazo donde se vea el acceso a la BD a través de la interfaz web de `Adminer` 

![4.-accesobd](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Redes\imágenes\4.-accesobd.JPG)

### Ejercicio 3

Pantallazo donde se vea la creación de una BD con la interfaz web `Adminer` 

![5.1-creacionbd](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Redes\imágenes\5.1-creacionbd.JPG)

![5.2-creaciobd2](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Redes\imágenes\5.2-creaciobd2.JPG)

### Ejercicio 4

Pantallazo donde se entre a la consola del servidor web en modo texto y se compruebe que se ha creado la BD 

```bash
docker exec -it mariaDB bash -c 'mysql -uroot -p$MYSQL_ROOT_PASSWORD'
show databases
```

![6.-mostrar bd desde terminal](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Redes\imágenes\6.-mostrar bd desde terminal.JPG)

### Ejercicio 5

Borrar los contenedores, la red y los volúmenes utilizados

```bash
docker rm $(docker ps -a -q)
docker network rm redbd
docker rm -v almacen
```

![7.-borrar](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Redes\imágenes\7.-borrar.JPG)