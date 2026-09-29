---
name: learn-plan
description: Use when the user wants to start or resume a learning topic in the "intern-to-senior" system — e.g. "today I want to learn about X", "let's start intern-to-senior on X", or asks to see/update their study checklist. Breaks a topic into an ordered checklist of subtopics (intern → senior depth) and creates/updates the plan file. Entry point of the intern-to-senior workflow (plan → research → report → exam → review, per subtopic).
---

# Learn Plan

The "intern-to-senior" system: learn one topic at a time by breaking it into a checklist of subtopics, then cycle research → report → exam → review per subtopic until the checklist is done.

## Storage (fixed location, independent of the current project)
Everything is stored at `<HOME>/intern-to-senior/<topic-slug>/`
- Resolve home directory with Bash: `echo $HOME`
- topic-slug: lowercase kebab-case of the topic, strip special characters (e.g. "Kubernetes Networking" → `kubernetes-networking`)
- Main file for this skill: `plan.md`

## Steps
1. If the user hasn't named a clear topic yet, ask what they want to learn today.
2. Check whether `<HOME>/intern-to-senior/<topic-slug>/plan.md` already exists.
   - **Exists**: read it, summarize current progress (which subtopic is at which stage), then ask whether to add new subtopics or resume an unfinished one.
   - **Doesn't exist**: create the folder with `mkdir -p`, then create a new `plan.md` from the template below.
3. Break the topic into a checklist of subtopics that covers enough ground to take the user from "basic understanding (intern)" to "deep understanding, able to reason about trade-offs (senior)", ordered from foundational to advanced. Typically 5-10 subtopics, adjusted to how broad the topic is.
4. Write/update `plan.md`.
5. Tell the user which unfinished subtopic comes first, and that the next step is `/learn-research` (or they can just name the subtopic they want to dig into — it will auto-trigger).

## Template: plan.md
```markdown
# Learning Plan: <Topic>
Created: <YYYY-MM-DD>
Last updated: <YYYY-MM-DD>

## Checklist
- [ ] <subtopic-1>
- [ ] <subtopic-2>
...

## Progress
| Subtopic | Research | Report | Exam | Review | Status |
|---|---|---|---|---|---|
| <subtopic-1> | - | - | - | - | not started |
```

Note: the other skills (learn-research / learn-report / learn-exam / learn-review) update the Progress table and checkboxes in this same file after each stage. Never delete existing history — only append/update.
