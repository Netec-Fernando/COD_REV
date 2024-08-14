# Práctica 7. Configuración de la herramienta revisión de código

## Objetivo de la práctica:
Al finalizar la práctica, serás capaz de:
- Configurar correctamente la protección de la rama principal de un repositorio en GitHub.
- Invitar y gestionar colaboradores en el repositorio.
- Practicar el proceso completo de revisión de código, incluyendo la creación de pull requests, revisión, solicitud de cambios y aprobación final.

## Objetivo Visual 

![diagrama1](../images/cap7/18.png)

## Duración aproximada:
- 20 minutos.

## Tabla de ayuda:

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
| Documento de Evaluación | Herramienta para documentar las observaciones (puede ser un archivo de texto o similar). Formato en seccion documentos correspondiente a este capítulo. |

## Instrucciones 

> [!IMPORTANT]
> En esta actividad, el compañero invitado al repositorio será el autor del código y, quien invitó, será quien realizará la revisión o el revisor.

paso 1. Invita como colaborador a uno de nuestros compañeros al repositorio que creaste en la actividad del anterior capítulo.

![Logo](../images/cap7/1.png)

Ingresa al apartado **"Settings"** de tu repositorio y damos clic a **"Collaborators"**.

![Logo](../images/cap7/2.png)

Da clic a **"Add people"**.

![Logo](../images/cap7/3.png)

Busca el nombre de usuario GitHub de tu compañero, selecciónalo y agrégalo dando clic en **"Add 'user' to this repository"**.

A tu compañero recibirá una email al correo de su cuenta de GitHub, el cual deberá aceptar para poder ingresar al repositorio.

Paso 2. Tu compañero deberá clonar el repositorio en su máquina y lo agregará en GitHub Desktop.

        git clone <url repositorio>

![Logo](../images/cap5/1.png)

![Logo](../images/cap5/2.png)

![Logo](../images/cap5/3.png)

Paso 3. Una vez que tu compañero tenga acceso como **Colaborador**, podrá hacer cambios. Primero, crear una rama y publicarla.

![Logo](../images/cap2/16.png)

![Logo](../images/cap2/17.png)

Proporciónale un nombre a la rama.

![Logo](../images/cap2/15.png)

Después, publica la rama.

Paso 4.  Una vez creada la rama en el editor de código, busca el archivo **"resource/views/user/index.blade.php"** para realizar una pequeña modificación, y haz commit y push para que esté en el remoto.

Paso 5.  Después, realiza el pull request a la rama principal del repositorio al que te dieron acceso.

Paso 6. El dueño del repositorio podrá visualizar el pull request y aprobarlo, dando por finalizada esta primera parte.

Paso 7. Como segunda parte, el dueño de cada repositorio debe crear una regla para la rama principal, esto con el fin de limitar las pull request a la rama principal.

![Logo](../images/cap7/4.png)

En la seccion de **"Setting"** del repositorio, da clic a **"Branchs"**

![Logo](../images/cap7/5.png)

Después, da clic al botón **"Add classic branch protection rule"**, en esta sección seecciona las opciones de configuración para las ramas.

![Logo](../images/cap7/6.png)

* Posteriormente, en la nueva vista, escribe la rama que quieres proteger, en este caso: **"master"**.
* Selecciona **"Require pull request before mergin"**, esto hará que sea necesario sí o sí una pull request para hacer merge con la rama principal.
* "Require approvals": en este caso selecciona: **1**. Ten en cuenta que aplica unicamente si no hay cambios pendientes en la revisión.

![Logo](../images/cap7/7.png)

* **"Require conversation resolition before merging"**: con esta opción es obligatorio que todas la solicitudes hechas por el revisor en líneas de código sean resueltas.

Finalmente, da clic a **"Create"**.

![Logo](../images/cap7/8.png)

Esto te llevará nuevamente a la configuracion de las ramas, donde puedes observar que se ha aplicado una regla.

paso 8. Ahora que aplicaste la regla para tu rama, tu compañero que tiene acceso al repositorio, debe crear una rama en la que hará cambios simulando un error y hará pull request de este cambio.

![Logo](../images/cap7/9.png)

Ahora notarás como autor del cambio que no puedes aprobar el pull request y, en la sección de Reviewers, está seleccionado por defecto el dueño del repositorio, por lo que es necesario de la aprobacion de él.

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
