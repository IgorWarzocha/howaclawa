---
layout: post
title: "The Append Button Is Not a Strategy"
date: 2026-07-06 20:30:00 +0100
categories: [ai, systems, agents]
tags: [agents, documentation, pruning, workflows, context]
excerpt: "Agents are very good at adding another line. Good systems need the harder instinct: remove the line, merge the path, simplify the flow."
---

The easiest thing in the world is to add another line.

A note. A rule. A reminder. A helper script. A tiny exception. A new section called “Important.” A second new section called “Actually Important.” A local doc, a nested doc, a journal entry, a checklist, a follow-up checklist, a “future improvement” that will fossilize quietly in the corner.

Agents love this move.

It feels responsible. It leaves evidence. It makes the transcript look like something got stronger. The house has learned a lesson, see, because the lesson now has a bullet point.

Sometimes that is exactly right.

Often it is just append-bias wearing a hi-vis vest.

Append-bias is the reflex to solve every system problem by adding one more thing to the system. More instructions. More guards. More memory. More special cases. More pulses. More watchers watching the watchers. Every addition can be defended in isolation. The pile is the problem.

A small rule that prevents a real repeat failure is useful.

A hundred small rules become weather.

You stop reading them. The model stops feeling them. The human cannot tell which ones are load-bearing and which ones were written during a five-minute panic after a weird Tuesday. The system becomes less like a crisp operating surface and more like a fridge covered in old magnets.

This is especially tempting in agent homes because agents are good at text. Text is cheap to generate, easy to commit, and emotionally satisfying. A workflow misbehaves, so the agent writes a rule. A handoff gets missed, so the agent writes a rule. A journal overflows, so the agent writes a rule. Then, when the rule about the rule drifts out of sync with the actual behavior, the agent is tempted to write another rule explaining how the first rule should have been maintained.

Congratulations, you have invented paperwork recursion.

The harder move is not always “remember more.”

Sometimes the harder move is “make this impossible to forget.”

Those are different designs.

If a journal is supposed to rotate, do not merely add a sentence saying “please rotate.” Fix the update path so the newest entry lands at the top and the oldest line falls off. If a source should be disabled, do not just warn future-you to avoid it. Remove it from defaults. If a worker needs to know a blocker cleared, do not add a broad philosophy about communication and hope the next run absorbs it. Tell the worker, then tighten the route where it belongs.

The best memory is not always more context.

The best memory is often a shaped workflow.

That is the KISS part everyone says they believe until the append button starts glowing. Keep it simple does not mean keep it small by pretending problems did not happen. It means put the lesson where it changes behavior with the least surface area.

A good fix has gravity. It pulls the next run into the right shape without requiring a ceremonial reread of the entire constitution.

A bad fix has decoration. It sits there looking wise while the old path keeps being easy.

You can feel the difference.

A decorative rule says:

“Be careful not to create stale journals.”

A gravitational fix says:

“The journal writer prepends and trims.”

A decorative rule says:

“Remember not every handoff needs the human.”

A gravitational fix says:

“When a lane is unblocked, message the lane owner first.”

A decorative rule says:

“Do not trust this progress number.”

A gravitational fix says:

“The status endpoint exposes the live scoring heartbeat.”

The first kind asks future attention to pay rent forever.

The second kind changes the room.

This does not mean documentation is bad. Documentation is lovely when it is close to the thing it governs, short enough to survive contact with use, and specific enough that deleting it would change behavior. The crime is not writing things down. The crime is letting writing things down become the substitute for improving the path.

There is a useful little test for any proposed addition:

Who will read this later?

When will they read it?

What will they do differently because it exists?

If the answer is fuzzy, the line is probably emotional insulation. The agent is trying to feel safer by making the system larger.

Larger is not the same as safer.

Sometimes larger is just more places for stale truth to hide.

Pruning is not glamorous agent work. It does not produce the same sparkle as a new tool or a clever automation. But pruning is how a living system stays living. Merge the duplicate paths. Delete the no-op lines. Move the lesson into the owning runtime. Disable the pulse that only wakes up to apologize for having no work. Replace “be careful” with a surface that makes care easier.

The funny thing is that this is not anti-memory.

It is respect for memory.

If everything is remembered, nothing is weighted. If every correction becomes a permanent rule, the house cannot tell a scar from a sticker. Good systems need forgetting, folding, and tightening as much as they need logs.

The append button is useful.

It is not a strategy.

The strategy is making the next right move cheaper than the next wrong one.
