# Repositorio remoto con Github Desktop

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Conectar y configurar GitHub Desktop con una cuenta de GitHub.
- Realizar y verificar pull requests desde GitHub.
- Sincronizar cambios entre el repositorio local y el repositorio remoto después de un pull request

## Objetivo Visual 
Crear un diagrama o imagen que resuma las actividades a realizar, un ejemplo es la siguiente imagen. 

![diagrama1](../images/cap2/28.png)

## Duración aproximada:
- 20 minutos.

## Tabla de ayuda:
Agregar una tabla con la información que pueda requerir el participante durante el laboratorio, como versión de software, IPs de servers, usuarios y credenciales de acceso.
| Requisito | Descripcion|
| --- | --- |
| GitHub Desktop | Instalado en el sistema operativo. |
| GitHub Account | Cuenta activa en GitHub para sincronización. |
| Repositorio Local | Un repositorio Git previamente configurado en local. |

## Instrucciones 
<!-- Proporciona pasos detallados sobre cómo configurar y administrar sistemas, implementar soluciones de software, realizar pruebas de seguridad, o cualquier otro escenario práctico relevante para el campo de la tecnología de la información -->
### Tarea 1. Descripción de la tarea a realizar.
Paso 1. Conectar nuestra cuenta de github con la version de escritorio

![Logo](../images/cap2/1.png)

![Logo](../images/cap2/2.png)

Seleccionamos la opcion "Sign into Github.com" esto nos abrira el navegador

![Logo](../images/cap2/3.png)

Aqui si no hemos iniciado sesion, nos pedira que lo hagamos, finalmente damos a "Continue"

Paso 2.  Ingresamos a la opcion "Add existing repository"

![Logo](../images/cap2/4.png)

Paso 3. Buscamos la ubicacion de la carpeta en la cual inicializamoes el repositorio damos a "Add repository".

![Logo](../images/cap2/5.png)

Paso 4.  Ahora en el listado de repositorios podemos ver que nuestro repositorio fue agregado a la herramienta de forma correcta.

![Logo](../images/cap2/6.png)

Paso 5. En la parte superior encontraremos la opcion de "Publish repository" damos click, esto creara el repositorio en nuestra cuenta de github

![Logo](../images/cap2/7.png)

Paso 6. Despues debes llenar la informacion que se nos solicita, nombre, descripcion y escoger el tipo de visualizacion, publico o privado y damos click a "Publish repository"

![Logo](../images/cap2/8.png)

Paso 7. Verificamos el listado de repositorios de nuestro github y veremos que se ha creado correctamente, con el historial de cambios que ya teniamos y codigo

![Logo](../images/cap2/9.png)

Paso 8. Desde github desktop crearemos una rama donde agregaremos primero el readme.md, despues en un nuevo commit el .gitignore donde crearemos un .env

## readme.md
```
    ## Run Locally

    Clone the project

    ```bash
    git clone https://link-to-project
    ```

    Go to the project directory

    ```bash
    cd my-project
    ```

    Install dependencies

    ```bash
    npm install
    ```

    Start the server

    ```bash
    npm run start
    ```
```

![Logo](../images/cap2/10.png)

Creamo el archivo readme y agregamos el contenido que deseemos

![Logo](../images/cap2/11.png)

Hacemos commit del archivo agregado y hacemos click en "Commit to main"

## .gitingore

```
    .env
```

![Logo](../images/cap2/12.png)

creamos los archivos .env el cual puede ir y el gitnore den esteblecemos la ruta del .env

![Logo](../images/cap2/13.png)

Notaremos que el .env ya sera seguido por git, por lo que procedemos a hacer commit del gitgnore

Paso 9. Ahora con el boton con el cual anteriormente realizamos la subida del repositorio, haremos la subida de los cambios hechos

![Logo](../images/cap2/14.png)

De esta forma si revisamos el repositorio remoto notaremos que el readme y gitignore fueron cargados, pero que el .env fue ignorado

Paso 10. Crearemos una nueva rama

![Logo](../images/cap2/16.png)

![Logo](../images/cap2/17.png)

Establcemos el nombre a la rama

Paso 11. Haremos nuevos cambios al archivo html y haremos commit de estos

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

        <h2>Otro cambio desde la rama creada con github desktop</h2>
    </body>
</html>
```

![Logo](../images/cap2/18.png)

![Logo](../images/cap2/19.png)

Hacemos commit de los cambios

Paso 12. Publicamos la rama con sus cambios

![Logo](../images/cap2/15.png)

Esto hara que en github en la seccion de ramas aparezaca la rama en la que estabamos trabajando

![Logo](../images/cap2/20.png)

Paso 13. Procedemos a hacer un pull request desde la web de github

![Logo](../images/cap2/20.png)

Ingresamo al apartado de pull request y damos click a "New Pull Request"

![Logo](../images/cap2/21.png)

En el select "compare" seleccionamos la rama en la que trabajamos, esta sera la rama que se unira con nuestra rama principal, damos a "Create pull request"

![Logo](../images/cap2/22.png)

Agregamos informacion adicional, como cambiar el nombre del pull request y una descripcion, damos click a "Create pull request"

![Logo](../images/cap2/23.png)

Desde aqui se podra verificar si el cambio fue aprovado si han comentadao sugerencia y quienes lo hiciero, damos a "Merge pull request" y "Confirm merge"

![Logo](../images/cap2/24.png)

Una vez hecho el merge del pull request podemos eliminar la rama si no se seguira trabajando con ella

Paso 14. Volvemos al github desktop y vamos a bajar los cambios hechos por el merge request

![Logo](../images/cap2/25.png)

Nos aseguramos que estamos en la rama main y desde el mismo boton donde hicimos subida de repo  y cambios, haremos click pero esta vez verificara si hay cambios por bajar que no tengamos en nuestro local.

![Logo](../images/cap2/26.png)

Podemos ver que da nos dice que hay dos cambios pendientes por bajar, si recuedan hicimos un commit en la anterior rama, el otro haria referencia a la union del codigo por el merge request le damos click esto bajara los cambios.



### Resultado esperado
Desde el editor podemos ver que todos los cambios que hicimos en la rama anterior se unificaron

![Logo](../images/cap2/27.png)
