# Capitulo 7: Configuracion herramienta revision de codigo

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Configurar correctamente la protección de la rama principal de un repositorio en GitHub.
- Invitar y gestionar colaboradores en el repositorio.
- Practicar el proceso completo de revisión de código, incluyendo la creación de pull requests, revisión, solicitud de cambios y aprobación final.

## Objetivo Visual 
Crear un diagrama o imagen que resuma las actividades a realizar, un ejemplo es la siguiente imagen. 

![diagrama1](../images/cap7/18.png)

## Duración aproximada:
- 20 minutos.

## Tabla de ayuda:
Agregar una tabla con la información que pueda requerir el participante durante el laboratorio, como versión de software, IPs de servers, usuarios y credenciales de acceso.
| Requisito | Descripcion|
| --- | --- |
| GitHub Account | Cuenta activa para acceder al repositorio y revisar pull requests. |
| GitHub Desktop | Herramienta opcional para clonar y gestionar el repositorio localmente. |
| Laragon | Herramienta para iniciar servicios de PHP, Apache y MySQL. |
| Composer | Utilizado para instalar Laravel y sus dependencias. Incluido en laragon |
| Editor de Código | Recomendado para modificar archivos (ej. Visual Studio Code). |
| Terminal/Comando CLI | Necesario para ejecutar comandos de Git y Laravel. |
| PHP8 y MySQL | Lenguaje y base de datos utilizados en el proyecto Laravel. Incluidos en laragon |
| Correo Electrónico | Acceso al correo electrónico asociado a la cuenta de GitHub para aceptar la invitación como colaborador y recibir notificaciones sobre las revisiones. |
| Permisos de Propietario | Permisos necesarios en GitHub para configurar la protección de ramas y gestionar pull requests en el repositorio. |
| Documento de Evaluación | Herramienta para documentar las observaciones (puede ser un archivo de texto o similar). Formato en seccion documentos correspondiente a este capitulo |

## Instrucciones 
<!-- Proporciona pasos detallados sobre cómo configurar y administrar sistemas, implementar soluciones de software, realizar pruebas de seguridad, o cualquier otro escenario práctico relevante para el campo de la tecnología de la información -->
### Tarea 1. Descripción de la tarea a realizar.

> [!IMPORTANT]
> En esta actividad el compañero invitado al repositorio sera el autor del codigo y quien invito sera quien hara la revision o el revisor.

paso 1. Invitaremos como colaborador a uno de nuestros compañeros al repositorio que creamos en la actividad del anterior capitulo

![Logo](../images/cap7/1.png)

Ingresamos al apartodo "settings" de nuestro repositorio y damos click a "Collaborators"

![Logo](../images/cap7/2.png)

Damos click a "Add peoplo"

![Logo](../images/cap7/3.png)

Buscamos el nombre de usuario github de nuestro compañero, lo seleccionamos y agregamos dando click "Add 'user' to this repository"

A nuestro compañero le llegara una email al correo de su cuenta de github el cual debera aceptar para poder ingresar al repo

paso 2. Nuestro compañero clonara el repositorio en su maquina y lo agregara en github desktop

        git clone <url repositorio>

![Logo](../images/cap5/1.png)

![Logo](../images/cap5/2.png)

![Logo](../images/cap5/3.png)

paso 3. Ya que nuestro compañero tiene acceso como colaborador, podra hacer cambios, primero crear una rama y publicarla

![Logo](../images/cap2/16.png)

![Logo](../images/cap2/17.png)

Nombre a la rama

![Logo](../images/cap2/15.png)

Publicar la rama

paso 4.  Una vez creada la rama en el editor de codigo buscar el archivo "resource/views/user/index.blade.php", para realizar una pequeña modificacion, y hacer commit y push para que este en el remoto.

paso 5.  Despues haremos pull request a la rama principal del repo que nos dieron acceso.

paso 6. El dueño del repositorio podra visualizar el pull request y aprobarlo, dando por finalizada esta primera parte.

paso 7. Como segunda parte, el dueño de cada repositorio creara una regla para la rama principal, esto con el fin de limitar las pull request a la rama principal


![Logo](../images/cap7/4.png)

En la seccion de "setting" del repositorio, daremos click a "Branchs"

![Logo](../images/cap7/5.png)

Luego al boton "Add classic branch protection rule", aqui podremos las opciones de configuracion para las ramas

![Logo](../images/cap7/6.png)

* Luego en la nueva vista, escribimos la rama que queremos proteger, en este caso "master"
* Seleccionamos "Require pull request before mergin", esto hara que sea necesario si o si una pull request para hacer merge con la rama principal
* "Require approvals" en este caso seleccionamos 1, tener en cuenta que aplica solo si no hay cambios pendientes en la revision

![Logo](../images/cap7/7.png)

* "Require conversation resolition before merging", con esta opcion es obligatorio que todas la solicitudes hechas por el revisor en lineas de codigo sean resueltas

Finalmente se da click a "Create"

![Logo](../images/cap7/8.png)

Esto nos llevara nuevamente a la configuracion de las ramas, donde vemos que se a aplicado una regla.

paso 8. Ahora que ya aplicamos una regla para nuestra rama, nuestro compañero que tiene acceso a nuestro repositorio, creara una rama en la que hara cambios simulando un error y hara pull request de este cambio.

![Logo](../images/cap7/9.png)

Ahora notaremos nostros como autor del cambio que no podemos aprobar el pull request y en la seccion de reviewers esta seleccionado por defecto el dueño del repositorio, por lo que es necesario de la aprobacion de el

![Logo](../images/cap7/10.png)

En caso de haber mas miembros de equipo podriamos cambiar el reviewer o agregar a otros

Por lo que en este momento debemos esperar a que nuestro compañero dueño del repositorio haga su revision

paso 9. El dueño del repositorio hara la revision desde "file changed", este caso como se busca simular un error, se debera comentar el fragmento de codigo y enviar la revision

![Logo](../images/cap7/11.png)

El dueño del repositorio, comentara el fragmento de codigo que simula como error

![Logo](../images/cap7/12.png)

Despues finalizara la revision agregando un comentario y seleccionando la opcion de "request changes", haciendo referencia a solicitud de cambios, finalmente dando click a "Submit review"

![Logo](../images/cap7/13.png)

Ahora veremos en la seccion "comments" que ahora la seccion de "No unresolved conversations", ya no es valida como al inicio ya que tambien hay cambios pendiente.

Por lo que se tendra que resolver dicho cambio, para poder marcar la revision como aprobada y asi hacer el merge.

paso 10. El autor del cambio, ahora desde local tendra que cambiar la linea solicitada y hacer push de ese cambio.

paso 11. El autor del cambio, en la seccion de comentarios comentara que esta listo y lo marcara como resuelto desde "Resolve conversation"

![Logo](../images/cap7/14.png)

De esta forma cerraremos la solicitud de cambios

paso 12. Una vez que este el cambio solicitado, el dueño del repo podra verificar desde "files changed" nuevamente, y en este caso aprobar el pull request.

![Logo](../images/cap7/15.png)

![Logo](../images/cap7/16.png)

Y notaremos tanto autor como dueño, que ya estan habilitadas las opciones de merge, por que se resolvio la solicitud de cambios, y se aprobo el pull request desde la revision.

paso 13. Ya que se aprobo ya sea el dueño o el autor de los cambios podra hacer el merge para unificar los cambios con la rama principal

> [!NOTE]
> Cabe recalcar que todo este proceso de solicitud de cambios sera notificado en las cuentas de correo, las solicitudes de cambio, los comentarios y la aprobacion.

### Resultado esperado
Documento en el que se evidenciara el como realizo el ajuste de ramas para la seguridad del pull request y revision de codigo obligatorio. Como tambien evidencia del proceso de revision de codigo.
![imagen resultado](../images/cap7/17.png)
