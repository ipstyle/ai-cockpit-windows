# AI Cockpit: AI Usage Monitor — Windows downloads

*[Deutsch](README.de.md)*

All your AI limits in one place, in the notification area of the taskbar —
Claude, ChatGPT/Codex, the OpenAI and Anthropic APIs, Kimi K3, OpenRouter,
Grok (xAI), GitHub Copilot, DeepSeek, and your running Claude Code sessions.
Nine services, up to eleven cards — Claude counts twice if you keep a second account.

This is the Windows edition of [AI Cockpit for macOS](https://apps.apple.com/app/id6802014255).
It is **free**.

**This repository carries the downloads and nothing else.** There is no source
code here: it is shared with the macOS edition and stays closed.

## Download

**[→ Latest release](../../releases/latest)**

| File | For |
|---|---|
| `AI-Cockpit-<version>-win-x64.exe` | ordinary Windows PCs |
| `AI-Cockpit-<version>-win-arm64.exe` | Windows on ARM — Snapdragon machines, and Windows VMs on Apple-silicon Macs |

Each file is self-contained; the .NET runtime does not need to be installed.

### Windows will warn you

The files are not signed with a code-signing certificate — one costs several
hundred francs a year, which I do not carry for a free app. SmartScreen
therefore says **"Windows protected your PC"**.

To run it anyway: **More info** → **Run anyway**.

If you would rather check first, every release ships a `.sha256` file next to
the executable:

```
certutil -hashfile AI-Cockpit-1.7.0-win-arm64.exe SHA256
```

The warning says nothing about the contents, only about how widespread the file
is, and it disappears once enough people have downloaded it. Note that some
managed company machines block unsigned executables outright — there no click
helps.

## What's new in 1.7

The full list is in the release notes; the headlines (the features of the Mac app 7.3 and 7.4):

- **No surprises** — a notification when a window resets ahead of schedule,
  and a cost alert when OpenRouter, DeepSeek or Kimi credit drops fast or
  OpenAI/Anthropic daily costs jump.
- **Plan check** — the API value of your Claude Code use against your plan
  price, plus a check from your weekly peaks ("Max 5× would likely do").
- **For developers** — optional status for Claude Code's status line
  (`stand.json` + `statusline.ps1`, off by default, no keys or account names),
  and a «Claude is done» notification.
- **Clarity** — one sentence on where you stand at the top of the panel, a tip
  which account or service still has room, and (i) buttons that explain the terms.
- **Your look** — color schemes Graphite (new default), Deep Blue and Classic,
  a color per subscription, and «Share as image» with account names hidden.

## Early builds

The current release **has never been run.** It is built and compiled on a Mac,
where WPF does not run. What is verified is everything that can be verified
without a running program: the whole solution compiles including XAML, 1506
core tests pass, and a differential tool proves the Windows core computes byte
for byte what the macOS core computes.

**Everything visible is unverified.** Read the release notes before you start
it — they list what that means in practice.

The fastest way to an impression: start it, then pick **See the demo** in the
setup assistant, or later Settings → Accounts → Demo mode. Every card fills
with sample figures without a single credential.

If something stays empty: Settings → Diagnostics → **Generate report**. The text
says what state each card is in and contains no key of any kind.

## What it needs

- Windows 11, x64 or arm64. Windows 10 is untested.
- No system permissions: no sandbox, no accessibility access.
- Credentials live in Windows Credential Manager, encrypted with your user
  account and only on that machine. There is no server, no account with the
  publisher, no analytics.

## Support and feedback

Questions, problems or feature requests: **[aicockpit.info](https://aicockpit.info)**
— the project's home for all four platforms (Mac, iPhone/iPad/Apple Watch and
Windows), with a feedback form. Bug reports for this edition specifically can
also go through this repository's issues.

## Not affiliated

AI-Cockpit is an independent app and is not affiliated with Anthropic, OpenAI,
Moonshot AI, OpenRouter, xAI, GitHub or DeepSeek. Those names appear solely to describe
which services the app can read.
