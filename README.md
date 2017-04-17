# Docker
Docker Memo

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
