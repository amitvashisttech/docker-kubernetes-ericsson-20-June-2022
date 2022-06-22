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


```
  617  docker ps
  618  docker ps -a
  619  docker rm $(docker ps -qa )
  620  ls
  621  docker ps
  622  docker ps -a
  623  docker images
  624  docker inspect amitvashist7/myapache-test
  625  :
  626  docker run -d --name test-apache-1 -p 8080:8080 amitvashist7/myapache-test
  627  docker run -d --name test-apache-1 -P  amitvashist7/myapache-test
  628  docker run -d --name test-apache-2 -P  amitvashist7/myapache-test
  629  docker ps
  630  curl localhost:8080
  631  curl localhost:32770
  632  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
  633  ip addr
  634  route -n
  635  docker network ls
  636  docker network inspect 977523e35ed7
  637  docker run -d --name test-apache-3 -P  amitvashist7/myapache-test
  638  docker run -d --name test-apache-4 -P  amitvashist7/myapache-test
  639  docker run -d --name test-apache-5 -P  amitvashist7/myapache-test
  640  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
  641  docker network inspect 977523e35ed7
  642  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
  643  docker kill test-apache-3
  644  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' $(docker ps -q)
  645  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
  646  docker run -d --name test-apache-6 -P  amitvashist7/myapache-test
  647  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
  648  docker start test-apache-3
  649  docker inspect --format '{{.Name}} {{.NetworkSettings.IPAddress}}' $(docker ps -qa)
  650  docker kill $(docker ps -qa )
  651  docker rm $(docker ps -qa )
  652  docker run -it --name net-tools ubuntu:16.04
  653  docker ps -a
  654  docker commit -p -m "Net Tools Installed" b47ba913baaf ubuntu-net-tools:v1
  655  docker images
  656  ls
  657  docker images
  658  docker ps
  659  netstat -tulnp
  660  docker run -itd --name test-nw-1 ubuntu-net-tools:v1
  661  docker ps
  662  docker exec -it test-nw-1 ping -c2 google.com
  663  docker exec -it test-nw-1 -c2 172.17.0.1
  664  docker exec -it test-nw-1 ping -c2 172.17.0.1
  665  docker run -itd --name test-nw-2 ubuntu-net-tools:v1
  666  docker exec -it test-nw-1 ping -c2 172.17.0.2
  667  docker exec -it test-nw-1 ping -c2 172.17.0.3
  668  docker ps
  669  docker exec -it test-nw-1 ping ifconfig
  670  docker exec -it test-nw-1 ifconfig
  671  docker exec -it test-nw-2 ifconfig
```
```
 229  ln -s  /var/run/docker/netns /var/run/
  230  ip netns
  231  ip addr
  232  ip netns
  233  ip netns  --help
  234  ip netns  -h
  235  ip netns c1a33b1448a2 -exec ifconfig
  236  ip netns -exec c1a33b1448a2  ifconfig
  237  ip netns exec c1a33b1448a2  ifconfig
  238  ip addr
  239  ip netns
  240  ip netns exec c1a33b1448a2  ifconfig
  241  ip netns exec fe1712a1c03d  ifconfig
  242  ls
  243  docker network  ls
  244  docker network create --help
  245  docker network create --driver "bridge" --subnet=172.28.0.0/16 --ip-range=172.28.7.0/24 --gateway=172.28.7.254 mybr0
  246  docker network  ls
  247  docker network inspect mybr0
  248  docker run -itd --name test-nw-2 --network mybr0 ubuntu-net-tools:v1
  249  docker run -itd --name test-nw-3 --network mybr0 ubuntu-net-tools:v1
  250  docker network inspect mybr0
  251  docker ps
  252  docker exec -it test-nw-2 ping -c2 google.com
  253  docker exec -it test-nw-3 ping -c2 google.com
```
```
  672  route -n
  673  ip addr
  674  ip netns
  675  ip netns exec c1a33b1448a2 ifconfig
  676  ip netns exec 7ca8e7f838f1 ifconfig
  677  ip addr
  678  ip route
  679  route -n
  680  ip addr
  681  ls
  682  cd 01-Docker/
  683  ls
  684  docker ps
  685  docker network ls
  686  docker run -itd --name test-none-1 --network none ubuntu-net-tools:v1
  687  docker ps
  688  ip addr
  689  docker ps
  690  docker exec -it test-none-1 ifconfig
  691  docker exec -it test-1 ifconfig
  692  docker network ls
  693  docker run -itd --name test-host-1 --network host ubuntu-net-tools:v1
  694  docker ps
  695  docker exec -it test-host-1 ifconfig
  696  ls
  697  cd 04-DockerNetwork/
```
