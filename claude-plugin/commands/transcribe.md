---
name: transcribe
description: Transcribe an MP3 audio file into a timestamped, speaker-labeled .docx transcript
tools: [Read, Write, Edit]
---

Apply the audio-to-transcript-skill to the provided MP3 file.

1. Ask the user for the following if not already provided:
   - Path to the MP3 file (or ask them to upload it)
   - Episode name/title
   - Guest name(s) or speaker list
   - (Optional) Recording date, host name, any additional context
2. Invoke the `audio-to-transcript-skill` to transcribe the audio, identify speakers, and apply timestamps
3. Format the output as a .docx with:
   - Metadata header (episode title, guest name(s), date)
   - Timestamped, speaker-labeled dialogue in [MM:SS] format
   - `[inaudible]` or `[unclear: possible text?]` markers for any unclear segments
4. Deliver the finished .docx and note any sections that may need manual review
