# netorep
# Домашнее задание к занятию «Настройка приложений и управление доступом в Kubernetes»

## Чеклист готовности к домашнему заданию
### Установленное k8s-решение MicroK8S на yandex VMs.
<img width="831" height="186" alt="image" src="https://github.com/user-attachments/assets/bd7c0ff8-110d-436d-a483-0c20cb6425d1" />

### Узлы собраны в кластер.
<img width="651" height="85" alt="image" src="https://github.com/user-attachments/assets/c14b1882-070b-4125-895b-a43fb7fc7769" />

### Установлен на локальном компьютере kubectl.
<img width="641" height="133" alt="image" src="https://github.com/user-attachments/assets/9379bb5f-74d6-439f-943d-3ace4db81aee" />

### Сылка на манифесты.
https://github.com/zhelanovalex/kuber-homeworks/tree/main/2.3/src

## Задание 1: Работа с ConfigMaps.
### Развернуть приложение (nginx + multitool), решить проблему конфигурации через ConfigMap и подключить веб-страницу.
#### Создан ConfigMap.
<img width="646" height="307" alt="image" src="https://github.com/user-attachments/assets/605b7241-3ff4-4c26-83d2-fa681f184aab" />
----
<img width="796" height="611" alt="image" src="https://github.com/user-attachments/assets/41ef6d81-678f-44fa-aef6-feed47daed79" />

#### Создан Deployment с двумя контейнерами nginx и multitool.
<img width="626" height="699" alt="image" src="https://github.com/user-attachments/assets/ca26f252-921d-4788-8e62-3880db962636" />
----
<img width="697" height="137" alt="image" src="https://github.com/user-attachments/assets/3d0ba6d9-039a-403d-a841-062539fe4424" />

#### Создан сервис для Deployment с двумя контейнерами nginx и multitool.
<img width="648" height="320" alt="image" src="https://github.com/user-attachments/assets/dda85c1e-9725-4ae6-b4c8-a29cd8c0d092" />
<img width="766" height="72" alt="image" src="https://github.com/user-attachments/assets/700cc122-4550-4006-9ffa-a5e1af34e9f0" />

#### Создан ingess.
<img width="606" height="402" alt="image" src="https://github.com/user-attachments/assets/ec471351-cd35-4703-b177-9a7378507398" />
<img width="854" height="292" alt="image" src="https://github.com/user-attachments/assets/60e08196-6e24-4582-a5aa-99339e48aa86" />
