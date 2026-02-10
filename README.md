<div align="center"> <p> <img align="center" alt="count" src="https://usagif.com/wp-content/uploads/gify/zero-two-26.gif"> </p> </div> 

<div <h2 alignt="center">ZERO TWO V1 </h> </div>

A WhatsApp Bot by NORA PROJECT, built with **Baileys** and **Node.js**.

---

## 📦 Requirements

- **Node.js:** v20+
- **npm:** v7+

---

## 🚀 Installation
1️⃣ Clone Repository
```bash
git clone https://github.com/blubryaaa/V1CODEZERO
cd V1CODEZERO
```

2️⃣ Automatic Installation (Recommended)
```bash
bash install.sh
```

This script will:
- Detect your package manager (`pkg`, `apt`, `dnf`, etc.)
- Install required system dependencies
- Install Node.js packages
- Start the bot automatically

---

## 📱 Termux (Android)
```bash
pkg update && pkg upgrade
pkg install git
pkg install nodejs
pkg install ffmpeg
pkg install imagemagick
git clone https://github.com/blubryaaa/V1CODEZERO
cd V1CODEZERO
npm install
```
RECOMMENDED INSTALL ON TERMUX
```bash
pkg install yarn
yarn
```
Use **yarn**:

```bash
yarn install
yarn start
```

> Make sure `nodejs` and `yarn` are installed. The `install.sh` script already handles this.

---

## ▶️ Running the Bot
```bash
node zerotwo.js
# or
npm start
```

Scan the QR Code or use Pairing Code, and the bot is ready to use.

---

## 🚀 Deployment

See [DEPLOYMENT.md](./DEPLOYMENT.md) for guide:

- 🐦 **Pterodactyl**
- ☁️ **Railway.app**
- 🎯 **Render.com**
- 🖥️ **VPS**
- 🐳 **Docker**

---

## 📁 Project Structure
```
📂 V1CODEZERO/
├── package.json
├── zerotwo.js
├── start.js
├── nora.js
├── settings.js
├── README.md
├── N∅RA
├── LICENSE
└── PATH

📂 lib/
├── afk.js
├── ai.js
├── anime.js
├── banana.js
├── converter.js
├── cuaca.js
├── data.js
├── downloader.js
├── exif.js
├── function.js
├── handler.js
├── rwm.js
├── scraper.js
├── system.js
├── uploader.js
└── welcome.js

📂 media/
├── 🖼️ 1.png
├── 🖼️ 2.png
├── 🖼️ 3.png
├── 🖼️ 4.png
├── 🖼️ 5.png
├── 🖼️ 6.png
├── 🖼️ 7.png
├── 🖼️ 8.png
├── 🖼️ 9.png
├── 🖼️ 10.png
├── 🖼️ donate.png
├── 🖼️ qris.png
└── 🎵 audio.mp3

📂 game/
├── asahotak.json
├── family100.json
├── susunkata.json
├── tebakbendera.json
├── tebakgambar.json
├── tebakkata.json
├── tebakkimia.json
├── tebaklagu.json
└── tebaktebakan.json

📂 database/
├── absen.json
├── badwords.json
├── banned.json
├── nines.json
├── order.json
├── owner.json
├── partner.json
├── req.json
├── sewa.json
├── user.json
└── warn.json

📂 codezero/
└── login.json

📂 subzero
└── partnermode.json
```

---

## ⚙️ Configuration

📁 **[settings.js](https://github.com/blubryaaa/V1CODEZERO/blob/master/settings.js)**

```javascript
global.owner = '628xxx'            // your number
global.namaowner = 'Akyra'         // owner name
global.namaBot = 'Zero Two V1'     // bot name
global.nobot = '628xxx'            // bot number
```

**.env (Optional - for production)**

```bash
cp .env.example .env
# Edit .env
```

settings.js:
```javascript
require('dotenv').config()

global.owner = process.env.OWNER_NUMBER
global.namaowner = process.env.OWNER_NAME
global.namaBot = process.env.BOT_NAME
```

---

## 🧩 Editing & Adding Features

📁 **[nora.js](https://github.com/blubryaaa/V1CODEZERO/blob/master/nora.js)**

Look for the **[switch (command)](https://github.com/blubryaaa/V1CODEZERO/blob/61052a01ea8e8975a99f0db7f5d40bad5ee39a5b/nora.js#L742)** section.

**Where to Add New Features?**
Add or edit commands inside the switch (command)

**Example: Adding a New Command**
```js
case 'ping': {
  m.reply('pong 🏓')
}
break
```

Guidelines:
- Always add new commands using `case`
- Do not remove the main switch structure
- Place feature logic inside each `case`

---

## 🔌 Connector & Core Handler

To understand the WhatsApp connection flow and event handling, see:

📁 **[start.js](https://github.com/blubryaaa/V1CODEZERO/blob/master/start.js)**
This file is responsible for:
- Initializing Baileys connection
- Handling WhatsApp events
- Loading [settings.js](https://github.com/blubryaaa/V1CODEZERO/blob/master/settings.js)
- Dispatching messages to [nora.js](https://github.com/blubryaaa/V1CODEZERO/blob/master/nora.js)

⚠️ **Editing [start.js](https://github.com/blubryaaa/V1CODEZERO/blob/master/start.js) is not recommended unless you fully understand the bot flow.**

---

## 🔧 Troubleshooting
**Connection Error: "Couldn't Link Device"**
- ✅ Make sure the number correct: `628xx` (without +62 or 0)
- ✅ The number must registered on WhatsApp
- ✅ Pairing code only 30s - ASAP!

**Module Not Found**
```bash
rm -rf node_modules package-lock.json
npm install --legacy-peer-deps
```

**Crash**
```bash
# Check logs for error details
npm start 2>&1 | tee bot.log
```

**Port already in use**
```bash
# Find process
lsof -i :3000

# Kill process
kill -9 <PID>
```

---

## 🔐 Security
**Important:**
- ❌ **DO NOT** commit folder `codezero/` (credentials)
- ❌ **DO NOT** hardcode number in public repo
- ✅ **USE** environment variables for production
- ✅ **SETUP** `.gitignore` (already done)

**Safe setup for Production:**

1. Use `.env`:
```bash
cp .env.example .env
# Edit .env with your sensitive data
```

2. Do not commit `.env`:
```bash
# .env already in .gitignore
git add .env.example  # Just example for commit
```

3. When deploy, set variables in platform:
   - Railway: Variables tab
   - Pterodactyl: Server Variables
   - VPS: `export` or `.env` file

---

## ✨ Features
| Menu     | Bot | Group | Search | Download | Tools | Ai | Game | Fun | Owner |
| -------- | --- | ----- | ------ | -------- | ----- | -- | ---- | --- | ----- |
| Work     |  ✅  |   ✅   |    ✅    |     ✅     |   ✅   | ✅ |   ✅   |  ✅  |    ✅    |

---

## 📦 Dependencies

|        Package          | Version |        Purpose         |
|-------------------------|---------|------------------------|
| @whiskeysockets/baileys | ^6.7.5  |      WhatsApp API      |
| jimp                    | ^0.16.3 |    Image processing    |
| fluent-ffmpeg           | ^latest | Video/Audio conversion |
| axios                   | ^1.13.2 |      HTTP requests     |
| chalk                   | ^4.1.2  | Colored console output |
| pino                    | ^8.14.1 |         Logging        |
| moment-timezone         | ^0.5.34 |      Time handling     |

---

## 🤍 Support Me

- [Trakteer](https://trakteer.com/akyra.jpg)

---

## 📞 Support & Contact

- **GitHub Issues:** Report here:3
- **Email:** [Click Me!](nxtzyrex@gmail.com)
- **Developer:** Check credits on top source code

---

## 📜 License: [MIT](https://choosealicense.com/licenses/mit/)

---

## 💫 Contributor

Built with ❤️ by NORA PROJECT

- **@akyra.jpg**   :   Project Lead / Core Developer / Designer
- **@22vyn**       :   Code Maintainer / Refactor Engineer
- **@keyshaa**     :   Feature Developer / Quality Assurance
- **@anyaxcurl**   :   Infrastructure & API Provider
- **@ryxzz18**     :   Structure Manager / Support

---

## ⭐ If you like this project, please star it! :D


See ya!~ 👋🏻









