

# Docker composer que levanta mariadb version 12.0.1-noble-rc

# Nombre del contenedor:
* > mariadb
  
# Datos de mariadb
* >  DATABASE: universidad
* >  USER: alumno
* >  PASSWORD: alumno1
* >  ROOT_PASSWORD: pass

# Carpetas creadas
* > databases : creada para incluir los **sql** que se cargarán cuando no exista la carpeta **mariadb-data**
* > querys : carpeta que guarda los **sql** en la carpeta de **/root/** para su ejecución con el comando **source**
* > mariadb-data: carpeta que mantiene el respaldo y la persistencia de la base de datos 
  
# Este contenedor se crea con linux:
```
cat /etc/os-release
```
# -
```
PRETTY_NAME="Ubuntu 24.04.2 LTS"
NAME="Ubuntu"
VERSION_ID="24.04"
VERSION="24.04.2 LTS (Noble Numbat)"
```

## Comandos utilizados para acceder a la bd una vez levantado el contenedor
```
docker exec -it mariadb  mariadb -h localhost -u alumno -p universidad

docker exec -it mariadb  mariadb -h localhost -u root -p 

docker exec -it mariadb sh

```
