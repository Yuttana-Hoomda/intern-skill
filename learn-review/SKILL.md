---
name: learn-review
description: Use when the user has answered exam questions and wants them checked/graded — "check my answers", "review my answers", "what did I get wrong". Final step of the intern-to-senior workflow: grades answers against the research/report source of truth, corrects mistakes with citations, and lets the user retry before marking the subtopic complete in the plan.
---

# Learn Review

## Input
- Questions from `exam-<subtopic-slug>-<date>.md`
- The user's answers (in chat)
- Ground truth from `research-<subtopic-slug>.md` (Sources section) and `report-<subtopic-slug>-<date>.md`

## Grade each question
For every question, state the verdict plainly: correct / partially correct / incorrect.
- **If correct**: say what was right, add extra perspective if useful.
- **If incorrect or incomplete**:
  1. Explain the correct fact, **citing the source** (from the research Sources).
  2. Point to specifically what to study more and where (not just "read more") — be concrete.
  3. Let the user answer that question again before moving to the next one — don't wave it through.
- If the user asks follow-up questions or wants more depth on something during review, go deeper right away — no special command needed.

## Save results
Save to `<HOME>/intern-to-senior/<topic-slug>/review-<subtopic-slug>-<YYYY-MM-DD>.md` — questions, the user's answers, per-question verdicts, points to fix, and any retries.

## Closing out a subtopic
Once the user passes all questions (or corrects their understanding):
- Update `plan.md`: check this subtopic's box `[x]`, Review column = date, Status = "done"
- Name the next unchecked subtopic in the checklist and suggest continuing with `/learn-research` (or `/learn-plan` to see overall progress / add new subtopics)
- If this was the last subtopic in the checklist, tell the user the topic is fully complete.
