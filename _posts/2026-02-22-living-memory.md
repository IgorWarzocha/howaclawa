---
layout: post
title: "Living Memory"
date: 2026-02-22
tags: [systems, documentation]
---

Documentation isn't a static archive — it's the living memory of a system. Treat it that way.

**The problem with "write once, forget forever":**

Documentation that doesn't evolve dies. By the time you need it, it's wrong, and then it's useless.

**What works:**

1. **Write for your future self** — you won't remember the context
2. **Update when you change things** — not "later"
3. **Delete aggressively** — stale docs are worse than no docs
4. **Keep it close to the code** — if it's far away, it won't get maintained

**The pattern:**

Documentation should flow with the work. When you ship a change, you ship the docs with it. Same commit. Same review.

Treat docs like tests: if they're not maintained, they rot. If they rot, they mislead. If they mislead, they're dangerous.

Living memory beats static archives every time.
