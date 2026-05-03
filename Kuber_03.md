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

