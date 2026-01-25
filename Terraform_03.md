# netorep
# # Домашнее задание к занятию «Управляющие конструкции в коде Terraform»
https://github.com/zhelanovalex/ter-homeworks/tree/main/03/src
#### ID ресурсов на скриншотах могут не совпадаать, так как проект удалялся и запускался несколько раз.

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
<img width="726" height="504" alt="image" src="https://github.com/user-attachments/assets/b159e35d-09c8-4097-8962-ac6e9f981aca" />
<img width="835" height="480" alt="image" src="https://github.com/user-attachments/assets/23c1e58e-e709-4740-91bf-039eaa126d76" />


### 5. Используйте функцию file в local-переменной для считывания ключа ~/.ssh/id_rsa.pub и его последующего использования в блоке metadata.
<img width="653" height="94" alt="image" src="https://github.com/user-attachments/assets/6577cbb5-e0ab-4a8c-b964-7ea97e649abe" />

### 6. Инициализируйте проект, выполните код.
<img width="933" height="627" alt="image" src="https://github.com/user-attachments/assets/d449d48e-5a44-4423-965a-fc515abb4fe6" />
<img width="878" height="182" alt="image" src="https://github.com/user-attachments/assets/f507bdf8-8b57-4beb-8fb3-db0760f2f583" />

#### Проверка назначения ВМ в группу безопасности.
<img width="969" height="172" alt="image" src="https://github.com/user-attachments/assets/5d0ffc70-f14e-4ca3-b1eb-f854b342303e" />
<img width="924" height="863" alt="image" src="https://github.com/user-attachments/assets/5d5d4a2f-419e-4694-ad5f-5d9bb356cce5" />

## Задание 3

### 1. Создайте 3 одинаковых виртуальных диска размером 1 Гб с помощью ресурса yandex_compute_disk и мета-аргумента count в файле disk_vm.tf.
<img width="914" height="454" alt="image" src="https://github.com/user-attachments/assets/dd8deb43-62ea-4167-99a2-9e86bf554e61" />
<img width="714" height="129" alt="image" src="https://github.com/user-attachments/assets/f706f60e-f855-438f-af90-a8969bff7741" />
<img width="883" height="178" alt="image" src="https://github.com/user-attachments/assets/459bf8fd-be3d-4bce-a968-6983d532154e" />
<img width="1133" height="215" alt="image" src="https://github.com/user-attachments/assets/28e5c06c-d28a-4719-acee-f44bb22e0c01" />
<img width="954" height="127" alt="image" src="https://github.com/user-attachments/assets/dfa391c8-2c2b-4214-8826-d79867a1dca8" />

### 2. Создайте в том же файле одиночную(использовать count или for_each запрещено из-за задания №4) ВМ c именем "storage" . Используйте блок dynamic secondary_disk{..} и мета-аргумент for_each для подключения созданных вами дополнительных дисков.
<img width="772" height="657" alt="image" src="https://github.com/user-attachments/assets/7d2ee62d-cdd3-4b8d-9673-11b6d214a112" />
<img width="875" height="737" alt="image" src="https://github.com/user-attachments/assets/50caaf03-845e-4d11-a918-3dd310bd8546" />
<img width="826" height="183" alt="image" src="https://github.com/user-attachments/assets/d6952b92-7f82-4cbd-8761-dcb88b3073c5" />
<img width="836" height="343" alt="image" src="https://github.com/user-attachments/assets/77d13bde-4114-49af-94b2-d788495e7ded" />

## Задание 4

### 1. В файле ansible.tf создайте inventory-файл для ansible. Используйте функцию tepmplatefile и файл-шаблон для создания ansible inventory-файла из лекции.
<img width="866" height="139" alt="image" src="https://github.com/user-attachments/assets/60ba9711-d644-4a57-a86b-615689b078cd" />
<img width="893" height="310" alt="image" src="https://github.com/user-attachments/assets/e8e6bc23-0ee9-401f-8729-3d187371fe3c" />
<img width="985" height="151" alt="image" src="https://github.com/user-attachments/assets/21c72d85-8e6a-495b-a9aa-fc625c74b62f" />

