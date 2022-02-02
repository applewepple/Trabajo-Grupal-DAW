---
author: Diego y Sergios
title: trabajando con imagenes
---

# Servidor web

### Ejercicio 1

Pantallazo que desde el navegador muestre el fichero `index.html` 

```bash
docker run -d --name web -p 8000:80 php:7.4-apache
docker exec -it web bash
(desde dentro del contenedor 'web'){
    echo "<h1>Hola, somos XXXXXXXXXXXXX</h1>" > index.html
    apt-get update
    apt-get install nano
    nano index.html
}
```

![1.-crear contenedor php](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\1.-crear contenedor php.png)

![2.-crear index en el directorio](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\2.-crear index en el directorio.png)

![3.-modificar index.html](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\3.-modificar index.html.png)

![4.-index desde nav](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\4.-index desde nav.png)

### Ejercicio 2

Pantallazo que desde un navegador muestre la salida del script `mes.php` 

```bash
touch mes.php
nano mes.php
```

![5.-crear mes.php](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\5.-crear mes.php.png)

![6.-mostrar mes](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\6.-mostrar mes.png)

![7.-mostrando mes nav](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\7.-mostrando mes nav.png)

### Ejercicio 3

Pantallazo donde se vea el tamaño del contenedor `web` después de crear los dos ficheros. 

```bash
docker system df
```

![8.-tamaño contenedor web](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\8.-tamaño contenedor web.png)



# Servidor de base de datos

### Ejercicio 1

Pantallazo donde desde un cliente de base de datos (instalado en tu ordenador) se pueda observar que hemos podido conectarnos al servidor de base de datos con el usuario creado y que se ha creado la base de datos `prueba` ( `show databases` ). El acceso se debe realizar desde el ordenador que tenéis instalado `docker`, no hay que acceder desde dentro del contenedor, es decir, no usar `docker exec`. 

```bash
docker run --name bbdd -e MYSQL_ROOT_PASSWORD=root -e MARIADB_USER=invitado -e MARIADB_PASSWORD=invitado -e MARIADB_DATABASE=prueba -d -p 3336:3336 mariadb
docker run --name myadmin -d --link bbdd:db -p 8080:80 phpmyadmin
```

![9.-conexion base de datos invitado](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\9.-conexion base de datos invitado.JPG)

![10.-conexion base de datos invitado 2](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\10.-conexion base de datos invitado 2.JPG)

### Ejercicio 2

Pantallazo donde se comprueba que no se puede borrar la imagen `mariadb` mientras el contenedor `bbdd` está creado.

```bash
docker rmi mariadb
```

![11.-borrar imagen](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Trabajo con Imágenes\imágenes\11.-borrar imagen.JPG)

