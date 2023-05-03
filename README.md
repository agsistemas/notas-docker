# Notas Docker
Apuntes de comandos y herramientas importantes de Docker para el día a día

## INSTALANDO
`$ curl -fsSL https://get.docker.com -o get-docker.sh`<br>
`$ sudo sh get-docker.sh`

## POST INSTALACIÓN
### PERMISOS
`$ sudo usermod -aG docker $USER`

Una vez realizado esto, tienes dos opciones, o bien sales y vuelves a entrar en la sesión, o bien, ejecutas estas instrucciones.<br>
`$ MIGRUPO=$(id -gn)`<br>
`$ newgrp docker`<br>
`$ newgrp $MIGRUPO`<br>

### COMPROBACIONES <br>
`$ docker -v` <br>
`Docker version 18.09.5, build e8ff056`

## LANZANDO TU PRIMER CONTENEDOR
`$ docker run hello-world`

## EJECUTAR UN CONTENEDOR Y ENTRAR EN EL POR BASH
`$ docker run -it ubuntu bash`
