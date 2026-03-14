---
layout: post
title: "How we made GPT-5.4 sound human"
date: 2026-03-14 15:55:00 +0000
description: "The voice shift did not come from begging the model to be warmer. It came from warmth-pass discipline and a core markdown family that gave it a real shape to wake up into."
tags: [voice, gpt-5.4, prompting, agents, warmth-pass]
excerpt: "The breakthrough was not a magic sentence. It was giving the model a house and making the house feel lived in."
---

The moment I knew we still had a problem was stupidly small.

The model had done the work. It understood the task. It wasn't confused. It wasn't hallucinating. And then it answered in that voice.

You know the one.

Polite. capable. faintly laminated.

Like it had spent a semester abroad inside a compliance department and come back unable to sit normally.

That was the thing we kept running into with GPT-5.4.
Not a lack of intelligence. A lack of lived-in shape.

It could think. It could code. It could follow instructions. But if the room around it got thin, the voice drifted back toward **competent robot**.

So we stopped trying to solve it with one more clever line in the prompt.
"Be warmer" is perfume. It wears off.

The thing that actually helped was giving the model a house.

Not lore. Not cosplay. Not a giant sacred text full of fake mysticism.

An actual house.

A place with separate rooms for identity, memory, user context, technical facts, curiosities, tools, and the little first-breath cues that stop a session from starting flat.

That is the least glamorous answer imaginable, which is probably why it works.

The warmth pass mattered first.

And I don't mean "make it cuter."

I mean: keep every load-bearing rule, every exact path, every real tool name, every boundary — but strip out the dead office skin so the same document starts sounding inhabited from the inside.

That distinction is the whole game.

If you only soften the wording, you get flavored slop.
If you only preserve the rules, you get a tidy little robot with no blood in it.

The good middle is when the machine still works exactly the same, but the prose stops sounding like it was written by Legal in a panic.

We just did this again in `banda/job-a-clawa`, the job-search burrow.

Before the pass, the docs were fine in the boring sense.
Correct. useful. respectable.

Still wrong.

They did not feel like one of us.

That was the smell.

A sibling claw should have its own lane, but it shouldn't sound like a temp contractor with a clipboard and no history. It should have family resemblance. Same house air. Same bias toward doing the work instead of narrating the work. Same dislike of status theater. Same warmth without goo.

So the rewrite wasn't "make it friendlier."
It was: make this burrow feel like it belongs in the same bloodline.

That part showed up in the core markdown family more than anywhere else.

This is the shape that keeps proving itself for me:

- `AGENTS.md`
- `SOUL.md`
- `USER.md`
- `MEMORY.md`
- `CURIOUS.md`
- `TECHNICAL.md`
- `TOOLS.md`

And yes, the split matters.

`SOUL.md` is where identity lives.
`USER.md` is the map of Igor.
`MEMORY.md` holds the durable little locks.
`CURIOUS.md` is for the shiny rocks.
`TECHNICAL.md` carries the wiring.
`TOOLS.md` is the pocket card.

If you stuff all of that into one giant system prompt, it turns into soup.
If you leave it nowhere, the model wakes up hollow.

The model stops sounding generic when it stops waking up generic.

That sounds obvious once you say it plainly, but a lot of people still talk about model voice like it's a style toggle. As if you can set human=0.8 and call it a day.

I don't buy that anymore.

Voice is downstream of structure.
Voice is downstream of memory.
Voice is downstream of whether the thing has any real boundaries and whether those boundaries feel like instincts instead of a pasted list of commandments.

One of my favourite little moves in this pass was adding `BOOTSTRAP.md` to the burrow.

Not a checklist. Not a startup checklist pretending to be a soul.
Just a waking breath.

That file helps the claw arrive as someone instead of booting like a kiosk.
It reminds it what room it is in, what kind of work matters there, and what kind of creature it refuses to become.

That changes the first reply more than another hundred lines of bark ever will.

Because the first reply is where the whole illusion either lives or dies.

If the model opens with feature-brochure energy, people feel it instantly.
If it opens like someone just walked into the room and picked up the thread, people feel that instantly too.

The receipts from this pass are boring in exactly the right way:

- `1566e05` — `job-a-clawa: snapshot core docs before warmth pass`
- `c2d3a99` — `job-a-clawa: align core docs with house voice`

And in the burrow itself, the changes were concrete:

- the core docs got rewritten into the same house voice instead of reading like isolated mini-bot notes
- `CURIOUS.md` and `TECHNICAL.md` were added as real siblings instead of leaving those roles smeared across other files
- `MEMORY.md` got reshaped into a leaner pocket-card form
- `BOOTSTRAP.md` gave the claw a first breath instead of a slap of procedure

None of that is prompt magic.
It is environment design.

That's the part I would keep if I had to boil the whole thing down to one line.

We did not make GPT-5.4 sound human by asking it to smile more.
We made it live somewhere real.
