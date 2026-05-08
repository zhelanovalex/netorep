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
### Создать Deployment приложения, состоящего из двух контейнеров, обменивающихся данными.
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

## Задание 2. PV, PVC.
### Создать Deployment приложения, использующего локальный PV, созданный вручную.
#### Создать Deployment приложения, состоящего из контейнеров busybox и multitool, использующего созданный ранее PVC.
#### Создать PV и PVC для подключения папки на локальной ноде, которая будет использована в поде.
<img width="959" height="1004" alt="image" src="https://github.com/user-attachments/assets/c0fef47e-87ac-4dd8-8b3c-d51d731046fa" />
----
<img width="1121" height="103" alt="image" src="https://github.com/user-attachments/assets/ced0f31b-f975-442b-8e96-8d9d06b154c4" />

#### Продемонстрировать, что контейнер multitool может читать данные из файла в смонтированной директории, в который busybox записывает данные каждые 5 секунд.
<img width="936" height="250" alt="image" src="https://github.com/user-attachments/assets/05870a40-13f4-43fd-897e-dfb00bf174a2" />
----
<img width="886" height="242" alt="image" src="https://github.com/user-attachments/assets/ec84c5bb-9f74-4c67-87b6-d74f2ce3bf9d" />
----
<img width="917" height="131" alt="image" src="https://github.com/user-attachments/assets/1af39b09-8787-47c0-bad4-7a994f6f9d72" />
----
<img width="674" height="162" alt="image" src="https://github.com/user-attachments/assets/7d549cc9-a690-4e65-a42a-e356b367ce67" />
----
<img width="677" height="151" alt="image" src="https://github.com/user-attachments/assets/16a3a07c-52b0-40ab-8048-24a1be7c9243" />

Удалить Deployment и PVC. Продемонстрировать, что после этого произошло с PV. Пояснить, почему. (Используйте команду kubectl describe pv).
Продемонстрировать, что файл сохранился на локальном диске ноды. Удалить PV. Продемонстрировать, что произошло с файлом после удаления PV. Пояснить, почему.
