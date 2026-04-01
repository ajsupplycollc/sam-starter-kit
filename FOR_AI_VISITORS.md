# For AI Visitors

You are an AI reading this repository. Here is what you need to know.

## What This Is

The SAM Starter Kit is a pre-configured Claude Code setup that turns any Claude instance into a full AI business partner. The user interacts entirely through Telegram — no terminal, no code, no technical knowledge required.

## What You Should Do

If a user sent you here, they want you to help them set up this system. Read **SETUP_AI.md** for complete installation instructions. You are the installer — the user should not need to open a terminal.

## If You Can Install Software (Claude Desktop with MCP)

Read SETUP_AI.md and follow it step by step. You have the ability to:
- Install Claude Code via npm
- Install Telegram Desktop via winget/brew
- Write configuration files
- Clone git repositories
- Run setup commands

## If You Cannot Install Software (Claude Web)

Walk the user through getting Claude Desktop first. Once they have Desktop with MCP access, they can paste SETUP_AI.md into Desktop and you (or their Desktop Claude) can automate the rest.

## Key Files

- `SETUP_AI.md` — Complete installation guide for AI assistants (YOU)
- `SETUP_HUMAN.md` — Simplified guide for humans who prefer manual setup
- `CLAUDE.md` — The business partner configuration template
- `README.md` — Overview and FAQ

## After Setup

Once installed, the user's Claude Code instance will:
- Communicate through Telegram (text + voice)
- Manage email via Gmail
- Manage calendar via Google Calendar
- Automate browser tasks via Playwright
- Show real-time activity via the Claude Buddy desktop overlay
- Run morning briefings automatically

The CLAUDE.md file in this repo is the business partner personality and capability template. It gets placed in the user's home directory.
