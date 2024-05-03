University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FTMI](https://ftmi.itmo.ru)
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/)
Year: 2024
Group: U4125
Author: Velitchenko Olga Evgenievna
Lab: Lab1
Date of create: 3.05.2024
Date of finished: 

## Отчет по лабораторной работе №4

В данной работе рассмотрена модель создания бота, который отправляет английские слова для изучения пользователю.

Инфраструктура
<img width="734" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/72287914-d8bf-451a-90be-a3fc61182752">

1) Начальное состояние \
100 тыс. запросов \

Сервер (Google Cloud Functions) для обработки запросов от пользователей: 0$/мес. (первые 2 млн вызовов) \
Google Cloud SQL для базы-данных слов (новых и изученных) с привязанными данными о пользователях: в начале можно использовать настройки db-f1-micro с 1 vCPU, 0.6 GB — ~$8/мес. \
<img width="1174" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/21593375-97b6-4af8-a2d1-24921fa6b490">

Мониторинг и логирование (Google Cloud Monitoring и Google Cloud Logging): 0$/мес., если менее 2 млн в месяц \
Хранение данных: Standard Persistent Disk — $0.040/GB/мес., 10GB — $0.40/мес. \

Итого: ~8-9$/мес.


2) Тестирование партнерами \
5 млн запросов \

   
Сервер (Google Cloud Functions) для обработки запросов от пользователей: 0.4$ за каждый дополнительный миллион запросов = 1.2$/мес.
Google Cloud SQL для базы-данных слов (новых и изученных) с привязанными данными о пользователях: db-g1-small с 1 vCPU, 1.7 GB ~$26/мес.
Мониторинг и логирование (Google Cloud Monitoring и Google Cloud Logging): 5-7$/мес. (приблизительное значение, тк непонятны объемы данных) \
Хранение данных: Standard Persistent Disk — 20GB — $0.8/мес. \

Итого: 33-35$/мес.

2) Продовое решение \
20-40 млн запросов \

   
Сервер (Google Cloud Functions) для обработки запросов от пользователей: 0.4$ за каждый дополнительный миллион запросов = 7.2$-15.2/мес.
Google Cloud SQL для базы-данных слов (новых и изученных) с привязанными данными о пользователях: db-n1-standard-1 с 1 vCPU, 3.75 GB ~$31/мес.
Мониторинг и логирование (Google Cloud Monitoring и Google Cloud Logging): 20-30$/мес. (приблизительное значение, тк непонятны объемы данных) \
Хранение данных: Standard Persistent Disk — 60GB — $2.4/мес. \

Итого: 61-79$/мес.

Вывод: на начальных этапах, когда запросов не так много, возможно пользоваться бесплатными тарифами сервисов, однако в дальнейшем для расширения необходимо развивать ограничения по объемам данных как в SQL (тк расширяется база пользователей и слов), так и в логировании и мониторинге с ростом новых запросов и пользователей. Можно было бы на начальных этапах использовать Firestore, однако из-за специфики данных (табличное хранение слов, связанная структура таблиц пользователей и статусов слов) лучше сразу начинать с SQL.
