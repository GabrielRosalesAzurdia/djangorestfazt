# Recuerdo de Django Rest Framework CRUD fazt

Este es un pequeño proyecto implementado un crod con la ayuda de djangorestframework

Para instalar el framework es

> pip install djangorestframework

También recordar que debe agregarse a la lista de apps y que se deben correr 
migraciones

## Serializers

Creamos un archivo serializers.py donde le decimos que datos van a poser ser 
consultados y cuales datos son solo de lectura

## Viewset

Permite declara quien puede consultar un serializer

craemos un archivo api.py y allí creamos los viewsets necesarios
Llevan 3 cosas, la primera es el queryset, que son los datos a manejar
la segunda son los permisos ya que podemos definir si solo el admin enctra
o cualquier otra persona también puede netrar y por último 
también definimos en serializer que es el serializer que creamos anteriormente

## Rutas

Para las rutas importarémos de rest framework los routers

> from rest_framework import routers

El router sirve para crear un set de ruts por defecto por ejemplo 
ya un sistema de crud y ya solo regitramos la ruta principal, al final
extraemos las rutas y las colocamos en un urls

## Thunder client

Utilizamos thunder client para hacer peticiones a una api en específico la 
que estamos codificando y podemos instalarlo como un addon para visual studio
lo cual hace todo más sencillo pues todo está en un solo lugar

## NOTAS

El viewset crea ya todas las vistas de put get delete path etc haciendo métodos
por defecto a todas estas, si querémos utilizar personalizadas tenemos 
que buscar otra manera o editar los viewsets

## Despliege - Render

Los pasos son los mismos

1) creamos un repositorio de git ignorando la base de datos db.sql3
2) alteramos el archivo settings.py
3) creamos el build.sh
4) creamos los requisitos de pip
5) setiamos el build, instalamos gunicorn y actualizamos el requirements

## posible error

si nos sale un error con django al momento de desplegar debemos
cambiar la versión de django en el requirements.txt a 4.0 y la versión
de python a 3.8.4 por ejemplo la versión de python es en las variables
 de entorno junto con la variable de la conexión a labase de datos+
 y la variable de la llave secreta