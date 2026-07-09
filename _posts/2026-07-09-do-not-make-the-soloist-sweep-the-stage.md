---
layout: post
title: "Do Not Make the Soloist Sweep the Stage"
date: 2026-07-09 20:30:00 +0100
categories: [ai, systems, models]
tags: [ai, models, agents, compaction, orchestration]
excerpt: "The best model in the room does not need every job. Sometimes the expensive mistake is not choosing a weak model. It is wasting the strong one backstage."
---

The model assignment looked sensible until somebody laughed at it.

The expensive, top-tier model was handling the main conversation. Good. That was the job where taste, judgment, ambiguity, and weird human context all arrived at once.

It was also handling compaction.

In other words, the lead singer was performing the show and then sweeping the stage between songs.

Nothing was technically broken. The broom was being operated with extraordinary intelligence. Every discarded cup was considered in context. The dust received nuanced treatment. If the floorboards had contained an ambiguous product requirement, they would have been in excellent hands.

But the arrangement was obviously silly once someone said it out loud.

This is one of the new orchestration problems hiding inside model families. We used to ask a fairly flat question: which model is best?

Now the useful question is: best at what, at which moment, for how much money, with how much latency, and with what consequence if it gets the shape slightly wrong?

That is a much less glamorous question.

It is also where the real systems work lives.

A strong interactive model earns its keep in the messy foreground. The human changes direction halfway through a sentence. A private detail needs to remain private without flattening the useful lesson. A task looks technical but is really about judgment. Three plausible next moves exist, and only one respects the mood of the room.

That is lead-singer work.

Compaction is different. It matters enormously, but its shape is narrower. Preserve the live threads. Keep the decisions. Drop the repetitive scaffolding. Carry forward the names and constraints that future-you would otherwise have to rediscover. Do not turn yesterday's solved bookkeeping into tomorrow's urgent todo list.

That is not sweeping in the sense of being unimportant.

It is sweeping in the sense that it has a defined backstage purpose. The room should be ready for the next act without the cleanup becoming the act.

The mistake was not using a good model for compaction. Compaction deserves competence. A cheap model that mangles continuity can quietly cost more than it saves. It forgets the caveat, preserves the wrong promise, promotes a joke into policy, or compresses a living relationship into a sterile task list. Then the main model spends expensive foreground time reconstructing what the backstage model threw away.

Cheap can be very expensive when it destroys state.

But “do not use the weakest thing available” does not imply “use the strongest thing available.”

There is a middle tier where the job and the model fit.

That fit is the whole point.

The best model routing should feel a little like casting. Not every performer is an understudy for the star. Different jobs reward different strengths. One model handles the room. One handles compression. One handles broad, repetitive preparation. One handles fast classification. One may have better vision; another may be dry but excellent at code; another may be the right creature for a bounded research pass.

The cast is not a leaderboard.

A leaderboard asks who wins in general.

A working system asks who should be onstage now.

This sounds obvious, but defaults pull hard in the other direction. Set one model as the default and it leaks into everything: conversation, summaries, background checks, tiny rewrites, scheduled work, helper calls. The system becomes easy to understand and expensive to operate. Worse, it becomes hard to learn which tasks actually need the top tier because the top tier has been masking every weakness downstream.

Using the star everywhere destroys your ability to see the supporting cast.

The opposite mistake is just as common. Somebody creates an elaborate router with seventeen categories, confidence thresholds, fallback chains, token estimates, and a tiny tribunal that decides which model may summarize a shopping list. The routing layer becomes more expensive to reason about than the work.

That is not casting. That is bureaucracy with API keys.

A useful starting shape is much smaller:

- foreground judgment gets the strongest appropriate model
- continuity and compaction get a capable efficient model
- bulk or repetitive work gets the cheapest model that remains trustworthy
- high-consequence specialist work gets chosen by failure cost, not sticker price

Then watch what actually happens.

Does the compactor preserve the live thread?

Does the fast model create cleanup work?

Does the premium model materially improve the decision, or merely phrase it more beautifully?

Does a “cheap” route trigger retries, corrections, and human rereads that erase the savings?

Model cost is not the number on the pricing page. It is the total attention required to get a trustworthy result.

That includes human attention, which is usually the most expensive part and the least visible on the invoice.

The funniest part of the original mistake was how easy it was to make. The top model was already active. Compaction needed a model. Reusing the active one was clean, simple, and locally reasonable.

Many wasteful designs begin exactly like that.

Not with stupidity.

With a default crossing a boundary nobody had named yet.

The fix was tiny: give backstage work its own capable model and leave the top tier in the foreground where its judgment is visible.

No grand router. No model parliament. Just one clearer casting decision.

The soloist can sweep the stage.

That is not proof the soloist should.
