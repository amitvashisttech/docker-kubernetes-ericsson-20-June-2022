```
 713  mkdir 05-DockerCompose/00-Setup -p
  714  cd 05-DockerCompose/
  715  cd 00-Setup/
  716  ls
  717  vim README.md
  718  ls
  719  sudo curl -L "https://github.com/docker/compose/releases/download/1.22.0/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
  720  chmod +x /usr/local/bin/docker-compose
  721  ls
  722  docker-compose version
  723  ls
  724  cd ..
  725  ls
  726  mkdir 01-Apache
  727  ls
  728  cd 01-Apache/
  729  ls
  730  vim docker-compose.yaml
  731  docker-compose up -d
  732  docker-compose ps
  733  docker ps
  734  vim docker-compose.yaml
  735  cd ../../
  736  ls
  737  pwd
  738  cd -
  739  ls
  740  vim docker-compose.yaml
  741  docker-compose ps
  742  docker-compose up -d
  743  docker-compose ps
  744  netstat -tulnp
  745  ip addr
  746  curl 172.31.0.100:8080
  747  docker ps
  748  docker inspect amitvashist7/myapache-test:v1
  749  docker images
  750  vim docker-compose.yaml
  751  docker-compose up -d
  752  docker images
```
