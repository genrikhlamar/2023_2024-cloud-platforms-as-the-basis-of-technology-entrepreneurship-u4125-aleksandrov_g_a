University: [ITMO University](https://itmo.ru/ru/) \
Faculty: [FTMI](https://ftmi.itmo.ru) \
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/) \
Year: 2024 \
Group: U4125 \
Author: Aleksandrov Genrikh Aleksandrovich \
Lab: Lab5 \
Date of create: 07.05.2024 \
Date of finished: 

## Лабораторная работа №5 "Интеграция Jira и Github"
### Шаг 1.
Зарегистрировались в Jira
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/238a2b78-c65b-415e-b686-48b8401907cd)

### Шаг 2.
Создал команду
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/e41a0eb2-cbd4-4cbf-922c-bbdfc73e2ab6)

Создал Team managed Scrum project
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/8e107b8c-2087-4b0a-a1d1-1f5898c2b140)
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/255ccd56-aa76-4deb-bbd0-7106e7eb5a1b)

### Шаг 3.
Фичи Backlog и Code были добавлены автоматически при создании Scrum проекта. В доске для выполнения задач создал колонку On Check.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/ce96e899-4e3a-47bb-a7a3-ea7a6d455cad)

В бэклоге и на доске создали несколько задач и запустил спринт.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/7f9486ab-32e8-49e8-8113-f5b20b0c271c)


### Шаг 4.
Привязал GitHub аккаунт и свой GitHub репозиторий через панель инструментов и провел Backfill на сегодняшнее число. 
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/0e6f57c0-595c-4d5f-a77b-581d3163da61)

![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/cce0bcce-080a-4256-95a5-d0bb56e47b56)


### Шаг 5.
**Автоматизации**
Создал все требуемые автоматизации: При создании ветки на GitHub, посвященной тикету, автоматически перемещать тикет в In Progress. При создании PR в dev ветки, посвященной тикету, автоматически перемещать тикет в On Check. При мердже ветки перемещать тикет в Done. При создании issue на GitHub добавлять тикет в Backlog (эту автоматизацию сделал с помощью встроенного ai-помощника (UPD: она не работала и я ее удалил)) 
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/11979741-aae3-4775-a264-dd1bd99b8984)
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/79194f45-1f45-49f5-85f1-2e253e349c7c)

### Шаг 6.
Дальнейшие шаги скринкастами:

### Шаг 7.
Создать тикет в бэклоге. \
https://drive.google.com/file/d/1j6oaB2jy2_TX9jecCLEfuVC3dg8iDz1l/view?usp=drive_link

### Шаг 8.
Создать спринт, переместить в него нашу задачу. Начать спринт.\
https://drive.google.com/file/d/1MymO1BulJcpJi5HCioyXCTLb_8nUJHoS/view?usp=drive_link

### Шаг 9.
Зашли через Termius в свой гитхаб-репозиторий. Создали тестовый файл для проверки, что все работает\
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/2d38e382-01dc-41ed-9932-214196ebfefb)

Создали в командной строке ветку, посвященную тикету. Проверили, что ее статус в Jira перешел в In Progress.\
https://drive.google.com/file/d/100lwjiMvK0_hO9AE1S8v4EvKEFvWVpGx/view?usp=drive_link

### Шаг 10.
Создал PR-ветку в dev. Проверил, что статус тикета в Jira перешел в On Check\
https://drive.google.com/file/d/1iunPEF0EOdpMmVAh2KjJRNYZ6waF0AaH/view?usp=drive_link

### Шаг 11.
Принял PR. Проверил, что статус тикета - Done. Все сработало!\
https://drive.google.com/file/d/11TN1dSQT7sIOAG6oUWJTS5gIkYR49flx/view?usp=drive_link
