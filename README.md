# Notas Docker
Apuntes de comandos y herramientas importantes de Docker para el día a día.

## INSTALANDO.
`$ curl -fsSL https://get.docker.com -o get-docker.sh`<br>
`$ sudo sh get-docker.sh`

## POST INSTALACIÓN.
### PERMISOS.
`$ sudo usermod -aG docker $USER`

Una vez realizado esto, tienes dos opciones, o bien sales y vuelves a entrar en la sesión, o bien, ejecutas estas instrucciones.<br>
`$ MIGRUPO=$(id -gn)`<br>
`$ newgrp docker`<br>
`$ newgrp $MIGRUPO`<br>

### COMPROBACIONES.
`$ docker -v` <br>
`Docker version 18.09.5, build e8ff056`

## LANZANDO TU PRIMER CONTENEDOR.
`$ docker run hello-world`

## EJECUTAR UN CONTENEDOR Y ENTRAR EN EL POR BASH.
`$ docker run -it ubuntu bash`

## VER LOS LOGS DEL CONTENDOR.
`$ docker logs -f NOMBRE_CONTENEDOR`

## LISTAR CONTENEDORES EN EJECUCIÓN.
`$ docker ps`

## LISTAR TODOS CONTENEDORES TANTO EN EJECUCIÓN COMO DETENIDOS.
`$ docker ps -a`

## LISTAR CONTENEDORES EN EJECUCIÓN SIN TRUNCADO DE LA INFORMACIÓN QUE SE LISTA.
`$ docker ps --no-trunc`

## EVITAR QUE ARCHIVOS QUE NO UTILIZAMOS SE AGREGUEN AL CONTEXTO DE DOCKERFILE
Creamos un archivo oculto llamado .dockerignore y agregamos los nombres de los archivos o carpetas que queremos que no se agreguen al contexto de construcción del Dockerfile.<br>

