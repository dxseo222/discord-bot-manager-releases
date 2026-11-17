# Discord Bot Manager

A Windows app for running your Discord bots in the background: it keeps them online, restarts them if they crash, and shows each bot's console, CPU and memory in one window.

**[⬇ Download the latest version](https://github.com/dxseo222/discord-bot-manager-releases/releases/latest)**: get the `Discord-Bot-Manager-Setup-x.y.z.exe` file under **Assets**.

## Install

1. Run the downloaded `Discord-Bot-Manager-Setup-….exe`.
2. Windows will probably say **"Windows protected your PC"**. That's because the installer isn't code-signed (signing certificates cost money), not because something is wrong. Click **More info**, then **Run anyway**.
3. Click through the installer. Bot Manager opens when it's done.

After that, Bot Manager updates itself: when a new version is out, a **Restart to update** button appears in the sidebar.

## Add your first bot

1. Click **Add bot** and choose your bot's project folder. Bot Manager guesses how to start it (`npm start`, `node index.js`, `python bot.py`...). Change it if it's wrong.
2. If your bot reads its token from a `.env` file, you're done. Otherwise, put `DISCORD_TOKEN=...` under **Environment variables**: it's encrypted on your PC.
3. Click **Start**.

If the bot can't start, Bot Manager tells you why instead of restarting it over and over:

- **Node.js / Python / Java isn't installed:** click the button to get it, install it, then click **Start** again.
- **Packages aren't installed:** click **Install and start**. It runs `npm install` or `pip install -r requirements.txt` for you.

## What you need

- Windows 10 or 11.
- Whatever your bot itself needs: [Node.js](https://nodejs.org/en/download) for JavaScript bots, [Python](https://www.python.org/downloads/windows/) for Python bots (tick **Add python.exe to PATH** when installing), [Java 17+](https://adoptium.net/temurin/releases/) if your bot runs Lavalink.

## Features

- Keeps bots running: restarts crashed bots with a back-off, and stops trying if one keeps crashing.
- Starts with Windows (optional), and starts your bots with it.
- Live console with colours and search; logs are saved.
- CPU and memory per bot, uptime and crash history.
- Optional crash alerts in a Discord channel, restarts on a schedule or when a bot uses too much memory.
- Themes, colours and groups.

## Getting help

In Bot Manager, open **Settings → Get help → Copy diagnostics** and paste the result to whoever is helping you. It includes your bots' status and recent errors, but never tokens, passwords or your Windows user name.

## Privacy

Bot Manager runs entirely on your PC. It only connects to the internet to check this page for updates, and to post to Discord if you turn on crash alerts. Tokens and webhooks you enter are encrypted with Windows' own encryption and never leave your PC.
