---
name: episode-research
description: Research a podcast case or topic and produce a structured episode brief with sources, timeline, suspects, outline, and open questions
triggers:
  - "research a case"
  - "find a new case"
  - "research this"
  - "give me something to research"
  - "episode research"
  - "what should I cover next"
  - "research brief for"
  - "find sources for"
  - "is this a good episode topic"
  - "help me research"
tools: [WebSearch, WebFetch, Read, Write]
---

# Episode Research Skill

## Purpose
Research a case or topic end-to-end and deliver a podcast-ready episode brief. This skill powers the Podcast Research Agent artifact and can also be invoked directly via `/research`.

## Output Deliverables
Every research run produces:
1. **Source list** — news, court docs, Wikipedia, books, and podcasts with relevance scores
2. **Episode outline** — 6-act structure with timestamps and talking points
3. **Case timeline** — chronological events in order
4. **Open questions** — unresolved threads worth investigating before recording
5. **Podcast potential score** — 1–10 rating based on narrative strength, source depth, and audience appeal

## Research Process

### Step 1 — Source Discovery
Search across source types in priority order:
- **News archives**: AP, local outlets, national papers covering the case
- **Court documents**: FOIA releases, trial transcripts, grand jury findings
- **Wikipedia / encyclopedias**: overview, key figures, linked sources
- **Books**: true crime titles, journalism, investigative accounts
- **Podcasts**: prior coverage, angles already explored

For each source capture: title, publication/outlet, date, a 1–2 sentence snippet, and an estimated relevance score.

### Step 2 — Key Player Identification
Identify and categorize:
- **Victims**: name, age, relationship to the case
- **Suspects**: named or unnamed, evidence for/against each
- **Investigators**: lead detectives, FBI agents, prosecutors
- **Witnesses**: eyewitnesses, family members, journalists
- **Other key figures**: authors, advocates, legal team members

### Step 3 — Timeline Construction
Build a chronological timeline with:
- Date/period label (can be approximate: "Oct 1989", "Week 1")
- Single-sentence event description
- Source attribution where available

### Step 4 — Episode Outline (6-Act Structure)
Structure every episode the same way:

| Act | Name | Typical timestamp | Purpose |
|-----|------|-------------------|---------|
| 1 | Cold open / hook | 0:00–2:00 | Grab the listener before they know what they're in for |
| 2 | Background / context | 2:00–7:00 | Ground the listener in place, people, and stakes |
| 3 | The crime / incident | 7:00–15:00 | What happened, chronologically, with narrative tension |
| 4 | The investigation | 15:00–22:00 | How the case unfolded, who was looked at, where it stalled |
| 5 | Suspects and theories | 22:00–27:00 | Evidence for and against each major theory |
| 6 | Legacy / where it stands | 27:00–30:00 | Current status, family impact, and a closing question |

Each act should have 3–5 specific talking points (not generic placeholders).

### Step 5 — Open Questions
Flag 4–6 unresolved questions the host should investigate further before recording. These are the threads that could break the case open or give the episode an exclusive angle.

## Podcast Potential Score
Score on a scale of 1–10 based on:
- **Narrative strength**: Is there a clear arc? A hook? Emotional stakes?
- **Source depth**: How much documented evidence exists?
- **Audience resonance**: Cold case? National profile? Ohio connection?
- **Guest potential**: Is there a detective, journalist, or family member worth pursuing?
- **Uniqueness**: Has this been done to death on other podcasts, or is it relatively fresh?

## Output Format
Present results in this order:
1. Case name + podcast potential score
2. Source list (tabular or card format)
3. Episode outline (expandable acts)
4. Case timeline
5. Open questions
6. Recommended next step (guest to pursue, document to obtain, etc.)

If the user asks, export the full brief as a .docx using the docx skill.

## Tone and Voice
Research briefs are written in a neutral, factual register. The episode outline talking points are written in Bill's voice — direct, journalistic, emotionally grounded. No hedging. No fluff. Every talking point should be something Bill could read aloud.
