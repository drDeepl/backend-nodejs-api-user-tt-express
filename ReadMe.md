## Требования:

- У каждого пользователя должно быть:
  - **ID**
  - **Имя**
  - **Фамилия**
  - **Email**
  - **Пароль**
  - **Пол(Мужской, Женский)**
  - **Фото**
  - **Дата регистрации**
- При регистрации указывается только

  - **Имя**
  - **Email**
  - **Пароль**

- При редактировании можно менять всю информацию кроме _id_, _Пароля_, _Дата регистрации_.
- При получение всех пользователей с пагинацией сортировать по дате регистрации.
- В базе данных хранить только название файла, все фото должны лежать в папке и раздаваться статически.

## API имееет следующие методы:

- Регистрация пользователя (POST /user/register)
- Авторизация пользователя (POST /user/login)
- Редактирование пользователя (PUT /profile/[id])
- Получение пользователя (GET /profile/[id])
- Получение всех пользователей с пагинацией (GET **profile**/profiles?page=1, 10 на страницу)

- Загрузка фото пользователя
- Получение фото пользователя

## Используется:

- валидация входных параметров
- в качестве ORM Prisma
- JWT
- Пароль хранится как хеш
- Проверка фото по размеру, и формату (до 10 мб, .jpg, .png)

## Стэк технологий

- Фреймворк Express.js
- jsonwebtoken
- Валидация запросов: Joi
- Prisma ORM
- logger winston

## База данных

Экспорт базы данных находится в папке `database`

## Запуск приложения

`npm run dev`
