
- Docker image :  
https://hub.docker.com/r/duniter/duniter  
next : https://hub.docker.com/r/duniter/duniter-v2s

- in order to persist config and database, give proper right to data directory (root right may be necessary) :  
$ mkdir data
$ chown -R 1111:1111 data  

- install and start container :  
$ docker-compose up -d  

- get container prompt :  
$ docker-compose exec duniter /bin/sh  

- web admin :  
http://0.0.0.0:9220/  

- node sync :  
[duniter]~ $ duniter sync g1.duniter.org   
or  
http://0.0.0.0:9220/#/sync  

- setup member key :  
[duniter]~ $ duniter wizard key  
or  
http://0.0.0.0:9220/#/main/settings/crypto  
