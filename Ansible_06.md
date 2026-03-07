# netorep
# Домашнее задание к занятию 6 «Создание собственных модулей»

## Подготовка к выполнению
### Создайте пустой публичный репозиторий в своём любом проекте: my_own_collection.
https://github.com/zhelanovalex/my_neto_collection

### Скачайте репозиторий Ansible: git clone https://github.com/ansible/ansible.git по любому, удобному вам пути.
<img width="1325" height="702" alt="image" src="https://github.com/user-attachments/assets/8906df3b-b53e-4fd0-8f1b-727b8d84db3c" />

#### Так как тестирование модуля выдавало ошибку. 
<img width="1365" height="40" alt="image" src="https://github.com/user-attachments/assets/fb9bc430-374a-4bb4-a1d5-e145d7a64b19" />

#### Проведено переключение на соответствующую ветку репозитория.
<img width="780" height="326" alt="image" src="https://github.com/user-attachments/assets/e77f7161-ea08-4469-bdab-4a272e970281" />

### Настроить виртуальное окружение.
<img width="1775" height="899" alt="image" src="https://github.com/user-attachments/assets/3d4f7c9d-2aaa-434c-8d19-298ba6ec0136" />

## Основная часть

### В виртуальном окружении создан новый my_neto_module.py файл с соответствующим содержимым.
<img width="1032" height="41" alt="image" src="https://github.com/user-attachments/assets/a4c8263d-835b-4f6b-a36e-aa6d3029d72e" />

### Проверьте module на исполняемость локально.

#### Создан файл.
<img width="783" height="117" alt="image" src="https://github.com/user-attachments/assets/4f7b4278-35a7-41a2-b698-657e13ee328e" />

#### Выполнена проверка.
<img width="1120" height="133" alt="image" src="https://github.com/user-attachments/assets/80cc24ee-e592-4c86-9289-9b23d5f71654" />

### Напишите single task playbook и используйте module в нём.
<img width="833" height="191" alt="image" src="https://github.com/user-attachments/assets/c2b89f7f-0081-48b8-a137-5fa62cc80d3e" />

### Проверьте через playbook на идемпотентность.
<img width="1838" height="532" alt="image" src="https://github.com/user-attachments/assets/dd87fb6f-55df-43cb-8f80-6592451f74db" />

### Инициализируйте новую collection.
<img width="961" height="354" alt="image" src="https://github.com/user-attachments/assets/84cb4ecf-c24d-4dd2-a50e-31b7f5bc50e5" />

### В эту collection перенесите свой module в соответствующую директорию.
<img width="800" height="99" alt="image" src="https://github.com/user-attachments/assets/ce46afeb-8dd0-4477-b632-8adb08bf7014" />

### 
