<div align="center">
  <img src="https://img.shields.io/badge/Python-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Python">
  <img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram">
  <img src="https://img.shields.io/badge/Flask-000000?style=for-the-badge&logo=flask&logoColor=white" alt="Flask">
  <img src="https://img.shields.io/badge/OpenCV-5C3EE8?style=for-the-badge&logo=opencv&logoColor=white" alt="OpenCV">
</div>

<h1 align="center">🤖 Advanced Computer Control Telegram Bot 🖥️</h1>

<p align="center">
  <em>Remote control your computer with an elegant, feature-rich Telegram bot</em>
</p>

<p align="center">
  <img src="https://github.com/LePhiAnhDev/assets/raw/main/telegram-bot-control.png" alt="Bot Control Computer" width="80%">
</p>

<div align="center">
  <a href="#-key-features">Features</a> •
  <a href="#-requirements">Requirements</a> •
  <a href="#%EF%B8%8F-installation">Installation</a> •
  <a href="#-usage">Usage</a> •
  <a href="#%EF%B8%8F-packaging-as-executable">Packaging</a> •
  <a href="#%EF%B8%8F-important-notes">Notes</a>
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
- Python 3.7 or higher
- Admin privileges (recommended for full functionality)

### Required Python Packages
```bash
# Core functionality
python-telegram-bot>=13.0
pyautogui
opencv-python
python-dotenv
nest_asyncio
numpy
playwright
pynput

# Virtual touchpad/volume control
flask
pyngrok

# Windows-specific audio control (optional)
pycaw
comtypes
```

### API Keys/Tokens
- Telegram Bot Token (from [@BotFather](https://t.me/BotFather))
- Ngrok Auth Token (optional, for virtual touchpad/volume control)

---

## ⚙️ Installation

### 1. Clone the repository
```bash
git clone https://github.com/yourusername/computer-control-telegram-bot.git
cd computer-control-telegram-bot
```

### 2. Set up virtual environment (optional but recommended)
```bash
python -m venv venv
# On Windows
venv\Scripts\activate
# On Linux/Mac
source venv/bin/activate
```

### 3. Install dependencies
```bash
pip install -r requirements.txt
```

### 4. Install Playwright browsers
```bash
python -m playwright install
```

### 5. Configure the environment variables
Create a `.env` file in the project directory with the following:
```
TOKEN=your_telegram_bot_token_here
ALLOWED_USERS=your_telegram_user_id,another_user_id
NGROK_AUTH_TOKEN=your_ngrok_auth_token_here
```

### 6. Customize settings (optional)
Open `Bot_Control_Computer.py` and adjust settings like:
- `DEFAULT_UPLOAD_FOLDER`: Default folder for uploaded files
- `BROWSER_PATHS`: Custom browser executable paths
- `FLASK_PORT`: Port for the virtual touchpad server

---

## 🚀 Usage

### Starting the Bot
```bash
python Bot_Control_Computer.py
```

### Available Commands

<details>
<summary><b>⚡️ Introduction Commands</b></summary>

| Command | Description |
|---------|-------------|
| `/introduce` | Introduction about the author |
| `/menu` | Display list of all commands |

</details>

<details>
<summary><b>⚡️ System Control Commands</b></summary>

| Command | Description |
|---------|-------------|
| `/shutdown` | Shutdown the computer |
| `/restart` | Restart the computer |
| `/sleep` | Put computer to sleep mode |
| `/cancel` | Cancel all shutdown/restart commands |

</details>

<details>
<summary><b>⚡️ Image Commands</b></summary>

| Command | Description |
|---------|-------------|
| `/screen_shot` | Take a screenshot and send it |
| `/record_video` | Record screen and send the video |

</details>

<details>
<summary><b>⚡️ File Management Commands</b></summary>

| Command | Description |
|---------|-------------|
| `/upload_file` | Upload a file from Telegram to your PC |
| `/download_file` | Download a file from your PC to Telegram |
| `/deletefile` | Delete a file at the specified path |

</details>

<details>
<summary><b>⚡️ System Information Commands</b></summary>

| Command | Description |
|---------|-------------|
| `/tasklist` | List of running processes |
| `/systeminfo` | System information |
| `/netuser` | List of users on the computer |
| `/whoami` | Current logged-in user |
| `/hostname` | Display computer name |

</details>

<details>
<summary><b>⚡️ Network Commands</b></summary>

| Command | Description |
|---------|-------------|
| `/ipconfig` | Network configuration information |
| `/release` | Release current IP address |
| `/renew` | Renew IP address |

</details>

<details>
<summary><b>⚡️ Browser Commands</b></summary>

| Command | Description |
|---------|-------------|
| `/playvideo` | Play YouTube video from link |
| `/openweb` | Open websites |
| `/setbrowser` | Set default browser (chrome, brave, edge, opera) |

</details>

<details>
<summary><b>⚡️ Utility Commands</b></summary>

| Command | Description |
|---------|-------------|
| `/mouse_virtual_system` | Control mouse with virtual touchpad |
| `/volume_virtual_system` | Control volume with virtual touchpad |
| `/keyboard_emulator` | Control with virtual keyboard |

</details>

---

## 🔧 Packaging as Executable

You can package this bot into a standalone Windows executable using PyInstaller.

### 1. Install PyInstaller
```bash
pip install pyinstaller
```

### 2. Create the executable
```bash
pyinstaller --onefile --icon=icon.ico Bot_Control_Computer.py
```

### 3. Advanced packaging (with hidden console)
```bash
pyinstaller --onefile --noconsole --icon=icon.ico Bot_Control_Computer.py
```

### 4. Package with dependencies
Create a `bot-control.spec` file:

```python
# -*- mode: python ; coding: utf-8 -*-

block_cipher = None

a = Analysis(['Bot_Control_Computer.py'],
             pathex=['.'],
             binaries=[],
             datas=[],
             hiddenimports=['pyngrok.ngrok', 'pkg_resources.py2_warn', 'playwright.sync_api', 'playwright.async_api'],
             hookspath=[],
             runtime_hooks=[],
             excludes=[],
             win_no_prefer_redirects=False,
             win_private_assemblies=False,
             cipher=block_cipher,
             noarchive=False)

pyz = PYZ(a.pure, a.zipped_data,
             cipher=block_cipher)

exe = EXE(pyz,
          a.scripts,
          a.binaries,
          a.zipfiles,
          a.datas,
          [],
          name='Computer_Control_Bot',
          debug=False,
          bootloader_ignore_signals=False,
          strip=False,
          upx=True,
          upx_exclude=[],
          runtime_tmpdir=None,
          console=False,
          icon='icon.ico')
```

Then run:
```bash
pyinstaller bot-control.spec
```

### 5. Make sure to include .env file
Place the `.env` file alongside the executable in the `dist` folder.

---

## ⚠️ Important Notes

- **Security Warning**: This bot gives extensive control over your computer. Only share access with trusted users.
- **Windows Focus**: Some features (especially volume control) are Windows-specific.
- **Administrator Rights**: Some operations require administrator privileges.
- **Browser Selection**: The bot will automatically switch to an available browser if your preferred one is not found.
- **File Size Limits**: Telegram has a 50MB file size limit for sending/receiving files.
- **Ngrok Sessions**: Virtual touchpad/volume control sessions expire after approximately 2 hours.
- **Error Handling**: The bot includes comprehensive error handling but may encounter issues with specific hardware configurations.

---

## 👨‍💻 Author & Contact

<div align="center">
  <img src="https://github.com/LePhiAnhDev/assets/raw/main/developer-avatar.png" alt="Le Phi Anh" width="150px" style="border-radius: 50%">
  <h3>Le Phi Anh</h3>
</div>

<div align="center">
  <a href="https://github.com/LePhiAnhDev"><img src="https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white" alt="GitHub"></a>
  <a href="https://t.me/lephianh386ht"><img src="https://img.shields.io/badge/Telegram-2CA5E0?style=for-the-badge&logo=telegram&logoColor=white" alt="Telegram"></a>
  <a href="https://lephianh.id.vn/"><img src="https://img.shields.io/badge/Website-FF7139?style=for-the-badge&logo=Firefox-Browser&logoColor=white" alt="Website"></a>
</div>

---

### 💰 Support This Project

If you find this project useful, consider supporting the developer:

- **Bank**: `1039506134` | LE PHI ANH | Vietcombank
- **MoMo**: `0971390849` | LE PHI ANH
- **Metamask**: `0x928F8c5443b13f71a4d7094E8bD2E74c86127243`

---

<p align="center">
  <sub>Made with ❤️ by <a href="https://github.com/LePhiAnhDev">Le Phi Anh</a></sub>
</p>
