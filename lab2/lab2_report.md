University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FTMI](https://ftmi.itmo.ru)
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/)
Year: 2024
Group: U4125
Author: Velitchenko Olga Evgenievna
Lab: Lab1
Date of create: 26.04.2024
Date of finished: 30.04.2024

## Отчет по лабораторной работе №2

Для работы был создан Cloud Run из представленного дефолтного сервиса Hello.
<img width="1428" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/2bd358d2-dfdd-4208-9174-188a40262617">


<img width="1427" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/7ae753bf-4279-4439-b168-258a47ace2dc">

Для начала был создан сервис с ограниченным доступом, поэтому перейти по ссылке не получалось, однако позже при смене настроек приложение заработало.
<img width="1420" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/24fe9227-884f-4174-8cf1-1bf1f255e337">


На вкладке Metrics есть несколько значений, который показывают работу сервиса. 
Request count показали кол-во запросов, их было 3. Request latencies показывает распределенное время запросов.
<img width="1429" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/d572ba53-63f9-4585-831a-5da449b28d7c">
<img width="1424" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/9bdb81ef-716f-45ed-984d-da91fd4e15c2">
<img width="1425" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/cba8b354-1874-491a-8c98-9fd256766983">


Во вкладке Logs можно посмотреть отправленные запросы и действия
<img width="1407" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/fd7ce14c-ae89-460e-a1da-20b3cfc81140">



Была создана дополнительная версия с портом 8090

<img width="1421" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/b89da68f-864c-4546-a66d-8891433cc020">

Здесь было попробовано перераспределить трафик, сначала 100% новой версии, потом 100% старой версии, а далее распределение 99 и 1, и 95 и 5. При каждом изменении на графиках метрик отображалась информация и дополнительные линии.
<img width="1432" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/51db1cce-8004-46e8-9779-6a648c46d3c4">

Вывод: Cloud Run – это управляемая вычислительная платформа, которая позволяет запускать контейнеры и разворачивать программный код. Так же при каждом изменении создаются revisions, которые можно далее отследить на графиках метрик.




