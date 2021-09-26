
- install and start container :  
$ docker-compose up -d  

- get container prompt :  
$ docker-compose exec duniter /bin/sh  

- node sync :  
[duniter]~ $ duniter sync g1.duniter.com  
or  
http://0.0.0.0:9220/#/sync  

- web admin :  
http://0.0.0.0:9220/  
http://plex:9220/  

- setup member key :  
[duniter]~ $ duniter wizard key  
or  
http://0.0.0.0:9220/#/main/settings/crypto  
