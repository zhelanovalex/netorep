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

### Single task playbook преобразуйте в single task role и перенесите в collection. У role должны быть default всех параметров module.
<img width="880" height="255" alt="image" src="https://github.com/user-attachments/assets/7e715034-a9a6-40e3-8f1a-327c95be1843" />

### Создайте playbook для использования этой role.
<img width="919" height="122" alt="image" src="https://github.com/user-attachments/assets/fed57cce-ab3d-46ec-9cef-69cae1abce23" />

### В эту collection перенесите свой module в соответствующую директорию.
<img width="800" height="99" alt="image" src="https://github.com/user-attachments/assets/ce46afeb-8dd0-4477-b632-8adb08bf7014" />

### Заполните всю документацию по collection, выложите в свой репозиторий, поставьте тег 1.0.0 на этот коммит.
https://github.com/zhelanovalex/my_neto_collection/tree/main/AnsibCollect/neto_collect

### Создайте .tar.gz этой collection: ansible-galaxy collection build в корневой директории collection.
<img width="1250" height="100" alt="image" src="https://github.com/user-attachments/assets/512012a4-8927-41dd-9b91-81f27e56b7c0" />

### Создайте ещё одну директорию любого наименования, перенесите туда single task playbook и архив c collection.
<img width="811" height="53" alt="image" src="https://github.com/user-attachments/assets/7fb4b9f2-62bf-4ff6-a5ca-bbfa64f8e56a" />

### Установите collection из локального архива: ansible-galaxy collection install <archivename>.tar.gz.
<img width="1328" height="154" alt="image" src="https://github.com/user-attachments/assets/1b6a4162-95c9-4357-a196-4e53268bb0bb" />

### Запустите playbook, убедитесь, что он работает.
#### Перед проверкой изменили содержимое искомого файла.
<img width="1431" height="795" alt="image" src="https://github.com/user-attachments/assets/bda71faf-1a6c-48ca-b1cf-9fe4c0a26202" />


