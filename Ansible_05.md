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

