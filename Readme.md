# Разработка микросервисных приложений на Golang

## Описание
Язык программирования Go (Golang) применяется для создания высокопроизводительных и надежных систем. Его используют для написания облачных сервисов, серверных приложений, для автоматизации процессов в больших масштабах, в работе с ИИ и большими данными.
Go используют DevOps-инженеры, backend-разработчики, специалисты по функциональной верификации цифровых устройств.

На курсе участники создадут микросервисное приложение. Научатся создавать и тестировать конкурентные приложения на Go, работать с популярными библиотеками и внешним API, развертывать свои решения в контейнерах.

[Подробнее](https://careers.yadro.com/practical-courses/golang/)

---
Данный репозиторий является ознакомительным и содержит задания, выполненные мной в течение курса. 

TODO добавить навигацию и краткое описание каждого из заданий

# Демонстрация финальной работы
## Поисковик для комиксов для сайта xkcd

```mermaid
flowchart LR
user([User])
web[Web]
api[API]
search[Search]
update[Update]
words[Words]
ext[(xkcd.com)]
db[(DB)]

    user --> web
    user --> api
    web --> api
    api --> search
    api --> update
    search --> words
    update --> words
    update --> ext
    update --> db
    search --> db


    linkStyle 0,1 stroke:#FFD700,stroke-width:4px
    linkStyle 2,3,4,5,6 stroke:#32CD32,stroke-width:4px
    linkStyle 7 stroke:#FFD700,stroke-width:4px
    linkStyle 8,9 stroke:#FF69B4,stroke-width:4px
```

```mermaid
graph TD
    User --> Web
    User --> API
    Web --> API
    API --> Search
    API --> Update
    Search --> Words
    Update --> Words
    Update --> DB
    Search --> DB
    Update --> xkcd.com
```

### Что было сделано?
* Добавлен frontend
  * Выполнен полностью на Go template с минимальным использованием javascript
  * Стили с использованием scss
* Заменен Postgres на Couchbase
  * Обновлен микросервис Update и Search

## Видео
[Демонстрация работы](https://youtu.be/q6A6eaBLETs)
