# netorep
# Домашнее задание к занятию 5 «Тестирование roles»

## Подготовка к выполнению
### Установите molecule и его драйвера: pip3 install "molecule molecule_docker molecule_podman.
<img width="1072" height="356" alt="image" src="https://github.com/user-attachments/assets/9d061d18-a904-4996-9455-9d21d0be73ae" />

### Выполните docker pull aragast/netology:latest — это образ с podman, tox и несколькими пайтонами (3.7 и 3.9) внутри.
<img width="844" height="41" alt="image" src="https://github.com/user-attachments/assets/b99dce79-eb36-4c6d-afe4-7da2d790e9e6" />

## Основная часть
## Molecule
### Запустите molecule test -s ubuntu_xenial (или с любым другим сценарием, не имеет значения) внутри корневой директории clickhouse-role, посмотрите на вывод команды.
<img width="681" height="106" alt="image" src="https://github.com/user-attachments/assets/51bed385-fff6-4b23-94b7-9d6d5dac0ce9" /> 

### Перейдите в каталог с ролью vector-role и создайте сценарий тестирования по умолчанию при помощи molecule init scenario --driver-name docker.
<img width="894" height="325" alt="image" src="https://github.com/user-attachments/assets/a55bb575-0594-4bd7-afff-a77432c53f17" />

### Добавьте несколько разных дистрибутивов (oraclelinux:8, ubuntu:latest) для инстансов и протестируйте роль, исправьте найденные ошибки, если они есть.
#### В связи смногочисленными ошибками для роли пришлось создать отдельный image на основе centos:centos7.9.2009.
<img width="769" height="377" alt="image" src="https://github.com/user-attachments/assets/dc50bcfd-2093-4cf7-9bed-06f62374098a" />

#### Ссылка на созданный docker image.
https://hub.docker.com/repository/docker/zzugly/centoc_ansib/general

#### В самой роле пришлось вносить некоторые изменеения, в частности ссылки на inventory playbook, которого нет.
<img width="793" height="379" alt="image" src="https://github.com/user-attachments/assets/67b54f27-3e40-471e-bd43-58d5664ae1d2" />

#### После решения дополнительных проблем с systemd в docker - тестирование роли отработало.
<img width="1160" height="452" alt="image" src="https://github.com/user-attachments/assets/1d004c3a-94a9-4927-b6d4-a061c7810e65" />

#### Добавьте новый тег "Molecule" на коммит с рабочим сценарием в соответствии с семантическим версионированием.
https://github.com/zhelanovalex/Vector_role

## Tox
### Запустите docker run --privileged=True -v <path_to_repo>:/opt/vector-role -w /opt/vector-role -it aragast/netology:latest /bin/bash, где path_to_repo — путь до корня репозитория с vector-role на вашей файловой системе.
<img width="1187" height="69" alt="image" src="https://github.com/user-attachments/assets/6e393172-fe36-474d-9603-fd50647eaad1" />

### Внутри контейнера выполните команду tox, посмотрите на вывод.
<img width="1406" height="488" alt="image" src="https://github.com/user-attachments/assets/6f5631c4-8638-4a7b-9276-ce44cec1f847" />

### Создайте облегчённый сценарий для molecule с драйвером molecule_podman. Проверьте его на исполнимость.
<img width="817" height="442" alt="image" src="https://github.com/user-attachments/assets/adbd75cb-a0a8-4bfd-a7a3-34325066391b" />

#### Тестирование роли с помощью tox не удалось. Любые комбинации tox.ini падают с одной ошибкой.
<img width="1383" height="914" alt="image" src="https://github.com/user-attachments/assets/246f89c4-adf9-462f-9689-c2b164457663" />



