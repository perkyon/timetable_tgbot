# timetable_tgbot
Телеграмм бот, показывающий расписание для студентов КМТ.

Бот может показывать расписание на сегодня (`/today`), завтра (`/tomorrow`) и, если у вас начались выходные, на ближайший учебный день (`/nearest`).

Расписание автоматически в каждую среду и субботу полностью сохраняется в базу данных, поэтому даже когда сайт упадёт, вы сможете его посмотреть. Если расписание было изменено есть возможность обновить расписание прямо сейчас (`/update`).

Бот на основе расписания всех групп строит расписание преподавателей, что может быть очень полезным во время зачётной недели.

Есть возможность указать предстоящие экзамены и смотреть их из команды `/exams`, а так же узнать имена преподавателей текущего семестра и преподаваемые ими дисциплины (`/teachers`).

Присутствует почти полная поддержка групповых чатов, поэтому бота можно добавлять в ваш студенческий чат, оповещая всех в 5 утра, что сегодня к первой паре. 

Разрабатывается возможность делать события для группы, чтобы не забывать о важном, например, о совместном походе на пересдачу.

[Ссылка на бота](https://t.me/)

## Что я о вас знаю?

Пользуясь ботом, вы соглашаетесь, что я знаю:
- Ваш никнейм и ID в Телеграмм
- Ваши настройки
- Колледж, курс и номер группы
- Расписание пар вашей группы
- Когда и какую команду вы написали (<a href="https://github.com/Elektroplayer/kubstu_timetable_tgbot/blob/master/src/events/MessageEvent.ts#L28-L32">не относится к обычным сообщениям!</a>)

Данные используются для анализа и исправления ошибок и мною не передаются третьим лицам. Все данные надёжно хранятся в базе данных с большим и сложным паролем. Подключение третьих лиц к БД исключено.

## Как запустить самостоятельно?

- Получите токен у [@BotFather](https://t.me/BotFather).
- Создайте файл `.env`
```
TOKEN="токен бота (получен выше)"
MONGO_URI="uri базы данных монги"
```

- Скачайте все библиотеки командой `npm i`
- Скомпилируйте бота `npx tsc`
- Запустите бота с помощью `node .`
