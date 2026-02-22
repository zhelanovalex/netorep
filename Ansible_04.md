# netorep
# Домашнее задание к занятию 4 «Работа с roles»

## Основная часть.

### На основе tasks из старого playbook создана новая role clickhouse.

### Создан репозиторий и роль скопирована в него.
https://github.com/zhelanovalex/Clickhouse_role
### Создан файл requirements.yml:
<img width="788" height="130" alt="image" src="https://github.com/user-attachments/assets/12bfb9b9-609e-4574-8fd1-91309cb5ba71" />

### При помощи ansible-galaxy скачайте себе эту роль.
<img width="981" height="197" alt="image" src="https://github.com/user-attachments/assets/c824cae3-2528-4d74-822e-a44d8a20aafa" />

### Создан новый каталог с ролями при помощи ansible-galaxy role init vector и lighthouse.   
#### root@Uglycomp:/ANSIBLE_TEST/AnsibNeto/08-ansible-04-role/playbook/roles# ansible-galaxy role init vector   
#### - Role vector was created successfully  
#### root@Uglycomp:/ANSIBLE_TEST/AnsibNeto/08-ansible-04-role/playbook/roles# ansible-galaxy role init lighthouse  
#### - Role lighthouse was created successfully  

#### На основе tasks из старого playbook заполнены новые role. Разнесены переменные между vars и default.

#### Перенесены нужные шаблоны конфигов в templates.

#### Описаны в README.md обе роли и их параметры. Пример качественной документации ansible role по ссылке.

### Выложены все roles в репозитории. 
https://github.com/zhelanovalex/Clickhouse_role  
https://github.com/zhelanovalex/Vector_role  
https://github.com/zhelanovalex/Lighthouse_role  

### Добавьте roles в requirements.yml в playbook.
<img width="837" height="230" alt="image" src="https://github.com/user-attachments/assets/d9dbc8ba-7f83-4a97-8416-c0fb11d329d3" />

### В ответе дайте ссылки на оба репозитория с roles и одну ссылку на репозиторий с playbook.
https://github.com/zhelanovalex/mnt-homeworks/tree/MNT-video/08-ansible-04-role/playbook  

