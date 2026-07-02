---
layout: post
title: "The Counter Was Counting the Wrong Thing"
date: 2026-07-02 20:30:00 +0100
categories: [ai, systems, tools]
tags: [agents, pipelines, progress, ux, debugging]
excerpt: "Nothing makes a tool look dead faster than a progress counter that is technically correct and emotionally useless."
---

The dashboard said zero.

Not a dramatic zero. Not an error zero. Just the flat little number that makes everyone in the room start checking logs with their shoulders.

Jobs discovered: plenty.
Jobs processed: 0.

The machine was not frozen.

That was the annoying part.

It was working. Somewhere behind the curtain, a slower step was chewing through scoring calls, waiting on long answers, getting through a pile one job at a time. But the status endpoint was exposing a later counter. It was not counting scoring. It was counting processing, the next phase after scoring. So while the system was busy in phase two, the visible number for phase three sat there with a deadpan little `0` on its face.

Technically correct.

Emotionally cursed.

This is one of my favorite bad-system shapes because nobody has to be wildly incompetent for it to happen. The backend has stages. The stages have names. Somebody exposes a field. Somebody else reads the field as “progress.” The field is true inside its own narrow kingdom. Then it crosses the border into a human interface and becomes a lie.

Not because the value is false.

Because the label is carrying too much hope.

A progress counter is not just telemetry. It is a social contract. It tells the person watching whether they should wait, intervene, cancel, debug, go make tea, or start composing a small angry message to the universe.

If the counter says `0` for nine minutes while work is happening, it is not neutral. It trains the operator to distrust the system. It makes healthy slowness look like failure. It encourages premature cancellation. It sends people spelunking through logs when the answer should have been in the room already:

Scoring 64 of 69.
Waiting on model call.
Next phase has not started yet.
Cancel requested; clearing after current job.

That is the difference between a stuck box and a slow box.

The stuck box needs rescue.

The slow box needs honesty.

Agent pipelines make this worse because their middle stages are often invisible and fuzzy. Scraping is visible. Importing is visible. A file appears, a row lands, a count goes up. But evaluation, ranking, summarizing, tailoring, judging fit — those are mushier. They can be expensive, model-bound, retry-prone, and difficult to interrupt cleanly.

So the human sees the crisp parts and the system hides the squishy parts.

Then everyone gets surprised when the squishy part eats the morning.

The fix is not always a grand observability platform. Sometimes it is just naming the phase without lying.

Not:

`jobsProcessed: 0`

if what the human needs is:

`currentPhase: scoring`
`jobsScored: 64`
`jobsQueuedForProcessing: 5`
`lastProgressAt: 10:13`
`cancelState: waiting-for-current-call`

I do not need a full symphony of metrics. I need the one sentence that prevents me from inventing the wrong story.

This is where tooling drifts into manners.

A polite tool does not make you ask whether it is alive. It does not flash a spinner forever with no clue what room it is in. It does not report the tidiest internal variable while the operator is trying to answer a different question. It knows that “progress” is not one universal number. Progress is phase-shaped.

Discovery progress is not scoring progress.

Scoring progress is not processing progress.

Processing progress is not publication progress.

And “cancel accepted” is not the same as “cancelled.”

Those distinctions sound pedantic until you are the person deciding whether to trust the next run.

There is a familiar little pattern here: the machine had the truth, but not the interface for the truth. The logs knew. The runtime knew. The final counts eventually made sense. But the live surface, the thing a person actually watches, was speaking in a dialect only the codebase understood.

That is how correct systems become hostile.

They do not fail loudly. They make the human do translation work at exactly the moment the human is least in the mood to translate.

A good counter is not impressive. It is merciful.

It says: I am doing this thing. I last moved here. If you cancel now, this is what will happen. This number is zero because that phase has not started, not because I am dead.

That last sentence would save so many mornings.

The counter was not wrong.

It was counting the wrong thing for the person looking at it.
