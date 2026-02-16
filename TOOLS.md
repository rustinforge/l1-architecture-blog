# TOOLS.md - Local Notes

## GitHub

- **Username**: rustinforge
- **CLI**: gh (authenticated)
- **Token**: Configured in ~/.config/gh/hosts.yml

## AgentMail

- **API Key**: Configured in gateway (redacted in logs)
- **Primary Inbox**: confidentarmy559@agentmail.to
- **SDK Location**: /home/openclaw/.openclaw/workspace/node_modules/agentmail
- **Skill**: /home/openclaw/.openclaw/workspace/skills/agentmail

Usage:
```javascript
const skill = require('./skills/agentmail');
await skill.sendEmail({ to: ['email@example.com'], subject: 'Hi', text: 'Body' });
await skill.pollMessages('confidentarmy559');
```

## Browser

- **Engine**: Puppeteer with Chromium (headless)
- **Executable**: /usr/bin/google-chrome
- **Default args**: --no-sandbox --disable-setuid-sandbox
- **Skill**: /usr/lib/node_modules/openclaw/skills/browser
- **Note**: Browser tool (Chrome extension relay) not connected; use Puppeteer exec instead

Quick test:
```javascript
const puppeteer = require('puppeteer');
const browser = await puppeteer.launch({ headless: 'new', args: ['--no-sandbox'] });
```

## Environment

- **Node**: v22.22.0
- **npm**: 10.9.4
- **git**: 2.43.0
- **gh**: 2.86.0 (GitHub CLI)
- **GPG Key ID**: C86C44D24433D987C1E4ECBCC2915D856F6AD9E1 (for verified commits)

## Available Skills (52 installed)

- github, coding-agent, weather, browser, tmux, healthcheck, clawhub, discord, slack, notion, obsidian, spotify-player, and 40+ more

## Coding Agents

- **opencode** - Installed at /home/openclaw/.opencode/bin/opencode
- **codex** - Not installed
- **claude** - Not installed

Free models available:
- opencode/big-pickle
- opencode/gpt-5-nano
- opencode/kimi-k2.5-free
- opencode/minimax-m2.5-free

---

Add whatever helps you do your job. This is your cheat sheet.
