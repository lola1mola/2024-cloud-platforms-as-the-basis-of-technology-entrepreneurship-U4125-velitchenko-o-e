University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FTMI](https://ftmi.itmo.ru)
Course: [Cloud platforms as the basis of technology entrepreneurship](https://itmo-ict-faculty.github.io/cloud-platforms-as-the-basis-of-technology-entrepreneurship/)
Year: 2024
Group: U4125
Author: Velitchenko Olga Evgenievna
Lab: Lab1
Date of create: 16.04.2024
Date of finished: 17.04.2024

## Отчет по лабораторной работе №1

Для начала был создан Service Account c доступом Storage Admin. Данная роль предоставляет полный контроль над объектами в хранилище.

<img width="861" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/391907e3-2857-4f66-98ad-3630a2e05a03">


Далее была запищена виртуальная машина с Machine type e2-micro в режиме spot. Service Account был выбран ранее созданный.

<img width="891" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/8f4964db-2f08-4961-888f-b99dfd1f2498">


С помощью команды gsutil удалось посмотреть и скопировать файлы из другого бакета в локальную папку ВМ.

<img width="876" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/456b0c4a-c56a-4731-b64b-1c5b2d4ae615">


После машина была остановлена, а роль Service Account изменена на Compute Viewer.

<img width="836" alt="image" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/45e29afa-ef46-4225-83b6-c6ffd8df50ff">


При попытке снова скопировать файлы ВМ выдала ошибку, связанную с органичением доступа. У роли Compute Viewer есть доступ только для чтения для получения и перечисления ресурсов Compute Engine без возможности чтения хранящихся на них данных.

<img width="882" alt="Pasted Graphic" src="https://github.com/lola1mola/2024-cloud-platforms-as-the-basis-of-technology-entrepreneurship-U4125-velitchenko-o-e/assets/149485440/3231382c-0593-425d-8f4b-afc8e0df47bc">


Таким образом, в Cloud Storage есть разные варианты ролей для ограничения доступа к бакетам или отдельным сервисам в облаке. 



