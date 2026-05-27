# netorep
# Домашнее задание к занятию «Установка Kubernetes»

## Чеклист готовности к домашнему заданию
### С помощью packer создан образ Ubuntu22, со всеми реквизитами для установки Kubernetes
<img width="1649" height="808" alt="image" src="https://github.com/user-attachments/assets/64cca6a8-f2b7-40fd-8f6e-2d3f4bbd523a" />
<img width="892" height="127" alt="image" src="https://github.com/user-attachments/assets/ee54bbed-272b-4433-9f73-bfc9d7dc7961" />

### На основании созданного образа, с помощью terraform создано 5 VM.
<img width="634" height="198" alt="image" src="https://github.com/user-attachments/assets/06dfc6b6-55de-4b33-b289-4471bd976b3d" /> 
<img width="860" height="181" alt="image" src="https://github.com/user-attachments/assets/b02500d6-29a5-4a7c-9fe0-8c9f406599d3" />
<img width="961" height="284" alt="image" src="https://github.com/user-attachments/assets/43e6b52e-e538-42fc-bcd1-19994c76d800" />

### Установлен на локальном компьютере kubectl.
<img width="586" height="57" alt="image" src="https://github.com/user-attachments/assets/3e661fc6-4190-4fb8-a740-1473ddc8e446" />

### Сылка на манифесты.
https://github.com/zhelanovalex/kuber-homeworks/tree/main/3.2/src

## Задание 1. Установить кластер k8s с 1 master node
### Так как все пререквизиты устанволены на всех узлах, выполняем инициализацию узла master кластера.
<img width="1641" height="628" alt="image" src="https://github.com/user-attachments/assets/5aea9437-efe8-441e-8be6-13b5ba01baab" />
<img width="1501" height="773" alt="image" src="https://github.com/user-attachments/assets/2fc78d80-8581-448b-a4a5-02ff2d833501" />

### Настраиваем kubectl на master узле и локальном компьютере.
<img width="730" height="55" alt="image" src="https://github.com/user-attachments/assets/58634802-5e54-437a-aada-e03635836d96" />
<img width="610" height="53" alt="image" src="https://github.com/user-attachments/assets/3cd81acf-0d7b-4f9a-9408-66ef33d8e54a" />

### Подключам к кластеру все worker узлы.
<img width="1503" height="317" alt="image" src="https://github.com/user-attachments/assets/442e1036-883c-4ca6-aecf-8f88f4b926af" />
<img width="560" height="123" alt="image" src="https://github.com/user-attachments/assets/86601941-d6b8-4a01-8419-a98eed43d3f6" />



