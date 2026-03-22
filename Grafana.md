# netorep
## Домашнее задание к занятию 14 «Средство визуализации Grafana»

## Обязательные задания
### Задание 1
#### В yandex cloud создан сервер для выполения ДЗ.
<img width="750" height="111" alt="image" src="https://github.com/user-attachments/assets/c32414d4-7aa0-4ac1-80b5-a0783fb87315" />  

### Скопированы данные из директории [help](./help) внутри этого домашнего задания, и запущена связка prometheus-grafana.
<img width="1297" height="86" alt="image" src="https://github.com/user-attachments/assets/f294a48a-aaac-46a6-b074-116e57309f23" />  

### Подключен поднятый prometheus, как источник данных.
<img width="711" height="42" alt="image" src="https://github.com/user-attachments/assets/068a2602-2597-41fa-aeed-3f230963272e" />
<img width="1324" height="515" alt="image" src="https://github.com/user-attachments/assets/c92577fc-3ab6-4e8c-8ac6-9bef58c218b2" />  

### Задание 2
#### Создайте Dashboard и в ней создайте Panels:
##### Утилизация CPU для nodeexporter (в процентах, 100-idle);
###### promql-запрос (100 - (avg(irate(node_cpu_seconds_total{mode="idle"}[30m])) * 100))
#### CPULA 1/5/15;
###### promql-запросы (node_load1), (node_load10), (node_load15)
#### количество свободной оперативной памяти;
###### promql-запрос ((1 - (node_memory_MemAvailable_bytes / node_memory_MemTotal_bytes)) * 100)
#### количество места на файловой системе.
###### promql-запрос (node_filesystem_avail_bytes{mountpoint="/", fstype!="tmpfs"}), (node_filesystem_size_bytes{mountpoint="/", fstype!="tmpfs"})
<img width="1233" height="811" alt="image" src="https://github.com/user-attachments/assets/65a754c1-d50c-49fe-985c-339916ff7f8f" />


