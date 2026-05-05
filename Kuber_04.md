# netorep
# Домашнее задание к занятию «Сетевое взаимодействие в Kubernetes».

## Чеклист готовности к домашнему заданию
### Установленное k8s-решение MicroK8S на yandex VMs.
<img width="846" height="180" alt="image" src="https://github.com/user-attachments/assets/cccfa400-ce0c-45f6-8ff9-f817a565b784" />

### Узлы собраны в кластер.
<img width="602" height="84" alt="image" src="https://github.com/user-attachments/assets/6dfb79f4-267d-4d5e-b5e0-23bc50c4ad64" />

### Установлен на локальном компьютере kubectl.
<img width="682" height="134" alt="image" src="https://github.com/user-attachments/assets/df007acf-5bde-4e9d-844a-610122b63d8e" />

### Сылка на манифесты.
https://github.com/zhelanovalex/kuber-homeworks/tree/main/1.4/src

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
#### Проверить доступность изнутри кластера.
<img width="1191" height="134" alt="image" src="https://github.com/user-attachments/assets/f8d2ffb4-9a9d-46c2-8e91-4b7a0a6a6877" />
----
<img width="1192" height="321" alt="image" src="https://github.com/user-attachments/assets/257b06d1-aa80-4931-85dd-3997a6cc31d0" />

### Создать Service типа NodePort для доступа к nginx снаружи.
<img width="835" height="327" alt="image" src="https://github.com/user-attachments/assets/c1494e90-a920-4424-a918-f25d287413c8" />
----
<img width="1033" height="120" alt="image" src="https://github.com/user-attachments/assets/34d77c58-41a8-47f3-ad0e-a8fb4d5b1d95" />
#### Проверить доступ с локального компьютера.
<img width="785" height="351" alt="image" src="https://github.com/user-attachments/assets/d570d4fc-8428-4043-b85c-25bf085842f1" />
----
<img width="1155" height="339" alt="image" src="https://github.com/user-attachments/assets/c30bdff0-6b34-4f0b-9feb-24ddb524c9b9" />
----
<img width="1167" height="335" alt="image" src="https://github.com/user-attachments/assets/4762c97c-6722-4348-96cf-6df2046fd1a3" />
----
<img width="1183" height="193" alt="image" src="https://github.com/user-attachments/assets/2cbe3a88-ce47-4f1c-930f-402325f8cb7f" />
----
<img width="1081" height="79" alt="image" src="https://github.com/user-attachments/assets/49dc7682-d5b8-4fc5-b260-326ea9668cc2" />
----
<img width="1091" height="94" alt="image" src="https://github.com/user-attachments/assets/b25bae97-9da6-421e-85f9-cc7747e36d86" />

## Задание 2: Настройка Ingress (Развернуть два приложения (frontend и backend) и обеспечить доступ к ним через Ingress по разным путям)
### Развернуть два Deployment: frontend (образ nginx) и backend (образ wbitt/network-multitool).
<img width="822" height="373" alt="image" src="https://github.com/user-attachments/assets/f4e17aec-3b58-443e-bd7a-313627a46d53" />
----
<img width="702" height="376" alt="image" src="https://github.com/user-attachments/assets/f9314ada-7782-43c1-aeb3-e47e456061ea" />
----
<img width="775" height="68" alt="image" src="https://github.com/user-attachments/assets/40a5f2e2-4bba-472f-8f9c-6d15b368f166" />
----
<img width="1056" height="106" alt="image" src="https://github.com/user-attachments/assets/56812875-7b96-4541-9d20-71ce1086cd39" />

### Создать Service для каждого приложения.
<img width="656" height="259" alt="image" src="https://github.com/user-attachments/assets/77e60c56-3368-4bf5-8272-333cda6c9153" />
----
<img width="617" height="265" alt="image" src="https://github.com/user-attachments/assets/7525fc5b-d564-42d1-9750-cf3700bfea17" />
----
<img width="776" height="84" alt="image" src="https://github.com/user-attachments/assets/7043220a-a80e-4c93-a7ce-21f79f58b984" />

### Включить Ingress-контроллер.
<img width="824" height="233" alt="image" src="https://github.com/user-attachments/assets/c30bb7af-36fe-4398-886a-c0e180d4007a" />

### Создать Ingress, который: открывает frontend по пути / и открывает backend по пути /api.
<img width="730" height="405" alt="image" src="https://github.com/user-attachments/assets/cd381f16-b442-4c6e-b7fd-072b63fb3389" />
----
<img width="824" height="91" alt="image" src="https://github.com/user-attachments/assets/a431a097-7b9f-403b-af2c-f5d7381abff6" />

#### Проверить доступность.
<img width="559" height="219" alt="image" src="https://github.com/user-attachments/assets/a61dfea7-ec8d-491b-82e4-8ee0a503c5da" />
----
<img width="1185" height="765" alt="image" src="https://github.com/user-attachments/assets/3b4ff666-bbbc-43ce-8d5b-8d436b4a1c81" />
----
<img width="1118" height="95" alt="image" src="https://github.com/user-attachments/assets/3887ecad-7ddc-4299-997c-8ad449205fd3" />
----
<img width="1133" height="113" alt="image" src="https://github.com/user-attachments/assets/d4eff50a-ddc2-4e0d-873a-8486cc16fe9a" />
----
<img width="1126" height="329" alt="image" src="https://github.com/user-attachments/assets/d746c6c3-e07f-4011-a3af-b91f07a9a718" />
----
<img width="1132" height="352" alt="image" src="https://github.com/user-attachments/assets/3e13a903-e0d1-4340-a913-3f69e8fa0b4f" />

