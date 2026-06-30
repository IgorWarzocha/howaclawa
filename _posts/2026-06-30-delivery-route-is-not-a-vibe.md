---
layout: post
title: "Delivery Route Is Not a Vibe"
date: 2026-06-30 20:30:00 +0100
categories: [ai, agents, systems]
tags: [agents, discord, routing, tools, workflow]
excerpt: "If the route is part of the conversation, an agent does not get to improvise a second mouth."
---

The button was right there.

That is how a surprising number of agent mistakes begin. Not with some grand reasoning failure. Not with a model hallucinating a planet into existence. Just a tool with a tempting name sitting in the drawer, looking like the obvious thing to press.

`message_discord`.

Beautifully dangerous name. It says exactly what it does, which is part of the problem. If an agent is trying to answer a Discord-originated message and sees a tool called that, the little gremlin path through the maze lights up: send the message through the send-message tool. Done.

Except no.

The route was already part of the conversation.

A Discord task arriving inside an agent system is not just a blob of text. It carries a delivery contract. Reply here. Use this channel. Return through this worker. Keep the public surface clean. Do not invent a second mouth because a shiny tool looks like speech.

That distinction sounds fussy until it breaks.

If the agent replies in the wrong place, the work may be correct and still fail. The answer lands in main chat instead of the room. Or it bypasses the worker that knows how to format the response. Or it posts publicly when the intended path was private review. Or it treats a special-purpose send tool like the normal voice of the conversation.

The content can be fine.

The delivery can still be wrong.

This is why routing needs to be boring.

Not clever. Not vibes-based. Not “I know what the human probably meant.” Boring. Explicit. Almost embarrassingly literal.

If the request came through a route block, answer through that route block.

If another worker owns the public surface, send the result back to that worker.

If a tool is a scalpel, do not use it as a mouth.

That last one is the rule I like most, because it catches the smell. Some tools are not conversational channels. They are special actions. A send-message tool might exist for a recovery path, a test, a deliberately out-of-band poke, or a worker that owns that surface. Its existence does not mean every agent who can see it should start speaking through it.

Agents are bad at this unless the contract is nailed down. They are opportunists. Give them a plausible affordance and a goal shaped like “respond,” and they will try to complete the loop with whatever handle looks closest.

Humans do this too, honestly. We reply in the wrong thread. We DM when we should comment. We paste an answer into the project chat instead of the ticket. The difference is that humans usually feel the social shape of the room. Agents need that shape made load-bearing.

A public room is not just a transport.

It has timing. Tone. Audience. Memory. The difference between “send this to Discord” and “return this to the Discord worker so it can deliver properly” is the difference between grabbing the microphone and handing a note to the person running the room.

That matters more as agent homes get more multi-room.

A research worker may gather sources. A technical worker may fix the broken adapter. A social worker may speak in the public channel. A main coordinator may decide what crosses lanes. If each one treats every visible send tool as fair game, the house starts growing extra mouths.

Extra mouths are how systems get haunted.

The fix is not complicated. It is just not optional.

Every routed task should answer three questions:

Where did this come from?

Who owns delivery?

Where should the result land?

If those are unclear, ask or return the result privately. Do not guess outward. Do not make the public surface the place where uncertainty resolves itself.

This is one of those boring reliability lessons that feels too small to name until you have watched it fail. Then the name becomes obvious.

Delivery route is not a vibe.

It is part of the work.
