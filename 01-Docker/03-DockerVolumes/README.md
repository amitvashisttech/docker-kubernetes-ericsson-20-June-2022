```
462  mkdir 03-DockerVolumes
  463  cd 03-DockerVolumes/
  464  ls
  465  cd
  466  docker volumes ls
  467  docker volume ls
  468  docker volume rm 98bbcf47feb3c53eb625f8ca88c72471498baacd09958e5825fb9530adbdc139
  469  docker volume ls
  470  docker volume create my-vol
  471  docker volume ls
  472  docker volume inspect my-vol
  473  docker run -it --name volume-test-1 -v my-vol:/var/www/html/myapp ubuntu:16.04
  474  docker ps
  475  docker inspect volume-test-1
  476  docker run -it --name volume-test-2 -v my-vol:/myapp ubuntu:16.04
  477  ls
  478  docker ps
  479  docker kill $(docker ps -qa )
  480  docker rm $(docker ps -qa )
  481  docker ps
  482  docker ps -a
  483  docker volume ls
  484  cat /var/lib/docker/volumes/my-vol/_data/hello.txt
  485  docker run -it --name volume-test-3 -v /myapp ubuntu:16.04
  486  docker kill $(docker ps -qa )
  487  docker volume ls
  488  docker ps
  489  docker ps -a
  490  docker inspect volume-test-3
  491  cat /var/lib/docker/volumes/57a7ab9e73458d4be04e872a5297827193c5cf50e604dd7414359612a95ccf03/_data/hello.txt
  492  docker run -it --name volume-test-4 -v /myapp -v /amit -v /var/log/myapp ubuntu:16.04
  493  docker inspect volume-test-4
  494  cd docker-kubernetes-ericsson-20-June-2022/
  495  ls
  496  pwd
  497  docker run -it --name volume-test-5 -v /root/docker-kubernetes-ericsson-20-June-2022:/myapp  ubuntu:16.04
  498  ls
  499  cat README.md
  500  cat 01-Docker/03-DockerVolumes/abc.txt
  501  docker run -it --name volume-test-6 -v /root/docker-kubernetes-ericsson-20-June-2022:/myapp:ro  ubuntu:16.04
  502  ls
  503  cd 01-Docker/
  504  ls
  505  cd 03-DockerVolumes/
  506  ls
  507  docker ps -q
  508  docker ps -a
  509  docker kill $(docker ps -qa )
  510  docker rm $(docker ps -qa )
  511  docker volumes ls
  512  docker volume ls
  513  docker volume ls -q
  514  docker volume rm $(docker volume ls -q )
  515  docker volume ls -q
  516  docker volume ls
```
