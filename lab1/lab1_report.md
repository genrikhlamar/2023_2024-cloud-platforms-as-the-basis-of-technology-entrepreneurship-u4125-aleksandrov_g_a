University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/)
Year: 2024
Group: U4125
Author: Aleksandrov Genrikh Aleksandrovich
Lab: Lab1
Date of create: 07.05.2024
Date of finished: 


##Шаг 1.
Зашел в Google Cloud, во вкладку IAM, в раздел Service Accounts. Через кнопку Create Service Account открыл интерфейс создания пользовательского доступа к серверам. Назвал доступ "galeksandrov-sa-lab1" и назначил доступ Service admin.

##Шаг 2.
Зашел во вкладку Computee Engine, в раздел VM Instances. Нажал на кнопку Create Instance. Задал название для виртуалки, выбрал конфигурацию type e2-micro в режиме spot. Выбрал администратора (того самого из шага 1). image

##Шаг 3.
Нажал на кнопку SSH, в открывшейся консоли с помощью утилиты gsutils нашел бакет lab1-bucket-itmo и скопировал 3 файла в локальную папку на VM. Используя команду ls -lah отобразил что эти файлы хранятся на моей VM. image

##Шаг 4.
Зашел во вкладку IAM, Поменял права доступа service account с Storage Admin на Compute Viewer. Нажал на кнопку SSH, в открывшейся консоли с помощью утилиты gsutils нашел бакет lab1-bucket-itmo и попробовал скопировать 3 файла в локальную папку на VM. Но не получилось :) image Вывод: Роль Storage Admin в Google Cloud дает пользователям полный доступ к управлению хранилищем данных, включая создание, удаление и настройку ресурсов, управление доступом, мониторинг активности и безопасности, а вот compute viewer дает ограниченный доступ и позволяет сохранить машину от утечки информации.
