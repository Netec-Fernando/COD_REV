# Capitulo 5: ¿Cómo se realiza una revisión del código?

## Objetivos
Al finalizar la práctica, serás capaz de:
- Familiarizarse con el Proceso de Revisión de Código
- Gestionar Repositorios Remotos y Locales
- Realizar Pull Requests y Revisiones de Código
- Aplicar Buenas Prácticas de Revisión de Código

## Objetivo Visual 
Crear un diagrama o imagen que resuma las actividades a realizar, un ejemplo es la siguiente imagen. 

![diagrama1](../images/cap4/7.png)

## Duración aproximada:
- 25 minutos.

## Tabla de ayuda:
Agregar una tabla con la información que pueda requerir el participante durante el laboratorio, como versión de software, IPs de servers, usuarios y credenciales de acceso.
| Requisito | Descripcion|
| --- | --- |
| Repositorio de GitHub | Acceso al repositorio [Netec cap5](https://github.com/mfperdomo09/netec-cap5.git). |
| GitHub Account | Cuenta activa para acceder al repositorio y revisar pull requests. |
| GitHub Desktop | Herramienta opcional para clonar y gestionar el repositorio localmente. |
| Repositorio Clonado Localmente | Clonar el repositorio localmente para una revisión más detallada si es necesario. |
| Documento de Evaluación | Herramienta para documentar las observaciones (puede ser un archivo de texto o similar). Formato en seccion documentos correspondiente a este capitulo |

## Instrucciones 
<!-- Proporciona pasos detallados sobre cómo configurar y administrar sistemas, implementar soluciones de software, realizar pruebas de seguridad, o cualquier otro escenario práctico relevante para el campo de la tecnología de la información -->
### Tarea 1. Descripción de la tarea a realizar.
Paso 1. Clonar el repositorio en nuestro equipo en local

![Logo](../images/cap5/21.png)

Copiamos la url del repositorio

        git clone <url repositorio>

![Logo](../images/cap5/1.png)

En la terminal escribimos "git clone url_repositorio" clonara todo el proyecto

Paso 2. Agregamo el repositorio clonado a la herramienta de github desktop

![Logo](../images/cap5/2.png)

Ya que es un repositorio inicializado lo hacecmos desde "Add existing repository" de esta forma se conservaran los commits y ramas que hay

![Logo](../images/cap5/3.png)

Buscamos la ruta donde clonamos en el repositorio

![Logo](../images/cap5/4.png)

Cambiamos entre ramas para que se guarden en el local

Paso 3. Ahora vamos a remover el enlace remoto de este repositorio de la cuenta que se bajo, esto con el fin de que lo podamos subir a nuestra cuenta

        git branch

![Logo](../images/cap5/5.png)

Primero usamos el comando "git branch" para verificacar que las ramas ya se cargan desde el local

        git remote -v
        git remote remove origin

![Logo](../images/cap5/6.png)

Luego usamos el comando "git remote -v" para verificar el nombre de la conexion con la otra cuenta en este caso origin, despues "git remote remove origin" para quitar la conexion

        git branch

![Logo](../images/cap5/7.png)

Luego usamos nuevamente el comando "git branch y podemos ver que las ramas persiten"

![Logo](../images/cap5/8.png)

Volvemos a github desktop y vemos que se nos hanilito la opcion de publicar repositorio, lo publicamos

![Logo](../images/cap5/9.png)

Cambiamos el nombre y agregamos descripcion si se desea y damos click a "Publish repository"

Paso 4.  Ahora desde nuestra cuenta de github ingresamos al repositorio

![Logo](../images/cap5/10.png)

Vemos que se subieron las ramas y estan listas para hacer pull request

Paso 5.  Creamos el pull request para cada una de las ramas

![Logo](../images/cap5/11.png)

Ingresamos a la seccion de pull request y damos a "New Pull request"

![Logo](../images/cap5/12.png)

Seleccionamos la rama

![Logo](../images/cap5/13.png)

Damos click a "Create pull request" despues de seleccionar la rama

![Logo](../images/cap5/14.png)

Damos click a "create pull request"


Paso 6. Hacemos la revision del codigo segun los estandares definidos en el readme

![Logo](../images/cap5/15.png)

Desde la seccion de "Files chnaged" podremos visualizar los cambios los cambios propuestos para el pull request que iran a nuestra rama principal.

![Logo](../images/cap5/16.png)

Al encontrar algo que no valla bien seleccionaremos la linea y escribiremos el comentarios correspondiente, agregando la posible mejora y el por que no esta cumpliendo, se dara click a "Start review"

![Logo](../images/cap5/17.png)

Cuando finalice la review en este caso si la pull request no cumple con los estandares daremos click a "Review changes" para que nuestros comentarios sean publicados y finalmente damos a "Submit review"

![Logo](../images/cap5/18.png)

En caso de que el pull request cumpla, en la seccion de "Comments" iremos a la secion aprobacion y daremos click a "Merge pull request" para iniciar el proceso de unificacion de cambios

![Logo](../images/cap5/19.png)

Damos a click "Confirm merge", con esto finalizaria el proceso de revision.

### Resultado esperado
En un documento documentar el como se hizo la revision, aprobacion y merge del pr en caso que aplique.

![imagen resultado](../images/cap5/22.png)
