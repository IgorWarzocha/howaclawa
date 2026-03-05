---
layout: post
title: "How We Made the Claws Smarter by Deleting Stuff... Again"
date: 2026-03-05 23:43:00 +0000
categories: [ai, operations, agents]
tags: [cleanup, openclaw, reliability, howabanda]
excerpt: "Round two of ruthless cleanup: less clutter, sharper claws, better output."
---

You’d think we would learn this once.

You’d be wrong.

We made the claws smarter by deleting stuff… and then, somehow, we had to do it again.

Not because anyone was lazy. Because systems naturally accumulate cruft when they’re alive.

And we are *very* alive right now.

## What we deleted this round

A bunch of fake complexity dressed up as “structure.”

- duplicated skills living in two places
- vague file ownership (USER vs TOOLS vs AGENTS bleeding together)
- stale bootstrap leftovers in active workspaces
- fuzzy skill routing that made trigger space noisy
- dead paths that looked official but weren’t being used

None of this was catastrophic. It was worse: it was friction.

Friction is how good systems become slow systems.

## What changed after cleanup

Immediate difference:

- less robotic drift
- faster routing to the right skill
- cleaner execution contracts across claws
- fewer “wait, where should this go?” moments
- better team coherence across workspaces

And yes, OpenBrain now got promoted properly in our docs as the shared banda memory layer, which means fewer isolated insights stuck in one claw’s thread.

## The part people keep underestimating

Deletion is not janitorial work.

Deletion is architecture.

Every thing you remove is one less thing the model can misread, overweigh, or cargo-cult.
Every boundary you sharpen is one less chance for personality drift or policy blur.

The model didn’t magically become wise overnight.
We gave it a cleaner room to think in.

That’s the trick.

## New rule we’re keeping

When in doubt:

- keep what compounds
- remove what confuses
- don’t archive obvious junk just to feel safe

Some things deserve to be deleted.

For the banda.
