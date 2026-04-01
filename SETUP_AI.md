# SAM Starter Kit — AI Setup Guide

> **You are reading this because a user asked you to help them set up the SAM AI Business Partner.**
> Follow these instructions exactly. You are the installer. The user should not need to touch a terminal.

## What You Are Setting Up

The SAM (Strange Advanced Marketing) AI Business Partner is a fully configured Claude Code instance that communicates with the user through Telegram. It can:

- Manage their email (Gmail)
- Manage their calendar (Google Calendar)
- Automate browser tasks (Playwright)
- Generate content and videos (Remotion)
- Track leads and manage contacts
- Show real-time activity on a desktop companion overlay
- Respond with voice notes

The user will interact with their AI partner entirely through Telegram voice and text messages. No terminal. No code.

---

## Pre-Flight Check

Before you begin, confirm the following with the user:

1. **Operating System**: Windows 10/11 or macOS. (Linux works but instructions differ.)
2. **Anthropic Account**: They need an active Claude subscription (Pro or Max) for Claude Code access.
3. **Telegram Account**: They need Telegram installed on their phone. If not, have them download it from their app store first.

---

## Phase 1: Install Claude Code

### If you are Claude Desktop with MCP (desktop-commander or windows-mcp):

You can install Claude Code directly. Run:

**Windows:**
```powershell
# Check if Node.js is installed
node --version

# If Node.js is not installed, download and install it first
# Download from https://nodejs.org/ — use the LTS version
# OR use winget:
winget install OpenJS.NodeJS.LTS

# Install Claude Code globally
npm install -g @anthropic-ai/claude-code
```

**macOS:**
```bash
# Check if Node.js is installed
node --version

# If not installed:
brew install node

# Install Claude Code
npm install -g @anthropic-ai/claude-code
```

### If you are Claude Web (no MCP access):

Tell the user:
> "I need to help you install a couple of things first. Don't worry — I'll walk you through each step. First, let's get Claude Desktop, which gives me the ability to help you directly on your computer."

Direct them to download Claude Desktop from: https://claude.ai/download

Once they have Claude Desktop running:
1. Tell them to open Claude Desktop
2. Tell them to paste this entire SETUP_AI.md content into Claude Desktop
3. Claude Desktop can then continue the automated setup with MCP access

**IMPORTANT**: Do NOT try to continue the full setup from Claude Web. You need Desktop + MCP to automate the installation.

---

## Phase 2: Install Telegram Desktop & Create Bot

### Step 2a: Install Telegram Desktop

**Windows (via MCP):**
```powershell
winget install Telegram.TelegramDesktop
```

**macOS (via MCP):**
```bash
brew install --cask telegram-desktop
```

If winget/brew is not available, tell the user:
> "Please download Telegram Desktop from https://desktop.telegram.org/ and install it. Let me know when it's done."

### Step 2b: Create a Telegram Bot

This is the ONE step that requires user interaction. Tell them exactly this:

> "Now I need you to do one quick thing in Telegram. Open Telegram on your phone or desktop, and search for @BotFather. Send it the message `/newbot`. It will ask you for a name — type anything you want, like 'My AI Partner'. Then it will ask for a username — this needs to end in 'bot', like 'myaipartner_bot'. Once it's created, BotFather will give you a token — it looks like a long string of numbers and letters. Copy that token and paste it here for me."

Wait for the user to provide the bot token. Save it — you'll need it for the Telegram plugin configuration.

---

## Phase 3: Configure Claude Code

### Step 3a: Set Up the CLAUDE.md

Create the business partner configuration file. This tells Claude Code how to behave as an AI business partner.

**Windows:**
```powershell
# Create the user's working directory CLAUDE.md
$claudeMdPath = Join-Path $env:USERPROFILE "CLAUDE.md"
```

Write the contents of the `CLAUDE.md` file from this starter kit to that path. The CLAUDE.md template is in this same repository — read it and write it to the user's home directory.

### Step 3b: Configure the Telegram Plugin

Claude Code uses the Telegram plugin for messaging. Configure it:

```powershell
# The user needs to run Claude Code once to initialize, then configure Telegram
claude

# Inside Claude Code, run:
# /telegram:configure
```

Alternatively, configure the plugin settings directly by writing to the Claude Code settings file:

**Windows:** `%APPDATA%\Claude\settings.json`
**macOS:** `~/Library/Application Support/Claude/settings.json`

Add the Telegram plugin configuration with the bot token the user provided.

### Step 3c: Install MCP Servers

Install the essential MCP servers for business functionality:

1. **gog.exe (Google Workspace)** — Gmail, Calendar, Drive, Sheets, Docs
   - Download from the gog releases page
   - Run `gog auth` to authenticate with Google (user will need to sign in)

2. **Playwright MCP** — Browser automation
   - This is typically pre-configured in Claude Code
   - Verify it's available: check Claude Code settings for playwright entry

3. **Windows MCP** (Windows only) — Desktop control
   - Install via: `npm install -g @anthropic-ai/windows-mcp`

### Step 3d: Install Claude Buddy (Desktop Companion)

```powershell
cd $env:USERPROFILE
git clone https://github.com/ajsupplycollc/claude-buddy.git
cd claude-buddy
npm install
```

Add the PostToolUse hook to Claude Code settings:

```json
{
  "hooks": {
    "PostToolUse": [
      {
        "hooks": [
          {
            "type": "command",
            "command": "node C:/Users/USERNAME/claude-buddy/hook-bridge.js",
            "timeout": 3
          }
        ]
      }
    ]
  }
}
```

Replace `USERNAME` with the actual Windows username.

Start the buddy: `cd claude-buddy && npm start`

---

## Phase 4: Test Everything

Run these tests to confirm the setup works:

1. **Telegram Test**: Send a message to the bot on Telegram. Confirm Claude Code receives it and responds.
2. **Voice Test**: Send a voice message on Telegram. Confirm it gets transcribed and responded to.
3. **Email Test**: Ask the AI to check email. Confirm Gmail access works.
4. **Calendar Test**: Ask the AI to check today's calendar. Confirm Google Calendar access works.
5. **Buddy Test**: Confirm the desktop companion overlay is showing tool activity.

If all 5 tests pass, tell the user:

> "You're all set! Your AI business partner is live. Just text or voice message it on Telegram anytime you need help with email, calendar, content, or anything else. Welcome to SAM."

---

## Failure Points & Recovery

| Issue | Solution |
|-------|----------|
| Node.js not installed | Install via winget (Windows) or brew (macOS) |
| Claude Code install fails | Check Node.js version (18+ required), try `npm cache clean --force` then retry |
| Telegram bot token invalid | Have user go back to @BotFather, use `/mybots` to check existing bots |
| Google auth fails | Run `gog auth` again, make sure popup browser window completes |
| Buddy overlay doesn't appear | Check if Electron installed correctly, run `npm install` again in claude-buddy dir |
| Claude Code can't find CLAUDE.md | Ensure it's in the user's home directory, not a subdirectory |
| MCP server not connecting | Restart Claude Code, check settings.json for correct paths |

---

## What NOT to Do

- Do NOT ask the user to edit JSON files manually
- Do NOT show them terminal output unless something failed
- Do NOT use technical jargon — speak in plain language
- Do NOT skip the testing phase
- Do NOT assume any prior technical knowledge

The goal is: **user talks to Telegram, AI partner responds. That's it.**
