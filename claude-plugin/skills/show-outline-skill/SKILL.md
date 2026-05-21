---
name: show-outline-skill
description: "Generates structural show outlines for each case in the Who Killed? podcast pipeline. Use this skill whenever Bill needs to create comprehensive production outlines from cases—whether from a PIPELINE.md file or individual case data. Triggers on phrases like \"create show outlines\", \"outline these cases\", \"generate outlines for the pipeline\", \"outline this case\", \"structural outline for\", or when Bill has cases ready and needs organized outlines covering hooks, timelines, suspects, investigative turns, interview targets, and episode structure."
---

# Show Outline Skill

Generates comprehensive structural show outlines for Who Killed? podcast cases. This skill takes raw case data (from PIPELINE.md or individual inputs) and produces production-ready outlines with cold opens, case timelines, suspect profiles, investigative turns, interview targets, and episode structure suggestions.

## Input

The skill accepts either:

1. **PIPELINE.md file** — Reads all cases marked for outlining, processes them in batch
2. **Individual case data** — One or more cases passed as structured input with the following fields:
   - `case_name` (string, required)
   - `key_facts` (string, required) — Brief summary of the case
   - `suspects` (array of objects) — Each suspect object should contain:
     - `name` (string)
     - `connection` (string) — Relationship to case/victim
     - `status` (string, optional) — e.g., "POI", "Cleared", "In custody"
     - `notes` (string, optional) — Key evidence or details
   - `timeline` (array of objects, required) — Chronological events:
     - `date` (string)
     - `event` (string)
   - `recent_developments` (string, optional) — Latest investigative updates
   - `interview_targets` (array of strings, optional) — Potential guests/sources
   - `case_status` (string, optional) — e.g., "Cold case", "Active investigation"

## Output

A single `.docx` file containing:

- **One outline per case** with clear visual separation
- **For each case:**
  - **Cold Open Hook** — Attention-grabbing opening line (1-2 sentences, not on-air voice)
  - **Case Timeline** — Chronological sequence of key events
  - **Suspect Profiles** — Structured overview of persons of interest
  - **Investigative Turns** — Major breaks, dead ends, recent developments
  - **Interview Targets** — Potential guests, sources, experts
  - **Episode Structure** — Suggested segments/act breaks for production
  - **Production Notes** — Pacing guidance, audio cue opportunities, narrative flow tips
  - **Sources** — Bulleted list of sources cited or referenced in the outline with links

## Workflow

1. Accept case input (PIPELINE.md or case data objects)
2. For each case, research any missing context if needed (recent developments, suspect updates)
3. Generate structural outline for each case, treating each as a discrete production problem
4. Organize all outlines into a single formatted .docx file
5. Return file to user for download

## Key Constraints

- **No named identification of unidentified suspects** — Use descriptive references (e.g., "The main POI" or "The boyfriend at time of incident")
- **Cite sources thoroughly** — Every outline includes a Sources section listing all police departments, forensic labs, court records, news archives, and investigative teams referenced
- **Structural focus** — Outlines are production-focused, not on-air voice
- **Template-agnostic** — Don't reference Bill's specific voice constraints or episode patterns; keep outlines universally actionable
- **Batch processing** — Handle multiple cases efficiently in a single output

## Example Outline Structure

```
CASE: [Case Name]

Cold Open Hook:
[1-2 sentence attention grabber, structural/production language]

Case Timeline:
[Date] — [Event]
[Date] — [Event]
...

Suspect Profiles:
[Suspect/POI Name]
  Connection: [Relationship to victim/case]
  Status: [POI/Cleared/In custody]
  Key Evidence: [Brief facts]
  Narrative Angle: [Why this matters for the story]

Investigative Turns:
[Major break / discovery]
  Impact: [What changed in the case]
  Timeline: [When it happened]
  Status: [Resolved/Dead end/Ongoing]

Interview Targets:
- [Potential guest/source 1] — [Why they matter]
- [Potential guest/source 2] — [Why they matter]

Episode Structure:
Segment 1: [Topic] — [Est. minutes, production notes]
Segment 2: [Topic] — [Est. minutes, production notes]
...

Production Notes:
[Pacing, audio cues, narrative flow guidance specific to this case]

Sources:
- [Source Name/Publication] — [Relevant detail or finding cited]
- [Source Name/Publication] — [Relevant detail or finding cited]
- [Source Name/Publication] — [Relevant detail or finding cited]
```

## Processing Multiple Cases

When handling batch input:
1. Process cases in the order provided
2. Apply consistent formatting across all outlines
3. Include a table of contents at the beginning of the .docx
4. Use page breaks between cases for clarity
5. Include a summary at the end listing all cases outlined and metadata (e.g., outline date, total cases)

## Integration Notes

This skill is designed to work independently of Bill's voice templates, show notes skill, and other Who Killed? production tools. It serves as a pre-scripting structural layer that informs episode planning and production sequencing.