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

#### - Role lighthouse was created successfully  
