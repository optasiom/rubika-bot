
# rubika-bot 

[![npm](https://img.shields.io/npm/v/rubika-bot-x.svg)](https://www.npmjs.com/package/rubika-bot-x)
[![Downloads](https://img.shields.io/npm/dt/rubika-bot-x.svg)](https://www.npmjs.com/package/rubika-bot-x)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](https://opensource.org/licenses/MIT)

🚀 Build powerful bots for the Rubika messaging platform with ease!

---

## ✨ Key Features

| Category | Features |
|----------|----------|
| 📱 Messaging | Full support for text, media, locations, contacts, polls |
| 🎛️ UI Elements | Interactive buttons, keyboards, selection menus, calendars |
| ⚡ Performance | Optimized polling, automatic offset management |
| 🔧 Tools | Command handling, message forwarding/editing |

---

## 🚀 Quick Start

```bash
# Install package
npm install rubika-bot-x

# Initialize bot
const { RubikaBot } = require('rubika-bot');

const bot = new RubikaBot('YOUR_TOKEN_HERE');
bot.start();
```

---

## 🎮 Example Usage

### Send a Message with Buttons
```javascript
const button = createSimpleButton('btn1', 'Click Me!');
const keyboard = createSimpleKeypad([button]);

bot.sendMessageWithInlineKeyboard(chatId, 'Try this button:', keyboard);
```

### Handle Commands
```javascript
bot.when('/start', async (msg) => {
  bot.sendMessage(msg.chat_id, 'Welcome! 👋');
});
```

---

## 🔧 Configuration

```javascript
const bot = new RubikaBot(token, {
  timeout: 30000,      // Request timeout
  maxRetries: 3,       // Retry attempts
  retryDelay: 2000,    // Delay between retries
  offsetFile: './data/offset.txt' // Persistent storage
});
```

---

## 🤝 Contributing

We welcome contributions! Here's how to help:

1. Fork the repo
2. Create a feature branch (`git checkout -b amazing-feature`)
3. Commit your changes (`git commit -am 'Add amazing feature'`)
4. Push to the branch (`git push origin amazing-feature`)
5. Open a pull request

---

## 📚 Documentation

- [Full API Reference](link-to-docs)
- [Examples Gallery](link-to-examples)
- [Troubleshooting Guide](link-to-troubleshooting)

---

## ❤️ Support the Project

This project needs your support! If you find it useful, please consider:

- ⭐ Starring the repository
- 💬 Providing feedback
- ☕ Buying us a coffee

---

## 📜 License

MIT © [Your Name](https://github.com/yourusername)
```

### Why this design works:

1. **Visual Hierarchy**: Uses bold headings, tables, and clear sections
2. **Badge Showcase**: Shows key metrics at the top
3. **Quick Start**: Provides instant runnable code
4. **Modern Icons**: Uses emojis and symbols for visual appeal
5. **Contribution Guide**: Clear instructions for contributors
6. **Call to Action**: Encourages engagement with stars/support
7. **Clean Layout**: Proper spacing and organization

This README follows current trends while maintaining professionalism and clarity. You can customize the placeholders (like `[link-to-docs]`) with actual links once your documentation is ready.
