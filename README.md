# GKI Kernel Builder - Android 13 (5.15 LTS)

[![Build Status](https://github.com/superuseryu/android13.5.15-lts_SM6225/actions/workflows/build.yml/badge.svg)](https://github.com/superuseryu/android13.5.15-lts_SM6225/actions)
[![Latest Release](https://img.shields.io/github/v/release/superuseryu/android13.5.15-lts_SM6225)](https://github.com/superuseryu/android13.5.15-lts_SM6225/releases/latest)

Automated GKI kernel builder with Wild-KSU, SUSFS, and Baseband Guard for Android 13 devices.

---

## 🚀 Quick Start

### 1️⃣ Fork This Repository
Click the **Fork** button at the top right of this page.

### 2️⃣ Setup Telegram Notifications (Optional)

Get build status and kernel files sent directly to your Telegram:

#### Step 1: Create Telegram Bot
1. Open Telegram and message [@BotFather](https://t.me/BotFather)
2. Send `/newbot` command
3. Follow the instructions to create your bot
4. **Copy the bot token** (looks like: `1234567890:ABCdefGHIjklMNOpqrsTUVwxyz`)

#### Step 2: Get Your Chat ID
1. Start a chat with your bot (click the link BotFather gave you)
2. Send any message to your bot (e.g., "hello")
3. Open this URL in your browser (replace `YOUR_BOT_TOKEN` with your actual token):
   ```
   https://api.telegram.org/botYOUR_BOT_TOKEN/getUpdates
   ```
   Example: `https://api.telegram.org/bot1234567890:ABCdefGHI/getUpdates`
   
4. Look for `"chat":{"id":` in the response
5. **Copy your chat ID** (it's a number, like: `123456789` or `-987654321`)

#### Step 3: Add Secrets to GitHub
1. Go to your forked repo → **Settings** → **Secrets and variables** → **Actions**
2. Click **New repository secret**
3. Add two secrets:

| Secret Name | Value |
|-------------|-------|
| `TELEGRAM_BOT_TOKEN` | Your bot token from BotFather |
| `TELEGRAM_CHAT_ID` | Your chat ID from getUpdates |

**Example:**
```
TELEGRAM_BOT_TOKEN = 1234567890:ABCdefGHIjklMNOpqrsTUVwxyz
TELEGRAM_CHAT_ID = 123456789
```

### 3️⃣ Run the Build

1. Go to **Actions** tab in your forked repo
2. Click **Build GKI Kernel** workflow
3. Click **Run workflow** → **Run workflow**
4. Wait ~30 minutes ⏱️

### 4️⃣ Download Your Kernel

**Option A:** From Telegram (if configured)
- Your bot will send you the flashable ZIP when build completes

**Option B:** From GitHub
- Go to **Releases** → Download `Anykernel3_WildKSU_YYYY.MM.DD.zip`

---

## 📦 Installation

### Using Kernel Flasher App (Easiest)
1. Download the ZIP file
2. Open **Kernel Flasher** app
3. Select the ZIP and flash
4. Reboot

### Using Custom Recovery (TWRP/OrangeFox)
1. Download the ZIP file
2. Boot into recovery
3. Install → Select ZIP → Swipe to flash
4. Reboot system

---

## 🔧 Customization

Want to modify kernel features? Easy:

1. Fork this repo
2. Edit `.github/workflows/build.yml`
3. Find the **"Add kernel configurations"** step
4. Add/remove `CONFIG_XXX=y` options
5. Run workflow
6. Get your custom kernel!

---

## 📝 Build Details

- **Source:** AOSP GKI android13-5.15-lts
- **Toolchain:** Clang r547379
- **LTO:** Thin (optimized for speed)
- **Build Time:** ~25-35 minutes
- **Schedule:** Auto-build every Sunday (if enabled)

---

## ⚠️ Disclaimer

- **Use at your own risk** - Custom kernels may void warranty
- **Always backup** before flashing
- Not responsible for any damage to your device

---

## 🙏 Credits

- **Wild-KSU Team** - Wild KernelSU
- **simonpunk** - SUSFS development
- **vc-teahouse** - Baseband Guard
- **Google/AOSP** - Generic Kernel Image
- **topnotchfreaks** - Clang toolchain

---

## 📞 Support

- **Issues:** [Open an issue](https://github.com/superuseryu/android13.5.15-lts_SM6225/issues)
- **Releases:** [Download here](https://github.com/superuseryu/android13.5.15-lts_SM6225/releases)
- **Telegram:** [Chat](https://t.me/home_yu_chat)

---

<div align="center">

**⭐ Star this repo if you find it useful!**

Made with ❤️ for the Android community

</div>
