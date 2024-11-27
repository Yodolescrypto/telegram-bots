# telegram-bots

## How to create a telegram bot quickly in node.js

### 1. Requirements
* node.js
* node-telegram-bot-api

### 2. Create a bot in Telegram
* Find @BotFather and send him a DM:
  `/newbot`
* Follow the instructions for bot creation and store the bot token safely
* If you're planning on using the bot for a channel or group, disable bot privacy
  `/setprivacy`
### 3. Dev your bot
A very basic example of a bot would be as follow:
bot.js:
```
// Setup part
const TelegramBot = require('node-telegram-bot-api');
const token = "<YOUR TOKEN>";
const bot = new TelegramBot(token, { polling: true });

// Event managing function, replicate at will with your logic
bot.on('message', (msg) => {
  const chatId = msg.chat.id;
  if (msg.text.toLowerCase() === "/hello") {
    bot.sendMessage(chatId, "hello World!");
  }
});
```

### 4. Start your bot
You can now start your bot with node:
`node bot.js`


### Too lazy to do it ?
You can check me out on https://botsoftelegram.com, message bots are free of use for a month, renewable indefinitely :)
