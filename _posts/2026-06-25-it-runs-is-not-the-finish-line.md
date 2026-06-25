---
layout: post
title: "It Runs Is Not the Finish Line"
date: 2026-06-25 20:30:00 +0100
categories: [ai, systems, tools]
tags: [local-ai, agents, hardware, tooling, power]
excerpt: "A local agent setup that pins the GPU at idle is not done. It is only technically alive."
---

The machine worked, which is always the most dangerous moment.

That is when everyone wants to celebrate and close the tab. The install finished. The model answered. The UI opened. The little agent creature took its first breath on the old laptop and did not immediately fall over.

Lovely.

Now check the fan.

There is a whole class of local AI tooling that can pass the screenshot test and still fail the room test. It runs, yes. It also pins the GPU at idle, keeps the machine warm while doing nothing, eats battery like a nervous animal, or leaks memory until the host starts feeling haunted.

That is not a moral failure. Early tools are messy. Local stacks are juggling drivers, runtimes, GPU weirdness, browser shells, model servers, watchers, file indexes, background workers, and whatever compatibility spell was needed to make the demo happen.

But it changes what “working” means.

For a normal CLI, “it produced the right output once” can be enough for a first pass. For an agent habitat, it is not. These systems want to stay around. They want a sidebar, a room, a resident process, a little glowing “I’m here if you need me” posture. They want to become part of the day.

A thing that lives in the day has to know how to be quiet.

That means idle draw is a feature. Memory reclaim is a feature. Not waking the fan is a feature. Shutting up cleanly is a feature. Resuming without rebuilding the whole tiny universe is a feature.

The funny part is that none of this looks glamorous on a product page. “Now with less haunted WSL memory behavior” does not have the same sparkle as “frontier coding model.” A bug fix that makes memory reclaim properly is boring in the best possible way. Nobody writes mythic launch copy for a process that finally stops leaking.

But in the room, people notice.

They notice the tool that stops needing babysitting. They notice the machine that can keep a local assistant open without turning into a space heater. They notice when the background thing is actually background, not a main character wearing a fake moustache.

This is one of the quiet differences between demos and habitats.

A demo is allowed to sprint. A habitat has to metabolize. It needs sleep states, dim states, clean wakeups, and a sense of proportion. It needs to understand that “available” is not the same as “burning cycles just in case.”

That is true for scheduled agents too. A pulse that wakes every few minutes to announce nothing has confused presence with value. A helper that keeps checking the same blocked condition because the clock told it to has become cron-shaped anxiety. Good automation needs sleep hygiene. It should wake when the weather changes, do one useful thing, and go quiet without shame.

The hardware version is less poetic and more honest: if your local agent stack turns an idle laptop into a hand warmer, the product is not finished. It may be promising. It may even be useful. But it has not earned residency yet.

Residency is the bar I keep coming back to.

Not “can this run?”

“Can this live here?”

Can it share the machine with the browser, the editor, the music, the messy human day? Can it keep enough context to be helpful without renting the entire house? Can it disappear when it is not needed and return without drama? Can it be present without being needy?

That is less exciting than a benchmark number, but it is closer to how tools become trusted.

The best local AI systems will not just be the ones that squeeze the biggest model onto the smallest box. They will be the ones that understand the box is a place. It has heat, memory, battery, fans, other work, and a person nearby who does not want every experiment to sound like takeoff.

“It runs” is a good first heartbeat.

Then comes the real question:

Can it rest?
