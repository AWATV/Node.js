## Шаг 1: Создание нового проекта на Replit

1. Перейдите на [веб-сайт Replit](https://replit.com/) и войдите в свою учетную запись (или создайте новую, если у вас ее еще нет).
2. Нажмите на кнопку "New Repl" (Новый Repl) для создания нового проекта.
3. Выберите "Node.js" в качестве языка программирования для вашего проекта.
4. Введите имя проекта и нажмите "Create Repl" (Создать Repl).

## Шаг 2: Установка зависимостей

1. Откройте терминал в Replit, который расположен внизу экрана.
2. В терминале выполните следующую команду для установки библиотеки `node-telegram-bot-api`:

```bash
npm install node-telegram-bot-api
```
## Шаг 3: Написание кода эхо-бота

1. Отредактируйте существующий файл index.js следующим образом:

```node
const TelegramBot = require('node-telegram-bot-api');

// Ваш токен бота Telegram
const token = 'YOUR_TELEGRAM_BOT_TOKEN';

// Создаем экземпляр бота
const bot = new TelegramBot(token, {polling: true});

// Обработчик входящих сообщений
bot.on('message', (msg) => {
  const chatId = msg.chat.id;
  const message = msg.text;

  // Отправляем обратно полученное сообщение
  bot.sendMessage(chatId, message);
});
```

2. Замените `'YOUR_TELEGRAM_BOT_TOKEN'` на свой токен бота Telegram. Если у вас еще нет токена, создайте его, следуя инструкциям по созданию бота в Telegram.

##Шаг 4: Запуск бота
1. В верхней панели Replit нажмите кнопку "Run" (Запустить).
2. Replit запустит ваш проект и бота.
