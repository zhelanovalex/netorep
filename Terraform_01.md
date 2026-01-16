# netorep
# Домашнее задание к занятию «Введение в Terraform»

## Чек-лист готовности к домашнему заданию.

### 1. Проверка terraform.
<img width="578" height="54" alt="image" src="https://github.com/user-attachments/assets/e1f384d2-aa64-4a9a-8ffb-c6ffe7f53e15" />

### 2. Проверка git.
<img width="492" height="213" alt="image" src="https://github.com/user-attachments/assets/ef916187-5c1b-4961-bd6f-f6dcbcecf245" />

### 2. Проверка docker.
<img width="565" height="452" alt="image" src="https://github.com/user-attachments/assets/e93eaf1e-29e8-4505-8f5c-944b8bb0e363" />

## Внимание!! Обязательно предоставляем на проверку получившийся код в виде ссылки на ваш github-репозиторий!
https://github.com/zhelanovalex/ter-homeworks

## Задание 1.

### 1. Перейдите в каталог src. Скачайте все необходимые зависимости, использованные в проекте.
<img width="718" height="561" alt="image" src="https://github.com/user-attachments/assets/30f4f182-76a7-4b09-8693-d87c18ab6b35" />

### 2. Изучите файл .gitignore. В каком terraform-файле, согласно этому .gitignore, допустимо сохранить личную, секретную информацию?(логины,пароли,ключи,токены итд)
Согласно данному файлу исключений, допустимо хранить секретную информацию в файлах terraform.tfstate, terraform.tfstate.backup и т.д.  
<img width="566" height="169" alt="image" src="https://github.com/user-attachments/assets/32f52770-12ba-4b90-b628-4365358d4267" />

### 3. Выполните код проекта. Найдите в state-файле секретное содержимое созданного ресурса random_password, пришлите в качестве ответа конкретный ключ и его значение.
<img width="583" height="149" alt="image" src="https://github.com/user-attachments/assets/33d3a1a0-bd65-49d9-a9fb-6bee9855b171" />

### 4. Раскомментируйте блок кода, примерно расположенный на строчках 29–42 файла main.tf. Выполните команду terraform validate. Объясните, в чём заключаются намеренно допущенные ошибки. Исправьте их.
<img width="783" height="612" alt="image" src="https://github.com/user-attachments/assets/8147e5d8-ffc1-4e6b-ada0-60af217f23e7" />  

1. Текущая версия terraform не поддерживает версию 1.12.0.  
2. Должно быть указано имя ресурса.  
3. Имя ресурса не должно начинаться с цифры.  
4. Не совпадает имя ресурса и ссылка на него.  
5. Опечатка в букве.

### 5. Выполните код. В качестве ответа приложите: исправленный фрагмент кода и вывод команды docker ps.
<img width="748" height="643" alt="image" src="https://github.com/user-attachments/assets/3d65a18f-fc6d-49e9-b780-db281d495dda" />
<img width="1112" height="52" alt="image" src="https://github.com/user-attachments/assets/744e736f-2026-407d-8ac4-db98be61b74a" />

### 6. Замените имя docker-контейнера в блоке кода на hello_world. Не перепутайте имя контейнера и имя образа. Мы всё ещё продолжаем использовать name = "nginx:latest". Выполните команду terraform apply -auto-approve. Объясните своими словами, в чём может быть опасность применения ключа -auto-approve. Догадайтесь или нагуглите зачем может пригодиться данный ключ? В качестве ответа дополнительно приложите вывод команды docker ps.

Данный ключ подразумевает отсутствие контороля и проверки, что может быть опасно при ошибках в плане.  
Подходит для скриптов, где естественно нет введения подтверждений.   

<img width="1019" height="52" alt="image" src="https://github.com/user-attachments/assets/98602ca8-841c-4c2b-80c8-d07906128bb9" />


### 7. Уничтожьте созданные ресурсы с помощью terraform. Убедитесь, что все ресурсы удалены. Приложите содержимое файла terraform.tfstate.
<img width="800" height="164" alt="image" src="https://github.com/user-attachments/assets/ca48970a-cb04-4eeb-9e02-1a0a7e0647c8" />

### 8. Объясните, почему при этом не был удалён docker-образ nginx:latest. Ответ ОБЯЗАТЕЛЬНО НАЙДИТЕ В ПРЕДОСТАВЛЕННОМ КОДЕ, а затем ОБЯЗАТЕЛЬНО ПОДКРЕПИТЕ строчкой из документации terraform провайдера docker. (ищите в классификаторе resource docker_image )

Выставлен параметр keep_locally = true в описании ресурса docker_image.

<img width="407" height="101" alt="image" src="https://github.com/user-attachments/assets/3bc5e3ef-0f1f-419b-9e78-8ccab1595ffb" />
<img width="866" height="381" alt="image" src="https://github.com/user-attachments/assets/1c0d72d9-1d53-429d-b82e-53734d7fd5a6" />















