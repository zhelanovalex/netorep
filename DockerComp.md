# netorep
# Домашнее задание к занятию 5. «Практическое применение Docker»
## Задача 0.

### 1 Задание.
#### Проверка docker compose.
<img width="600" height="194" alt="image" src="https://github.com/user-attachments/assets/b60c45b6-260c-43b3-8fbe-21b0f5ab25c5" />  

## Задача 1.

### 1 Задание. 
#### fork учебного репозитоия.
<img width="1341" height="595" alt="image" src="https://github.com/user-attachments/assets/3a6cefa5-6dab-4c43-a161-9c7b3cdf9be5" />  

### 2 Задание. 
#### Создание Dokerfile.python и сборка.
https://github.com/zhelanovalex/shvirtd-example-python/blob/main/Dockerfile.python  

<img width="1571" height="453" alt="image" src="https://github.com/user-attachments/assets/8bdb08d3-7a14-41c6-b68e-8e2313e42078" />  
<img width="1111" height="259" alt="image" src="https://github.com/user-attachments/assets/41659547-cce8-4c22-bf3d-db92f4ef9b39" />

### 3 Задание.
#### Запуск базы.  
<img width="1602" height="248" alt="image" src="https://github.com/user-attachments/assets/9b26ec93-050c-4329-9eb2-6db3115537ee" />
<img width="950" height="135" alt="image" src="https://github.com/user-attachments/assets/8358b331-adc7-4bfb-a5b4-cb3479999818" />

#### Запуск приложения. 
<img width="964" height="17" alt="image" src="https://github.com/user-attachments/assets/b375284a-68ba-4dd3-a130-dcb59d702a5b" />  
<img width="845" height="47" alt="image" src="https://github.com/user-attachments/assets/c496b55f-a1e9-47aa-82f6-b43fb6062ea1" />
<img width="865" height="197" alt="image" src="https://github.com/user-attachments/assets/0e6f229f-297d-41b1-94f1-02464f9612fc" />


## Задача 2.  
### 1 Задание.  

<img width="790" height="232" alt="image" src="https://github.com/user-attachments/assets/e383e3b7-491b-4fd3-82a1-fbb54d12c17d" />

### 2 Задание.

<img width="808" height="244" alt="image" src="https://github.com/user-attachments/assets/8ab2763a-b668-4397-95e5-7b9e1b7817fb" />

### 3 Задание.

<img width="944" height="354" alt="image" src="https://github.com/user-attachments/assets/ee881eb1-ac33-49e2-9bc7-2868ffcffcf8" />

### 4 Задание.

<img width="965" height="277" alt="image" src="https://github.com/user-attachments/assets/0bc7bed7-bfcd-41e2-9b6b-fb9defac1592" />

### 5 Задание.

<img width="1234" height="982" alt="image" src="https://github.com/user-attachments/assets/7630a95b-7701-462d-9e01-1b647ea50156" />
<img width="1085" height="115" alt="image" src="https://github.com/user-attachments/assets/9006668b-9833-4d50-9cdd-78504c0a9831" />

## Задача 3.  


<img width="1107" height="773" alt="image" src="https://github.com/user-attachments/assets/4b26d84c-a2cd-410e-b539-a4113bc038cb" />

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
