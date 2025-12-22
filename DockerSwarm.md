# netorep
# Домашнее задание к занятию 6. «Оркестрация кластером Docker контейнеров на примере Docker Swarm»
## Задача 1.

### 1-2 Задание.
#### С помощью packer из образа в котором уже есть Docker, cоздано 3 облачные виртуальные машины в одной сети в Яндекс облаке.
<img width="775" height="126" alt="image" src="https://github.com/user-attachments/assets/5c676ef8-39da-468c-9477-00cfc07320c4" />
<img width="802" height="165" alt="image" src="https://github.com/user-attachments/assets/f70fcc45-8fd9-4092-9b70-f7b347eefdbd" />

### 3 Задание. 
#### Инициализация кластреа на мастер узле.
<img width="1016" height="218" alt="image" src="https://github.com/user-attachments/assets/ec0ad30f-ebae-478d-a4a4-ad1bb800edac" />

#### Добавление node worker 1 в кластер.
<img width="1006" height="51" alt="image" src="https://github.com/user-attachments/assets/f281af31-ae2b-41f1-8716-4277b78b57bb" />

#### Добавление node worker 2 в кластер.
<img width="1066" height="48" alt="image" src="https://github.com/user-attachments/assets/bb880718-51b8-4774-8983-246f92173498" />

### 4 Задание.
#### Просмотр текущего состава кластера.
<img width="990" height="85" alt="image" src="https://github.com/user-attachments/assets/e61bbf37-61c4-4e14-8b56-21c9e48980e1" />

## Задача 2.

### 1 Задание.
#### Проект задиплоен просто в виде отдельных 4 сервисов. Как задумано приложение не работает - просто тестируется работа четырех сервисов в кластер swarm.
#### Создать общий compose.yaml.
<img width="882" height="981" alt="image" src="https://github.com/user-attachments/assets/872126b6-9c44-4d95-9436-55029af333b3" />

#### Выполнить деплой.
<img width="917" height="258" alt="image" src="https://github.com/user-attachments/assets/7e96398d-4c63-4678-819c-7dec86c8ece9" />

#### Просмотр стэка и сервисов.
<img width="1043" height="407" alt="image" src="https://github.com/user-attachments/assets/d4cd75a7-5ac5-4e92-bbed-0a4552d37f4d" />

#### Просмотр контейнеров по узлам кластера.
<img width="1068" height="53" alt="image" src="https://github.com/user-attachments/assets/d9116eb4-c453-4eba-adab-cb1f7f6615d9" />
<img width="1250" height="72" alt="image" src="https://github.com/user-attachments/assets/c7e10cd8-7974-4309-917d-5f12f3d9e1ab" />
<img width="1170" height="99" alt="image" src="https://github.com/user-attachments/assets/a812813a-3692-4182-be95-8cd02340a10d" />

#### Проверка кластера swarm
#### Выполнить выключение одного узла (worker) кластера.
<img width="1484" height="376" alt="image" src="https://github.com/user-attachments/assets/43e8c63a-5680-408b-b441-db7e00d56fd4" />

#### Просмотр текущего состава кластера.
<img width="754" height="84" alt="image" src="https://github.com/user-attachments/assets/f5c6989f-d995-44f6-82ae-9e18bf81d042" />

#### Просмотр стэка и сервисов. Два сервиса с отключенного узла поднялись на первом (worker) узле.
<img width="1028" height="126" alt="image" src="https://github.com/user-attachments/assets/dab589b8-0d74-4418-ba5b-26fba8d3b30a" />
<img width="1246" height="134" alt="image" src="https://github.com/user-attachments/assets/7878f30f-3c0c-4020-abc1-55b16fe93899" />












