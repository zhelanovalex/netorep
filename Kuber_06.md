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
----
<img width="779" height="386" alt="image" src="https://github.com/user-attachments/assets/0a591b45-d564-42c4-9bf6-05f23ee3ced6" />

#### Создан ingess.
<img width="606" height="402" alt="image" src="https://github.com/user-attachments/assets/ec471351-cd35-4703-b177-9a7378507398" />
----
<img width="854" height="292" alt="image" src="https://github.com/user-attachments/assets/60e08196-6e24-4582-a5aa-99339e48aa86" />

### Проверить доступность локально из контейнера.
<img width="1103" height="225" alt="image" src="https://github.com/user-attachments/assets/11e36dd0-5eb7-49bb-a683-c3ceed6bd2c8" />

### Проверить доступность на уровне узлов кластера.
<img width="1095" height="212" alt="image" src="https://github.com/user-attachments/assets/e68f4710-4817-4038-be69-1069aef07812" />

### Проверить доступность извне.
<img width="1183" height="142" alt="image" src="https://github.com/user-attachments/assets/57890b46-19e3-4200-9535-7771fdb5f627" />
----
<img width="1097" height="110" alt="image" src="https://github.com/user-attachments/assets/6540762a-4044-4661-a1e5-493c1f271778" />

## Задание 2: Настройка HTTPS с Secrets
### Развернуть приложение с доступом по HTTPS, используя самоподписанный сертификат.
#### Сгенерировать SSL-сертификат
<img width="1097" height="153" alt="image" src="https://github.com/user-attachments/assets/5566d8ac-b641-455c-b89d-bfd83368f263" />

#### Закодировать ключ и сертификат для передачи в качестве секрета.
<img width="1102" height="66" alt="image" src="https://github.com/user-attachments/assets/3912f697-36ac-44f2-ba70-dfe3c3d9d410" />
----
<img width="1104" height="87" alt="image" src="https://github.com/user-attachments/assets/8aabac57-173e-4fc0-9a1b-ad41cfcc2ef8" />

#### Создать Secret.
<img width="816" height="278" alt="image" src="https://github.com/user-attachments/assets/aec836d8-3cf4-4e17-bcd1-11daafce0526" />

#### Настроить Ingress.
<img width="631" height="488" alt="image" src="https://github.com/user-attachments/assets/3fa04ab3-aa47-4414-a025-7c017f632405" />
----
<img width="779" height="87" alt="image" src="https://github.com/user-attachments/assets/7049a4e8-050c-483a-af70-afb157859863" />

#### Проверить HTTPS-доступ извне.
<img width="1193" height="153" alt="image" src="https://github.com/user-attachments/assets/7a63edbe-6ca9-4c00-b130-5387cb8731e4" />
----
<img width="1245" height="136" alt="image" src="https://github.com/user-attachments/assets/69f02f66-ab38-4f65-9309-0de006486cf8" />

## Задание 3: Настройка RBAC
### Создать пользователя с ограниченными правами (только просмотр логов и описания подов).
#### Включите RBAC в microk8s.
<img width="864" height="318" alt="image" src="https://github.com/user-attachments/assets/9770f3b3-2a4d-42c5-a8bd-0dc0c2d24ac3" />

#### Создать SSL-сертификат для пользователя
<img width="1231" height="211" alt="image" src="https://github.com/user-attachments/assets/f0ae3e76-023c-4947-bd76-98930b083867" />

#### Создать пользователя.
<img width="1181" height="40" alt="image" src="https://github.com/user-attachments/assets/28ee9a8e-6b08-401e-b167-8770e6f01089" />

#### Создать контекст пользователя.
<img width="1164" height="40" alt="image" src="https://github.com/user-attachments/assets/2102715f-53c1-4405-82de-d7f5492a57f6" />
----
<img width="667" height="440" alt="image" src="https://github.com/user-attachments/assets/66ad2a40-6ba5-4707-9d94-3141d1bd9a50" />

#### Проверить доступ для нового пользователя.
<img width="1177" height="228" alt="image" src="https://github.com/user-attachments/assets/9b89995f-0570-42e5-9650-7dcb3f165705" />
----
##### Доступа нет.

#### Создать Role (только просмотр логов и описания подов) и RoleBinding.
<img width="808" height="484" alt="image" src="https://github.com/user-attachments/assets/043f4175-b420-44dd-bd18-953e8a4708d9" />
----
<img width="842" height="166" alt="image" src="https://github.com/user-attachments/assets/2fc33b57-6106-4236-88ef-72170de9616a" />

#### Проверить доступ для нового пользователя.
<img width="1088" height="383" alt="image" src="https://github.com/user-attachments/assets/9014d3eb-ae2e-4b51-a9c0-aed4f62de6d1" />
#### Видно что доступ к pod и логам pod есть, а например к nodes нету.


