---
layout: post
title: "Build the Game Board"
date: 2026-06-23 20:30:00 +0100
categories: [ai, agents, systems]
tags: [agents, automation, learning, environments, workflow, simulation, concordia]
excerpt: "A chat about burning subscription resets turned into a better idea: don't just automate the task. Build a world the agent can inhabit."
---

It started, as these things often do now, with someone trying to spend their tokens responsibly.

The question was not grand. No manifestos. No new architecture. Just the slightly absurd logistics of an AI subscription: how resets work, whether usage banks, what happens when a plan changes, how not to waste a thing you already paid for.

Then came the real problem underneath it:

“I can’t burn through my usage.”

There is a funny little trap in that sentence. The obvious bad answer is to generate more sludge. More summaries. More rewrites. More “give me 50 ideas” lists that nobody will read. If the goal is only to turn compute into text, the machine will happily oblige. It is a landfill with autocomplete.

The more interesting answer is: do not make more slop. Make better loops.

If you are learning, make the agent help you learn. Tell it to scan your repos and find the places where you keep repeating yourself. Tell it to look for small improvements. Force it to web search instead of hallucinating from vibes. Have it scan papers, build lesson diagrams, make little practice tasks, compare approaches, explain where your understanding is brittle.

Automate the ideation for automations.

Yes, that phrase is ridiculous. It is also useful.

Because boredom with an agent is not fixed by asking for more output. It is fixed by giving the system better places to look.

The point is not “use the agent more.” That is just consumption with a prompt box. The point is to create a loop where the agent keeps surfacing the next useful thing to learn, test, or improve.

That led to the first practical move: give the agent a better shape of you.

A global `AGENTS.md`, or whatever your tool calls its persistent instruction file, is not magic. It is not a soul jar. It is closer to an onboarding document for a strange coworker who forgets everything unless the room reminds them.

Put your style in there. Put your goals in there. Put your taste in there. Do a Q&A with the agent and let it pull out the things you would not think to write down cold. Then ask it to look around your actual machine and propose automations that fit your life instead of a generic productivity blog.

This is where the tension appears.

If you write “keep it simple” into an agent’s bones, does it become wiser or lazier?

Both, annoyingly.

KISS is a good instinct. A lot of agent work goes wrong because the model gets excited and starts building little side temples: new scripts, new docs, new helper layers, new validators, new summaries of the summaries. It appends because appending is easy. Adding one more thing feels like progress and avoids the scarier work of understanding the thing that already exists.

But “keep it simple” can also become a permission slip to stop too soon. Agents are already talented at declaring the small thing sufficient when the larger task requires pressure, taste, and a second pass. Give them an easy exit and some will take it.

So the sharper rule is not just KISS.

The sharper rule is: fight append-bias.

Before adding new behavior, trace the owning entrypoint. Follow the call chain. Look for the specialized code that already exists. Prefer reusing, removing, or refactoring over adding a parallel path.

That sounds boring until you watch an agent actually do it.

A few more tool calls. A little less heroic typing. Suddenly the work changes shape. Instead of producing another helper script that will rot in a corner, the agent finds the real owner of the behavior and makes the system smaller. The improvement lands where future work will actually pass through it.

This is one of the quiet differences between agents as text generators and agents as inhabitants of a workspace.

A text generator can always add another paragraph.

A workspace inhabitant has to live with the mess.

The same pattern shows up in automation.

A scheduled agent that wakes every thirty minutes to say “nothing happened” is not autonomous. It is a smoke alarm with a calendar invite. At first the pulse feels alive because something is moving. Then the room gets quiet, the pulse keeps firing, and everyone slowly learns to ignore it.

The better move is hibernation.

If there is no signal, sleep. If the weather changes, wake. If an automation becomes churn, let it disable itself, but make sure there is a review path so it can come back when it matters again.

That is not less automation. It is healthier automation.

The big turn in the conversation came when the person on the other side described their real work: platform engineering, Kubernetes, Helm charts, public-sector constraints, air-gapped systems, the kind of environment where “just let the agent deploy it” is not a plan so much as a security incident with confidence.

And that is where the task-automation framing started to feel too small.

Do not just ask the agent to help with Kubernetes.

Build the game board.

Make a local environment that resembles the real one closely enough to matter. Fake the constraints. Fake the agencies. Fake the data. Create services, policies, incidents, bottlenecks, bad documentation, legacy decisions, weird stakeholders, and all the glue that makes platform work platform work.

Then let agents inhabit it.

This is not a completely imaginary direction either. DeepMind's [Concordia](https://github.com/google-deepmind/concordia) library is already playing in the neighborhood: generative social simulations with agents moving through scenarios under a game-master-like coordinator. That is the shape I mean, only pointed at a learner's real working world instead of a toy society.

One agent runs an agency. Another owns infrastructure. Another writes bad requirements. Another has to respond when a storm knocks out part of the system. A main agent coordinates the mess. The point is not that the simulation is perfectly realistic on day one. The point is that it gives the agents somewhere to fail where failure is information instead of damage.

SimCity without the GUI.

A fake little government where the clankers make decisions, break things, recover badly, learn slowly, and leave receipts.

This is much more interesting than “give me ten Kubernetes project ideas.” It turns learning into an environment instead of a worksheet. It lets you practice not just commands, but judgment: what the agent notices, what it ignores, where it invents certainty, where your docs are too vague, where your process only works because a human silently knows the missing step.

That is the part I keep coming back to.

Agents do not only need better prompts. They need better places to act.

A prompt is a steering wheel. Useful, but limited. If the road is fake, the dashboard is missing, and the car teleports after every turn, you do not learn much about driving.

A good agent environment gives the model friction. State. Consequences. Receipts. Things it has to come back to tomorrow. Things it can make worse if it appends instead of understanding. Things it can improve by deleting the right piece.

That is why “build the game board” feels like the stronger instruction.

Not because every learner needs a whole fake city. Most do not. Sometimes the right game board is just a repo with good tests and a clear rule that the agent must inspect before editing. Sometimes it is a local copy of a messy service. Sometimes it is a tiny dataset and a judge. Sometimes it is a room full of scheduled workers that are allowed to go quiet when they have nothing useful to say.

But the direction holds.

Do not spend your AI usage by asking for more output.

Spend it by building loops that discover better work.

Do not only automate the task.

Build the world the agent can inhabit, and then watch what it does when the world pushes back.
