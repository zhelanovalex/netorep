# netorep
# Домашнее задание к занятию «Сетевое взаимодействие в Kubernetes».

## Чеклист готовности к домашнему заданию
### Установленное k8s-решение MicroK8S на yandex VMs.
<img width="846" height="180" alt="image" src="https://github.com/user-attachments/assets/cccfa400-ce0c-45f6-8ff9-f817a565b784" />

### Узлы собраны в кластер.
<img width="602" height="84" alt="image" src="https://github.com/user-attachments/assets/6dfb79f4-267d-4d5e-b5e0-23bc50c4ad64" />

### Установлен на локальном компьютере kubectl.
<img width="682" height="134" alt="image" src="https://github.com/user-attachments/assets/df007acf-5bde-4e9d-844a-610122b63d8e" />

## Задание 1: Настройка Service (ClusterIP и NodePort)
### Создать Deployment приложения, состоящего из двух контейнеров (nginx и multitool), с количеством реплик 3.
<img width="811" height="565" alt="image" src="https://github.com/user-attachments/assets/0eae006c-d720-49fc-ac65-e251b6587a5c" />
----
<img width="824" height="39" alt="image" src="https://github.com/user-attachments/assets/47f956fe-e9f1-455e-8869-9d8e918bf5a8" />
----
<img width="1050" height="90" alt="image" src="https://github.com/user-attachments/assets/f0a61bbf-4831-4f49-90eb-62a3ce76a9c8" />

### Создать Service типа ClusterIP, который обеспечит доступ внутри кластера до контейнеров приложения из п.1 по порту 9001 — nginx 80, по 9002 — multitool 8080.
<img width="674" height="322" alt="image" src="https://github.com/user-attachments/assets/69c94da8-9d03-4dc0-a656-a7aeecc64e6a" />
----
<img width="833" height="102" alt="image" src="https://github.com/user-attachments/assets/677fa53e-681e-46a5-b837-5116c476b2d6" />
