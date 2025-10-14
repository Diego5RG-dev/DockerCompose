<h1 align="center">   Tareas de Docker Compose </h1> <br>
<p align="center">
    <img alt="logo" title="logo" src="https://github.com/Diego5RG-dev/DockerCompose/blob/main/recursosDockerCompose/logo.jpg "width="75%">
</p>

---
¡Atención!
---

Lo primero antes que nada es comprobar que tenemos activo Docker Compose. Una vez comprobemos eso, podemos comenzar.
<p align="center">
    <img alt="logo" title="logo" src="https://github.com/Diego5RG-dev/DockerCompose/blob/main/recursosDockerCompose/1.png ">
</p>

---
Fichero Docker Compose
---

Hice la parte complicada de la tarea: creé el archivo de Docker Compose y su correspondiente environment para la seguridad de nuestros datos.
<p align="center">
    <img alt="prestashop" title="prestashop" src="https://github.com/Diego5RG-dev/DockerCompose/blob/main/recursosDockerCompose/prestashop.png "width="75%">
</p>

Explicare un poco lo que se puede ver en esta pestaña, la cual servirá también para los apartados de las siguientes capturas.

**image** = Aquí simplemente ponemos la imagen de la que queremos que parta nuestro contenedor.

**port** =  El puerto que queremos utilizar.

**enviroment** = Aquí es donde pondremos la información codificada en otro archivo .env, o las variables de entorno que queremos recoger.

**volume** = Está relacionado con el sistema de carpetas o la persistencia de datos.

**depends_on** = Aquí es una opción que dice que depende de que el servicio esté sano (healthy), cosa que veremos más adelante.

**network** = Información de la red a la que se conecta el contenedor.

**restart** = Para que el contenedor se reinicie automáticamente a la hora de crearse o si falla.

<p align="center">
    <img alt="db" title="db" src="https://github.com/Diego5RG-dev/DockerCompose/blob/main/recursosDockerCompose/db.png " width="75%">
</p>

Aquí la única diferencia grande que vemos es la de condition: healthy. Lo que hace es que, antes de crear los contenedores, haga unas pruebas de validación o estado de salud.


<p align="center">
    <img alt="enviroment" title="enviroment" src="https://github.com/Diego5RG-dev/DockerCompose/blob/main/recursosDockerCompose/enviroment.png " width="75%">
</p>

Esto es lo que he escrito para el archivo de environment (o entorno), generando contraseñas y demás datos falsos.

---
Comprobaciones y ejecución.
---

En este apartado realizaremos las comprobaciones de que nuestro Docker Compose funciona correctamente.

p align="center">
    <img alt="chequep" title="chequep" src="https://github.com/Diego5RG-dev/DockerCompose/blob/main/recursosDockerCompose/chequep.png " width="75%">
</p>

Lo que aparece en esta imagen es una comprobación (o chequeo) de Docker Compose para que valide que está bien escrito. Si hubiera algún aviso (warning) o algo, aparecería aquí.

p align="center">
    <img alt="dockerUP" title="dockerUP" src="https://github.com/Diego5RG-dev/DockerCompose/blob/main/recursosDockerCompose/dockerUP.png " width="85%">
</p>

Aquí lanzamos el comando docker compose up para generar los contenedores, y como vemos, no nos da fallo.

p align="center">
    <img alt="phpmyadmin" title="phpmyadmin" src="https://github.com/Diego5RG-dev/DockerCompose/blob/main/recursosDockerCompose/phpmyadmin.png " width="75%">
</p>

Por último, comprobamos que se crearon las tablas en phpMyAdmin y la base de datos para comprobar que todo ha salido bien y lo tenemos corriendo.
