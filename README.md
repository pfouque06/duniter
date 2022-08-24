
# Docker compose for duniter image  

- Docker image :  
https://hub.docker.com/r/duniter/duniter  
next : https://hub.docker.com/r/duniter/duniter-v2s

- In order to persist config and database, give proper right to data directory (root right may be necessary) :  
If data directory is not present, run 'mkdir data' mounted to /var/lib/duniter  
``` 
$ chown -R 1111:1111 data/*  
``` 

- If you have a keychain file :  
If keychain directory is not present, run 'mkdir keychain' mounted to /etc/duniter  
``` 
$ chown -R 1111:1111 keychain/*  
``` 

- install and start container :  
``` 
$ docker-compose up -d  
``` 

- get container prompt :  
``` 
$ docker-compose exec duniter /bin/sh  
``` 

- web admin :  
http://0.0.0.0:9220/  

- node sync :  
``` 
[duniter]~ $ duniter sync g1.duniter.org   
``` 
or  
http://0.0.0.0:9220/#/sync  

- setup member key :  
``` 
[duniter]~ $ duniter wizard key  
``` 
or  
http://0.0.0.0:9220/#/main/settings/crypto  

- setup network :  
``` 
[duniter]~ $ duniter wizard network  
``` 
or  
http://0.0.0.0:9220/#/main/settings/network  

- duniter image update :
When a new duniter docker image is released, run :  
```
$ docker-compose up -d
$ docker image prune
```

If these does not update the image, try :   
```
$ docker-compose stop
$ docker-composer image
$ docker image ls
$ docker image rm duniter/duniter
$ docker image pull duniter/duniter:<version>
$ docker image ls
$ docker-compose up -d
$ docker-composer image
```