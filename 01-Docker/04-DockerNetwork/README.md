```
529  docker images
  530  docker run -d --name apache-1 amitvashist7/myapache-test
  531  docker ps
  532  docker inspect apache-1
  533  ip addr
  534  route -n
  535  curl 172.17.0.2:8080
  536  docker inspect apache-1
  537  ip addr
  538  netstat -tulnp
  539  docker run -d --name apache-1 -p 80:8080 amitvashist7/myapache-test
  540  docker run -d --name apache-2 -p 80:8080 amitvashist7/myapache-test
  541  docker ps
  542  netstat -tulnp
  543  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
  544  systemctl status docker
  545  docker run -d --name apache-3 -p 80:8080 amitvashist7/myapache-test
  546  docker run -d --name apache-3 -p 81:8080 amitvashist7/myapache-test
  547  docker run -d --name apache-4 -p 81:8080 amitvashist7/myapache-test
  548  docker run -d --name apache-5 -p 82:8080 amitvashist7/myapache-test
  549  docker ps
  550  netstat -tulnp
  551  systemctl status docker
  552  ls
  553  docker ps
  554  docker run -d --name apache-6 -P  amitvashist7/myapache-test
  555  docker ps
  556  ls
  557  cd 01-Docker/
  558  ls
  559  cd 03-DockerVolumes/
  560  ls
  561  cd ..
  562  ls
  563  cd 02-Dockerfile/apache/
  564  ls
  565  cd v6/
  566  ls
  567  cat index.html
  568  pwd
  569  docker run -d --name apache-7 -v /root/docker-kubernetes-ericsson-20-June-2022/01-Docker/02-Dockerfile/apache/v6:/var/www/html/myapp -P  amitvashist7/myapache-test
  570  docker ps
  571  ls
  572  mv index.html index.html.old
  573  ls
  574  vim index.html.old
  575  s
  576  ls
  577  mv index.html.old index.html
  578  ls
  579  history
  580  docker ps
  581  docker inspect apache-7
  582  ls
  583  vim index.html
  584  ls
  585  mv index.html index.html.old
  586  mv index.html.old index.html
  587  mv index.html info.html

```
