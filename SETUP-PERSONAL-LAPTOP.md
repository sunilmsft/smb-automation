# Personal Laptop Setup Guide

> Step-by-step instructions to continue working on the SMB Automation project from a personal laptop.

---

## Prerequisites

You need three things installed:

### 1. Visual Studio Code (Free)
- Download: https://code.visualstudio.com
- Install with default settings
- Windows, Mac, or Linux all work

### 2. Git (Free)
- Download: https://git-scm.com
- During install, accept all defaults
- After install, open a terminal and configure your identity:
  ```
  git config --global user.name "Your Name"
  git config --global user.email "your-email@example.com"
  ```

### 3. GitHub Copilot Extension
- Open VS Code
- Go to Extensions (Ctrl+Shift+X)
- Search for **"GitHub Copilot"**
- Click Install (it will also install "GitHub Copilot Chat")
- Sign in with your GitHub account when prompted

---

## GitHub Copilot Plans & Costs

| Plan | Price | What You Get |
|------|-------|-------------|
| **Free** | $0/mo | 2,000 code completions + 50 chat messages/month (limited models) |
| **Pro** | $10/mo | Unlimited completions + unlimited chat (GPT-4o, Claude Sonnet) |
| **Pro+** | $39/mo | Everything in Pro + premium models (Claude Opus, etc.) |

**Recommendation:** Start with **Pro ($10/mo)** — it's unlimited chat and completions, which is all you need for this project. Upgrade to Pro+ later if you want access to the most advanced models.

Sign up at: https://github.com/features/copilot

---

## Opening the Project

### Option A: OneDrive (Easiest — No Setup)
Since the project folder lives on your personal OneDrive, it should already be syncing:

1. Sign into OneDrive on your personal laptop (if not already)
2. Wait for sync to complete
3. Open VS Code
4. File → Open Folder → navigate to:
   ```
   OneDrive\GitHub Copilot Fun Projects\Tim and Sunil building Stuff!
   ```
5. Done — all files including git history are already there

### Option B: Git Clone (If OneDrive isn't set up)
If you'd rather clone fresh from GitHub:

1. Open a terminal (PowerShell on Windows, Terminal on Mac)
2. Navigate to where you want the project:
   ```
   cd ~\Documents
   ```
3. Clone the repo:
   ```
   git clone https://github.com/sunilmsft/smb-automation.git
   ```
4. Open it in VS Code:
   ```
   cd smb-automation
   code .
   ```

---

## Verify Everything Works

Once the project is open in VS Code:

1. **Check the file tree** — you should see:
   - `index.html` (the main dashboard — ~2,000 lines)
   - `context.md` (project context)
   - `memory.md` (conversation/decision log)
   - `.github/copilot-instructions.md` (Copilot reads this automatically)

2. **Open Copilot Chat** — press `Ctrl+Shift+I` (or click the Copilot icon in the sidebar)
   - Ask it: "What is this project about?"
   - It should know — because it reads `.github/copilot-instructions.md` automatically

3. **Test Live Preview** — right-click `index.html` → "Open with Live Server" (install Live Server extension if you want local preview), or just open the file directly in a browser

4. **Test Git** — in the terminal:
   ```
   git status
   git log --oneline -5
   ```
   You should see recent commits

---

## Pushing Changes to GitHub

When you make edits and want them to go live on GitHub Pages:

```
git add -A
git commit -m "Your commit message here"
git push
```

**Note:** `git push` may show an error that looks like exit code 1 — this is normal (stderr output). The push still succeeds. Check https://sunilmsft.github.io/smb-automation/ to confirm.

If this is a fresh clone, you may need to authenticate with GitHub first:
- Install GitHub CLI: https://cli.github.com
- Run: `gh auth login`
- Follow the prompts to authenticate with your GitHub account

---

## What Carries Over vs. What Doesn't

| Item | Carries Over? | How |
|------|:---:|---|
| All code (index.html, etc.) | ✅ | OneDrive sync or git clone |
| Project context | ✅ | `.github/copilot-instructions.md` — Copilot reads this automatically |
| Decision history | ✅ | `memory.md` and `context.md` in the repo |
| Git history | ✅ | Full commit history comes with the repo |
| Live site | ✅ | GitHub Pages stays live at the same URL |
| Chat conversation history | ❌ | Stored locally on the work laptop — not in the repo |
| Copilot memory/preferences | ❌ | Per-device; but `copilot-instructions.md` replaces most of this |

**Bottom line:** The only thing you lose is the scrollback of past chat conversations. But all the decisions, code, and context are preserved in the repo files. Copilot will pick up the project context automatically from `copilot-instructions.md`.

---

## Quick Reference

| Resource | Link |
|----------|------|
| Live Dashboard | https://sunilmsft.github.io/smb-automation/ |
| GitHub Repo | https://github.com/sunilmsft/smb-automation |
| VS Code Download | https://code.visualstudio.com |
| Git Download | https://git-scm.com |
| GitHub Copilot Plans | https://github.com/features/copilot |
| GitHub CLI | https://cli.github.com |
