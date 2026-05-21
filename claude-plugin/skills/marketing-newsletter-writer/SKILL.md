---
name: marketing-newsletter-writer
description: >
  Writes a ready-to-send marketing newsletter for a podcast episode — delivered as a .docx
  file formatted for Mailchimp, Substack, Beehiiv, or any email platform. Use this skill
  whenever any podcast host needs to promote an episode to their subscriber list.
  Triggers on phrases like "write the newsletter", "draft this month's newsletter",
  "newsletter for this episode", "newsletter for [topic/case/guest]", "email blast for
  [episode]", "write me something to send to subscribers", "promo email for [episode]",
  "subscriber email for [episode]", or any time an episode script, brief, or show notes
  are in hand and an audience-facing email needs to come out of it. Always use this skill
  rather than writing newsletters ad hoc — it enforces a consistent structure (teaser hook
  + episode summary), calibrates tone to the show's voice, and produces a copy-paste-ready
  .docx every time.
---

# Marketing Newsletter Writer

Produces a subscriber email for a podcast episode. Output is a `.docx` file with two
sections: an attention-grabbing episode teaser and a tight episode summary. The whole
thing should be copy-paste-ready for Mailchimp, Substack, Beehiiv, or any email platform.

Works for any podcast genre — true crime, business, interview, narrative, comedy, etc.

---

## Step 0: Read Brand Voice

Before writing anything, look for `.claude/brand-voice.md` and read it if it exists.
It governs tone, language, and what the show sounds like. If not found, apply the
voice principles in Step 3 and adapt them to whatever genre and tone the host describes.

---

## Step 1: Gather Inputs

The minimum you need:

- The episode's source material — a script, research brief, show notes, or any combination
- The show name and episode name or topic
- The host's name (for the sign-off), if provided

If source material hasn't been provided, ask for it before writing. A newsletter
written without it will be generic — and generic emails don't get opened.

Optional but useful:
- Episode number / season
- The single most surprising, funny, or revealing moment from the episode (makes the best hooks)
- Release date
- Any links to include (listen link, show notes, Patreon, social handles)
- Show genre and target audience — helps calibrate tone

---

## Step 2: Identify the Hook

Before writing, read through the source material and find the single most compelling
moment, fact, or question the episode raises. This is the hook — the one thing that
makes a subscriber stop scrolling and click play.

A good hook has at least one of these qualities:
- Creates a question the reader can't immediately answer
- Surfaces a detail so specific it feels true
- Reframes something familiar in a surprising way
- Puts the reader in the room at a pivotal moment

If the genre is narrative or investigative, the hook is usually the central tension or
mystery. If it's an interview show, the hook is the sharpest insight or most unexpected
thing the guest said. If it's a comedy or culture show, the hook is the bit or premise
that would make someone laugh or nod before they've even hit play.

If nothing in the source material jumps out, ask the host: "What's the one thing you'd
tell a friend to get them to listen to this episode?" That answer is almost always the hook.

---

## Step 3: Write the Newsletter

The newsletter has two sections. Keep the whole thing under 350 words. Subscriber
emails are skimmed, not read — every sentence has to earn its place.

### Voice Principles (if no brand-voice.md is found)

Match the tone of the show. A true crime show calls for restraint and specificity.
An interview show calls for warmth and curiosity. A comedy show calls for wit and
energy. When in doubt, write like a smart, enthusiastic friend who just listened to
the episode and wants to tell you why it's worth your time.

**Universal avoids — regardless of genre:**
- Generic openers ("This week on [Show]..." — every newsletter starts this way, which
  means none of them stand out)
- Passive voice
- Filler superlatives: "incredible", "mind-blowing", "game-changing", "you won't believe"
- Teasing without landing: hinting at something without saying what it is
- Padding that doesn't add information

---

### Section 1: Episode Teaser (Hook)

**Purpose:** Get the reader to click play. One tight paragraph — 3 to 5 sentences max.

**Structure:**
1. Open with the hook identified in Step 2. No wind-up. Start in the middle of the story
   or idea. The first sentence should make the reader lean in.
2. One or two sentences of context — enough to orient, not enough to spoil.
3. Close with the show name and a soft call to listen. Keep it low-key — the hook
   already did the work.

**Example — true crime (adapt, don't copy):**
> In October 1989, a ten-year-old girl walked out of a shopping plaza in Bay Village,
> Ohio after receiving a phone call from a stranger. She was never seen alive again.
> Her killer has never been charged. New episode is out now — link below.

**Example — interview show (adapt, don't copy):**
> Maya Chen built a $40M company with no outside funding and sold it in year six. In
> this episode she explains why she turned down a Series A three times — and what she
> thinks founders get wrong about venture capital. New episode out now.

**Example — narrative/documentary (adapt, don't copy):**
> For 11 years, the town of Harlan believed the fire was an accident. This episode
> is about what actually happened. New episode out now.

---

### Section 2: Episode Summary

**Purpose:** Give readers enough context to follow the episode, and remind existing
fans why this particular episode matters. Three to five short paragraphs.

**Adapt the structure to the genre:**

For **narrative / investigative** episodes:
1. Who or what is at the center of this story — briefly, as a person or situation (not just a headline)
2. The core facts — what happened, clinical not dramatic
3. The complication — what makes this unresolved, contested, or surprising
4. Why now / why this episode
5. What the episode actually covers and what the listener will come away with

For **interview** episodes:
1. Who the guest is and why they're worth an hour of the listener's time
2. What they built, did, or know that's relevant
3. The sharpest or most counterintuitive thing they say in the episode
4. What the listener will take away

For **solo / educational** episodes:
1. The topic and why it matters right now
2. The key insight or frame the host brings to it
3. What the listener will understand or be able to do differently after listening

When in doubt, lead with people and stakes — not process.

---

## Step 4: Add Placeholder CTAs

At the end of the newsletter, add a placeholder block the host can fill in before
sending. Make placeholders obvious and easy to swap:

[LISTEN LINK — paste episode URL here]
[SHOW NOTES — optional]
[SUBSCRIBE on Apple Podcasts / Spotify / your platform]
[OPTIONAL: Patreon, newsletter, community link]

One primary action (listen) is the goal. Keep it short.

Do not add any production company, network, or partner credits. The host will add
those if and when they want them.

---

## Step 5: Output

Save as a `.docx` file named:

[EpisodeName]-newsletter.docx

Use the `docx` skill. Read its SKILL.md at:
/var/folders/rb/hq7f3vwn2lgd_2d1k95wmm_40000gn/T/claude-hostloop-plugins/45827ee1babc8a7d/skills/docx/SKILL.md
before generating the file.

Format the document:
- **Header:** Show name + episode name + "Subscriber Newsletter" + today's date
- **EPISODE TEASER** — hook paragraph (slightly larger or bold)
- **EPISODE SUMMARY** — background paragraphs
- **CTAs** — placeholder block
- **Notes for [Host]** at the bottom:
  - Word count for teaser and summary
  - Any details inferred from source material (flag for host to verify before sending)
  - 3 subject line options

---

## Step 6: Subject Lines

Generate three subject line options. Good subject lines are short, specific, and
create enough curiosity to earn the open — without being clickbait.

Calibrate to the genre:
- **Narrative/true crime:** Lead with a specific detail, name, or unanswered question
- **Interview:** Lead with the guest's sharpest insight or most counterintuitive claim
- **Solo/educational:** Lead with the outcome or the reframe — what you'll know after listening

Three options — the host picks. Include in the Notes section of the .docx.

---

## Step 7: Handoff

After saving the file, share the link and note:
- Which hook you chose and why (one sentence)
- Any details inferred from source material the host should verify before sending
- Total word count (teaser + summary)

Do not summarize the newsletter back to the host — they can read the document.
