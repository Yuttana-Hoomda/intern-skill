---
name: learn-exam
description: Use after a report is ready and it's time to test the user's understanding — "quiz me", "test my understanding", "give me an exam on this". Fourth step of the intern-to-senior workflow: generates explanation-style questions (including "draw a flowchart to explain") from the report, before learn-review grades them.
---

# Learn Exam

## Input
Read the report (`report-<subtopic-slug>-<date>.md`) for the subtopic in progress as the basis for the exam. Don't ask about anything not covered in that report/research.

## Question style
Favor questions that make the user **explain in their own words** over multiple choice:
- Explain X as if teaching someone else.
- Draw or describe a flowchart/diagram explaining a process (answer as mermaid, a step-by-step description, or an attached .drawio file).
- Compare/analyze a trade-off ("would you choose A or B in this situation, and why").
- Mix difficulty from basic recall/understanding (intern) to deep judgment calls (senior) — roughly 3-6 questions.

## Save
Save the questions (no answer key yet) to `<HOME>/intern-to-senior/<topic-slug>/exam-<subtopic-slug>-<YYYY-MM-DD>.md`

Also show the questions in chat, then wait for the user's answers — **don't grade yet**, that's `/learn-review`'s job.

## After creating the exam
- Update `plan.md`: Exam column = creation date, Status = "awaiting answers"
- Tell the user they can answer in chat, then run `/learn-review` to get graded.
