# netorep
# Домашнее задание к занятию «Запуск приложений в K8S»

## Чеклист готовности к домашнему заданию
### Установленное k8s-решение MicroK8S на yandex VMs.
<img width="799" height="163" alt="image" src="https://github.com/user-attachments/assets/d9472410-25e5-4039-abbc-411e3f58c905" />

### Второй узел добавлен в кластер.
<img width="555" height="69" alt="image" src="https://github.com/user-attachments/assets/e1c9a382-7c0a-444e-b3fb-0d3e564495dc" />

### Установлен на локальном компьютере kubectl.
<img width="631" height="102" alt="image" src="https://github.com/user-attachments/assets/4e74f6fb-3786-4f0e-850a-01463189328b" />

## Задание 1. Создать Deployment и обеспечить доступ к репликам приложения из другого Pod
### Создать Deployment приложения, состоящего из двух контейнеров — nginx и multitool. Решить возникшую ошибку.
#### Ошибка была выявлена до создания Deployment из описания образов приложений - они используют одни и те же порты и в таком виде применять их в одном pod нельзя. Поэтому в Deployment уже исправлена данная ошибка.
<img width="713" height="562" alt="image" src="https://github.com/user-attachments/assets/b1a78837-b78c-4bd3-8a38-9f1f2fc6d25a" />
----
<img width="666" height="110" alt="image" src="https://github.com/user-attachments/assets/3906402d-d799-425e-9f0a-933a4b44bed8" />
----
<img width="679" height="55" alt="image" src="https://github.com/user-attachments/assets/b83f7be5-3e25-472e-bb0f-9cbae374bd89" />

### После запуска увеличить количество реплик работающего приложения до 2.
<img width="803" height="34" alt="image" src="https://github.com/user-attachments/assets/4cb7f0ce-3151-4510-968c-6971a44c634d" />

### Продемонстрировать количество подов до и после масштабирования.
<img width="752" height="53" alt="image" src="https://github.com/user-attachments/assets/a6843cbf-a8a6-4ce8-9235-017e5a2bf492" />
----
<img width="726" height="73" alt="image" src="https://github.com/user-attachments/assets/6175e0d6-938c-4311-a457-b77f59c58fe5" />
----
<img width="795" height="120" alt="image" src="https://github.com/user-attachments/assets/b7fc8e7e-a719-46e9-a1b9-c42c98ae9131" />

### Создать Service, который обеспечит доступ до реплик приложений из п.1.
<img width="751" height="310" alt="image" src="https://github.com/user-attachments/assets/904a64d4-cf97-4119-b5c2-1392ba0ccf9d" />
----
<img width="746" height="75" alt="image" src="https://github.com/user-attachments/assets/ec754204-f04b-49e7-bd06-80e29e758012" />
----
<img width="1216" height="168" alt="image" src="https://github.com/user-attachments/assets/b2350139-e4c2-4b3f-8940-50039102bb55" />
----
<img width="1183" height="71" alt="image" src="https://github.com/user-attachments/assets/47aabccb-6c29-4143-8c6e-51568e8b00bd" />
----
<img width="544" height="175" alt="image" src="https://github.com/user-attachments/assets/7e63dec8-f388-4b99-882c-d57e0e7b5618" />
----
<img width="600" height="172" alt="image" src="https://github.com/user-attachments/assets/d618f2c7-337a-4fc3-825b-c5e7eabe66be" />

### Создать отдельный Pod с приложением multitool и убедиться с помощью curl, что из пода есть доступ до приложений из п.1.
<img width="763" height="184" alt="image" src="https://github.com/user-attachments/assets/f1b5b968-70c2-4702-b247-696b335b0fbc" />
----
<img width="687" height="88" alt="image" src="https://github.com/user-attachments/assets/86b75d72-6137-445a-8b8e-610c3f6ade21" />
----
<img width="1262" height="72" alt="image" src="https://github.com/user-attachments/assets/05fb10f8-075c-4e09-b85b-e5e68fd76a9d" />


