University: [ITMO University](https://itmo.ru/ru/) \
Faculty: [FTMI](https://ftmi.itmo.ru) \
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/) \
Year: 2024 \
Group: U4125 \
Author: Aleksandrov Genrikh Aleksandrovich \
Lab: Lab1 \
Date of create: 05.05.2024 \
Date of finished: 07.05.2024 \

## Лабораторная работа №1 "Обзор Google Cloud и исследование основных сервисов."
### Шаг 1.
Зашел в Google Cloud, заранее запросив доступ у Ивана. Перешел во вкладку IAM и в разделе Service Accounts создал сервис-аккаунт, назвал его "galeksandrov-sa-lab1". Далее в разделе IAM назначил созданному сервис-аккаунту доступ Storage admin.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/e1bc01ed-fde4-448c-b4aa-88a0d928b4ea)

### Шаг 2.
Зашел во вкладку Computee Engine, в разделе VM Instances нажал на кнопку Create Instance. Задал название по инструкции, выбрал конфигурацию type e2-micro в режиме spot и запустил вирутальную машину. Затем с помощью кнопки edit вернулся к настройкам выбрал свой сервис-аккаунт в качестве администратора (забыл изначально)
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/34182ccb-d428-41ff-8c19-8ef2e2724d74)

### Шаг 3.
Нажал на кнопку SSH. Открылась консоль и в ней я с помощью утилиты gsutils нашел бакет lab1-bucket-itmo. Скопировал оттуда 3 файла в локальную папку на VM. 
При помощи команды ls -lah отобразил что эти файлы хранятся на моей VM.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/865356e9-1cf8-42ed-8fc0-9ede6874fd43)

![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/205eaf60-a2fd-4be8-b039-cb1036ab1243)

### Шаг 4.
Зашел во вкладку IAM, Поменял права доступа своего сервис-аккаунта со Storage Admin на Compute Viewer. 
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/865e07a9-057c-4e09-b625-4d172b2e4335) \
Нажал на кнопку SSH в разделе VM Instances, но зайти в консоль и что-либо сделать уже не получилось.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/ef96fe93-f606-4600-8777-316d2c10bd85) 

### Шаг 5.
Удалил за собой созданный ранее сервис.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/81f79591-7444-4ce7-bae1-18e80fa89880)

**Вывод**: Использование Google Cloud позволяет эффективно управлять доступом к ресурсам, предоставляя возможность дать каждому участнику команды необходимый уровень прав в зависимости от его задач и обязанностей. Роль Storage Admin наделяет пользователя полным контролем над сервисами хранилища, а роль Compute Viewer предоставляет ограниченный доступ к вычислительным ресурсам. Пользователь с ролью Compute Viewer может просматривать информацию о машинах, но не может вносить изменения в конфигурацию или данные, что помогает предотвратить утечки информации.
