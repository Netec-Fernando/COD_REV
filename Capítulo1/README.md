# GIT repositorio

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Configurar la información básica del usuario en Git.
- Crear un repositorio Git desde cero e inicializarlo en un proyecto.
- Crear y gestionar ramas en Git para desarrollar nuevas funcionalidades.

## Objetivo Visual 
Crear un diagrama o imagen que resuma las actividades a realizar, un ejemplo es la siguiente imagen. 

![diagrama1](../images/cap1/21.png)

## Duración aproximada:
- 28 minutos.

## Tabla de ayuda:
Agregar una tabla con la información que pueda requerir el participante durante el laboratorio, como versión de software, IPs de servers, usuarios y credenciales de acceso.
| Requisito | Descripcion|
| --- | --- |
| Git | Git instalado en el sistema operativo. |
| Editor Codigo | Un editor de texto como VSCode, Sublime Text, o similar. |
| Terminal | Acceso a la terminal de comandos del sistema. |

## Instrucciones 
<!-- Proporciona pasos detallados sobre cómo configurar y administrar sistemas, implementar soluciones de software, realizar pruebas de seguridad, o cualquier otro escenario práctico relevante para el campo de la tecnología de la información -->
### Tarea 1. Descripción de la tarea a realizar.
Paso 1. Tener configurado la informacion de usuario

        git config --global user.name "nombre"

        git config --global user.email emai@email.cmo

![Logo](../images/cap1/1.png)

![Logo](../images/cap1/2.png)

        git config --list

![Logo](../images/cap1/3.png)


> [!TIP]
> Tener en cuenta que el email sea el mismo en caso de manejar cuenta de github

Paso 2. En una carpeta creamos un archivo html, en este se podria unicamente establecer una estructura html basica

```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <h1>Usando Git</h1>
    </body>
    </html>
```

![Logo](../images/cap1/6.png)

Paso 3. Por medio de la terminal inicializar el repositorio

        git init

![Logo](../images/cap1/7.png)

Paso 4. con el siguiente comando podemos visualizar que git ya esta haciendo seguimiento a nuestro archivos.

        git status

![Logo](../images/cap1/8.png)

Paso 5. Con el siguiente comando agregaremos el archivo al area de stage para hacer commit

        git add .

![Logo](../images/cap1/9.png)

Paso 6. Usando status se podra verificar que ya no esta el archivo en el registro de cambios pendientes

        git status

![Logo](../images/cap1/10.png)

Paso 7. Proceder a realizar commit despues de agregar el archivo al stage

        git commit -m "Initial commit"

![Logo](../images/cap1/11.png)

Paso 8. Ahora procedemos a crear una rama y verificamos que halla hecho correctamente

        git branch feature/list
        git branch

![Logo](../images/cap1/13.png)

Paso 9. cambiamos a la rama creada y modificamos el html con una lista o otro contenido

        git checkout feature/list
        git branch

![Logo](../images/cap1/14.png)

```html
    <!DOCTYPE html>
    <html lang="en">
    <head>
        <meta charset="UTF-8">
        <meta name="viewport" content="width=device-width, initial-scale=1.0">
        <title>Document</title>
    </head>
    <body>
        <h1>Usando Git</h1>

        <br>

        <h2>Tecnologias</h2>

        <ul>
            <li>HTML</li>
            <li>CSS</li>
            <li>JavaScript</li>
            <li>PHP</li>
        </ul>
    </body>
    </html>
```
![Logo](../images/cap1/15.png)

Paso 10. agregamos los cambios al area de stage y hacemos commit del cambio

        git add .
        git commit -m "add list"

![Logo](../images/cap1/16.png)

Paso 11. cambiamos a la rama master y hacemos merge con la rama creada anteriormente

        git checkout master
        git merge feature/list

![Logo](../images/cap1/17.png)

Paso 12. despues de unificados los cambios eliminamos la rama anteriormente creada

        git branch -d feature/list

![Logo](../images/cap1/19.png)

### Resultado esperado
Una vez eliminada podemos podemos verificar que los cambios aun percisten, lo que significa que todo el proceso fue realizado de forma corracta

        git log

![Logo](../images/cap1/20.png)
