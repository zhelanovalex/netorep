# netorep
# Домашнее задание к занятию 4 «Оркестрация группой Docker контейнеров на примере Docker Compose»
## Задача 1.
https://hub.docker.com/repository/docker/zzugly/custom-nginx/general  
https://hub.docker.com/r/zzugly/custom-nginx/tags
## Задача 2.
### 1 Задание.  
**/DOCKER_TEST# docker run --name zhelanov-custom-nginx-t2 -d -p 8080:80 zzugly/custom-nginx:1.0.0**  
Unable to find image 'zzugly/custom-nginx:1.0.0' locally  
1.0.0: Pulling from zzugly/custom-nginx  
af7c915c8849: Already exists  
c5ada5e7d698: Already exists  
9dbfe0b105c9: Already exists  
dea1652b095a: Already exists  
85003794a6a5: Already exists  
fea7cebc499c: Already exists  
856c000ad0ec: Already exists  
a2f0033eba7b: Already exists  
Digest: sha256:9f47a8b80cd1474ca46698d9e9de1fdbf2688e23471887538784b1f8177a96b7  
Status: Downloaded newer image for zzugly/custom-nginx:1.0.0  
113a1b8e2ed90b1e906dd1c4823c1b401b37ddb15445978f0b3c5c690dc25738  
**/DOCKER_TEST# docker ps -a**  
CONTAINER ID   IMAGE                       COMMAND                  CREATED          STATUS         PORTS                                     NAMES  
113a1b8e2ed9   zzugly/custom-nginx:1.0.0   "/docker-entrypoint.…"   11 seconds ago   Up 9 seconds   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   zhelanov-custom-nginx-t2
### 2 Задание. 
**/DOCKER_TEST# docker stop zhelanov-custom-nginx-t2**  
zhelanov-custom-nginx-t2  
**/DOCKER_TEST# docker ps -a**  
CONTAINER ID   IMAGE                       COMMAND                  CREATED         STATUS                     PORTS     NAMES  
113a1b8e2ed9   zzugly/custom-nginx:1.0.0   "/docker-entrypoint.…"   2 minutes ago   Exited (0) 6 seconds ago             zhelanov-custom-nginx-t2  
**/DOCKER_TEST# docker rename zhelanov-custom-nginx-t2 custom-nginx-t2**  
**/DOCKER_TEST# docker ps -a**  
CONTAINER ID   IMAGE                       COMMAND                  CREATED         STATUS                      PORTS     NAMES  
113a1b8e2ed9   zzugly/custom-nginx:1.0.0   "/docker-entrypoint.…"   2 minutes ago   Exited (0) 30 seconds ago             custom-nginx-t2  
**/DOCKER_TEST# docker start custom-nginx-t2**  
custom-nginx-t2  
**/DOCKER_TEST# docker ps -a**  
CONTAINER ID   IMAGE                       COMMAND                  CREATED         STATUS         PORTS                                     NAMES  
113a1b8e2ed9   zzugly/custom-nginx:1.0.0   "/docker-entrypoint.…"   3 minutes ago   Up 2 seconds   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   custom-nginx-t2  
### 3 Задание. 
**/DOCKER_TEST# date +"%d-%m-%Y %T.%N %Z" ; sleep 0.150 ; docker ps ; ss -tlpn | grep 127.0.0.1:8080  ; docker logs custom-nginx-t2 -n1 ; docker exec -it custom-nginx-t2 base64 /usr/share/nginx/html/index.html**  
08-12-2025 14:19:33.070281594 MSK  
CONTAINER ID   IMAGE                       COMMAND                  CREATED         STATUS          PORTS                                     NAMES  
113a1b8e2ed9   zzugly/custom-nginx:1.0.0   "/docker-entrypoint.…"   3 minutes ago   Up 41 seconds   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   custom-nginx-t2  
172.17.0.1 - - [08/Dec/2025:11:19:00 +0000] "GET / HTTP/1.1" 200 95 "-" "curl/7.68.0" "-"  
PGh0bWw+CjxoZWFkPgpIZXksIE5ldG9sb2d5CjwvaGVhZD4KPGJvZHk+CjxoMT5JIHdpbGwgYmUg  
RGV2T3BzIEVuZ2luZWVyITwvaDE+CjwvYm9keT4KPC9odG1sPgo=  
### 4 Задание. 
**/DOCKER_TEST# curl http://127.0.0.1:8080**  
<html>
<head>
Hey, Netology
</head>
<body>
<h1>I will be DevOps Engineer!</h1>
</body>
</html>

## Задача 3.
### 1 Задание. 
**/DOCKER_TEST# docker logs --follow custom-nginx-t2**  
