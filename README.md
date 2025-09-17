
# rubika-bot

## 📚 Node.js Library for Building Rubika Bots

**rubika-bot** is a Node.js library that allows you to easily create bots for the Rubika messaging platform. It provides a comprehensive wrapper around the official Rubika API with tools to build powerful messaging bots.

---

## ✨ Features

- **Full Message Support**: Text, images, audio, locations, contacts, polls, and more
- **Interactive Buttons**: Simple buttons, selection menus, calendars, location pickers, and many others
- **Keyboards**: Both chat and inline keyboards with customizable sizes and timing
- **Smart Polling**: Automatic polling system with offline management
- **Command Management**: Add and manage bot commands
- **Message Forwarding**: Forward messages between chats
- **Message Editing**: Edit existing messages
- **Message Deletion**: Delete messages
- **Poll Creation**: Create and manage polls

---

## 📦 Installation

```bash
npm install rubika-bot
```

or

```bash
yarn add rubika-bot
```

---

## 🔧 Usage

### Basic Setup

```javascript
const { RubikaBot } = require('rubika-bot');

const botToken = 'YOUR_BOT_TOKEN'; // Replace with your bot token
const bot = new RubikaBot(botToken);

// Start the bot
bot.start().catch(console.error);
```

### Send Text Message

```javascript
bot.sendMessage(chatId, 'Hello World!');
```

### Send Message with Interactive Buttons

```javascript
const button = createSimpleButton('btn1', 'Button 1');
const keyboard = createSimpleKeypad([button]);

bot.sendMessageWithInlineKeyboard(chatId, 'Choose an option:', keyboard);
```

### Respond to /start Command

```javascript
bot.when('/start', async (message) => {
    bot.sendMessage(message.chat_id, 'Welcome to my bot!');
});
```

---

## 🎯 Advanced Examples

### Create a Selection Button

```javascript
const selectionItems = [
    new ButtonSelectionItem('Option 1', '', ButtonSelectionTypeEnum.TextOnly),
    new ButtonSelectionItem('Option 2', '', ButtonSelectionTypeEnum.TextOnly)
];

const selection = new ButtonSelection(
    'selection1',
    UpdateEndpointTypeEnum.ReceiveSelection,
    UpdateEndpointTypeEnum.GetSelectionItem,
    selectionItems,
    false,
    1,
    'Please select'
);

const button = new Button('selBtn', ButtonTypeEnum.Selection, 'Select', selection);
const keyboard = createSimpleKeypad([[button]]);

bot.sendMessageWithInlineKeyboard(chatId, 'Please choose:', keyboard);
```

### Send Location

```javascript
bot.sendLocation(chatId, 35.6895, 51.3890); // Tehran coordinates
```

### Create a Poll

```javascript
bot.sendPoll(chatId, 'What\'s the best programming language?', ['JavaScript', 'Python', 'Java', 'C++']);
```

---

## ⚙️ Configuration Options

```javascript
const bot = new RubikaBot(token, {
    timeout: 30000,          // Request timeout in milliseconds
    maxRetries: 3,           // Maximum number of retry attempts
    retryDelay: 2000,        // Delay between retries in milliseconds
    offsetFile: './offset.txt' // Path to store last message ID
});
```

---

## 🤝 Contributing

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

---

## 📄 License

This project is licensed under the MIT License.

---

## 💬 Contact

For questions or issues, please open an issue on GitHub.

---

**Note:** This library is not officially supported by Rubika. For official support, visit the [Rubika website](https://rubika.ir).
```

You can simply copy this entire block and paste it into your `README.md` file. The README includes all essential sections in a clean, organized format with proper markdown syntax that will render correctly on GitHub.
