# lab08
____

***Task: learn some information about Docker and Dockerfile***

- [X] **First step(download Docker on Ubuntu)**
```
  sudo apt-get update
  sudo apt-get install ./docker-desktop-<version>-<arch>.deb
```
- [X] **Second step(learn some prefix and command)**
```
  -it
  -h (--hostname)
  --name
  -d
  -p
  inspect
  logs
  run
  diff
  ps -a (ps)
  rm
 ```
- [X] **Third step(create repos on DockerHub)**
```
sudo docker run -it --name koala -h Kyala16 ubuntu bash
> apt update
> apt install -y cowsay
> ln -s /usr/games/cowsay /usr/bin/cowsay
>exit
sudo docker commit koala kyala16/koala-vader
sudo docker login
sudo docker push kyala16/koala-vader
```
- [X] **Fourth step(create Dockerfile with my repos and create some small main scene from Star Wars)**
```
FROM ubuntu

RUN apt-get update && apt-get install -y cowsay && ln -s /usr/games/cowsay /usr/bin/cowsay

ENTRYPOINT ["cowsay", "-f"]
```
Some usefull instructions:
```
  FROM
  RUN
  ENTRYPOINT
  ENV
  COPY
  WORKDIR
  VOLUME
 ```
