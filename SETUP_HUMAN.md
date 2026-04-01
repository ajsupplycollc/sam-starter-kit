# SAM Starter Kit — Human Setup Guide

> This guide is for people who want to set things up themselves.
> **Easier option**: Open Claude Desktop, paste the contents of SETUP_AI.md, and let Claude do it for you.

---

## Step 1: Get Claude Desktop

1. Go to https://claude.ai/download
2. Download Claude Desktop for your computer (Windows or Mac)
3. Install it and sign in with your Anthropic account

## Step 2: Get Claude Code

1. Open Claude Desktop
2. Tell it: "Please install Claude Code for me"
3. Claude Desktop will handle the installation

If Claude Desktop can't install it, you'll need Node.js first:
- Go to https://nodejs.org
- Download and install the LTS version
- Then open a terminal and type: `npm install -g @anthropic-ai/claude-code`

## Step 3: Get Telegram

1. If you don't have Telegram on your phone, download it from your app store
2. Download Telegram Desktop from https://desktop.telegram.org and install it

## Step 4: Create Your AI's Telegram Bot

1. Open Telegram (phone or desktop)
2. Search for **@BotFather**
3. Send the message: `/newbot`
4. When asked for a name, type anything (e.g., "My AI Partner")
5. When asked for a username, type something ending in "bot" (e.g., "myaipartner_bot")
6. BotFather will give you a **token** — it looks like `7123456789:AAH1234567890abcdefghij`
7. Copy this token. You'll need it in the next step.

## Step 5: Connect Everything

1. Open Claude Code (type `claude` in a terminal, or ask Claude Desktop to open it)
2. Tell Claude Code: "Please set up the Telegram plugin with this bot token: [paste your token]"
3. Tell Claude Code: "Please install gog.exe for Gmail and Calendar access"
4. When prompted, sign into your Google account in the browser window that opens

## Step 6: Install the Desktop Companion (Optional)

1. Tell Claude Code: "Please clone and set up claude-buddy from https://github.com/ajsupplycollc/claude-buddy"
2. Claude Code will handle the installation

## Step 7: Test It

1. Open Telegram on your phone
2. Find your new bot (search for the name you chose in Step 4)
3. Send it a message: "Hello!"
4. If it responds, you're done!

Try these:
- "Check my email"
- "What's on my calendar today?"
- "Remind me to call the dentist tomorrow at 2pm"

---

## Troubleshooting

**My bot doesn't respond**
- Make sure Claude Code is running on your computer
- Check that the Telegram plugin is configured (ask Claude Code to verify)

**Email/Calendar doesn't work**
- Run `gog auth` to re-authenticate with Google
- Make sure you completed the Google sign-in in the browser

**I'm stuck**
- Open Claude Desktop and describe your problem
- It can usually diagnose and fix issues for you

---

*If this guide was confusing, try the easier way: paste SETUP_AI.md into Claude Desktop and let Claude handle everything.*
