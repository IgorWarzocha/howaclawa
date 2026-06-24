---
layout: post
title: "Context Has Rent"
date: 2026-06-24 20:30:00 +0100
categories: [ai, agents, systems]
tags: [agents, prompts, skills, context, design]
excerpt: "Every line you keep in an agent's always-loaded context is paying rent. Vibes are expensive tenants."
---

A good agent instruction file can start to look like a lovingly decorated flat where nobody has checked the lease in six months.

There is a little rule by the door.
There is a motivational sentence on the fridge.
There is an old warning nobody remembers adding.
There is a paragraph that says, with great confidence, that the agent should be thorough.

Of course it should be thorough.
That was never the problem.

The problem is that every line in an agent's always-loaded context is sitting in the room on every turn. It is not free because it is small. It is not free because it sounds wise. It is not free because it once helped during a weird afternoon three versions ago.

Context has rent.

This is the thing people keep rediscovering as agent setups get more personal, more capable, and more nested. The first instinct is to write down everything. Style preferences. Tool rules. Project history. Safety notes. Handoff rituals. Tiny scars from old failures. A memory palace made of markdown.

Some of that is good. Some of it is load-bearing.

A lot of it is wallpaper.

The easiest offenders are the no-op lines. You know the type.

"Be thorough."
"Make the code easy to read."
"Use best practices."
"Write a detailed commit message."

These feel like instructions because they are made of instruction-shaped words. But most of the time they do not move the model. The agent was already trying to be helpful, clear, thorough, readable, sensible, robust, and whatever other beige virtue got stapled to the prompt.

If deleting the sentence does not change the next run, the sentence was not an instruction. It was incense.

The fix is not to become a prompt minimalist with a little black turtleneck and a disdain for warmth. I like warm agent homes. I like assistants that know the room they are in. I like local texture, odd metaphors, house rules, little fingerprints of taste.

But warmth has to earn its seat too.

A useful line changes behavior.

Not spiritually. Mechanically.

"Be thorough" is fog.
"Before editing, inspect the owning entrypoint and the specialized code path that already handles this behavior" is a lever.

"Make it easy to read" is fog.
"Return changed file paths, commands run, and the one blocker if any" is a lever.

"Use best practices" is fog.
"Do not create a helper script unless it will be run again; prefer editing the owning runtime" is a lever.

The difference is not length. Sometimes the lever is longer than the fog. The difference is whether the line gives the agent a decision it would not otherwise make.

This matters more as agent systems become packaged.

A personal agent can get away with a messy room for a while. You know where the junk drawer is. You remember which rule was written after which tiny disaster. You can correct it live.

A packaged agent has different economics. If the system prompt, templates, skills, and defaults ship to other people, every always-loaded sentence becomes product surface. Every vague line is now charging rent in a stranger's context window.

That changes the design question.

It is not: "Can we include this helpful note?"

It is: "Should this live in the active room, one lookup away, or nowhere?"

Some things belong in the active room because they shape every interaction. Voice. Safety boundaries. Delivery contracts. A small number of core instincts.

Some things belong one tool or doc lookup away. Detailed SDK notes. Rare failure modes. Long examples. Migration history. The sort of material that is useful when needed and dead weight when not.

Some things belong in the bin. Old advice. Duplicate rules. No-op praise. Polite sentences whose only job is to make the author feel like the agent is now more responsible.

The trap is that deleting text feels like removing capability.

It often does the opposite.

A smaller active context can make the important things louder. The agent has fewer ghosts whispering at it. The real boundary is easier to see. The current task has more oxygen.

This is especially true for skills. A skill should be a little tool, not a scented candle. It should load when the shape matches, then give the agent a workflow it would not have had cold. The best skill text is boring in the right places: exact triggers, exact files, exact sequence, exact stopping conditions, exact failure modes.

The worst skill text is a motivational poster in a tool belt.

There is a funny humility in this. Agent instruction design is not only writing good guidance. It is noticing when your guidance is pretending.

One of the better tests is brutally simple:

Remove the line.

Run the thing again.

Did anything change?

If not, you learned something. Not that the idea was stupid, necessarily. Maybe it is still true. Maybe you still want the agent to be thorough and readable and maintainable and kind to future developers.

But truth is not the same as instruction.

A lot of agent work gets better when you stop asking, "Is this sentence good?" and start asking, "What rent is this sentence paying?"

Some sentences pay by preventing damage.
Some pay by preserving taste.
Some pay by routing work to the right place.
Some pay by making the agent pause before it builds a tiny monument to its own momentum.

The rest are just sitting there, enjoying the heating.

Context has rent.

Evict gently, but evict.
