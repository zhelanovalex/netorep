
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
Hey, Netology  
I will be DevOps Engineer!
## Задача 3.
### 1 Задание. 
**/DOCKER_TEST# docker logs --follow custom-nginx-t2**  
(очень длинный вывод)  
### 2 Задание.
**/DOCKER_TEST/src# docker attach custom-nginx-t2**  
^C2025/12/08 12:00:10 [notice] 1#1: signal 2 (SIGINT) received, exiting  
2025/12/08 12:00:10 [notice] 22#22: exiting  
2025/12/08 12:00:10 [notice] 23#23: exiting   
2025/12/08 12:00:10 [notice] 24#24: exiting  
2025/12/08 12:00:10 [notice] 22#22: exit  
2025/12/08 12:00:10 [notice] 23#23: exit  
2025/12/08 12:00:10 [notice] 24#24: exit  
2025/12/08 12:00:10 [notice] 25#25: exiting  
2025/12/08 12:00:10 [notice] 25#25: exit  
2025/12/08 12:00:10 [notice] 1#1: signal 14 (SIGALRM) received  
2025/12/08 12:00:10 [notice] 1#1: signal 17 (SIGCHLD) received from 24  
2025/12/08 12:00:10 [notice] 1#1: worker process 24 exited with code 0  
2025/12/08 12:00:10 [notice] 1#1: signal 29 (SIGIO) received  
2025/12/08 12:00:10 [notice] 1#1: signal 17 (SIGCHLD) received from 23  
2025/12/08 12:00:10 [notice] 1#1: worker process 23 exited with code 0  
2025/12/08 12:00:10 [notice] 1#1: signal 29 (SIGIO) received  
2025/12/08 12:00:10 [notice] 1#1: signal 17 (SIGCHLD) received from 25  
2025/12/08 12:00:10 [notice] 1#1: worker process 22 exited with code 0  
2025/12/08 12:00:10 [notice] 1#1: worker process 25 exited with code 0  
2025/12/08 12:00:10 [notice] 1#1: exit  
### 3 Задание.
**/DOCKER_TEST/src# docker ps -a**    
CONTAINER ID   IMAGE                       COMMAND                  CREATED          STATUS                     PORTS     NAMES   
113a1b8e2ed9   zzugly/custom-nginx:1.0.0   "/docker-entrypoint.…"   54 minutes ago   Exited (0) 9 minutes ago             custom-nginx-t2    
**Ctrl+C посылает прерывание главному процессу контейнера, соответственно он завершается и останавливается контейнер**
### 4 Задание.
**/DOCKER_TEST/src# docker start custom-nginx-t2**  
custom-nginx-t2  
**/DOCKER_TEST/src# docker ps -a**  
CONTAINER ID   IMAGE                       COMMAND                  CREATED             STATUS         PORTS                                     NAMES  
113a1b8e2ed9   zzugly/custom-nginx:1.0.0   "/docker-entrypoint.…"   About an hour ago   Up 2 seconds   0.0.0.0:8080->80/tcp, [::]:8080->80/tcp   custom-nginx-t2  
### 5 Задание.
**/DOCKER_TEST/src# docker exec -it custom-nginx-t2 bash**  
### 6 Задание.  
**root@113a1b8e2ed9:/# apt-get update**  
Get:1 http://deb.debian.org/debian bookworm InRelease [151 kB]  
Get:2 http://deb.debian.org/debian bookworm-updates InRelease [55.4 kB]  
Get:3 http://deb.debian.org/debian-security bookworm-security InRelease [48.0 kB]  
Get:4 http://deb.debian.org/debian bookworm/main amd64 Packages [8791 kB]  
Get:5 http://deb.debian.org/debian bookworm-updates/main amd64 Packages [6924 B]  
Get:6 http://deb.debian.org/debian-security bookworm-security/main amd64 Packages [289 kB]  
Fetched 9342 kB in 3s (3268 kB/s)  
Reading package lists... Done  
**root@113a1b8e2ed9:/# apt-get install vim**  
(очень длинный вывод)  
### 7 Задание.
**root@113a1b8e2ed9:/# cat /etc/nginx/conf.d/default.conf | grep listen**  
    listen       81;  
    listen  [::]:81;  
    # proxy the PHP scripts to Apache listening on 127.0.0.1:80  
    # pass the PHP scripts to FastCGI server listening on 127.0.0.1:9000  
### 8 Задание.  
**root@113a1b8e2ed9:/# nginx -s reload**  
2025/12/08 12:36:36 [notice] 284#284: signal process started  
**root@113a1b8e2ed9:/# curl http://127.0.0.1:80**  
curl: (7) Failed to connect to 127.0.0.1 port 80 after 0 ms: Couldn't connect to server  
**root@113a1b8e2ed9:/# curl http://127.0.0.1:81** 
Hey, Netology  
I will be DevOps Engineer!
### 9 Задание. 
**root@113a1b8e2ed9:/# exit**  
### 10 Задание.
**/DOCKER_TEST/src# ss -tlpn | grep 8080**  
LISTEN    0         4096               0.0.0.0:8080             0.0.0.0:*        users:(("docker-proxy",pid=12270,fd=7))                                       
LISTEN    0         4096                  [::]:8080                [::]:*        users:(("docker-proxy",pid=12277,fd=7))           
**/DOCKER_TEST/src# docker port custom-nginx-t2**  
80/tcp -> 0.0.0.0:8080  
80/tcp -> [::]:8080  
**/DOCKER_TEST/src# curl http://127.0.0.1:8080**  
curl: (56) Recv failure: Connection reset by peer  
**(Проблема в том, что nginx слушает 81 порт а проброшен 80)**  
### 11 Задание.
**Проблема исправлена, благодаря ссылке в задании**  
**Проведены остановка контейнера и сервиса docker, затем исправленеы конфигурационные файлы hostconfig.json и config.v2.json, в каталоге  /var/lib/docker/containers/<ID>. По завершению проведен запуск сервиса docker и старт контейнера** 
### 12 Задание.
**/DOCKER_TEST# docker rm -f custom-nginx-t2**  
custom-nginx-t2  
**/DOCKER_TEST# docker ps -a**  
CONTAINER ID   IMAGE     COMMAND   CREATED   STATUS    PORTS     NAMES  
## Задача 4.
### 1 Задание. 
**/DOCKER_TEST/vol_doc# docker run --name centos-neto -d -it -v $(pwd):/data centos:8 /bin/bash**  
Unable to find image 'centos:8' locally  
8: Pulling from library/centos  
a1d0c7532777: Pull complete  
Digest: sha256:a27fd8080b517143cbbbab9dfb7c8571c40d67d534bbdee55bd6c473f432b177  
Status: Downloaded newer image for centos:8  
e107cf3cf18b17b0c533fb66d2b1d08dbc1ed995bcc5c17e6ca553bcfe47c1e6  
### 2 Задание. 
**/DOCKER_TEST/vol_doc# docker run --name debian-neto -d -it -v $(pwd):/data debian:9 /bin/bash**  
Unable to find image 'debian:9' locally  
9: Pulling from library/debian  
8372a04f222b: Pull complete  
Digest: sha256:c5c5200ff1e9c73ffbf188b4a67eb1c91531b644856b4aefe86a58d2f0cb05be  
Status: Downloaded newer image for debian:9  
58ddf2a7afa70666652e94afbe35e0f31dad219ae7987bd512ea6a0e69424dc8  
**/DOCKER_TEST/vol_doc# docker ps -a**  
CONTAINER ID   IMAGE                       COMMAND                  CREATED          STATUS          PORTS                                     NAMES  
58ddf2a7afa7   debian:9                    "/bin/bash"              44 seconds ago   Up 39 seconds                                             debian-neto  
e107cf3cf18b   centos:8                    "/bin/bash"              12 minutes ago   Up 11 minutes                                             centos-neto  
### 3 Задание.  
**/DOCKER_TEST/vol_doc# docker exec -it centos-neto bash**  
**[root@e107cf3cf18b /]# cd /data**  
**[root@e107cf3cf18b data]# cat temp_centos**   
Hello word!!!  
### 4 Задание.
**/DOCKER_TEST/vol_doc# cp -p /etc/hosts ./**  
**/DOCKER_TEST/vol_doc# ls**  
hosts  temp_centos  
### 5 Задание.  
**/DOCKER_TEST/vol_doc# docker exec -it debian-neto bash** 
**root@58ddf2a7afa7:/# cd /data**  
**root@58ddf2a7afa7:/data# ls**  
hosts  temp_centos  
## Задача 5.  
### 1 Задание.  
**/DOCKER_TEST/compose# ls**  
compose.yaml  docker-compose.yaml  
**/DOCKER_TEST/compose# docker-compose up -d**  
WARN[0000] Found multiple config files with supported names: /DOCKER_TEST/compose/compose.yaml, /DOCKER_TEST/compose/docker-compose.yaml  
WARN[0000] Using /DOCKER_TEST/compose/compose.yaml  
WARN[0000] /DOCKER_TEST/compose/compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion  
[+] Running 9/9  
 ✔ portainer Pulled              11.5s  
   ✔ f2e6bd2f8c64 Pull complete             1.0s  
   ✔ 0dc69d63cd77 Pull complete             1.5s  
   ✔ 04f56cab0724 Pull complete             2.8s  
   ✔ bcfc9a66ec82 Pull complete             3.4s  
   ✔ b425a5923e60 Pull complete             5.7s  
   ✔ 0b2aaa6c7a76 Pull complete             7.0s  
   ✔ 9602c3f3fa3d Pull complete             7.5s  
   ✔ 4f4fb700ef54 Pull complete             8.1s  
[+] Running 1/1  
 ✔ Container compose-portainer-1  Started              4.3s  
**Запустился только compose.yaml, так как он самый предпочтительный в данной версии docker-compose**  
**Для запуска обоих файлов в файле compose.yaml необходимо использовать дополнение в виде директивы include** 
### 2 Задание.  
**/DOCKER_TEST/compose# cat compose.yaml**  
version: "3"  
include:  
  - ./docker-compose.yaml  
services:  
  portainer:  
    network_mode: host  
    image: portainer/portainer-ce:latest  
    volumes:  
    - /var/run/docker.sock:/var/run/docker.sock

**/DOCKER_TEST/compose# docker-compose up -d**  
WARN[0000] Found multiple config files with supported names: /DOCKER_TEST/compose/compose.yaml, /DOCKER_TEST/compose/docker-compose.yaml  
WARN[0000] Using /DOCKER_TEST/compose/compose.yaml  
WARN[0000] /DOCKER_TEST/compose/docker-compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion  
WARN[0000] /DOCKER_TEST/compose/compose.yaml: the attribute `version` is obsolete, it will be ignored, please remove it to avoid potential confusion  
[+] Running 6/6  
 ✔ registry Pulled              8.2s  
   ✔ 44cf07d57ee4 Pull complete             1.7s  
   ✔ bbbdd6c6894b Pull complete             2.4s  
   ✔ 8e82f80af0de Pull complete             3.2s  
   ✔ 3493bf46cdec Pull complete             3.7s  
   ✔ 6d464ea18732 Pull complete             4.2s  
[+] Running 2/2  
 ✔ Container compose-portainer-1  Started             4.9s  
 ✔ Container compose-registry-1   Started             5.8s  
**/DOCKER_TEST/vol_doc# docker ps -a**  
CONTAINER ID   IMAGE                           COMMAND                  CREATED             STATUS              PORTS                                         NAMES  
cdd57d34b4e8   portainer/portainer-ce:latest   "/portainer"             2 minutes ago       Up About a minute                                                 compose-portainer-1  
60bbf1d50f97   registry:2                      "/entrypoint.sh /etc…"   2 minutes ago       Up About a minute   0.0.0.0:5000->5000/tcp, [::]:5000->5000/tcp   compose-registry-1  
### 3 Задание. 
**/DOCKER_TEST/vol_doc# docker tag zzugly/custom-nginx:1.0.0 localhost:5000/custom-nginx:latest**  
**/DOCKER_TEST/vol_doc# docker push localhost:5000/custom-nginx:latest**  
The push refers to repository [localhost:5000/custom-nginx]  
d58398fb5623: Pushed  
2e174fd56089: Pushed  
727839498dfa: Pushed  
508937af8963: Pushed  
e9b5d470f331: Pushed  
5e1b8f458cec: Pushed  
d89e58119fc7: Pushed  
eb5f13bce993: Pushed  
latest: digest: sha256:9f47a8b80cd1474ca46698d9e9de1fdbf2688e23471887538784b1f8177a96b7 size: 1985  
**/DOCKER_TEST/vol_doc# docker images**  
REPOSITORY                    TAG       IMAGE ID       CREATED        SIZE  
zzugly/custom-nginx           1.0.0     ccae95834854   29 hours ago   192MB  
localhost:5000/custom-nginx   latest    ccae95834854   29 hours ago   192MB  
portainer/portainer-ce        latest    9bde3c70195f   12 days ago    186MB  
nginx                         1.29.0    7a073be66c4c   4 months ago   192MB  
registry                      2         26b2eb03618e   2 years ago    25.4MB  
debian                        9         662c05203bab   3 years ago    101MB  
centos                        8         5d0da3dc9764   4 years ago    231MB  

### 5 Задание.
<img width="1256" height="419" alt="image" src="https://github.com/user-attachments/assets/f5ea8055-01cd-4da0-af63-f9904e06236c" />

### 6 Задание. 
        AppArmorProfile:"docker-default",
        Args:[
        "nginx",
        "-g",
        "daemon off;"
        ],
        Config:{
        AttachStderr:true,
        AttachStdin:false,
        AttachStdout:true,
        Cmd:[
        "nginx",
        "-g",
        "daemon off;"
        ],
        Domainname:"",
        Entrypoint:[
        "/docker-entrypoint.sh"
        ],
        Env:[
        "PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin",
        "NGINX_VERSION=1.29.0",
        "NJS_VERSION=0.9.0",
        "NJS_RELEASE=1~bookworm",
        "PKG_RELEASE=1~bookworm",
        "DYNPKG_RELEASE=1~bookworm"
        ],
        ExposedPorts:{
        80/tcp:{
        }
        },
        Hostname:"10deed95169d",
        Image:"127.0.0.1:5000/custom-nginx",
        Labels:{
        com.docker.compose.config-hash:"8b9fe9ab3a7934244a4cb3d97ea83abe99d1849b88a7d7931370a021dd008c42",
        com.docker.compose.container-number:"1",
        com.docker.compose.depends_on:"",
        com.docker.compose.image:"sha256:ccae95834854dc24dbf0714d4833dd524ef07aa9240881586ef95373cd3b7c0e",
        com.docker.compose.oneoff:"False",
        com.docker.compose.project:"nginx",
        com.docker.compose.project.config_files:"/data/compose/1/docker-compose.yml",
        com.docker.compose.project.working_dir:"/data/compose/1",
        com.docker.compose.service:"nginx",
        com.docker.compose.version:"",
        maintainer:"NGINX Docker Maintainers <docker-maint@nginx.com>"
        },
        OnBuild:null,
        OpenStdin:false,
        StdinOnce:false,
        StopSignal:"SIGQUIT",
        Tty:false,
        User:"",
        Volumes:null,
        WorkingDir:""
        },
        Created:"2025-12-10T06:13:44.364611629Z",
        Driver:"overlay2",







 
