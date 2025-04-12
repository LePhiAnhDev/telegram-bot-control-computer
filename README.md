<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV">
  <img src="https://img.shields.io/badge/Ngrok-1F1E37?style=for-the-badge&logo=ngrok&logoColor=white" alt="Ngrok">
</div>

<h1 align="center">🤖 Advanced Computer Control Telegram Bot 🖥️</h1>

<p align="center">
  <em>Remote control your computer with an elegant, feature-rich Telegram bot</em>
</p>

<div align="center">
  <a href="#-key-features">Features</a> •
  <a href="#-requirements">Requirements</a> •
  <a href="#-usage">Usage</a> •
  <a href="#%EF%B8%8F-packaging-as-executable">Packaging</a>
</div>

---

## ✨ Key Features

### 🖥️ System Control
- Shutdown, restart, and sleep commands
- Cancel pending shutdown/restart operations

### 📸 Screen Capture
- High-quality screenshots with OpenCV
- Screen recording with customizable quality
- Real-time transmission to Telegram

### 📁 File Management
- Upload files from Telegram to your computer
- Download files from your computer to Telegram
- Delete files from specified paths

### 🌐 Browser Control
- Launch and control web browsers (Chrome, Brave, Edge, Opera)
- Play YouTube videos with playback controls
- Navigate websites with forward/back/refresh controls

### 🔍 System Information
- View running processes list
- System hardware & software information
- Network configuration and user accounts
- IP management (release/renew)

### 🖱️ Remote Control Interfaces
- Virtual touchpad with Ngrok public URL
- Volume control interface with interactive slider
- Virtual keyboard for text input and hotkeys

---

## 📋 Requirements

### System Requirements
- Windows OS (primary target, most features supported)
- Linux/Mac (limited functionality for some features)
- Python 3.10.11
- Admin privileges (recommended for full functionality)

### Ngrok Setup
1. Visit [ngrok.com](https://ngrok.com) and create an account
2. Download ngrok from the website
3. Extract ngrok.exe to a folder
4. Get your Auth Token from the ngrok dashboard
5. Open command prompt in the folder containing ngrok.exe
6. Run the command: `ngrok config add-authtoken $YOUR_AUTHTOKEN`

### Required Python Packages
Install all dependencies with this command:
```bash
pip install oscpy regex pyautogui nest_asyncio numpy opencv-python comtypes pynput playwright python-telegram-bot python-dotenv flask pyngrok pycaw pyinstaller
```

Then install the Playwright browsers:
```bash
playwright install
```

### API Keys/Tokens
- Telegram Bot Token (from [@BotFather](https://t.me/BotFather))

---

## 🚀 Usage

### Starting the Bot
1. Create a `.env` file with the following content:
```
TOKEN=REPLACE-YOUR-TOKEN
ALLOWED_USERS=REPLACE-YOUR-ID-CHAT
```

2. Run the bot:
```bash
python Bot_Control_Computer.py
```

---

### Available Commands

#### ⚡️ Introduction Commands

| Command | Description |
|---------|-------------|
| `/introduce` | Introduction about the author |
| `/menu` | Display list of all commands |

#### ⚡️ System Control Commands

| Command | Description |
|---------|-------------|
| `/shutdown` | Shutdown the computer |
| `/restart` | Restart the computer |
| `/sleep` | Put computer to sleep mode |
| `/cancel` | Cancel all shutdown/restart commands |

#### ⚡️ Image Commands

| Command | Description |
|---------|-------------|
| `/screen_shot` | Take a screenshot and send it |
| `/record_video` | Record screen and send the video |

#### ⚡️ File Management Commands

| Command | Description |
|---------|-------------|
| `/upload_file` | Upload a file from Telegram to your PC |
| `/download_file` | Download a file from your PC to Telegram |
| `/deletefile` | Delete a file at the specified path |

#### ⚡️ System Information Commands

| Command | Description |
|---------|-------------|
| `/tasklist` | List of running processes |
| `/systeminfo` | System information |
| `/netuser` | List of users on the computer |
| `/whoami` | Current logged-in user |
| `/hostname` | Display computer name |

#### ⚡️ Network Commands

| Command | Description |
|---------|-------------|
| `/ipconfig` | Network configuration information |
| `/release` | Release current IP address |
| `/renew` | Renew IP address |

#### ⚡️ Browser Commands

| Command | Description |
|---------|-------------|
| `/playvideo` | Play YouTube video from link |
| `/openweb` | Open websites |
| `/setbrowser` | Set default browser (chrome, brave, edge, opera) |

#### ⚡️ Utility Commands

| Command | Description |
|---------|-------------|
| `/mouse_virtual_system` | Control mouse with virtual touchpad |
| `/volume_virtual_system` | Control volume with virtual touchpad |
| `/keyboard_emulator` | Control with virtual keyboard |

---

## 🔧 Packaging as Executable

You can package this bot into a standalone Windows executable using PyInstaller:

```bash
python -m PyInstaller --onefile --noconsole Bot_Control_Computer.py
```

---

## 👨‍💻 Author & Contact

<div align="center">
  <h3>Le Phi Anh</h3>
</div>

<div align="center">
  <a href="https://github.com/LePhiAnhDev" target="_blank"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
  <a href="https://t.me/lephianh386ht" target="_blank"><img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
  <a href="https://lephianh.id.vn/" target="_blank"><img src="https://img.shields.io/badge/Website-FF7139?style=for-the-badge&logo=Firefox-Browser&logoColor=white" alt="Website"></a>
</div>

---

### 💰 Support This Project

If you find this project useful, consider supporting the developer:

- **Bank**: `1039506134` | LE PHI ANH | Vietcombank
- **MoMo**: `0971390849` | LE PHI ANH
- **Metamask**: `0x928F8c5443b13f71a4d7094E8bD2E74c86127243`

---

<p align="center">
  Made with ❤️ by <a href="https://github.com/LePhiAnhDev" target="_blank">LePhiAnhDev</a>
</p>
