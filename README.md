# dsm-ex2-SpringDataREST_Containerized
``` bash
 docker ps
 docker ps -a | awk '{print $1}' | while read id; do  docker rm $id; done
 docker run -d --env MONGO_INITDB_ROOT_USERNAME=mongoadmin --env MONGO_INITDB_ROOT_PASSWORD=secret mongo
 docker inspect 4ab8cf549a15
 mvn run
 mvn spring-boot:run
 MONGO_USER=mongoadmin MONO_PSWD=secret MONGO_HOST="172.17.0.2" MONGO_PORT=27017 mvn spring-boot:run

 ping 172.17.0.2
 
 docker build -t myspringapp .
 docker run myspringapp
 docker run -p 8080:8080 --env "MONGO_USER=mongoadmin" --env "MONGO_PSWD=secret" --env "MONGO_HOST=172.17.0.2" --env "MONGO_PORT=27017" myspringapp 
 docker image ls
 docker build -t mymultistageapp .
 docker run -p 8080:8080 --env "MONGO_USER=mongoadmin" --env "MONGO_PSWD=secret" --env "MONGO_HOST=172.17.0.2" --env "MONGO_PORT=27017" mymultistageapp 

 mkdir democompose
 mv demo democompose/

 docker-compose build 
 docker compose  up -d
 ```
