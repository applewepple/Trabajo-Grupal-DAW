---
author: Diego, Velasco y Frisuelos
title: ejercicio de redes
---

[TOC]

# Almacenamiento

### Ejercicio 1

Pantallazo con la orden correspondiente para arrancar el contenedor `c1` (puerto 8181) realizando el `bind mount` solicitado

```bash
docker run -d --name c1 --mount type=bind,src=/home/sergio/Escritorio/saludo,dst=/var/www/html -p 8181:80 php:7.4-apache
```

![1.-c1 creacion](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Almacenamiento\imágenes\1.-c1 creacion.JPG)



### Ejercicio 2

Pantallazo con la orden correspondiente para arrancar el contenedor `c2` (puerto 8282) realizando el `bind mount` solicitado

```bash
docker run -d --name c1 --mount type=bind,src=/home/sergio/Escritorio/saludo,dst=/var/www/html -p 8181:80 php:7.4-apache
```

![2.-c2 creacion](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Almacenamiento\imágenes\2.-c2 creacion.JPG)



### Ejercicio 3

Pantallazo donde se pueda apreciar que accediendo a `c1` se puede ver el contenido de `index.html`

![3.-index c1 sin modificar](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Almacenamiento\imágenes\3.-index c1 sin modificar.JPG)



### Ejercicio 4

Pantallazo donde se pueda apreciar que accediendo a `c2` se puede ver el contenido de `index.html`

![4.-index c2 sin modificar](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Almacenamiento\imágenes\4.-index c2 sin modificar.JPG)



### Ejercicio 5

Otros dos pantallazos donde se vea el acceso al fichero `index.html` después de modificarlo

![5.-c1 index modificao](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Almacenamiento\imágenes\5.-c1 index modificao.JPG)

![6.-c2 index modificao](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Almacenamiento\imágenes\6.-c2 index modificao.JPG)



### Ejercicio 6

Borrar los dos contenedores. Mostrar que se han borrado

```bash
docker rm -f c1
docker rm -f c2
```

![7.-contenedores borrados](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Almacenamiento\imágenes\7.-contenedores borrados.JPG)