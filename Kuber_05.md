# netorep
# Домашнее задание к занятию «Хранение в K8s»

## Чеклист готовности к домашнему заданию
### Установленное k8s-решение MicroK8S на yandex VMs.
<img width="794" height="182" alt="image" src="https://github.com/user-attachments/assets/7fb36dc6-2679-4003-9fe0-b30ba4001b81" />

### Узлы собраны в кластер.
<img width="620" height="88" alt="image" src="https://github.com/user-attachments/assets/8ea2b89d-cc65-4cd3-9f32-d99a8bcb2b5b" />

### Установлен на локальном компьютере kubectl.
<img width="698" height="134" alt="image" src="https://github.com/user-attachments/assets/15d4ed08-c1aa-492a-bb35-1f276014cb1a" />

### Сылка на манифесты.
https://github.com/zhelanovalex/kuber-homeworks/tree/main/2.1/src

## Задание 1. Volume: обмен данными между контейнерами в поде.
### Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
#### Создать Deployment приложения, состоящего из контейнеров busybox и multitool.
#### Настроить busybox на запись данных каждые 5 секунд в некий файл в общей директории.
#### Обеспечить возможность чтения файла контейнером multitool.
<img width="778" height="532" alt="image" src="https://github.com/user-attachments/assets/25017cb2-7346-4724-bb70-8b6520425551" />
----
<img width="1011" height="215" alt="image" src="https://github.com/user-attachments/assets/2e0e5658-0745-429e-9d4b-688b3e8e7b26" />
----
<img width="888" height="120" alt="image" src="https://github.com/user-attachments/assets/7df34c42-f0c7-4f34-875d-efaeed51a28e" />
----
<img width="894" height="245" alt="image" src="https://github.com/user-attachments/assets/f4ac1eea-6b67-43a2-a97c-2a330f92fa9a" />
----
<img width="966" height="294" alt="image" src="https://github.com/user-attachments/assets/d5dea62b-cf56-4772-a203-e894c844bac8" />
----
<img width="1016" height="177" alt="image" src="https://github.com/user-attachments/assets/3187bb91-4070-46a2-be4a-38c227bb863a" />

