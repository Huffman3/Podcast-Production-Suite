# Fact-Check Script Skill

A comprehensive fact-checking skill for scripts across any domain (true crime, marketing, documentary, social, etc.).

## What It Does

Takes a script and returns a .docx working document with:
- **Verified/flagged claims** (with confidence scores and sources)
- **Voice audit results** (forbidden words, passive voice, tone consistency)
- **Narrative gaps** (logical issues, unexplained references, redundancy)
- **Suggested rewrites** (how to fix problems)
- **Web search recommendations** (where to verify claims)

## Installation

```bash
cp -r fact-check-script-skill /mnt/skills/user/
```

Then reload your skill list in Claude.ai.

## Usage

### Basic Usage
```
Fact-check this script: [paste your script]
```

### True Crime Script (auto-voice audit)
```
Fact-check this Who Killed? script: [paste your script]
```

### Non-True Crime Domain
```
Fact-check this marketing script for accuracy: [paste your script]
```

## Output

A .docx file containing:

1. **Script Input** (verbatim)
2. **Flagged Claims Table**
   - Claim text
   - Type (date, statistic, attribution, statement)
   - Verification status (✓ verified | ⚠ needs source | ✗ contradicted | ? unclear)
   - Confidence percentage

3. **Search Queries** — Ready-to-use Google searches for verification

4. **Voice Audit** (True Crime Only)
   - Forbidden words found
   - Forbidden phrases detected
   - Passive voice percentage
   - Missing warmth markers
   - Suggested replacements

5. **Narrative Issues**
   - Unexplained names/references
   - Logical gaps
   - Redundancy

6. **Your Notes Section** — Blank space to record decisions

7. **Summary** — High-level overview + action items

## What Gets Checked

### Factual Claims
- Dates, locations, proper nouns
- Statistics and percentages
- Historical events
- Attributions (who said what)
- Any verifiable statement

### Voice Consistency (True Crime Only)
**Forbidden Words:** robust, delve, leverage, harness, landscape, utilize, realm, transformative, game-changer, seamless, testament

**Forbidden Phrases:**
- "It's important to note"
- "In today's digital age"
- "Furthermore" / "Moreover"
- "In conclusion"
- "Let that sink in"
- "At the end of the day"
- "It goes without saying"

**Positive Markers:** "I mean...", hedging language, self-corrections, warmth

### Narrative Health
- Unexplained character introductions
- Logical gaps (markers like "therefore" without setup)
- Repetitive phrasing or concepts
- Flow and transitions

## Behind the Scenes

**Pipeline:**
1. Claim Extraction (regex patterns for ~15 key claims)
2. Verification Engine (heuristics + search query generation)
3. Voice Audit (pattern matching against brand rules)
4. Narrative Check (reference tracking + logic flow)
5. .docx Generation (formatted working document)

**Technologies:**
- Python 3.x (extraction, audit, narrative)
- JavaScript/docx library (document generation)
- Regex + heuristics (no external APIs required)

## Files

```
fact-check-script-skill/
├── SKILL.md                    # Core skill definition
├── README.md                   # This file
├── scripts/
│   ├── fact_check_engine.py    # Claim extraction + voice audit + narrative
│   ├── web_verifier.py         # Verification engine + search queries
│   └── unified_checker.py      # Main orchestrator
└── test_prompts.json           # Test cases
```

## Testing

Run the test suite:
```bash
cd fact-check-script-skill
python3 scripts/fact_check_engine.py
python3 scripts/web_verifier.py
python3 scripts/unified_checker.py
```

## Limitations

- **Web searches are recommendations only** — The skill generates optimized search queries but doesn't execute them automatically (you'll do that manually)
- **Heuristic verification** — Confidence scores are probabilistic, not definitive. Always review flagged claims against primary sources
- **Local/obscure claims** — Difficult to verify without additional context
- **Opinion-based statements** — Not fact-checkable; flagged as unclear

## For Bill (Who Killed? Specific)

This skill is built to enforce your voice standards:
- Catches every forbidden word and phrase
- Checks passive voice ratio (targets ~30% or lower)
- Flags missing warmth markers ("I mean...", hedging)
- Treats wrongful conviction subjects with extra scrutiny (flagged for review)
- Integrates with your existing brand voice guidelines

Run this on every script draft before recording.

---

**Questions or improvements?** Edit SKILL.md or the scripts and reload.
