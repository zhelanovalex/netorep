# netorep
# Домашнее задание к занятию 1 «Введение в Ansible»
https://github.com/zhelanovalex/ter-homeworks/tree/main/02/src

## Подготовка к выполнению
### 1. Установите Ansible версии 2.10 или выше.
<img width="903" height="168" alt="image" src="https://github.com/user-attachments/assets/a8212e27-c8e6-43e2-9d8b-7c286a0bf438" />

### 2. Создайте свой публичный репозиторий на GitHub с произвольным именем.  
https://github.com/zhelanovalex/mnt-homeworks

## Основная часть.

### 1. Попробуйте запустить playbook на окружении из test.yml, зафиксируйте значение, которое имеет факт some_fact для указанного хоста при выполнении playbook.
<img width="989" height="322" alt="image" src="https://github.com/user-attachments/assets/373dd6a1-f497-4cce-953a-e3b248374779" />

### 2. Найдите файл с переменными (group_vars), в котором задаётся найденное в первом пункте значение, и поменяйте его на all default fact.
<img width="787" height="54" alt="image" src="https://github.com/user-attachments/assets/5ab376cf-45fd-4bef-8bcb-f7b1b4458cdf" />
<img width="1012" height="317" alt="image" src="https://github.com/user-attachments/assets/139dd08a-5582-4ff4-8ac8-5d249cccbd21" />

### 3. Воспользуйтесь подготовленным (используется docker) или создайте собственное окружение для проведения дальнейших испытаний.
<img width="852" height="76" alt="image" src="https://github.com/user-attachments/assets/2fdac454-766b-48cd-8420-202116ca705e" />

### 4. Проведите запуск playbook на окружении из prod.yml. Зафиксируйте полученные значения some_fact для каждого из managed host.
<img width="974" height="382" alt="image" src="https://github.com/user-attachments/assets/dfe71ed3-77d4-4cca-85e0-21468062bb8e" />

### 5. Добавьте факты в group_vars каждой из групп хостов так, чтобы для some_fact получились значения: для deb — deb default fact, для el — el default fact.
<img width="849" height="97" alt="image" src="https://github.com/user-attachments/assets/f66aaf68-b119-48d4-a55c-7bcb07188f76" />

### 6. Повторите запуск playbook на окружении prod.yml. Убедитесь, что выдаются корректные значения для всех хостов.
<img width="983" height="450" alt="image" src="https://github.com/user-attachments/assets/8ff9ada9-6139-42c0-baa3-255606701c89" />

### 7. При помощи ansible-vault зашифруйте факты в group_vars/deb и group_vars/el с паролем netology.
<img width="948" height="162" alt="image" src="https://github.com/user-attachments/assets/e07628d9-74aa-42ef-ac67-3e33b7287022" />

### 8. Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь в работоспособности.
<img width="1123" height="461" alt="image" src="https://github.com/user-attachments/assets/a783baff-eaeb-49fb-8e32-b19a3ac5efe3" />

### 9. Посмотрите при помощи ansible-doc список плагинов для подключения. Выберите подходящий для работы на control node.
<img width="858" height="532" alt="image" src="https://github.com/user-attachments/assets/e2e72357-e259-41d2-b309-5fe8b3f76004" />

### 10. В prod.yml добавьте новую группу хостов с именем local, в ней разместите localhost с необходимым типом подключения.
<img width="797" height="230" alt="image" src="https://github.com/user-attachments/assets/796b8996-7e98-4ca9-8ea0-51c081aafe58" />

### 11. Запустите playbook на окружении prod.yml. При запуске ansible должен запросить у вас пароль. Убедитесь, что факты some_fact для каждого из хостов определены из верных group_vars.
<img width="1196" height="598" alt="image" src="https://github.com/user-attachments/assets/2e431c8e-bb0d-4bae-abca-65b642be878a" />
