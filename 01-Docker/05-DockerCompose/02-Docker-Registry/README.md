```
766  mkdir 02-Docker-Registry
  767  ls
  768  cd 02-Docker-Registry/
  769  ls
  771  ls
  772  vim docker-compose.yaml
  773  docker ps -aq
  774  docker kill $(docker ps -q)
  775  docker rm $(docker ps -aq)
  776
  777  ls
  778  docker network ls
  779  docker network delete mybr0
  780  docker network rm mybr0
  781  docker network ls
  782  docker-compose up -d
  783  docker ps
  784  docker inspect 0bf7b7bdf8bb
  785  docker network ls
  786  docker network inspect 02-docker-registry_registry-ui-net
  787  docker-compose  ps
  788  curl localhost:8080
  789  docker ps
  790  docker exec -it f53145200ea5 env
  791  vim docker-compose.yaml
  792  docker-compose up -d
  793  docker images
  794  docker tag ubuntu-net-tools 172.31.0.100:8080/ubuntu-net-tools:v1
  795  docker tag ubuntu-net-tools:v1  172.31.0.100:8080/ubuntu-net-tools:v1
  796  docker images
  797  hostname -f
  798  docker tag ubuntu-net-tools master.example.com:8080/ubuntu-net-tools:v1
  799  docker tag ubuntu-net-tools:v1  master.example.com:8080/ubuntu-net-tools:v1
  800  ls
  801  docker images
  802  docker push master.example.com:8080/ubuntu-net-tools:v1
  803  docker push 172.31.0.100:8080/ubuntu-net-tools:v1
  804  docker push 172.31.0.100:8080/ubuntu-net-tools:v1
  805  docker images
  806  docker tag amitvashist7/myapache-test:latest master.example.com:8080/myapache-test:latest
  807  docker tag amitvashist7/myapache-test:v1 master.example.com:8080/myapache-test:v1
  808  docker images
  809  docker push master.example.com:8080/myapache-test:v1
  810  docker push master.example.com:8080/myapache-test:latest
  811  docker images
  812  docker images | grep -i master
  813  docker images | grep -i master  | awk -F" " '{print $3}'
  814  docker rmi $(docker images | grep -i master  | awk -F" " '{print $3}')
  815  docker rmi $(docker images | grep -i master  | awk -F" " '{print $3}') --force
  816  docker images
  817  history
  818  docker run -d master.example.com:8080/myapache-test:latest
  819  docker images
  820  docker ps
  858  docker-compose kill
  859  docker-compose rm
  860  docker-compose ps
```
