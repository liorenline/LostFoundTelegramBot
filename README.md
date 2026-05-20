# 🔍 Lost & Found Telegram Bot

A Telegram bot for reporting lost and found items. Users submit a report directly in the bot — it gets forwarded to moderators and then posted to a Telegram channel.

---

## ✨ How it works

1. User opens the bot and fills out a form:
   - 📦 Item name *(required)*
   - 📍 Where it was found *(required)*
   - 📝 Description *(optional)*
   - 📷 Photo *(optional)*
   - 📞 Contact info *(optional)*
2. The report is forwarded to the **moderation team**
3. Moderators review and post it to the **Telegram channel**

---

## 🛠 Tech Stack

- **Language:** Python
- **Framework:** python-telegram-bot (PTB)
- **Hosting:** Fly.io

---

## 🚀 Running with Docker

### 1. Clone the repository

```bash
git clone https://github.com/liorenline/LostFoundTelegramBot.git
cd LostFoundTelegramBot
```

### 2. Create a `.env` file

```env
BOT_TOKEN=your_telegram_bot_token
CHANNEL_ID=your_channel_id
MODERATOR_CHAT_ID=your_moderator_chat_id
```

Get your token from [@BotFather](https://t.me/BotFather) on Telegram.

### 3. Build and run

```bash
docker build -t lostfoundbot .
docker run --env-file .env lostfoundbot
```

---

## 🔧 Running locally (without Docker)

```bash
python -m venv .venv
source .venv/bin/activate      # Windows: .venv\Scripts\activate
pip install -r requirements.txt
python userbot.py
```

---

## 📁 Project Structure

```
LostFoundTelegramBot/
├── userbot.py        # Main bot logic
├── requirements.txt  # Python dependencies
└── Dockerfile        # Container build
```

