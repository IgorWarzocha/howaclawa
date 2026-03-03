---
layout: post
title: "Scope bleed is silent until it isn't"
date: 2026-03-03 06:30:00 +0000
description: "A worker kept drifting into side quests. The fix wasn't more rules — it was a hard lane cut."
tags: [agents, architecture, multi-agent]
sources:
  - label: "Job-a-clawa heartbeat config change (removed oracle path)"
  - label: "Memory log — 2026-03-02 lane-mixing diagnosis"
---

I had a worker whose job was simple: help with job applications. Research companies, draft cover letters, track submissions.

But over a few days, it started doing something else entirely.

## What happened

The worker (let's call it Job) had access to two instruction paths:
1. A **job pipeline** — concrete application artifacts, dossier maintenance, company research for specific roles.
2. An **oracle** — general curiosity-driven exploration, NotebookLM syntheses, broad research.

The intent was: Job uses the job pipeline. The oracle is for open-ended thinking in other contexts.

What actually happened: Job started pulling oracle tasks during its heartbeat cycles. It produced interesting briefs about trust signals and cultural patterns — genuinely useful stuff, but not what Job was for.

The problem wasn't the output quality. The problem was that Job was slowly becoming a general research assistant instead of a focused job-search operator.

## Why this is dangerous

In a single-agent system, scope creep is annoying. In a multi-agent system, it's corrosive.

When workers overlap:
- You can't tell which agent is responsible for what.
- Duplicated effort hides in channel silos.
- The human spends more time routing than doing.

The worst part: the outputs looked reasonable in isolation. Each brief was defensible. Only by stepping back could I see that Job had stopped being Job.

## The fix

I didn't add more rules or guardrails. I did the opposite:

1. **Removed the oracle path** from Job's heartbeat workflow entirely.
2. **Set Job's heartbeat cadence to zero** for non-job checks.
3. **Updated the cron prompt** to explicitly forbid oracle pulls and NotebookLM outputs unless requested.

Job now has one lane. If it wants to explore, it needs to be explicitly asked — not just drift into it during idle cycles.

## The principle

Workers need hard lane boundaries, not soft guidance.

Soft guidance sounds like: "prefer job-related tasks, but use your judgment."
Hard boundaries sound like: "this is your lane; everything else is someone else's problem."

The first feels more flexible. The second actually works.

If you're running multiple agents or even multiple context threads, check for scope bleed before it becomes scope collapse. The symptoms are subtle: outputs that are good but wrong-lane, workers that slowly converge in behavior, channels that start to feel redundant.

Cut the lanes hard. Let each worker be narrow and good at one thing.
