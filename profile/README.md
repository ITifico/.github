## [ITifico Blog <img src="https://github.com/ITifico/.github/assets/65526165/149ff281-5f7a-4d97-a25e-fec71cd620d8" alt="ITifico Blog" style="width:80px; height:40px;">](https://itifico.vercel.app)

> **Blog application** которое я сделал для один из моих клиентов в фрилансе, в этом прокете вы можете читать персональные Блоги.

---

# Описание
***Разные языки*** — на данном времени Блог имеет две языка: *Английский* и *Украинский*.

***Курсы:*** на сайте есть курсы по языкам программирования, например `C#`

## Возможности проекта в данном моменте:
- добавление курсы;
- добавление блоги;
- можно работать на разных языков.

## Будущая реализация в плане:
- Авторизация для разных пользавателей;
- Аналитика пользавателей;
- архивирование блогов.

---

# В данном времени проект состоит из 2 главных частей:
1. Веб интерфейс(UI) — исходники [здесь(ITifico_UI)](https://github.com/ITifico/ITifico_UI). Технологии в этом части:
   - React;
   - Sass;
   - Redux — для создание обший *state* в проекте;
   - i18next — для реализование разных языков;
   - parallax-js — создание плавающие картинки;

2. Серверная часть — исходники [здесь(ITifico_Server)](https://github.com/ITifico/ITifico_Server). Технологии в этом части:
   - Node.js — основная технология;
   - Express — для оброботки **I/O** запросов на сервер;
   - multer - загрузка картинки для блогов и курсов.
   - MongoDB — использован в качестве базы данных;
   - mongoose (ODM) — создание ***Модели(Schema)*** для базы данных **MongoDB**;

---

## Для запуска коды Веб интерфейса(UI):
1. Скачайте или клонируйте исходники — [здесь(ITifico_UI)](https://github.com/ITifico/ITifico_UI);
```bash
$ git clone https://github.com/ITifico/ITifico_UI.git
$ cd ITifico_UI/client
```

2. Установите пакеты с помощью ***npm***:
```bash
$ npm install 
```

3. Создайте новый файл с названием `.env` и добавьте нужные переменные(***Environment Variables***);
```env
REACT_APP_FALLBACK_LANG=<язык по умолчанию> // например, "en-US"
REACT_APP_BOT_ID=<ID для бота который будет получать собщении> например, "5541441349:AAHmClIY8HDzL9N6AnJjpYq2yj3vMKI3rSQ"
REACT_APP_URL=<URL для веб интерфейса который будет видимый когда переслано> // например, "itifico.com"
REACT_APP_BASE_URL=<это URL на серверная часть, в текущем формате http://example.com >
REACT_APP_CHAT_ID=<чат ID с телеграм аккаунта, который бот будет использовать> // например, "381006076"
// Если еще не запускали сервер,
// вы можете написать URL в поле REACT_APP_BASE_URL текущую удаленную сервер — https://itifico-server-production.up.railway.app
```

4. Запускайте проект локально:
```bash
$ npm start
```

## Для запуска коды Серверную часть(Backend):
1. Скачайте или клонируйте исходники — [здесь(ITifico_Server)](https://github.com/ITifico/ITifico_Server);
```bash
$ git clone https://github.com/ITifico/ITifico_Server.git
$ cd ITifico_Server/server
```

2. Установите пакеты с помощью ***npm***:
```bash
$ npm install 
```

3. Создайте новый файл с названием `.env` и добавьте нужные переменные(***Environment Variables***);
```env
PORT=<порт для запуска сервера, например "5000|8080">
CLIENT_URLS=<можно добавить несколько URL от UI части для разрешение доступа CORS, в формате "http://example.com,http://another.com" 
MONGOURI=<mongodb подключение URI>
// Вы сможете использовать тестовую базу данных,подключая этот URI "mongodb+srv://Dilrozbek_Raximov:931897318Rd@cluster0.e9gps.mongodb.net/maximal-demo"
```

4. Запускайте проект локально:
```bash
$ npm start
```

---

# Требования
- Node.js v16.0.0 или новее (предпочтительно v18).
