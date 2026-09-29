---
name: learn-research
description: Use when the user wants to research or find information on a topic/subtopic to learn it — "research this topic", "find info on X from reliable sources", or continuing to the next unchecked subtopic in an intern-to-senior learning plan. Second step of the intern-to-senior workflow (after learn-plan, before learn-report).
---

# Learn Research

## Before starting
- Determine the subtopic to research: if inside the intern-to-senior flow, read `<HOME>/intern-to-senior/<topic-slug>/plan.md` and pick the first unchecked subtopic (or whatever subtopic the user names directly).
- If no `plan.md` exists (user jumped straight to research without learn-plan), work standalone — don't force creating a plan first.

## Search order (important)
1. **Reliable sources first, always**: official documentation, standards/RFCs, academic papers, docs from the actual vendor/maintainer of the technology or field.
2. **Then broaden to as many other sources as possible**: articles/blogs from well-regarded engineers or experts, tutorials, case studies, verified answers on Q&A sites — use these to cross-check and add practical perspective that official docs lack.
3. Every fact/claim used must **cite its source** (name + URL) inline. Never state a conclusion without a citation.
4. If sources conflict, tell the user plainly how they conflict and which source is more trustworthy and why.

## Save output
Save to `<HOME>/intern-to-senior/<topic-slug>/research-<subtopic-slug>.md`:
```markdown
# Research: <Subtopic>
Date: <YYYY-MM-DD>

## Key findings
- ...

## Sources
### Primary (official/authoritative)
- [Source name](URL) — brief note on what it was used for
### Secondary
- [Source name](URL) — brief note on what it was used for
```

## After saving
- Update the Progress table in `plan.md`: Research column for this subtopic = completion date, Status = "researched"
- Tell the user the next step is `/learn-report`
