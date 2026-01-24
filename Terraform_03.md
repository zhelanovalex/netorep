# netorep
# # Домашнее задание к занятию «Управляющие конструкции в коде Terraform»
https://github.com/zhelanovalex/ter-homeworks/tree/main/03/src

## Задание 1

### 1. Изучите проект.
#### Внес переменную для имени security_group.
<img width="443" height="85" alt="image" src="https://github.com/user-attachments/assets/f0c7ed1e-6772-4e67-87fc-08a13da8639e" />
<img width="579" height="88" alt="image" src="https://github.com/user-attachments/assets/9fe1baa7-f5ca-4226-9e64-0035f7e4bf6d" />

### 2.Инициализируйте проект, выполните код
<img width="749" height="370" alt="image" src="https://github.com/user-attachments/assets/0905cccc-98cf-46f9-a3ab-97f01ed3acd3" />
<img width="844" height="178" alt="image" src="https://github.com/user-attachments/assets/f73e2e58-e079-46e3-be3e-d0adc7f19948" />

### 3.Приложите скриншот входящих правил «Группы безопасности» в ЛК Yandex Cloud.
<img width="572" height="785" alt="image" src="https://github.com/user-attachments/assets/4e224428-66bf-40a0-8949-cb2b57360e53" />
<img width="925" height="560" alt="image" src="https://github.com/user-attachments/assets/8ca6dab7-447b-4cc6-9f7e-c5f27c52a95e" />

## Задание 2

### 1. Создайте файл count-vm.tf. Опишите в нём создание двух одинаковых ВМ web-1 и web-2 (не web-0 и web-1) с минимальными параметрами, используя мета-аргумент count loop. Назначьте ВМ созданную в первом задании группу безопасности.
<img width="608" height="313" alt="image" src="https://github.com/user-attachments/assets/2f048ebc-a1f9-4f9d-be14-ed1769e00cbb" />
<img width="647" height="530" alt="image" src="https://github.com/user-attachments/assets/c5b21165-5f33-4ae3-9bd3-16a345ef1a16" />  

### 2. Создайте файл for_each-vm.tf. Опишите в нём создание двух ВМ для баз данных с именами "main" и "replica" разных по cpu/ram/disk_volume , используя мета-аргумент for_each loop. Используйте для обеих ВМ одну общую переменную/
<img width="648" height="460" alt="image" src="https://github.com/user-attachments/assets/a878e501-dcb5-45d7-8f1f-3cac34bedf4f" />
<img width="611" height="478" alt="image" src="https://github.com/user-attachments/assets/9482ba31-a6a8-4faf-8cd9-e3195e611204" />  

