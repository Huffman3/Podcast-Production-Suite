---
name: fact-check-script-skill
description: Fact-checks any script for factual accuracy, source attribution, and brand voice consistency. Use this skill whenever Bill (or any user) needs to verify claims in a script, audit tone against brand guidelines, identify narrative gaps, or prepare a script for production. Triggers on phrases like "fact-check this script", "verify these claims", "check my script", "is this accurate", "audit this for voice", "fact-check before we record", or any request to validate or improve script accuracy and consistency. Always use this skill for scripts requiring verification — even casual requests like "does this look right?" — rather than doing ad hoc fact-checking.
---

# Fact-Check Script Skill

Fact-checks scripts for accuracy, source attribution, voice consistency, and narrative coherence. Outputs a working document (.docx) with extracted claims, verification status, voice audit results, narrative gaps, and suggested fixes.

## How It Works

### Input
- Script text (any domain: true crime, marketing, documentary, social, etc.)
- Optional: Known sources you've already gathered

### Process

1. **Claim Extraction** — Parses the script and identifies every factual statement (dates, names, places, statistics, attributions, events)
2. **Auto-Verification** — Web-searches each claim to verify accuracy, find contradictions, or flag unclear statements
3. **Voice Audit** — If true crime: checks against *Who Killed?* brand guidelines (forbidden words/phrases, sentence patterns, tone consistency). For other domains: applies general copywriting standards
4. **Narrative Check** — Identifies logical gaps, redundancies, flow issues, or missing context
5. **Suggested Rewrites** — Proposes fixes for unsourced, muddled, or inconsistent claims

### Output Format
A .docx **working document** (conversational, not formal) including:
- **Flagged Claims** table with verification status (✓ verified | ⚠ needs source | ✗ contradicted | ? unclear)
- **Search Results & Sources** — What was found (or not found) for each claim
- **Voice Audit Results** — Tone issues, forbidden words/phrases, sentence structure notes
- **Narrative & Logic Issues** — Gaps, redundancies, flow problems
- **Suggested Rewrites** — Options for problematic claims
- **Working Notes Section** — Space for your decisions/comments

## Usage

### Basic Fact-Check
```
Fact-check this script: [paste script text]
```

### Fact-Check + Voice Audit (True Crime)
```
Fact-check this Who Killed? script: [paste script text]
```
(Voice audit triggers automatically if the script is true crime)

### Custom Domain Voice Audit
```
Fact-check this script for [marketing/documentary/social/etc.] voice: [paste script text]
Note: [any specific tone/style rules to check]
```

## What Gets Checked

### Factual Claims
- Dates, names, locations, statistics
- Historical events, case details, attributions
- Any statement that can be verified or contradicted

### Voice Consistency (True Crime)
- Forbidden words: *delve, leverage, harness, robust, landscape, utilize, realm, transformative, game-changer, seamless, testament*
- Forbidden phrases: "It's important to note," "In today's digital age," "Furthermore," "In conclusion," "Let that sink in," "At the end of the day"
- Sentence variety (not starting consecutive sentences with same word)
- Passive voice overuse
- Corporate jargon, over-explanation
- *Who Killed?* markers: "I mean..." opener, self-corrections, hedging, warm sign-off

### Narrative Issues
- Missing context or setup
- Redundancy (same point made twice)
- Logical jumps or unexplained references
- Weak transitions

## Notes

- This skill assumes you'll review and approve all web search findings before publication
- For sensitive claims (suspect naming, wrongful conviction risk), results are flagged for extra care
- The .docx output is designed for iteration — mark it up, make your changes, keep notes

---

## Behind the Scenes

**Unified Processing Pipeline:**

1. **Claim Extraction** (Python)
   - Regex patterns for dates, statistics, attributions, temporal claims
   - Extracts ~15 top claims (sorted by type priority)
   - Context preservation for cross-reference

2. **Verification Engine** (Python + heuristics)
   - Date validation (historical range check)
   - Statistic flagging (requires source docs)
   - Attribution analysis (requires citations)
   - Generates optimized web search queries for unverified claims
   - Confidence scoring (0-100%)
   - Status tags: ✓ verified | ⚠ needs_source | ✗ contradicted | ? unclear

3. **Voice Audit** (Python regex + pattern matching)
   - Scans for all 10 forbidden words (case-insensitive)
   - Checks for all 8 forbidden phrases
   - Analyzes sentence starters to catch repetition
   - Measures passive voice density percentage
   - Checks for *Who Killed?* warmth markers ("I mean...", hedging)
   - Only runs on true-crime domain (skips for marketing/other)

4. **Narrative Check** (Python NLP-lite)
   - Identifies unexplained character names
   - Flags logical gaps (markers like "therefore" without setup)
   - Catches potential redundancy (repeated phrases)
   - Flow analysis

5. **.docx Generation** (JavaScript/docx library)
   - Converts all findings into a conversational working document
   - Embeds tables, formatting, suggested rewrites
   - Includes space for your notes and decisions

**Web Search Integration:**
- Auto-generates targeted search queries for flagged claims
- Includes recommended searches in .docx for manual verification
- Example: "disappearance John Doe 1985 Ohio" for better recall
- Notes what sources to prioritize (court records, news archives, academic)
