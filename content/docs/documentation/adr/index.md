---
title: Architectural Decision Records
type: docs
bookToc: false
---
# Archetectural Decision Records

The 805th SHOC uses [archetectural decision records](https://adr.github.io)(ADRs) to document engineering decisions. These include choices about composition of the tech stack, using one module or library over others, infrastructure, features, etc. "Architectural" should be interpreted broadly: any decision that could impact the project at the archectural level is a candidate or an ADR.

ADRs are useful for recording context with decisions that may become unclear over time, or as engineers rotate on and off the project.
Therefore, the best time to write an ADRs is shortly after - or before! - Making the decision it documents.

We also encourage writing ADRs when a decision is made not to do something, as these decisions are often no less significant.

We typically use the markdown ADR format, or [mADR](https://adr.github.io/madr). When Starting a new project or repository, review the mADR documentation.

## Writing a new ADR
to begin a new ADR, check out a branch and copy the template. You can add new ADR's indexed by a simple sequence of integers, e.g. 0001-my-new-adr.md. In busier projects, it may be useful to use a unix timestamp to avoid index collisions when more then ond ADR is being drafted Simultaneously:

```console
cp docs/adr/0000-template.md docs/adr/"$(date %+s)"-my-adr-title.md
```

## Changing an old ADR
In General, once an ADR is added in an "accepted" state, it should not be changed. IF the decision is documents is later reversed, publish a new ADR explaining the decision, and change the status of the old ADR to "superseded" and outlined in the template.
