# SAM Onboarding Email Template

**Subject:** Your AI Business Partner is Ready to Set Up

---

Hey Darleen,

Jereme set something up for you -- it's an AI business partner that you can talk to through Telegram. It manages your email, calendar, content, and daily tasks. You just text it or send it a voice message and it handles the rest.

It takes about 15 minutes to set up. Here's everything you need to do.

---

**STEP 1: Activate Your Free Claude Account**

Click this link to get 7 days of Claude Pro for free (no charge during the trial):

https://claude.ai/referral/oAYebqM6kw

If you already have a Claude account (even a free one), just sign in with that same account. The guest pass will upgrade it to Pro for 7 days. If you don't have an account yet, it will walk you through creating one. Either way, it will ask for a credit card but you will NOT be charged during the 7 days. If you decide you don't want to keep it after the trial, just cancel before the 7 days are up.

---

**STEP 2: Download Claude Desktop**

This is the app that will help you get everything else set up. Download it here:

https://claude.ai/download

Install it and sign in with the account you just created in Step 1.

---

**STEP 3: Download Telegram**

This is how you'll talk to your AI partner -- like texting a friend.

- **On your phone first:** Download Telegram from the App Store (iPhone) or Google Play (Android). Open it and sign up with your phone number. This takes about 1 minute.
- **Then on your computer:** Download Telegram Desktop from https://desktop.telegram.org. When you open it, it will show you a QR code on screen. Open Telegram on your phone, go to Settings > Devices > Link Desktop Device, and point your phone camera at the QR code. That links them together.

You need Telegram on your phone AND your computer for the setup.

---

**STEP 4: Let Claude Set Everything Up**

This is the easy part. Open Claude Desktop on your computer and copy-paste EVERYTHING between the two lines that say "COPY START" and "COPY END" below into the chat:

--- COPY START ---

Hi Claude. I need you to help me set up the SAM AI Business Partner. You are my installer -- I should not need to open a terminal or do anything technical. Walk me through everything in plain language.

Here are the full setup instructions. Please follow them step by step:

Here is the full list of things to install, in order. Handle each one silently and only ask me if something needs my input.

1. PREREQUISITES: Check if these are installed and install any that are missing: Node.js (winget install OpenJS.NodeJS.LTS), Python (winget install Python.Python.3.11), Git (winget install Git.Git), and FFmpeg (winget install Gyan.FFmpeg). These are needed for everything else to work.

2. CLAUDE CODE: Install with "npm install -g @anthropic-ai/claude-code".

3. TELEGRAM BOT: I already have Telegram installed. Walk me through creating a bot -- tell me to open Telegram, search for @BotFather, send /newbot, and guide me step by step. When I get the token, I'll paste it here for you. Then set up the Telegram plugin in Claude Code with my bot token.

4. GOOGLE WORKSPACE: Install gog.exe for Gmail and Calendar access. Walk me through the Google sign-in when the browser opens. IMPORTANT: Tell me to sign in with my MAIN Google account -- the one I use for my primary email and calendar. Not a secondary or old account.

5. VOICE TOOLS: Run "pip install edge-tts" and "pip install openai-whisper". The default voice should be en-GB-RyanNeural for all voice replies.

6. WINDOWS MCP: Install the Windows MCP server so the AI can interact with my desktop when needed.

7. CLAUDE.MD: Download the business partner configuration from https://raw.githubusercontent.com/ajsupplycollc/sam-starter-kit/master/CLAUDE.md and save it to my home directory (C:\Users\[my username]\CLAUDE.md on Windows).

8. CLAUDE BUDDY: Clone the desktop companion from https://github.com/ajsupplycollc/claude-buddy, run npm install, and configure the PostToolUse hook in Claude Code settings.

When everything is installed, test it by having me send a message to my new Telegram bot.

IMPORTANT RULES FOR YOU: Do not show me terminal output. Do not use technical jargon. Explain everything like I've never used a computer before. If something fails, fix it yourself or explain exactly what to click. Do not skip testing.

--- COPY END ---

Claude will take it from there. It will:
- Install what's needed on your computer
- Ask you to approve a couple of permissions (just click "Allow")
- Walk you through creating your Telegram bot (takes 2 minutes -- you just copy and paste one code)
- Ask you to sign into your Google account for email and calendar access (use your MAIN Google account -- the one with your primary email and calendar)
- Test everything to make sure it works

When it's done, you'll have a bot on Telegram that you can talk to anytime.

**PRO TIP: Use voice messages instead of typing.** In Telegram, hold down the microphone button and just talk. Slide up to lock it so you can talk hands-free. Your AI partner understands voice messages and responds with voice notes back. This is the best way to use it -- just talk naturally like you're on the phone with an assistant. Don't worry about being perfect. Just say what you need and your AI will figure out the rest.

Try it now -- send a voice message saying:
- "Hey, can you check my email?"
- "What do I have going on today?"
- "Remind me to call the dentist tomorrow at 2pm"

---

**WHAT YOUR AI PARTNER CAN DO**

Now that you're set up, here's what you can ask it to do -- just by texting or voice messaging on Telegram:

- **Email:** "Check my email" / "Reply to that email from Sarah" / "Draft an email to my client about the project update"
- **Calendar:** "What's on my schedule today?" / "Set a meeting for Thursday at 3pm" / "Remind me to follow up with Carlos tomorrow"
- **Research:** "Look up the best CRM software for small businesses" / "What are the top competitors in my area?"
- **Content:** "Write me an Instagram caption for this project photo" / "Draft a proposal for a new client"
- **Daily Briefing:** Every morning, just say "What do I need to know today?" and it'll check your email and calendar and give you a summary
- **General Help:** "Help me write a reply to this customer complaint" / "What should I charge for this service?"

Think of it like a business partner who's always available, never sleeps, and remembers everything you've talked about.

**POWER TIPS -- Things Most People Don't Realize They Can Do**

- **Set up recurring tasks:** Just say "Every morning at 8am, check my email and send me a summary." Your AI will set that up automatically. You don't need to know how it works -- just tell it what you want to happen and when.
- **Automate repetitive work:** If you find yourself doing the same thing over and over (like sending the same type of email, or checking the same website), just say "Can you do this for me automatically from now on?" and your AI will figure out how.
- **Running checks on repeat:** Say "Every hour, check if I got a reply from Sarah and let me know." Your AI will keep checking until it finds what you're looking for.
- **Ask it to remember things:** "Remember that my supplier's number is 555-1234" or "Remember that I charge $50/hour for consultations." It keeps track so you don't have to.
- **Let it think for you:** Instead of figuring out what to do next, just describe your situation: "I have a client who's unhappy about the timeline. What should I do?" Your AI will think through the options and give you a recommendation.

The key is: **just talk to it like a person.** You don't need special words or commands. If you can explain it to a friend, you can explain it to your AI.

---

**IF YOU GET STUCK**

Don't stress. Just open Claude Desktop and describe what happened. Claude can diagnose and fix most issues. You can also show Claude this email and say "I'm stuck at Step [X], can you help?"

If you're really stuck, text Jereme.

---

That's it. Welcome to the future of running your business.

-- Jereme / Strange Advanced Marketing
