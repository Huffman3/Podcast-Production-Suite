# Changelog — Podcast Production Suite

All notable changes to this project are documented here.

---

## v1.4.3 (May 21, 2026)

### ✨ New Features
- **Guest CRM Artifact** — Manage your entire guest outreach pipeline in one visual dashboard. Track contacts, next steps, follow-up dates, and interview status.
- **Improved Error Messages** — Better troubleshooting guidance when things go wrong. Clearer descriptions of what failed and how to fix it.
- **Early Adopter Lifetime Pricing** — Lock in your rate now ($29/month or $290/year). Future features won't increase your price.

### 🚀 Improvements
- **Research Command 30% Faster** — Optimized data synthesis reduces research generation time from ~60s to ~40s
- **Cleaner Dashboard Layouts** — Reorganized Production Pipeline and Research Agent for better visual hierarchy
- **Enhanced Fact-Checking** — Improved accuracy in claim verification and source attribution
- **Multi-Guest Transcript Formatting** — Better handling of episodes with multiple speakers; cleaner speaker labels and timestamps

### 🐛 Bug Fixes
- Fixed date handling in event scheduler (was incorrectly parsing dates with hyphens)
- Resolved issue with special characters (™, ®, ©) in episode titles crashing export
- Improved PDF parsing for research sources with embedded images
- Fixed plugin not loading if Claude Desktop path had spaces in it

### 📚 Documentation
- Updated INSTALLATION.md with full FAQ section
- Added system requirements (macOS 12+, Windows 10/11)
- Clarified pricing and refund policy
- Added troubleshooting section for common issues
- Highlighted early adopter lifetime pricing benefit

---

## v1.4.1 (April 15, 2026)

### ✨ New Features
- **Podcast Production Suite** — Initial public release
- **5 Slash Commands:** `/setup`, `/research`, `/transcribe`, `/check-writing`, `/newsletter`
- **10 Interactive Dashboards:** Suite Hub, Production Pipeline, Podcast Research Agent, Guest CRM, Anti-AI Checker, Marketing Newsletter, Episode Performance, Monthly Revenue, Sponsorship Tracker, Setup Wizard
- **6 Built-in Skills:** Case tracking, guest outreach, fact-checking, transcription, research synthesis, content repurposing

### 🎯 Included from Start
- Case research with sources and timeline
- Script fact-checking and AI language detection
- Guest outreach email drafting
- MP3 to transcript conversion
- Show notes and newsletter generation
- Episode performance tracking
- Revenue and sponsorship management

---

## Roadmap (Coming Soon)

- **Mobile App** — Claude plugin on Claude iOS/Android app
- **Team Licensing** — Discount pricing for multiple team members
- **Discord Community** — User community server for tips and feedback
- **Custom Workflows** — Ability to create and save your own custom commands
- **API Access** — Programmatic access for integration with other tools
- **Advanced Analytics** — Listener demographics, download trends, revenue forecasting
- **Video Transcription** — Support for video episodes (YouTube, etc.)
- **Multi-Language Support** — Translations for non-English podcasts

---

## How to Update

Updates are automatic. When you open Claude with the plugin installed, you'll get the latest version.

To check your version:
1. Type `/setup` in Claude
2. Look for "Version X.X.X" at the top of the Suite Hub
3. Current version is **v1.4.3**

---

## Report Issues

Found a bug? Have a feature request? Email: support@sloburnmedia.com

Include:
- Your operating system (Mac/Windows)
- Your Claude Desktop version
- What you were doing when the issue happened
- Screenshot if possible

---

© 2026 Slo Burn Media LLC
