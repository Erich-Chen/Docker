# Docker
Docker Quick Referrence.

## Install 
On Ubuntu Server 16.04.2 LTS for my case; ref. https://get.docker.com/ for more.  
```curl -sSL https://get.docker.com/ | sh```  
or  
```wget -qO- https://test.docker.com/ | sh```    

You will get a promot to add your account into "docker" group, then logoff and logon again to take effect.  
```
sudo usermod -aG docker *your_user_name*
exit
```


## HelloWorld
```docker run hello-world```

## Cheatsheet
### Container
```
docker run   # create and starts a container
docker kill  # kill a running container
docker rm    # delete a container
docker ps    # show running containers, -a to show all containers
```
Useful examples
```
docker run -it 
```
For full commands, ref. https://github.com/wsargent/docker-cheat-sheet/blob/master/README.md
```
docker create | rename | run | rm | update
docker start | stop | restart | pause | unpause | wait | kikk | attach
docker ps (-a) | logs | inspect | events | port | top | stats | diff
docker cp | export
docker exec
```

### Image
```
docker pull    # pull an image from repo
docker images  # show all images
docker rmi     # remove an image
```
For full commands, ref. https://github.com/wsargent/docker-cheat-sheet/blob/master/README.md
```
docker images | import | build | commit | rmi | load | save
docker history | tag
```

### Dockerfile
```
mkdir *docker_builds* && cd $_
mkdir *test1* && cd $_ && nano Dockerfile
#edit Dockerfile
docker build -t *docker-whale* .
docker run *docker-whale*
```
sample of Dockerfile
>FROM docker/whalesay:latest  
>RUN apt-get -y update && apt-get install -y fortunes  
>CMD /usr/games/fortune -a | cowsa  


