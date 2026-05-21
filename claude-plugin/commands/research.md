---
name: research
description: Research a podcast topic or case and produce an episode brief with sources, timeline, suspects, and outline
tools: [WebSearch, WebFetch, Read, Write]
---

Apply the episode-research skill to the provided topic or case.

1. Ask the user for the following if not already provided:
   - Case name or research topic
   - Content type (true crime case, cold case, guest interview, news event)
   - Any specific angles or questions to investigate
   - (Optional) Episode format length preference

2. Open the **Podcast Research Agent** artifact for the interactive research experience, then:
   - Search news archives, court records, Wikipedia, books, and podcasts related to the case
   - Identify key players, suspects, and witnesses
   - Extract a chronological case timeline
   - Build a 6-act episode outline with timestamps
   - Flag open questions for further investigation

3. Deliver the full research brief including:
   - Source list with relevance scores and publication metadata
   - Episode outline (hook → context → case → investigation → suspects → legacy)
   - Case timeline (chronological events)
   - Open questions (what still needs answering before you record)
   - Podcast potential score and recommended episode angle

4. Offer to export the brief as a .docx and to queue the case in the Production Pipeline
