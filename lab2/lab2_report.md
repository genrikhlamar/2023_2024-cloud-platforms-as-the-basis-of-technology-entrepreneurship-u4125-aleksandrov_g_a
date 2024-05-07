University: [ITMO University](https://itmo.ru/ru/) \
Faculty: [FICT](https://fict.itmo.ru) \
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/) \
Year: 2024 \
Group: U4125 \
Author: Aleksandrov Genrikh Aleksandrovich \
Lab: Lab1 \
Date of create: 07.05.2024 \
Date of finished: 

## Лабораторная работа №2 "Исследование Cloud Run"
### Шаг 1.
Во вкладке Cloud Run нажал на кнопку Create Service и создал свой. В Container image URL выбрал дефолтный сервис Hello с минимальным количеством ресурсов.  \
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/46f12cd7-313e-46fd-85c8-deba4028a654) \
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/dfa2232c-a9fa-4871-bdd2-1687d2d4e408) 

### Шаг 2.
Перешел по представленной ссылке, протестировал сервис.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/439a089f-8ab3-409d-815a-aed8f01ba5a9) 

### Шаг 3.
Зашел в раздел логи, увидел запросы к серверу и процесс создания сайта.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/de66fc69-1a2f-408e-880a-a69f30472be9)

Зашел в раздел с метриками, увидел графики. Но они ничего интересного не показывали (было включено отображение за 1 день), так как сервис был создан только что. Но в перспективе по ним можно отслеживать количество запросов, задержку в ответе на запрос и так далее.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/78db1bfd-e3f9-42a0-8761-959f904e30a6)

### Шаг 4.
Изменил свой Cloud Run, поменяв порт на 8090, посмотрел что произойдет. Попробовал попереключать трафик между версиями, сравнил результаты работы. \
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/2c3218ff-dee4-4551-9fc0-6e08511d1094)
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/49420ae0-0181-47b6-ad04-acf4d691cc37) 

Метрики с портом 8090 (15 минут) 
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/8f50df13-ec3e-46b8-95f9-6a77c642ba68) 

Метрики с портом 8080 (15 минут) 
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/06cf691b-1ad7-468a-90bc-493beb9953a2) 

**Вывод:** Проведенная лабораторная работа продемонстрировала возможности Cloud Run как платформы для быстрого развертывания, эффективного мониторинга и анализа веб-приложений. 
