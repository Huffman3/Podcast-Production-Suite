# Podcast Production Suite — Installation & Setup

Welcome to the **Podcast Production Suite** for Claude. This guide will get you up and running in 5 minutes.

---

## What You Got

A complete plugin with:
- **5 commands** (`/setup`, `/transcribe`, `/check-writing`, `/research`, `/newsletter`)
- **10 interactive artifacts** (dashboards, trackers, analyzers)
- **6 built-in skills** (case tracking, guest outreach, fact-checking, transcription, research, marketing)

Everything is designed for solo podcast producers, especially true crime shows.

---

## Installation

### Step 1: Unzip the Plugin
After purchasing, you'll receive `podcast-production-suite-v1.4.1.plugin`. This is already zipped.

In Claude (claude.ai or the Claude app):
1. Go to **Settings** → **Plugins**
2. Click **Add Plugin**
3. Select the `.plugin` file you downloaded
4. Click **Install**

Claude will automatically extract and register all commands, artifacts, and skills.

### Step 2: Verify Installation
In Claude, type:
```
/setup
```

You should see a guided overview of all tools in the suite. If this loads, you're good to go.

---

## Quick Start: Your First Command

### Try `/setup` (2 min)
```
/setup
```
This walks you through every tool and when to use it.

### Try `/transcribe` (5 min)
Drop in an MP3 file and get a timestamped transcript:
```
/transcribe
```
The plugin will ask for the episode name and guest info, then produce a .docx.

### Try `/check-writing` (3 min)
Paste any text you've written (script draft, show notes, social post):
```
/check-writing
```
The plugin checks for AI-sounding language and rewrites it to sound like you.

---

## Your Main Commands

| Command | What It Does | Use When |
|---------|--------------|----------|
| `/setup` | Tour of all tools | First time, or need a refresher |
| `/transcribe` | MP3 → timestamped .docx | You have a guest interview or audio to document |
| `/check-writing` | Audit text for AI language | You've written a draft and want it to sound human |
| `/research` | Research a case + produce brief | You're developing a new episode |
| `/newsletter` | Turn episode into email | You're promoting a new episode to subscribers |

---

## Artifacts vs. Skills: How They Work Together

This plugin has two layers: **Procedural Skills** (commands you run) and **Visual Artifacts** (dashboards you explore).

### When to Use Commands (Skills)
Commands are fast, procedural workflows. Type `/command` and follow the steps to get a .docx output.

**Use a command when you want to:**
- Get something done quickly (research a case, transcribe an interview, write an email)
- Output a file you can save and edit
- Follow a guided workflow with clear next steps

**Example:** `/research` → research a new case → get a structured .docx brief in 10 minutes

### When to Use Artifacts (Dashboards)
Artifacts are interactive visual tools for managing your workflow. Click into them, explore visually, make decisions.

**Use an artifact when you want to:**
- See your entire pipeline at once (cases, revenue, outreach, episode performance)
- Visually organize or track something
- Reference data without running a command
- Manage a complex project state

**Example:** Open **Production Pipeline** artifact → see all cases from idea to published → drag to update status → see what's ready to record

### Real Example: Research Workflow

Here's how commands and artifacts work together in practice:

**Day 1: Research a new case**
- Type `/research`
- Follow the steps (case name, initial sources, suspects)
- Get a .docx research brief → save it
- Update your case status in the **Production Pipeline** artifact

**Day 7: Review all active research**
- Open **Podcast Research Agent** artifact
- Visually see all cases you're investigating
- Check progress on each → organize by priority
- Click into a case to dive deeper

The skill (`/research`) *creates*. The artifact (**Podcast Research Agent**) *manages and visualizes*.

---

## Your Main Artifacts (Dashboards)

Click any of these in Claude to open them:

- **Production Pipeline** — Track every case from idea to published
- **Podcast Research Agent** — Visual command center for your research workflow. Manage investigations, organize findings, see all active research at a glance
- **Guest CRM** — Manage your outreach pipeline (who you've contacted, next steps)
- **Anti-AI Checker** — Paste text, get a "Human Score" showing how AI-sounding it is
- **Marketing Newsletter** — Build a subscriber email from an episode
- **Episode Performance** — See how each episode is performing
- **Monthly Revenue Chart** — Track sponsorship revenue month by month
- **Sponsorship Tracker** — Log ad deals and invoice deadlines
- **Suite Hub** — Command center for all tools (live data dashboard)

---

## Common Questions

### Q: Do I need to do anything after installation?
**A:** No. Run `/setup` once to see all the tools, then start using commands as you need them.

### Q: Can I use this on mobile?
**A:** Yes, if you're using the Claude mobile app. All commands and artifacts work on phone/tablet.

### Q: What happens if I have a problem?
**A:** Each command has built-in guidance. If something doesn't work, try:
1. Run `/setup` to see what you're supposed to do
2. Check that you've provided the right inputs (e.g., paste text before running `/check-writing`)
3. If still stuck, paste the error message in chat and I'll help troubleshoot

### Q: Can I use this for a different podcast (not true crime)?
**A:** Absolutely. The tools are generic podcast production tools. Some language is tuned to true crime, but they work for any solo-host podcast.

### Q: What if I want to customize something?
**A:** You can ask me to modify any command or skill. For example: "Make /newsletter tone more formal" or "Add a command to track listener growth."

---

## Support & Feedback

This plugin was built by **Slo Burn Media** with over 5 years of podcast production experience.

- **Questions?** Ask in Claude and I'll help
- **Feature request?** Describe what you want, and I can build it
- **Bug report?** Tell me what went wrong and what you were doing

---

## What's Inside (Technical)

If you're curious about the structure:
- `/commands` — The 5 main commands
- `/artifacts` — 10 HTML interactive tools
- `/skills` — 6 reusable skill modules
- `/plugin.json` — Plugin metadata (version, keywords, description)
- `README.md` — High-level overview

You don't need to edit anything. Just use the commands.

---

## Version
**Podcast Production Suite v1.4.1** — May 2026

Built for Claude. Works in claude.ai and the Claude app.

© 2026 Slo Burn Media LLC. Licensed under MIT.
