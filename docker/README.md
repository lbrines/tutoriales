##Docker para desarrollo
 
Instalación de docker
https://docs.docker.com/engine/install/

Instalación de docker-compose
https://docs.docker.com/compose/install/

#### Arquitectura
![](https://docs.docker.com/engine/images/architecture.svg)


#### Objetos básicos:
- Imágenes
- Contenedores

#### Objetos adicionales
- Volúmenes
- Redes

#### Comandos básicos
Información del daemon de docker
`docker info `

Ayuda de comandos
`docker  help`

Primer contenedor
`docker run hello-world`

Imágenes
Listar imagenes
`docker image ls`
Borrar imagenes
`docker image rm ID`

#### Contenedor
Listar los contenedores activos
`docker container ps = docker ps`

Listar todos los contenedores
`docker ps -a`

Usar una imagen nginx
`docker run nginx`

##### Buscar imagenes: https://hub.docker.com/

Nombre de contenedores
`docker run --name con1 nginx`

detach contenedor
`docker run -d --name con2 nginx`

#### Puertos
`docker run -p 8080:80 nginx:1.18.0`

#### Volumen
`docker run -p 8080:80 -v ~/html:/usr/share/nginx/html nginx:1.18.0`

#### Red
Ver redes disponibles
`docker network  ls`

Crear redes
`docker network create red`

Contenedores en la misma Red
`docker run --network red -d --name con1 nginx`
`docker run --network red -d --name con2 nginx`


https://docs.docker.com/engine/reference/commandline/docker/