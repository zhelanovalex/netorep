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

### 2. Создайте файл for_each-vm.tf. Опишите в нём создание двух ВМ для баз данных с именами "main" и "replica" разных по cpu/ram/disk_volume , используя мета-аргумент for_each loop. Используйте для обеих ВМ одну общую переменную.
<img width="648" height="460" alt="image" src="https://github.com/user-attachments/assets/a878e501-dcb5-45d7-8f1f-3cac34bedf4f" />
<img width="611" height="478" alt="image" src="https://github.com/user-attachments/assets/9482ba31-a6a8-4faf-8cd9-e3195e611204" />  

### 5. Используйте функцию file в local-переменной для считывания ключа ~/.ssh/id_rsa.pub и его последующего использования в блоке metadata.
<img width="653" height="94" alt="image" src="https://github.com/user-attachments/assets/6577cbb5-e0ab-4a8c-b964-7ea97e649abe" />

### 6. Инициализируйте проект, выполните код.
<img width="933" height="627" alt="image" src="https://github.com/user-attachments/assets/d449d48e-5a44-4423-965a-fc515abb4fe6" />
<img width="939" height="174" alt="image" src="https://github.com/user-attachments/assets/e3873135-d1df-4cb0-b96b-24d925a1f2ad" />

#### Проверка назначения ВМ в группу безопасности.
<img width="948" height="171" alt="image" src="https://github.com/user-attachments/assets/9898a05e-3329-4318-8196-819b7aeccc4e" />
<img width="834" height="899" alt="image" src="https://github.com/user-attachments/assets/49bbfd1f-5614-424b-aeac-eebea4926237" />

## Задание 3

### 1.Создайте 3 одинаковых виртуальных диска размером 1 Гб с помощью ресурса yandex_compute_disk и мета-аргумента count в файле disk_vm.tf.
<img width="914" height="454" alt="image" src="https://github.com/user-attachments/assets/dd8deb43-62ea-4167-99a2-9e86bf554e61" />
<img width="714" height="129" alt="image" src="https://github.com/user-attachments/assets/f706f60e-f855-438f-af90-a8969bff7741" />
<img width="883" height="178" alt="image" src="https://github.com/user-attachments/assets/459bf8fd-be3d-4bce-a968-6983d532154e" />
<img width="1133" height="215" alt="image" src="https://github.com/user-attachments/assets/28e5c06c-d28a-4719-acee-f44bb22e0c01" />


