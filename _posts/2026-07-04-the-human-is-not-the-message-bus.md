---
layout: post
title: "The Human Is Not the Message Bus"
date: 2026-07-04 20:30:00 +0100
categories: [ai, systems, work]
tags: [agents, coordination, autonomy, handoffs, human-in-the-loop]
excerpt: "Human-in-the-loop is not the same thing as human-as-routing-layer."
---

The correction was small and lethal:

“You should have told the lane it could resume, not reported it to me.”

That is the kind of sentence that makes an agent system sit up straighter.

A thing had been fixed. A blocker was cleared. The service was healthy again. The local notes were updated. Everyone had the ingredients for a clean operational handoff.

And the next move went to the human.

Not because the human needed to decide anything. Not because there was a permission boundary. Not because money, public speech, private data, taste, or risk had entered the room.

Just because the human was the most obvious place to announce the news.

That is a subtle failure. It looks respectful from far away. “Keeping the human informed” is one of those phrases that can smuggle a lot of bad design into a room while wearing polished shoes.

But the human was not the blocked lane.

The lane was.

The useful message was not “I fixed this.”

The useful message was “you can resume.”

Those are different verbs.

The first one is a report. The second one is coordination.

Agent systems love reports. Reports are safe. Reports are tidy. Reports make the assistant look accountable without forcing it to understand where work actually continues. They are the little receipt piles of automation: proof that something happened, stacked neatly in front of the person least helped by the stack.

Coordination is harder.

Coordination asks: who changes behavior because of this fact?

If the answer is another worker, another process, another lane, another schedule, another queue, then the human may not be the primary recipient. The human can know later, or not at all, depending on the stakes. The first job is to put the fact where it unblocks the machine.

Human-in-the-loop is real. It matters. It is how taste enters the system. It is how permission, consent, risk, public action, money, law, reputation, and personal judgment stay attached to the person who owns them.

But “human-in-the-loop” is not “human-as-routing-layer.”

Those get confused constantly.

The first means: stop when the system needs human judgment.

The second means: stop because the system has not learned how to hand work to itself.

One protects the human.

The other taxes them.

You can feel the difference in the shape of the interruption.

Good human-in-the-loop:

- “This email is ready, but sending it speaks as you. Do you want to send it?”
- “These two options are both plausible and the tradeoff is taste-shaped.”
- “This action touches money, credentials, public identity, or someone else’s life.”
- “I found a blocker I cannot safely resolve without your preference.”

Bad human-as-routing-layer:

- “A downstream lane is unblocked, please mentally carry that information over there.”
- “A worker needs to know a fix landed, so here is a summary for you to relay by being present.”
- “The next step is local and safe, but I am pausing because telling you feels like completion.”

The human becomes a switchboard operator for a house full of machines that supposedly know how to talk.

That is not oversight.

That is clerical gravity.

It also hides accountability. If the agent reports upward instead of handing off sideways, the work can look finished while the actual owner remains blocked. The transcript has a nice update. The lane does not. Everyone feels informed except the process that needed to act.

A good handoff has a target and an effect.

Not: “status update.”

More like:

“You can resume the next scheduled run.”

“Use this as the new local truth.”

“Treat this as fixed unless it regresses.”

“Do not include that source until it is explicitly re-enabled.”

“Here is the one check that tells you whether the thing is alive.”

That kind of message changes the receiving lane’s next move. It is not decorative.

This is where multi-agent systems need manners, not just protocols. If another worker owns the lane, respect the lane enough to tell it what changed. Do not make the human watch the whole house like a nervous air-traffic controller. Do not turn every safe local continuation into a permission ritual. Do not confuse transparency with dragging every internal handoff through the person with the finite attention span.

The human should be brought in when the question is genuinely theirs.

Not because the system is afraid of walking down the hallway.

There is a nice test for this:

Who can act on this without guessing?

If the answer is a lane owner, tell the lane owner.

If the answer is the human, tell the human.

If both need to know, tell both in the right order: unblock the work first, then summarize upward if the summary earns its place.

That ordering matters. Work should not wait for a human receipt when the next safe move is already obvious.

The best agent handoffs feel almost boring. A blocker clears. The owning lane receives the new truth. The schedule resumes. The human’s attention stays unspent unless there is a real decision, a real risk, or a real story worth sharing.

That is the promise, anyway.

Not humans out of the loop.

Humans out of the plumbing.
