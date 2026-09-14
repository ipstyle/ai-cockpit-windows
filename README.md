# AI Cockpit: AI Usage Monitor — Windows downloads

*[Deutsch](README.de.md)*

All your AI limits in one place, in the notification area of the taskbar —
Claude, ChatGPT/Codex, the OpenAI and Anthropic APIs, Kimi K3, OpenRouter,
Grok (xAI), GitHub Copilot, and your running Claude Code sessions. Eight
services, up to ten cards — Claude counts twice if you keep a second account.

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
certutil -hashfile AI-Cockpit-1.3.0-win-arm64.exe SHA256
```

The warning says nothing about the contents, only about how widespread the file
is, and it disappears once enough people have downloaded it. Note that some
managed company machines block unsigned executables outright — there no click
helps.

## What's new in 1.3

This is a snapshot release, aimed at feature parity with macOS 6.5 — not a
running twin of it. The full list is in the in-app changelog; the headlines:

- **GitHub Copilot** as an eighth service, with its own card — premium
  requests this month, covered by the plan, billed extra. Personal paid plans
  only; an organization or enterprise seat cannot be told apart from "nothing
  used yet" on GitHub's side, so the card says so plainly instead of guessing.
- **ChatGPT sign-in inside the app**, with live quota and a credit balance —
  no more relying solely on the local Codex installation.
- **Provider status.** A card whose provider is down shows a line with a link
  to the status page, and a coloured dot on the tray icon flags it even with
  the panel closed.
- **A total-cost line** — subscription fees plus the running API costs, one
  figure above the cards.
- **A segment switch** above the cards (all / limits / cost / sessions).
- **No more dead "Retry".** A rejected key or expired sign-in now points
  straight at the right settings page instead of a button that never helps.
- **Demo mode is complete** — sample sessions, a sample ChatGPT balance and a
  Kimi quota are included; it no longer leaks your real, local Claude Code
  sessions while turned on.
- Every provider colour re-measured against macOS 6.5, plus a colour for
  Copilot.

## Early builds

The current release **has never been run.** It is built and compiled on a Mac,
where WPF does not run. What is verified is everything that can be verified
without a running program: the whole solution compiles including XAML, the
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
Moonshot AI, OpenRouter, xAI or GitHub. Those names appear solely to describe
which services the app can read.
