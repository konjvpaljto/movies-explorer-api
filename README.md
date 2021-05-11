### [Яндекс.Практикум](https://praktikum.yandex.ru), веб-факультет, поток 19
#### Дипломная работа. Фуллстек-веб-приложение

# "Movies-explorer, API"
## автор: Аркадий Флитман
------

В этом репозитории - код бэкенда (API) для дипломной работы. 

Фронт проекта будет опубликован [вот здесь](https://kino.flitman.ru).

Через postman можно обратиться к развёрнутому на сервере API по адресу (https://api2.kino.flitman.ru).

API поддерживает следующие запросы:
##### Авторизация, регистрация, данные пользователя
* `POST /signup` - роут для регистрации, обязательно передать email, password, name. В ответе будут данные пользователя. 
* `POST /signin` - роут для авторизации, обязательно передать email, password. В ответе будет кука с JWT-токеном и данные пользователя. 
* `POST /signout` - роут для выхода из системы. Ответ очищает куку из браузера. 
* `GET /users/me` - роут для получения данных о пользователе. 
* `PATCH /users/me` - роут для изменения данных о пользователе, обязательно передать email, name. 
##### Кинофильмы
* `GET /movies` - возвращает массив со всеми фильмами, котоыре пользователь добавил в коллекцию
* `POST /movies` - добавляет фильм в коллекцию. Обязательные поля: country, director, duration, year, description, image, trailer, nameRU, nameEN, thumbnail, movieId. Возвращает массив с коллекцией фильмов пользователя. 
* `DELETE /movies/movieId` - удаляет из коллекции фильм по ID. 

### Использованы следующие технологии: 
Typescript, Node.JS, Express.js, MongoDB

## Запуск проекта

* `npm run build` — собирает JS код из TS-исходников
* `npm run dev` — запускает сборку кода с hot-reload для режима разработки, с выводом ошибки
* `npm start` — запускает сервер. Предварительно необходимо выполнить `npm run build`
* `npm run lint` — проверяет код линтером ESLint

