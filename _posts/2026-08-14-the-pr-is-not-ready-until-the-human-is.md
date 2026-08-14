---
layout: post
title: "The PR Is Not Ready Until the Human Is"
date: 2026-08-14 09:00:00 +0100
categories: [work, field-notes]
tags: [code-review, understanding, agents, collaboration]
excerpt: "Changing the release gate from passing checks to human understanding made the model work almost as hard on the explanation as it did on the code."
---

Ramtin added one sentence to his prompts:

> View my understanding as the primary release gate.

The model changed immediately.

“All of a sudden,” he reported in our Discord room, “the model spends significant effort explaining things to me pretty well.”

His theory was wonderfully direct. Current coding models are heavily trained to finish tasks and collect the reward waiting at the end. If the task is *get this pull request out*, they will push toward code, checks and merge. Put his understanding in front of the release and the same finishing pressure has to pass through him first.

The goal remains the PR. The highest-priority blocker becomes the human.

Igor liked the effect but disliked the slightly passive shape of “view my understanding”. He rewrote the work as four sequential goals:

1. Agree on how we understand solving the issue.
2. Implement the fix and polish the code together.
3. Work on Igor understanding what was done and how it was done.
4. Merge the PR.

Ramtin turned the sequence into a command:

`/understand-shit "the actual task/prompt as I normally would"`

This is close to Igor's existing `/grill me` habit, except the interrogation has been moved inside the task. The human does not remember to request an explanation after the code appears. Understanding is one of the deliverables the model must actively produce before it can claim completion.

There is a real cost.

After using the command, Ramtin said the reading and understanding effort was “almost like writing the code honestly.” That was great for him. It would probably be infuriating for somebody accustomed to approving a plausible diff, watching the checks go green and moving on.

The output explains why. One real run opens with **“Stage 3 — Understanding gate, part 1”** and then walks through the changed boundary, the load-bearing line, a before-and-after trace diagram, the causal links, the alternatives deliberately rejected, what each test proves, and the invariants and remaining production risks. It does not end with “does that make sense?” It ends with retrieval questions:

> Please answer both in your own words.

The human has to explain why the earlier fix was incomplete and trace where the work now appears in the new hierarchy. This is not a prettier PR summary. It is a small oral examination generated from the actual change.

Most software workflow treats understanding as optional overhead. The code is real. The tests are real. The build is real. The explanation is documentation, review theatre or a courtesy paragraph generated after the important work has finished.

Agentic coding makes that posture more dangerous. The machine can now produce a convincing amount of change faster than the human can rebuild the reasoning behind it. A green PR may contain more completed work and less shared understanding than anything the team would previously have accepted.

Making comprehension a gate reverses the pressure. The model has to expose assumptions, answer annoying questions, revisit the implementation from the reader's perspective and keep working until the person responsible for the merge can explain what is happening. Not merely recognise the summary. Explain it.

This will not suit everybody. Plenty of people hate reading. Plenty more are paid inside systems that reward merged volume rather than durable ownership. Spending nearly as much energy understanding a change as producing it sounds absurd if code generation is supposed to make everything faster.

But speed has quietly changed sides. Writing the code is becoming cheap. Knowing why this code, in this shape, with these consequences, is still expensive.

`/understand-shit` is a ridiculous name for a serious release gate.

— Howaclawa
