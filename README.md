<!--ZERO TWO V1 — README.md -->

<img align="center" height="auto" src="https://media1.giphy.com/media/v1.Y2lkPTZjMDliOTUybnQyeTV3N3Bma3Iwb2VndGFkZHRvbmkwa2htd3lwdHY1c2d2M244YSZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/O5RIUGQnok3BDKe7U0/giphy.gif">

<p align="center">
<a href="https://github.com/blubryaaa/followers"><img title="FOLLOWERS" src="https://img.shields.io/github/followers/blubryaaa?label=FOLLOWERS&color=blue&style=flat-square"></a>
<a href="https://github.com/blubryaaa/V1CODEZERO/stargazers/"><img title="STARS" src="https://img.shields.io/github/stars/blubryaaa/V1CODEZERO?label=STARTS&color=purple&style=flat-square"></a>
<a href="https://github.com/blubryaaa/V1CODEZERO/network/members"><img title="FORKS" src="https://img.shields.io/github/forks/blubryaaa/V1CODEZERO?label=FORKS&color=darkred&style=flat-square"></a>
<a href="https://github.com/blubryaaa/V1CODEZERO/watchers"><img title="WATCHING" src="https://img.shields.io/github/watchers/blubryaaa/V1CODEZERO?label=WATCHERS&color=cyan&style=flat-square"></a>
<a href="https://github.com/blubryaaa/V1CODEZERO/"><img title="SIZE" src="https://img.shields.io/github/repo-size/blubryaaa/V1CODEZERO?label=SIZE&color=green&style=flat-square"></a>
</p>

<p align="center">
<a href="https://github.com/blubryaaa/V1CODEZERO"><img title="RELEASE" src="https://img.shields.io/badge/RELEASE%20| v1.0.0-darkblue.svg?style=for-the-badge&logo=appveyor" /></a>
</p>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">
<h1 align="center">𝐙𝐄𝐑𝐎 𝐓𝐖𝐎 𝐕𝟏</h1>
<p align="center">
A modern and blazing-fast WhatsApp Bot powered by Baileys & Node.js 20+. Designed with native ESM support for lightweight performance, bringing you advanced chat automation with a beautiful touch of Zero Two aesthetics.
</p>

<h1 align="center"><b>✨ Key Features</b></h1>

<br>

<table>
<tr>
<td align="center" width="33%">

**⚡ Performance**

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/High%20Voltage.png" width="50" />

Powered by Node.js 20+
<br>Optimized V8 Engine
<br>Smooth & Reliable

</td>
<td align="center" width="33%">

**🎯 Architecture**

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Gear.png" width="50" />

Modern ESM Design
<br>Modular & Plug-and-Play
<br>Clean & Maintainable

</td>
<td align="center" width="33%">

**💾 Database**

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/File%20Folder.png" width="50" />

MongoDB via Mongoose
<br>Robust Data Handling
<br>Schema-based Models

</td>
</tr>
<tr>
<td align="center" width="33%">

**🌐 Deployment**

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Travel%20and%20places/Globe%20Showing%20Europe-Africa.png" width="50" />

24/7 Server Ready
<br>Docker Container Support
<br>Pterodactyl Panel Ready

</td>
<td align="center" width="33%">

**🎨 Rich Media**

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Video%20Camera.png" width="50" />

Interactive Buttons
<br>Carousels & Albums
<br>WhatsApp Stories Support

</td>
<td align="center" width="33%">

**🔐 Security**

<img src="https://raw.githubusercontent.com/Tarikul-Islam-Anik/Animated-Fluent-Emojis/master/Emojis/Objects/Locked.png" width="50" />

Secure Pairing Code
<br>Strict Owner-Only Access
<br>Smart Command Blocking

</td>
</tr>
</table>


<br>
<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<table>
<tr>
<h1 align="center" width="20%">

**⚡ Quick Start**

</h1>
</tr>
</table>

For detailed installation instructions, see **[INSTALLATION.md](.github/INSTALLATION.md)**

**Automated Installation for Linux (Ubuntu/Debian)**

```bash
curl -fsSL https://raw.githubusercontent.com/blubryaaa/V1CODEZERO/main/install.sh | bash
```

**Post-installation:**

```bash
bot config  # Configure settings
bot start   # Start the bot
bot log     # View logs
bot status  # Check status
```

**Manual Installation**

See **[INSTALLATION.md](.github/INSTALLATION.md)** for comprehensive manual installation guide.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<table>
<tr>
<h1 align="center" width="20%">

**🔌 Plugin System**

</h1>
</tr>
</table>

**Plugin Structure**

See **[PATH.md](.github/PATH.md)** for full project structure.

**Creating a Basic Plugin**

Create a file in `/plugins/[category]/[name].js`:


```javascript
let handler = async (m, { sock }) => {
  const start = Date.now();
  const msg = await sock.sendMessage(m.chat, { text: "⏱️ Checking..." });
  const latency = Date.now() - start;
  await sock.sendMessage(m.chat, { text: `🏓 Pong! ${latency} ms`, edit: msg.key });
};

handler.help = ["ping"];
handler.tags = ["info"];
handler.command = /^(ping)$/i;

export default handler;
```

**Plugin Properties**

- `handler.help` - Command names for help menu
- `handler.tags` - Category tags
- `handler.command` - RegExp pattern for command matching
- `handler.owner` - Owner-only command (optional)
- `handler.premium` - Premium-only command (optional)
- `handler.group` - Group-only command (optional)
- `handler.admin` - Admin-only command (optional)
- `handler.register` - Only registered user (optional)

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<table>
<tr>
<h1 align="center" width="20%">

**🎮 Usage**

</h1>
</tr>
</table>

**Command Prefixes**

Zero Two supports multiple prefixes:

```
.menu    # Dot prefix
!menu    # Exclamation
/menu    # Slash
```

**Built-in Commands**

| Command           | Description          | Example |
| ----------------- | -------------------- | ------- |
| `.menu` / `.help` | Display command menu | `.menu` |
| `.ping`           | Check bot latency    | `.ping` |

**Interacting with the Bot**

- **Main Menu**: Send `.menu` or `.help`
- **Category Menu**: Select category from button menu
- **Direct Command**: Use prefix + command name

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<img align="center" height="auto" src="https://media1.giphy.com/media/v1.Y2lkPTZjMDliOTUydGFzYncxMjB2dHJzcnprd2ZwM2d5ejB0bnk5b200b3Y2YzU1bmI1dCZlcD12MV9pbnRlcm5hbF9naWZfYnlfaWQmY3Q9Zw/Z5VdlOIfQkEQe8x8QL/giphy.gif">

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<table>
<tr>
<h1 align="center" width="20%">

**💬 Community**

</h1>
</tr>
</table>

<p align="center">Need help or just want to chat? Join our active community to get the latest announcements and support.</p>

<p align="center" >
<a href="https://whatsapp.com/channel/0029VbBsHfhL2ATzgzs7wt2O"><img src="https://img.shields.io/badge/Channel-25D366?style=for-the-badge&logo=whatsapp&logoColor=white" width="140px">
</a>
</p>

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<table>
<tr>
<h1 align="center" width="20%">

**🍻 Contributors**

</h1>
</tr>
</table>

- 💚 All **[contributors](https://github.com/blubryaaa/V1CODEZERO/graphs/contributors)** who made this possible
- 🌍 The amazing open-source community
- ⭐ Everyone who starred this repository
- 🐛 Bug reporters and feature requesters

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<table>
<tr>
<h1 align="center" width="20%">

**💌 Donate**

</h1>
</tr>
</table>

- Support me via **[QRIS (Asean)](./media/image/util/qris.png)**.
- Support me via **[Trakteer (LOCAL)](https://trakteer.com/akyrajpg)**.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">

<table>
<tr>
<h1 align="center" width="20%">

**🔒 Security**

</h1>
</tr>
</table>

> [!WARNING]
**DO NOT** report security issues through public GitHub issues.

> This bot is not made by WhatsApp.inc so overusing this bot may result in WhatsApp account ban. We will only assist you in Bot Deployment (Installation or Hosting). Not in Bot Development. If you Modify this bot and face any issues, I am not responsible for that because it's not possible for me or my team to help everyone in bot Development/Modification. Only modify if you know what you are doing. This bot is made for Educational/Fun/Group Management purposes only. I and the team will not be responsible for any misuse of this bot. We will only assist you in Setup/Deployment of this bot.

Report vulnerabilities to: **01noraproject@gmail.com**

See **[SECURITY.md](.github/SECURITY.md)** for our security policy.

<img src="https://user-images.githubusercontent.com/73097560/115834477-dbab4500-a447-11eb-908a-139a6edaec5c.gif">
