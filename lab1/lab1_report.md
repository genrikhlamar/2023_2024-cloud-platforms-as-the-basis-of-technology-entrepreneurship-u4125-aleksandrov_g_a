University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/)
Year: 2024
Group: U4125
Author: Aleksandrov Genrikh Aleksandrovich
Lab: Lab1
Date of create: 07.05.2024
Date of finished: 


### Шаг 1.
Зашел в Google Cloud, во вкладку IAM. В разделе Service Accounts создал сервис-аккаунт и назвал его "galeksandrov-sa-lab1". Далее в разделе IAM назначил созданному сервис-аккаунту доступ Service admin.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/e1bc01ed-fde4-448c-b4aa-88a0d928b4ea)

### Шаг 2.
Зашел во вкладку Computee Engine, в разделе VM Instances нажал на кнопку Create Instance. Задал название по инструкции, выбрал конфигурацию type e2-micro в режиме spot. Выбрал свой сервис-аккаунт в качестве администратора
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/34182ccb-d428-41ff-8c19-8ef2e2724d74)


### Шаг 3.
Нажал на кнопку SSH, в открывшейся консоли с помощью утилиты gsutils нашел бакет lab1-bucket-itmo и скопировал 3 файла в локальную папку на VM. 
Используя команду ls -lah отобразил что эти файлы хранятся на моей VM.
![image](https://github.com/imkonyahin/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-konyahin_i_m/assets/167180041/147ceb56-f6ba-4fe2-9629-834b01d8f99e)

### Шаг 4.
Зашел во вкладку IAM, Поменял права доступа service account с Storage Admin на Compute Viewer. 
Нажал на кнопку SSH, в открывшейся консоли с помощью утилиты gsutils нашел бакет lab1-bucket-itmo и попробовал скопировать 3 файла в локальную папку на VM. Но не получилось :)
![image](https://github.com/imkonyahin/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-konyahin_i_m/assets/167180041/a1f2f493-ee52-469e-8cd0-8f481b06209b)
Вывод: Роль Storage Admin в Google Cloud дает пользователям полный доступ к управлению хранилищем данных, включая создание, удаление и настройку ресурсов, управление доступом, мониторинг активности и безопасности, а вот compute viewer дает ограниченный доступ и позволяет сохранить машину от утечки информации.
