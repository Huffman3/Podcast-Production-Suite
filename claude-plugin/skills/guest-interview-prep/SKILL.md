---
name: guest-interview-prep
description: >
  Researches and prepares a formatted .docx guest interview prep packet for Who Killed…? podcast episodes. Use this skill whenever Bill needs to prepare for an upcoming guest interview — regardless of guest type. Triggers on phrases like "prep me for an interview with", "I'm interviewing [name]", "guest interview prep", "help me prep for [name]", "who am I talking to", "what should I ask [guest]", "interview questions for", "I have [name] coming on", or any mention of an upcoming guest by name plus their connection to a case. Always use this skill rather than generating ad hoc questions — it produces a structured, research-backed prep packet tailored to the guest type and case.
---

# Guest Interview Prep — Who Killed…?

Produces a polished, podcast-ready interview prep packet as a .docx file. Input is minimal: guest name + their connection to the case.

---

## Step 1: Identify Guest Type

Based on the guest's connection to the case, classify them into one of these categories — this determines question tone and structure:

| Type | Examples |
|---|---|
| **Detective / Law Enforcement** | Lead investigator, retired detective, FBI agent |
| **Family Member / Victim Advocate** | Parent, sibling, close friend, advocate org rep |
| **Journalist / Author** | True crime writer, investigative reporter, book author |
| **Forensic Expert / Academic** | Profiler, DNA analyst, criminologist, medical examiner |
| **Fellow Podcaster** | True crime host, investigative podcast producer |
| **Other** | Tipster, neighbor, witness, community member |

---

## Step 2: Web Research

Use web search to build a research brief on the guest. Gather:

- **Bio**: Full name, current role/title, career background
- **Case connection**: How and when they got involved with this specific case
- **Prior coverage**: Interviews, articles, books, podcast appearances — especially anything that touches *this* case
- **Public positions**: What have they said publicly about the case? Any stated theories, criticisms of the investigation, or notable claims?
- **Potential landmines**: Controversies, past statements that conflict with known facts, anything sensitive

Search queries to run (adapt to guest):
- `"[Guest Name]" [Case Name]`
- `"[Guest Name]" interview OR podcast OR article`
- `"[Guest Name]" [role/title]`

Flag any information gaps — if something is missing from public record, note it explicitly in the brief.

---

## Step 3: Build Question Set

Tailor question organization to guest type. Bill's style is **conversational — let the guest lead** — so questions are open-ended, non-leading, and designed to open doors rather than extract specific answers.

**Universal openers (use one, adapt to guest):**
- "How did you first come across this case?"
- "Tell me how you got involved."
- "What was your first impression when you heard about [victim]?"

**By guest type:**

### Detective / Law Enforcement
Organize: *How they came to the case → what they found → what frustrated them → what they wish had been done differently → where it stands now*
- Avoid yes/no on open investigations
- Focus on process, not conclusions
- Good closing: "If you could go back and change one thing about how this was handled, what would it be?"

### Family Member / Victim Advocate
Organize: *Who the victim was as a person → the impact of the loss → experience with investigators → what justice looks like to them*
- Lead with humanity, not case facts
- Don't push on grief — if they go there, follow; if not, don't force it
- Good closing: "What do you want people to remember about [victim]?"

### Journalist / Author
Organize: *What drew them to the case → what their research uncovered → what surprised them → what the public gets wrong → what's next*
- Ask about sources and access — what doors opened, what doors didn't
- Good closing: "What's the one thing you found that you still can't explain?"

### Forensic Expert / Academic
Organize: *Their specialty and how it applies → what the evidence in this case tells them → what's missing or degraded → what modern methods could add*
- Ask for plain-language explanations of technical points
- Good closing: "If this case were reopened today with current technology, what's the first thing you'd test?"

### Fellow Podcaster
Organize: *How they found the case → what angle they took → what their listeners responded to → what they learned that surprised them*
- Collegial tone — peer conversation, not interview
- Good closing: "What do you think we as true crime podcasters get wrong about cases like this?"

### Core question bank (use across types, adapt as needed):
1. Walk me through the timeline as you understand it.
2. What's the thing investigators got right that doesn't get enough credit?
3. What's the theory you keep coming back to — and why?
4. What piece of evidence do you think has been overlooked?
5. Is there anyone you wish had been looked at harder?
6. What's your relationship with the [family / investigators / other parties] like now?
7. Where does this case stand today, in your view?
8. What would it take to solve this?

---

## Step 4: Build the .docx Prep Packet

Read `/mnt/skills/public/docx/SKILL.md` before writing any code.

### Document Structure

```
[GUEST NAME] — Interview Prep
Who Killed…? | [Date if known, otherwise omit]

─────────────────────────────

SECTION 1: BIO SUMMARY
  Quick snapshot: name, role, case connection, why they matter to this episode.
  3–5 sentences max. This is the "30 seconds before you hit record" reminder.

SECTION 2: RESEARCH BRIEF
  Full research findings. Organized as:
    — Background (career, relevant expertise)
    — Case involvement (how, when, what they've said publicly)
    — Prior coverage (links or descriptions of notable interviews/articles/books)
    — Potential landmines (flagged clearly)
    — Open questions / gaps in public record

SECTION 3: QUESTION SET
  Organized per guest type (see Step 3).
  Format:
    OPENER
    [question]

    CORE QUESTIONS
    [numbered list]

    FOLLOW-UPS TO WATCH FOR
    [2–3 situational follow-ups, e.g., "If they mention X, ask Y"]

    CLOSING
    [closing question]
```

### Styling notes
- Clean, minimal formatting — this is a working document, not a presentation
- Guest name and show name in header
- Section headers bold, clearly separated
- Question set uses numbered list (docx numbering config, not unicode bullets)
- No color flourishes — black and white, readable at a glance
- US Letter, 1-inch margins, Arial 12pt

---

## Step 5: Output

Save to `/mnt/user-data/outputs/[GuestLastName]_InterviewPrep.docx` and present to Bill.

Close with a 2–3 sentence verbal summary: who the guest is, what angle to push on, and one thing to watch out for.
