# netorep
# Домашнее задание к занятию 3 «Использование Ansible»

## Подготовка к выполнению
### Подготовьте в Yandex Cloud три хоста: для clickhouse, для vector и для lighthouse.
<img width="868" height="151" alt="image" src="https://github.com/user-attachments/assets/965692d6-d91d-4e91-bc53-951b47f63502" />

## Основная часть
### Допишите playbook: нужно сделать ещё один play, который устанавливает и настраивает LightHouse.
#### Рабочий playbook был переработан для связи всех указанных приложений.
https://github.com/zhelanovalex/mnt-homeworks/blob/MNT-video/08-ansible-03-yandex/site.yml  
#### Были созданы отдельные шаблоны для конфигурационных файлов приложений.
<img width="635" height="165" alt="image" src="https://github.com/user-attachments/assets/bbcec5d2-f87c-4e3c-b0d7-41e837bca45a" />
#### Дополнены и созданы новые переменные.
<img width="807" height="574" alt="image" src="https://github.com/user-attachments/assets/43d0f944-4ad0-4df1-8f0e-65ded9b1373b" />
### Запустите playbook на prod.yml окружении с флагом --diff. Убедитесь, что изменения на системе произведены.
#### Запуoty playbook на prod.yml окружении с флагом --diff. 
#### Проведены исправления ошибок - в итоге все изменения на указанных серверах произведены.
<img width="1070" height="99" alt="image" src="https://github.com/user-attachments/assets/14523346-8efc-4ec7-b009-692463dc6fc9" />

### Проверка работоспособности приложений.  

#### Clickhouse. Сервис запущен. Данные от vector поступают.
<img width="1356" height="282" alt="image" src="https://github.com/user-attachments/assets/78b8d0b9-5efe-45c2-aca4-b5bdbc559031" />
<img width="1263" height="622" alt="image" src="https://github.com/user-attachments/assets/fcc8b6b1-780f-4ad4-a801-3c7b13cb727f" />

#### Vector. Сервис запущен.
<img width="1452" height="308" alt="image" src="https://github.com/user-attachments/assets/80f4ea63-4742-4512-ad0a-9e8393758574" />

#### Lighthouse + nginx. Коннект к clickhouse есть.
<img width="1342" height="605" alt="image" src="https://github.com/user-attachments/assets/54d82daf-2318-4d94-acf5-67506400c5d7" />
