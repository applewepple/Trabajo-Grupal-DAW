---
author: Sergio Frisuelos, Sergio Rodríguez, Diego García
title: Ejercicio inicial del Trabajo Grupal
---

[TOC]

# Ejercicio Inicial

## Parte 1

**Pantallazo  donde  se  vea  la  creación  del  contenedor  y  podamos  comprobar  que  el**
**contenedor está funcionando**

```bash
docker run -d --name servidorNginx -p 8080:80 nginx
docker ps -a
```

![1.-creacion contenedor](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Inicial\imágenes\1.-creacion contenedor.png)

## Parte 2

**Pantallazo  donde  se  vea  el  acceso  al  servidor  web  utilizando  un  navegador  web**
**(recuerda  que  tienes  que  acceder  a  la  ip  del  ordenador  donde  tengas  instalado**
**Docker)**

![2.-acceso por web](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Inicial\imágenes\2.-acceso por web.png)

## Parte 3

**Pantallazo donde se vean las imágenes que tienes en tu registro local**

```bash
docker images
```

![3.-imagenes utilizadas](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Inicial\imágenes\3.-imagenes utilizadas.png)

## Parte 4

**Pantallazo donde se vea cómo se elimina el contenedor (recuerda que antes debe**
**estar parado el contenedor)**

```bash
docker rm servidorNginx
```

![4.-eliminar contenedor](C:\Users\apple\Desktop\trabajo-grupal-daw-final\Ejercicio Inicial\imágenes\4.-eliminar contenedor.png)

