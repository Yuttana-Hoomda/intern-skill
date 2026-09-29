---
name: learn-report
description: Use after research on a subtopic is done, when the user wants a summary/report of what was learned — "summarize this", "make a report", "turn this into a flowchart". Third step of the intern-to-senior workflow: turns research notes into a structured report (plus a draw.io flowchart when useful), before learn-exam.
---

# Learn Report

## Input
Read `<HOME>/intern-to-senior/<topic-slug>/research-<subtopic-slug>.md` for the subtopic currently in progress (from plan.md or as named by the user) as the sole source for the summary. Do not add new information that isn't in the research.

## Write the report
Write a clearly structured summary suited to someone progressing from intern to senior level: brief overview, core concepts, deeper detail/reasoning (why it works this way), pros/cons and trade-offs, common pitfalls, best practices — with a citation next to each key point (drawn from the Sources in the research file).

Save to `<HOME>/intern-to-senior/<topic-slug>/report-<subtopic-slug>-<YYYY-MM-DD>.md`

## Flowchart (.drawio)
If this subtopic involves a sequence of steps/a process/states that a diagram explains better than prose (e.g. a pipeline, lifecycle, decision flow), also create a `.drawio` file (mxGraph XML) in the same folder, named `report-<subtopic-slug>-<YYYY-MM-DD>.drawio`.

Use this minimal template as a base (adjust labels/positions/node count to fit the actual content):
```xml
<mxfile>
  <diagram name="Flow">
    <mxGraphModel dx="800" dy="600" grid="1" gridSize="10" guides="1" tooltips="1" connect="1" arrows="1" fold="1" page="1" pageScale="1" pageWidth="850" pageHeight="1100" math="0" shadow="0">
      <root>
        <mxCell id="0" />
        <mxCell id="1" parent="0" />
        <mxCell id="n1" value="Step 1" style="rounded=1;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="80" y="80" width="160" height="60" as="geometry" />
        </mxCell>
        <mxCell id="n2" value="Step 2" style="rounded=1;whiteSpace=wrap;html=1;" vertex="1" parent="1">
          <mxGeometry x="320" y="80" width="160" height="60" as="geometry" />
        </mxCell>
        <mxCell id="e1" style="edgeStyle=orthogonalEdgeStyle;html=1;" edge="1" parent="1" source="n1" target="n2">
          <mxGeometry relative="1" as="geometry" />
        </mxCell>
      </root>
    </mxGraphModel>
  </diagram>
</mxfile>
```
- Use `rhombus;whiteSpace=wrap;html=1;` style for decision nodes.
- Every `mxCell` needs a unique `id` within the file — never reuse one.
- If the subtopic isn't flow/process-shaped, skip the flowchart entirely — don't force one.

## After saving
- Update `plan.md`: Report column = completion date, Status = "reported"
- Tell the user the next step is `/learn-exam`
