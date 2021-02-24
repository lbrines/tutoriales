```
docker network create red  

docker run --name mysql --rm -e MYSQL ROOT PASSWORD=1234qwerty --network red -d mysql:5.7

docker exec -it mysql bash 

CREATE DATABASE dbtest;

docker build -t mysqltest:v1 .

docker run --rm --network red -it mysqltest:v1

```