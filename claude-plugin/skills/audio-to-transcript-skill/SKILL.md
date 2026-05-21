---
name: audio-to-transcript-skill
description: Converts MP3 audio files to timestamped, speaker-identified transcripts saved as formatted .docx documents. Use this skill whenever you need to transcribe a podcast episode, guest interview, or any audio file and produce a clean, production-ready transcript with episode metadata (episode name, guest names), timestamps, and speaker labels. Triggers on phrases like "transcribe this audio", "convert this MP3 to text", "make a transcript from this file", "transcribe the interview", "audio to transcript", or when you have an MP3 file and need a .docx transcript with speaker identification and timestamps.
compatibility: Requires Anthropic API audio transcription capability
---

# Audio-to-Transcript Skill

Converts MP3 audio files into professionally formatted, timestamped transcripts with speaker identification, saved as .docx files. Designed for podcast production, guest interviews, and audio content requiring documentation.

## Workflow Overview

1. **Accept audio input** — MP3 file path or uploaded audio
2. **Transcribe using Anthropic's audio API** — Extract speech-to-text with timing data
3. **Parse and structure output** — Identify speakers, extract timestamps, organize by speaker turns
4. **Format as .docx** — Clean, readable document with metadata header and timestamped dialogue
5. **Deliver** — Ready-to-use transcript for archiving, editing, or repurposing

## Input Requirements

- **Audio file**: MP3 format
- **Metadata** (user provides):
  - Episode name/title
  - Guest name(s) or speaker identifier(s)
  - (Optional) Host name, recording date, additional context

## Output Specification

### Document Structure

```
EPISODE TRANSCRIPT
==================

Episode: [Episode Name]
Guest(s): [Guest Name(s)]
[Optional: Date, Host, Duration]

---

[00:00] Host: Opening remarks or introduction...

[00:15] Guest Name: Guest's first response...

[00:45] Host: Follow-up question or comment...

[01:20] Guest Name: Continued dialogue...

[Etc.]
```

### Formatting Rules

- **Timestamps**: [MM:SS] format, accurate to nearest second
- **Speaker labels**: Clear identification (Host, Guest Name, or role descriptor)
- **Dialogue**: Exact transcription, minimal editing unless clarified otherwise
- **Paragraph breaks**: Between speaker turns for readability
- **File format**: .docx with:
  - Header section with metadata (title, guest, date if applicable)
  - Body text in readable serif or sans-serif font
  - Consistent spacing and indentation
  - Optional: Page numbers, episode details in footer

## How to Use This Skill

### Step 1: Provide Audio + Metadata

User provides:
- Path to MP3 file (or upload it)
- Episode name
- Guest name(s) or speaker list

### Step 2: Transcribe

Claude uses Anthropic's audio API to:
- Transcribe the entire MP3 to text
- Extract timing information where available
- Identify speaker transitions (tone, cadence) if possible
- Flag unclear sections or inaudible segments

### Step 3: Structure & Speaker ID

Claude parses the transcription to:
- Align timestamps with speaker turns
- Label each speaker (Host, Guest, or named participant)
- Organize into dialogue blocks
- Flag any ambiguous speaker transitions for review

### Step 4: Generate .docx

Claude produces a formatted Word document with:
- Metadata header (episode title, guest names, date)
- Full timestamped transcript
- Clean typography and spacing
- Ready for sharing, archiving, or further editing

## Edge Cases & Notes

### Speaker Identification
- If only one speaker detected, label as "Speaker" or request clarification
- If multiple speakers, Claude will attempt to distinguish based on vocal patterns; flag uncertain attributions
- User can provide speaker list upfront to improve accuracy

### Timing Accuracy
- Timestamps reflect best estimate from audio analysis
- Some files may have variable accuracy depending on audio quality
- Manual timestamp review recommended for publication-quality transcripts

### Audio Quality Issues
- Unclear/inaudible segments marked as `[inaudible]` or `[unclear: possible text?]`
- Background noise noted but not removed (use audio repair tools separately)
- Heavily accented or technical speech may require manual review

### Long-Form Audio
- Skill handles files of any length; processing time scales with duration
- Very long files (2+ hours) may benefit from splitting into sections
- Deliverable is always a single .docx per file

## Integration with Podcast Production

This skill complements broader podcast workflows:
- **Guest interviews**: Transcribe for show notes, social clips, or fact-checking
- **Episode rough cuts**: Reference transcript during editing
- **Archive**: Create a text record of all published/unpublished content
- **Repurposing**: Use transcripts as source material for articles, social posts, or show notes

## Success Criteria

A successful transcript:
- ✓ All spoken content captured (within reason for audio quality)
- ✓ Timestamps align with speaker turns (±1-2 seconds acceptable)
- ✓ Speakers clearly labeled and consistent throughout
- ✓ Formatted as clean, readable .docx
- ✓ Metadata header complete
- ✓ Ready for immediate use or light editing

## User Workflow Example

**User says:**
> "Transcribe this interview with Detective Sarah Chen. It's a 45-minute MP3. Episode is 'Cold Case Breakthrough' and we recorded it on May 2, 2026."

**Skill executes:**
1. Receives MP3 file path
2. Calls Anthropic audio API to transcribe
3. Parses output, identifies two speakers (Host, Detective Sarah Chen)
4. Creates timestamps from audio timeline
5. Formats as .docx with header:
   - Episode: Cold Case Breakthrough
   - Guest: Detective Sarah Chen
   - Date: May 2, 2026
6. Delivers document ready for sharing or editing
