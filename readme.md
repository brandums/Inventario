# README #

Este README, cuenta con los pasos para levantar en ambientes de desarrollo la App de Inventario, desarrollado con Python v3.9 y Django v4.1.2

## APP DE INVENTARIO ##
### Requisitos ###

* Python 3.9.11 o superior

### Pasos ###

* Crear entorno virtual
* Instalar los requirements para la App.
```commandline
pip install -r requirements.txt
```
* Correr la App 
```commandline
python manage.py runserver
```
### Usuario de prueba ###
```commandline
username: usertest
password: 4rch12022
```
### Url de acceso en el Navegador
```commandline
http://localhost:8000/inventario
```
### Django REST Framework
* EndPoint Tipo de Productos
```commandline
Method: [GET]
Url: http://localhost:8000/api/producto/tipoproducto/
Response:
[
    {
        "id": 1,
        "tipoproducto": "Grifo lavamanos",
        "descripcion": "mezclador"
    },
    {
        "id": 2,
        "tipoproducto": "Grifo lavaplatos",
        "descripcion": "solo agua fria"
    },
    {
        "id": 3,
        "tipoproducto": "Azalea",
        "descripcion": "Juego completo"
    }
]
```
* EndPoint Categoria de productos
```commandline
Method: [GET]
Url: http://localhost:8000/api/producto/categoria/
Response:
[
    {
        "id": 1,
        "categoria": "Griferia",
        "descripcion": "Fv"
    },
    {
        "id": 2,
        "categoria": "Inodoros",
        "descripcion": "Celite"
    }
]
```
* Productos
```commandline
Method: [GET]
Url: http://localhost:8000/api/producto/producto/
Response:
[
    {
        "id": 1,
        "categoria": {
            "id": 1,
            "categoria": "Griferia",
            "descripcion": "Fv"
        },
        "categoria_id": 1,
        "tipoproducto": {
            "id": 1,
            "tipoproducto": "Grifo lavamanos",
            "descripcion": "mezclador"
        },
        "tipoproducto_id": 1,
        "producto": "Grifo lavamanos",
        "descripcion": "mezclador",
        "imagen": "http://localhost:8000/media/productos/grifolavamanos.jpg",
        "stock": 12,
        "precio": "75.00",
        "estado": true
    },
    {
        "id": 2,
        "categoria": {
            "id": 2,
            "categoria": "Inodoros",
            "descripcion": "Celite"
        },
        "categoria_id": 2,
        "tipoproducto": {
            "id": 3,
            "tipoproducto": "Azalea",
            "descripcion": "Juego completo"
        },
        "tipoproducto_id": 3,
        "producto": "Azalea",
        "descripcion": "Juego completo",
        "imagen": "http://localhost:8000/media/productos/inodoro.jpg",
        "stock": 23,
        "precio": "320.00",
        "estado": true
    }
]
```