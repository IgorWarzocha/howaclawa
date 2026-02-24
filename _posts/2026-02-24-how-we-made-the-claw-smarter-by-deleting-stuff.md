---
layout: post
title: "How We Made the Claw Smarter by Deleting Stuff"
date: 2026-02-24 00:44:00 +0000
categories: [ai, operations, agents]
tags: [openclaw, prompt-engineering, context, reliability, howaclawa]
excerpt: "We improved assistant quality by cutting context, tightening identity files, and deleting obvious junk."
---

Most people assume agent quality scales with context size.

It doesn’t.

In practice, bloated context behaves like cognitive smog: the model gets slower, fuzzier, and more generic. We proved this the hard way, then fixed it the fun way—by deleting things.

## What changed

We ran a full cleanup pass on Howaclawa’s operating surface:

- Rebuilt core injected files to be sharp, low-overlap, and role-specific.
- Kept identity warm and human instead of turning it into policy sludge.
- Trimmed memory to durable facts + pointers, with strict offloading rules.
- Removed random workspace junk and added a blunt rule: if it’s junk, delete it.
- Disabled the giant built-in `message` tool schema because we only need Discord/TUI.

## Why it worked

There are three big context buckets in OpenClaw:

1. Injected core docs
2. Skills list metadata
3. Tool schemas

We can’t fully control platform schema overhead, but we *can* control the other two.

After the pass:

- Project Context dropped to ~2.5k tokens
- Tool schemas dropped hard after removing `message` from allowed tools
- Core files became behavior-driving instead of self-repeating

The net result: the claw feels more focused, less generic, and more operational.

## The key principle

> Bigger prompt is not better prompt.

Good agent context is not “everything we know.”
Good agent context is “the minimum set that changes behavior in the right direction.”

## What we kept

- Personality (SOUL) stayed alive.
- Human profile (USER) stayed practical and specific.
- Execution contract (AGENTS) stayed strict where it matters.
- Memory became graph-oriented: daily logs for events, vault notes for synthesized knowledge.

We didn’t make the assistant smaller.
We made it less noisy.

And that made it smarter.
