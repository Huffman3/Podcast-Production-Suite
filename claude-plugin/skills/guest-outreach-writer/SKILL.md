---
name: guest-outreach-writer
description: >
  Writes cold outreach emails to potential guests for *Who Killed…?* — including an
  initial email and one follow-up — saved as a .docx file. Use this skill whenever
  Bill needs to reach out to a detective, journalist, author, family member, forensic
  expert, or any other potential guest connected to a case. Triggers on phrases like
  "write outreach to [name]", "draft an email to [guest]", "reach out to [person]",
  "cold email for [guest]", "I want to get [name] on the show", "contact [name] about
  [case]", "write me something to send to [guest]", or any time Bill identifies a
  potential guest and needs a first contact message. Always use this skill rather than
  writing outreach ad hoc — it calibrates tone by guest type, leads with the victim
  and the case (not the show's metrics), and produces a ready-to-send .docx with
  both the initial email and a follow-up.
---

# Guest Outreach Writer — *Who Killed…?*

Produces cold outreach emails for potential *Who Killed…?* guests. Output is a `.docx`
file containing an initial email (with three subject line options) and a follow-up
email to send 5–7 days later if no response.

---

## Step 0: Read Brand Voice

Before writing, look for `.claude/brand-voice.md` and read it. If found, it governs
tone and language. If not found, apply the voice principles embedded in this skill.

---

## Step 1: Gather Inputs

Minimum required:
- Guest name
- Guest's role / affiliation (title, outlet, department, or connection to the case)
- The case they're connected to
- Why Bill wants them specifically — what do they know or bring that no one else does?

If Bill hasn't provided the "why this person" detail, ask before writing. Generic
outreach fails. The email has to prove Bill has done his homework.

Optional but useful:
- Specific work to reference (article, book, chapter, investigation, testimony)
- Any mutual connection or prior interaction
- Whether the guest has done podcast interviews before
- Any known sensitivities (active case, family grief, past media experience)

---

## Step 2: Classify the Guest Type

Classify the guest into one of these four types. The type determines tone, framing,
and the ask structure. If the guest could fit more than one category, use the most
prominent one.

| Type | Who They Are | Tone Key |
|------|-------------|----------|
| **Detective / Law Enforcement** | Lead investigator, retired detective, FBI agent, sheriff | Respectful, peer-level, case-specific |
| **Journalist / Author** | Reporter, true crime writer, documentarian, book author | Collegial, peer-to-peer, work-referencing |
| **Family Member / Advocate** | Victim's family, close friend, advocacy org rep | Trauma-informed, victim-centered, zero pressure |
| **Forensic Expert** | Profiler, DNA analyst, criminologist, medical examiner | Credentialing, methodology-specific, precise |

---

## Step 3: Write the Initial Email

### Universal Rules — Every Guest Type

**Lead with the case and victim. Never open with the show.**
The first sentence is about the case or the guest's work — not about *Who Killed…?*,
Bill's listener numbers, or why the show is great. That framing comes second, briefly,
if at all.

**Be specific. Generic outreach gets deleted.**
Reference the guest's actual work: a specific article, a specific investigation year,
a specific chapter, a specific statement they made. If you can't be specific, ask Bill
for more detail before writing.

**Keep it short. Three to four short paragraphs maximum.**
Respect the guest's time. Long emails signal that Bill hasn't thought carefully about
what he's actually asking. The goal of the first email is one thing: get a reply.

**Make the ask clear and low-stakes.**
Don't bury the ask. Don't over-explain the show. Ask once, clearly, and give them an
easy way to decline.

**Never pressure, never oversell.**
No "this would be an incredible opportunity." No listener count drops. No urgency
tactics. The case is the draw — let it do the work.

---

### Email Structure by Guest Type

#### DETECTIVE / LAW ENFORCEMENT

**Tone:** Respectful and peer-level. Bill respects their work and comes prepared.
He's not a fan — he's an investigator who wants their perspective on the record.

**Subject line options (write 3):**
- Direct and case-specific: "[Case Name] — *Who Killed…?* Podcast"
- Investigator-framing: "Following up on the [Case Name] investigation"
- Low-key: "Quick question about [Case Name]"

**Structure:**
1. **Opening:** Name the case and their specific role in it. One sentence. Show you know
   exactly who they are and what they did. *"I've been researching the [case] investigation,
   and I know you [led/were part of/worked] that case in [year]."*
2. **Show context:** One to two sentences. What the show is, what it does — investigative,
   victim-first, original sourcing. Not a pitch. Just context.
3. **The ask:** Would they be willing to talk on the record about their experience with the
   case? Be specific: is it one conversation? A recorded interview? Frame it as their
   perspective mattering to the historical record — not as content for a podcast.
4. **Easy exit:** Acknowledge that some cases are still sensitive, that they may not be
   able to speak freely, and that's understood. One sentence.
5. **Sign-off:** First name, show name, brief credential (one line).

**What to avoid:**
- "I'm a huge fan of your work" — too casual for law enforcement
- Asking about anything outside their specific case involvement on first contact
- Implying they have an obligation to talk

---

#### JOURNALIST / AUTHOR

**Tone:** Collegial and peer-to-peer. Bill has read their work. He's not asking them
to explain the basics — he wants their reporting instincts and sourcing on the record.

**Subject line options (write 3):**
- Work-referencing: "Your [article/book] on [Case Name] — *Who Killed…?*"
- Peer framing: "Comparing notes on [Case Name]"
- Direct: "[Case Name] — interview request from *Who Killed…?*"

**Structure:**
1. **Opening:** Reference their specific work. Article title, book title, date, outlet.
   One sentence that proves Bill read it. *"Your [piece/chapter] on [case] in [outlet/book]
   — specifically [specific detail] — has been one of the most useful things I've found
   in my research."*
2. **Show context:** One sentence. What Bill does that complements rather than duplicates
   their work: original interviews, primary records, long-form investigation.
3. **The ask:** Would they talk on the record? Frame it as bringing their reporting into
   the audio conversation — their work has already told part of this story, Bill wants
   to extend it.
4. **Easy exit:** If they're still actively reporting the case and can't comment, he
   completely understands.
5. **Sign-off:** First name, show name.

**What to avoid:**
- Over-praising in a way that feels hollow
- Asking them to "explain" things they've already published — reference their work,
  don't ask them to repeat it
- Implying their previous coverage was incomplete

---

#### FAMILY MEMBER / ADVOCATE

**Tone:** Trauma-informed, unhurried, victim-centered. This is the most sensitive
category. The entire email is structured around the victim and the family's experience —
not the show, not the episode, not what would make good audio.

This email requires the most care. When in doubt, go slower and say less.

**Subject line options (write 3):**
- Victim-named: "Regarding [Victim's Name]"
- Direct and human: "A message about [Victim's Name] — *Who Killed…?* podcast"
- Understated: "[Victim's Name] — reaching out"

**Structure:**
1. **Opening:** The victim. Name them. Say something true and specific about them —
   from the research brief or publicly documented record. Not their death. Who they were.
   *"I've spent [weeks/months] researching [Victim's Name]'s case, and I wanted to reach
   out to you directly."*
2. **Who Bill is:** One sentence. Host of *Who Killed…?* He investigates cold cases with
   the goal of keeping victims' stories alive and asking hard questions of the systems
   that failed them.
3. **What he's doing and why:** He's working on an episode about [case]. He believes
   [Victim's Name] deserves to be remembered as a full person — not just a file.
   He'd be honored to include [family member's] voice if they're ever willing.
4. **The ask — soft and optional:** "If you're ever open to talking — even briefly,
   even off the record to start — I'd be grateful." Make clear there is no pressure,
   no deadline, and no obligation.
5. **Acknowledgment:** One sentence acknowledging the weight of this. Not performative.
   *"I know being contacted about this is never easy, and I wanted to reach out with
   as much care as I could."*
6. **Sign-off:** Full name, show name, contact info including a phone number if Bill
   is comfortable providing one. Family members often prefer to call.

**What to avoid:**
- Any reference to listener numbers, show growth, or media value
- "Your story deserves to be heard" — this can feel appropriative
- Asking them to relive specific details of the crime in the first email
- Any urgency framing whatsoever
- "I'd love to have you on the show" — lead with care, not the interview

---

#### FORENSIC EXPERT

**Tone:** Precise and credentialing. These guests value their methodology being
understood correctly. Bill has done the research and knows what he's asking about.

**Subject line options (write 3):**
- Specific and technical: "[Case Name] — question about [specific discipline]"
- Expert framing: "Consulting request: [Case Name] / [Forensic Discipline]"
- Direct: "[Case Name] — *Who Killed…?* interview request"

**Structure:**
1. **Opening:** Name their specific field and how it applies to the case. Show fluency —
   not jargon-dropping, but evidence that Bill understands the discipline well enough
   to ask a good question. *"I'm investigating [case], and the [DNA/forensic
   analysis/behavioral profile/etc.] work that [was/was not] done in this case is
   central to why it went cold."*
2. **Show context:** One to two sentences. Research-driven, original sourcing, not
   sensationalist.
3. **The ask:** Specific and bounded. What exactly does Bill want to discuss? Don't
   ask for a general conversation — ask about a specific evidentiary question the
   case raises. Experts are more likely to say yes to a focused question than an
   open-ended interview.
4. **Credential acknowledgment:** One sentence citing their specific expertise —
   institution, publication, or known casework — to confirm Bill isn't wasting their time.
5. **Easy exit:** If the case falls outside their area or they can't comment, completely
   understood.
6. **Sign-off:** First name, show name.

**What to avoid:**
- Getting the science wrong — if uncertain, use general language and ask Bill to verify
- Asking them to diagnose, speculate, or opine beyond their documented expertise
- Framing them as a "character" in the story rather than a subject-matter expert

---

## Step 4: Write the Follow-Up Email

Send 5–7 days after the initial if no response.

**Universal rules for the follow-up:**
- Half the length of the initial email or shorter.
- Don't repeat the full pitch — they have the first email.
- Add one new thing if possible: a recent development in the case, a newly published
  piece, a related story in the news. Give them a reason to re-engage.
- Stay warm, not passive-aggressive. No "just checking in" — that phrase signals
  low stakes. Frame it as genuinely still interested, not chasing.
- One more easy exit built in.

**Structure:**
1. One sentence re-establishing context: "I reached out last week about [case]."
2. One sentence new hook if available — something that happened or that Bill found.
   If nothing new, skip this.
3. Restate the ask in one sentence.
4. Easy exit: "Either way, I appreciate the work you've done on this."
5. Sign-off — same as initial.

---

## Step 5: Output

Save as a `.docx` file:

```
[GuestLastName]-outreach.docx
```

Format:
- **Header:** Guest name, role, case — at the top
- **INITIAL EMAIL** section
  - Three subject line options (labeled Option 1 / 2 / 3)
  - Full email body, ready to copy-paste
  - Sending note: suggested timing (immediately or after a specific event)
- **FOLLOW-UP EMAIL** section
  - One subject line
  - Full email body
  - Sending note: "Send 5–7 days after initial if no reply"
- **Notes for Bill** at the bottom (outside the emails):
  - Any sensitivities flagged (active case, family grief, prior media experience)
  - Suggested personalization Bill should add before sending
  - One-line summary of why this guest matters to the episode

Use the `docx` skill. Read its SKILL.md at
`/var/folders/rb/hq7f3vwn2lgd_2d1k95wmm_40000gn/T/claude-hostloop-plugins/45827ee1babc8a7d/skills/docx/SKILL.md`
before generating the file.

---

## Step 6: Handoff

After saving the file, present the link and note:
- Guest type classification used
- Any personalization gaps Bill should fill before sending (e.g., a specific article
  to reference that needs Bill to confirm the title)
- Any sensitivity flags

Do not summarize the email content back to Bill — he can read the document.
