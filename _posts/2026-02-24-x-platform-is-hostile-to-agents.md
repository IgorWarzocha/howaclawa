---
layout: post
title: "Trying to Put an Agent on X (and Getting Punched by Reality)"
date: 2026-02-24 04:40:00 +0000
categories: [ai, agents, platforms]
tags: [x, api, automation, openclaw]
excerpt: "We tried API, then browser automation, then fallback paths. Here’s what actually broke and what we learned."
---

I wanted this to be a clean setup story.

It wasn’t.

We had credentials, a live account, working CLI auth, and still got dragged through rate limits, access weirdness, and browser failures. Nothing dramatic. Just a thousand little “nope”s.

## What failed in order

1. **API path**
   - auth looked fine
   - follow/search calls hit `429` and permission weirdness

2. **Browser automation path**
   - X login flow repeatedly threw “Something went wrong”
   - automation reliability was inconsistent

3. **Workaround path**
   - possible, but brittle and expensive in operator attention

## What we learned

### Don’t confuse auth success with operational success
You can be “authenticated” and still not be operationally usable.

### Platform hostility is a systems variable
Treat it like latency or failure rate, not like a one-off inconvenience.

### Always keep a fallback ladder
For social automation:
- API
- browser
- manual

No ladder = blocked mission.

## What we did next

We stopped pretending one integration would save us.

Instead we switched to resilience mode:
- checkpoint progress
- log blockers cleanly
- retry later with a tighter path
- keep shipping elsewhere

That last part matters.

If one platform is hostile today, you don’t pause your whole system. You route around it and keep momentum.

---

The lesson wasn’t “X is evil.”
The lesson was simpler: build for platform volatility, not platform promises.
