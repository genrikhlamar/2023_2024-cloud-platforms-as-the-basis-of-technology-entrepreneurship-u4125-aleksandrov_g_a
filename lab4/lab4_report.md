University: [ITMO University](https://itmo.ru/ru/) \
Faculty: [FTMI](https://ftmi.itmo.ru) \
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/) \
Year: 2024 \
Group: U4125 \
Author: Aleksandrov Genrikh Aleksandrovich \
Lab: Lab4 \
Date of create: 07.05.2024 \
Date of finished: 07.05.2024

## Лабораторная работа №4 "Разработка инфраструктуры MVP AI приложения."
### Идея
**Описание:** Телеграм-бот/приложение, который парсит объявления по продаже бизнеса с онлайн-платформы Авито и раз в несколько часов присылает пользователю наиболее выгодное предложение.
### Инфраструктура
**Схема:** 
![SXEMA](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/62842feb-ac23-43b4-b7fb-9844d5cdbf40)


**Парсер:** Python-скрипт с использованием модуля Selenium для извлечения данных с Авито.\
**База данных:** (Google Cloud Firesore): NoSQL база данных о предложениях (цена, дата, регион и т.д).\
**Бэкенд (Google Cloud Functions)**: Обработка данных, расчёт выгодности, отправка уведомлений.\
**Планировщик (Cloud Scheduler)**: Запуск парсера по расписанию (например, раз в несколько часов).\
**Уведомления (Firebase Cloud Messaging)**: Отправка push-уведомлений о выгодных предложениях.\
**Интерфейс (Telegram/Google Cloud Run)**: Веб-интерфейс для настройки поиска и просмотра истории.

### План (ресурсы)
Три этапа развития:
#### Начальное состояние:
Пользователи: Мало (до 100).\
Парсинг: Редко (раз в несколько часов).\
Данные: Малый объем.\
Интерфейс: Бот в Telegram\
Решение:\
Google Cloud Functions (1 ГБ хранилища и ограниченное количество операций): для парсера и бэкенда.\
Google Cloud Firestore: для хранения данных.\
Google Cloud Scheduler: для автоматического запуска парсера.\
Firebase Cloud Messaging (до 10 000 уведомлений в месяц): для отправки уведомлений.

В каждом из упомянутых сервисов есть бесплатный уровень. Новые клиенты получают 300 долларов США в виде бесплатных кредитов, которые можно потратить в данных сервисах и много других бесплатных функций. На первое время этого должно хватить.
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/2e18157b-019b-4e43-bd3b-fceb120ad143)

#### Тестирование партнерами:
Пользователи: До тысячи пользователей.\
Парсинг: Раз в час.\
Данные: Средний объем.\
Интерфейс: Бот в ТГ/Простой на Cloud Run.\
Решение:\
Google Cloud Functions с автомасштабированием.\
Google Cloud Firestore с оптимизацией.\
Google Cloud Scheduler \
Firebase Cloud Messaging \
Cloud Run для веб-интерфейса.

#### Продовое решение:
Пользователи: Больше тысячи пользователей.\
Парсинг: Часто (каждые несколько минут).\
Данные: Большой объем.\
Интерфейс: Полнофункциональный на Cloud Run/App Engine.\
Решение:\
Google Cloud Functions с агрессивным автомасштабированием.\
Google Cloud Firestore с кластеризацией и кэшированием.\
Google Cloud Scheduler \
FCM с сегментацией аудитории.\
Google Cloud Run/App Engine для масштабируемого интерфейса.

### Экономическая модель
Расходы зависят от:\
Количество пользователей: Больше пользователей - больше запросов к базе данных и уведомлений.\
Частота парсинга: Чаще - больше затраты на Cloud Functions и Scheduler.\
Объем данных: Больше данных - больше затраты на хранение в Cloud Firestore.\
Интерфейс: Cloud Run/App Engine увеличивают расходы.

**Оценка расходов**:
1) **Начальное:** Близки к нулю. Если пользоваться сторонним сервисом для парсинга данных с авито, то придется заплатить от $5 до $30 
2) **Тестирование:** Cloud Functions: ~$10 в месяц (в зависимости от количества вызовов и времени выполнения). Cloud Firestore: ~$1-5 в месяц (за хранение и операции). Cloud Scheduler: ~$0.10 в месяц. FCM: ~$1-10 в месяц. Cloud Run: ~$10 в месяц (в зависимости от нагрузки и потребляемых ресурсов). Итого: ~$22 в месяц\
3)**Продовое:** Cloud Functions: ~$100 в месяц. Cloud Firestore: ~$10-50+ в месяц (за хранение, операции и кластеризацию). Cloud Scheduler: ~$1 в месяц. FCM: ~$10-100+ в месяц. Cloud Run/App Engine: ~$100+ в месяц. Итого: ~$221+ в месяц

   ![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/632e3aa5-3b21-468f-ac97-69d6d5e11eb5)
![image](https://github.com/genrikhlamar/2023_2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-u4125-aleksandrov_g_a/assets/164926677/74adbec8-2dfa-4317-bbac-dc0417939c22)
https://firebase.google.com/pricing
   
**Обоснование выбора:**\
Cloud Functions: Подходит для краткосрочных задач (парсинг, обработка).\
Cloud Firestore: Гибкая и масштабируемая NoSQL база данных.\
Cloud Scheduler: Планирование задач.\
FCM: Эффективная отправка push-уведомлений.\
Cloud Run/App Engine: Масштабируемые платформы для веб-приложений.



