# netorep
# Домашнее задание к занятию «Основы Terraform. Yandex Cloud»

## Задание 1

### 2. Создайте сервисный аккаунт и ключ. service_account_key_file.
<img width="774" height="307" alt="image" src="https://github.com/user-attachments/assets/8f8df6b1-874a-44ad-a20e-cd11d71369c5" />
<img width="1312" height="114" alt="image" src="https://github.com/user-attachments/assets/f6403afa-0123-4322-bbb5-2e6445ddbbc1" />
<img width="986" height="111" alt="image" src="https://github.com/user-attachments/assets/383385a5-87d5-4270-b468-2c9c29dea45b" />
<img width="1023" height="47" alt="image" src="https://github.com/user-attachments/assets/29e314d3-b3d3-40c4-b1cb-32cd84f601d2" />

### 3. Сгенерируйте новый или используйте свой текущий ssh-ключ. Запишите его открытую(public) часть в переменную vms_ssh_public_root_key.
<img width="816" height="166" alt="image" src="https://github.com/user-attachments/assets/4742cef9-9a73-4a8d-8842-a5dc0818fe2e" />
<img width="916" height="141" alt="image" src="https://github.com/user-attachments/assets/e7e1d0a7-fce0-4866-8645-07df51ac175d" />

### 4. Инициализируйте проект, выполните код. Исправьте намеренно допущенные синтаксические ошибки. Ищите внимательно, посимвольно. Ответьте, в чём заключается их суть..
<img width="736" height="596" alt="image" src="https://github.com/user-attachments/assets/5aad92cb-ec80-4c93-bf54-6d5cc32d9d90" />
<img width="1443" height="305" alt="image" src="https://github.com/user-attachments/assets/8e75d13b-0e56-4ec8-a933-cc551b21919f" />
<img width="971" height="128" alt="image" src="https://github.com/user-attachments/assets/5aaa3291-7eb2-4708-ba82-013aac39ff3b" />  


Намеренно допущенные синтаксические ошибки это:
1. В файле variables.tf не указаны переменные "cloud_id" и "folder_id" - terraform требует их введения при запуске apply.
2. В файле providers.tf ошибка в переменной service_account_key_file = file("~/.authorized_key.json")
3. В файле main.tf ошибка в описании ресурса resource "yandex_compute_instance" "platform". platform_id = "standarе-v4" - такой платформы нет в yandex облаке. cores         = 1 - такое коллическтво CPU не поддерживает выбранная платформа - минимум 2 должно быть.

### 5. Подключитесь к консоли ВМ через ssh и выполните команду  curl ifconfig.me. Подключитесь к консоли ВМ через ssh и выполните команду  curl ifconfig.me. 
<img width="853" height="724" alt="image" src="https://github.com/user-attachments/assets/86efd457-f8c7-477b-8964-9503d849cde0" />

### 6. Ответьте, как в процессе обучения могут пригодиться параметры preemptible = true и core_fraction=5 в параметрах ВМ.

Параметр preemptible = true полезен тем что:
1. Экономит средлства, так как это опция щначительно удешевляет VM.
2. Привнудительно останавливаются через 24 часа или в случае нехватки ресурсов для обычной виртуальной машины в той же зоне.

Параметр core_fraction=5 полезен тем что:
1. Подходит для приложений, которые редко обращаются к CPU или имеют постоянную, но очень низкую активность.
2. Подходит для тестовых систем и систем разработки, где не нужна производительность.
3. Экономит средлства, так как это самая дешевая опция CPU для VM.


