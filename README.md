# 🤖 Telegram Bot for Render

A simple yet powerful Telegram bot hosted on Render that demonstrates integration of Telegram bot API with cloud deployment.

![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)
![Status](https://img.shields.io/badge/Status-Archived-inactive.svg)
![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)

---

## 📝 Project Overview

This project showcases how to deploy a Telegram bot on Render cloud platform. While the current implementation displays date and time before terminating, it serves as a foundation for building more complex Telegram bots with persistent hosting.

> **Note:** The server process has been deleted. This repository is kept for reference and educational purposes.

---

## ✨ Features

- ✅ Telegram Bot API Integration
- ✅ Cloud Deployment on Render
- ✅ Python-based Implementation
- ✅ Simple Message Handling
- ✅ Webhook Configuration Support

---

## 🛠️ Tech Stack

| Component | Technology |
|-----------|-----------|
| **Language** | Python 3.8+ |
| **Bot Framework** | python-telegram-bot |
| **Hosting** | Render |
| **Deployment** | Webhook |

---

## 📋 Prerequisites

- Python 3.8 or higher
- Telegram Bot Token (from [@BotFather](https://t.me/botfather))
- Render account (for deployment)
- pip package manager

---

## 🚀 Local Setup

### Step 1: Clone Repository
```bash
git clone https://github.com/Anuj230977/telegram-bot-render.git
cd telegram-bot-render
```

### Step 2: Install Dependencies
```bash
pip install -r requirements.txt
```

### Step 3: Configure Environment
Create a `.env` file:
```env
TELEGRAM_BOT_TOKEN=your_bot_token_here
BOT_USERNAME=@your_bot_username
```

### Step 4: Run Locally
```bash
python main.py
```

---

## 🌐 Deployment on Render

### Prerequisites
- GitHub repository pushed
- Render account created

### Step-by-Step Deployment

1. **Create Web Service on Render:**
   - Go to https://render.com
   - Click "New Web Service"
   - Connect your GitHub repository

2. **Configure Settings:**
   ```
   Name: telegram-bot-render
   Environment: Python 3
   Start Command: python main.py
   ```

3. **Add Environment Variables:**
   - `TELEGRAM_BOT_TOKEN`: Your bot token
   - `BOT_USERNAME`: Your bot username
   - `RENDER_DEPLOY_HOOK`: Render webhook URL

4. **Deploy:**
   - Click "Create Web Service"
   - Wait for deployment to complete

---

## 📁 Project Structure

```
telegram-bot-render/
├── main.py                 # Bot entry point
├── requirements.txt        # Dependencies
├── .env.example           # Environment template
├── .gitignore             # Git ignore rules
└── README.md              # This file
```

---

## 📦 Dependencies

```
python-telegram-bot>=13.0
python-dotenv>=0.19.0
requests>=2.26.0
```

Install with:
```bash
pip install -r requirements.txt
```

---

## 🔧 Configuration

### Telegram Bot Token
- Get token from [@BotFather](https://t.me/botfather)
- Store securely in `.env` file
- Never commit `.env` to Git

### Webhook Setup
```python
BOT_TOKEN = os.getenv('TELEGRAM_BOT_TOKEN')
WEBHOOK_URL = "https://your-render-url.onrender.com/telegram"
```

---

## 💡 Example Usage

The bot can be extended with various features:

```python
# Handle /start command
@bot.message_handler(commands=['start'])
def start(message):
    bot.send_message(message.chat.id, "Hello! I'm a Telegram bot.")

# Handle /time command
@bot.message_handler(commands=['time'])
def send_time(message):
    import datetime
    current_time = datetime.datetime.now().strftime("%H:%M:%S")
    bot.send_message(message.chat.id, f"Current time: {current_time}")
```

---

## 🔐 Security Best Practices

- ✅ Keep `.env` out of Git (use `.gitignore`)
- ✅ Never share bot tokens
- ✅ Use environment variables for secrets
- ✅ Validate all user inputs
- ✅ Implement rate limiting for API calls

---

## 🐛 Troubleshooting

| Issue | Solution |
|-------|----------|
| "Bot token not found" | Check `.env` file and `TELEGRAM_BOT_TOKEN` |
| "Webhook connection failed" | Verify Render URL and bot token are correct |
| "Module not found" | Run `pip install -r requirements.txt` |
| "Connection timeout" | Check internet connection and firewall |

---

## 📚 Resources

- [Telegram Bot API Docs](https://core.telegram.org/bots/api)
- [python-telegram-bot Docs](https://python-telegram-bot.readthedocs.io/)
- [Render Documentation](https://render.com/docs)
- [Webhook Setup Guide](https://core.telegram.org/bots/webhooks)

---

## 🚀 Future Enhancements

- [ ] Add persistent message handling
- [ ] Implement database integration
- [ ] Add user authentication
- [ ] Create interactive inline buttons
- [ ] Add logging and monitoring
- [ ] Implement command handlers
- [ ] Add scheduled tasks

---

## 📝 License

MIT License - See LICENSE file for details

---

## 📞 Support

- 📧 Email: [Your Email]
- 💬 Issues: [GitHub Issues](https://github.com/Anuj230977/telegram-bot-render/issues)
- 🔗 Telegram: [@YourBotUsername](https://t.me/your_bot_username)

---

**⭐ If helpful, please star this repository!**
