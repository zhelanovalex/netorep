# netorep
# Домашнее задание к занятию «Helm»

## Чеклист готовности к домашнему заданию
### Установленное k8s-решение MicroK8S на yandex VMs.
<img width="862" height="187" alt="image" src="https://github.com/user-attachments/assets/4b31c1a5-cf6b-43f8-8e2c-40ead3dc8686" />

### Узлы собраны в кластер.
<img width="709" height="87" alt="image" src="https://github.com/user-attachments/assets/3885a70e-9f80-44d8-8fb6-f798f5e23da0" />

### Установлен на локальном компьютере kubectl.
<img width="809" height="136" alt="image" src="https://github.com/user-attachments/assets/9fba5312-e1e7-4035-9c58-fb599530c89f" />

### Установлен на локальном компьютере helm.
<img width="1093" height="53" alt="image" src="https://github.com/user-attachments/assets/3e1d2ead-0f14-4766-bd29-6c3aabe00f99" />

### Сылка на манифесты.
https://github.com/zhelanovalex/kuber-homeworks/tree/main/2.4/src

## Задание 1. Подготовить Helm-чарт для приложения.
### Необходимо упаковать приложение в чарт для деплоя в разные окружения.
<img width="880" height="521" alt="image" src="https://github.com/user-attachments/assets/9a5d2fe9-7c6a-469a-82f7-2afda585ec59" />
----
<img width="821" height="738" alt="image" src="https://github.com/user-attachments/assets/645f9480-e29b-4aac-943d-6e753e4ff12c" />
<img width="637" height="229" alt="image" src="https://github.com/user-attachments/assets/bb621a90-f993-45d8-b38d-b46a75dbbd69" />

### Проверка манифестов.
<img width="756" height="694" alt="image" src="https://github.com/user-attachments/assets/4fc0ff57-0422-4f7c-8430-c6673cd3693e" />

### Запуск по умолчанию.
<img width="734" height="132" alt="image" src="https://github.com/user-attachments/assets/882bd965-8269-457d-84da-ebd17896f559" />
----
<img width="1072" height="53" alt="image" src="https://github.com/user-attachments/assets/678e2ea4-5340-4122-9646-22a85f4ea462" />
<img width="715" height="120" alt="image" src="https://github.com/user-attachments/assets/a146f060-85d2-436d-a1a3-0a21a52d6d2a" />

### Запуск c изменением версии образа и количества репдик.
<img width="1231" height="376" alt="image" src="https://github.com/user-attachments/assets/b5edd7e9-03d2-4904-ac68-5e63f1f34cd4" />
<img width="1153" height="519" alt="image" src="https://github.com/user-attachments/assets/5381a20a-5d86-480f-a7a1-e116bb969754" />
<img width="682" height="71" alt="image" src="https://github.com/user-attachments/assets/4af92106-3997-4d46-99b8-ca0f6563a488" />

## Задание 2. Запустить две версии в разных неймспейсах.
### Запуститe несколько копий приложения. Одну версию в namespace=neto-app1, вторую версию в том же неймспейсе, третью версию в namespace=neto-app2.
### Создать namespace neto-app1 и neto-app2.
<img width="791" height="234" alt="image" src="https://github.com/user-attachments/assets/af59b5ce-c6bf-4306-9f89-8eec5e483e24" />

### Запуск первого приложения в namespace=neto-app1 с переменными по умолчанию.
<img width="1130" height="390" alt="image" src="https://github.com/user-attachments/assets/f5e6efc3-be3c-4d97-9d4f-b7d7d5473b10" />

### Запуск второго приложения в namespace=neto-app1 c изменением версии образа и количества репдик.
<img width="1145" height="467" alt="image" src="https://github.com/user-attachments/assets/e9af1b6c-feed-40f9-a3a6-1d84cc284df3" />
<img width="1102" height="565" alt="image" src="https://github.com/user-attachments/assets/6ca8ab25-68ba-4abd-9497-90b68e58b047" />

### Запуск третьего приложения в namespace=neto-app2 c изменением версии образа и количества репдик.
<img width="1147" height="395" alt="image" src="https://github.com/user-attachments/assets/b77d91b2-d57c-42c5-8e89-b372ca9d6970" />
<img width="1124" height="541" alt="image" src="https://github.com/user-attachments/assets/36eec36b-ffe3-4da9-ae3b-32a6bc32cc41" />


