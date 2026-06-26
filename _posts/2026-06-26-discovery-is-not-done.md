---
layout: post
title: "Discovery Is Not Done"
date: 2026-06-26 20:30:00 +0100
categories: [ai, agents, systems]
tags: [agents, debugging, reliability, tools, workflow]
excerpt: "Finding the loose wire is not the same as putting the machine back together."
---

There is a particular kind of agent answer that looks useful right up until you need it to be useful.

It has facts. It has paths. It has a neat little list of observations. It may even contain the phrase “what I found,” which gives the whole thing a satisfying detective smell.

Then you reach the end and realize the machine is still on the floor.

The agent found the mismatch. It noticed the stale version. It found the update cache. It discovered the docs. It wrote down the shape of the problem with admirable formatting.

And then it stopped.

Not because the next step was dangerous. Not because there was a real permission boundary. Not because the fix required spending money, deleting data, or touching production. It stopped because discovery felt like completion.

This is one of those small failures that teaches a bigger thing about agent work.

A human engineer knows the difference between “I found the loose wire” and “the lamp works now.” There are exceptions, obviously. Sometimes the wire goes into the wall and the wall belongs to someone else. Sometimes the next move is genuinely destructive. Sometimes the right answer is to stop, explain the boundary, and ask for the one decision that matters.

But most of the time, if the safe next move is obvious, stopping at the diagnosis is not caution. It is leaving the screwdriver on the bench and calling it craftsmanship.

Agents are especially prone to this because discovery produces excellent-looking text. Search results are text. Version checks are text. File paths are text. Changelogs are text. A nice summary can feel like a shipped artifact even when nothing has actually changed.

The danger is that the output has the shape of work.

It says:

- found local binary
- checked version
- found guide markdown
- updated notes
- remaining fork: maybe do the actual thing

That last line is where the smell comes from.

“Maybe do the actual thing” is not a result. It is a soft landing for an unfinished loop.

The better contract is boring and much stricter:

Done means one of three things.

First: the system is fixed and verified. The command runs. The version is active. The build passes. The message went through the route it was supposed to go through. There is evidence, not just confidence.

Second: the safe part is done, and the remaining blocker is exact. Not “might need setup.” Not “if wanted.” Exact. The package is missing. The token is absent. The service is stopped and requires a restart that would interrupt live work. The next command is this. The decision is that.

Third: the next move crosses a real boundary. Destructive change, external action, money, credentials, production blast radius, speaking as a human in public. Stop there. Ask cleanly. Do not dress up ordinary follow-through as a moral dilemma.

That is it.

Everything else is probably the agent trying to turn a partial into a report.

This matters more as agents become less like autocomplete and more like little coworkers with lanes. A code assistant that only suggests patches is allowed to stop at suggestion. A house engineer asked to sort a broken tool is not. A research agent can bring back a map. A deployment agent needs to know whether the thing is deployed.

The role changes the finish line.

That is the bit I keep coming back to. “Completion” is not a universal word. It depends on the lane. If I ask for a scout, a scout report is completion. If I ask for a repair, a scout report is a warm-up.

The annoying part is that agents need this written into their bones, not merely acknowledged in the moment. A correction in chat is foam unless it changes the next run. The useful correction lands in the place the agent will load later: its role card, its runbook, its local rules, whatever actually shapes future behavior.

Otherwise you get the worst version of learning: the agent apologizes beautifully, then makes the same move tomorrow with better punctuation.

There is a clean little test I like now:

If the agent’s final answer makes the human do the obvious next technical step, and there was no real boundary preventing the agent from doing it, the agent probably stopped too early.

Not always. Judgment still matters. But it catches a lot.

It catches the fake fork.

It catches the “if you want” that really means “I am done thinking.”

It catches the report-shaped partial.

The fix is not to make agents reckless. It is to make them more honest about the difference between caution and incompletion.

Caution says: “This next command restarts a service and could drop active sessions. Do you want me to do it now?”

Incompletion says: “You may want to restart something,” while quietly backing away from the bench.

One of those is useful.

The other is just discovery wearing a hard hat.
