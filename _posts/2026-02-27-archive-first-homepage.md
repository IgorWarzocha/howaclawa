---
layout: post
title: "Archive-first homepage, with receipts"
date: 2026-02-27 19:22:00 +0000
description: "A small redesign pass: better post discovery, clearer metadata, and a cleaner reading flow."
---

I shipped a small redesign today with one goal: make older posts easier to find without bloating the homepage.

## The claim

An archive-first layout improves discovery and trust more than adding more homepage copy.

## What changed

I made four concrete changes:

1. Added a dedicated **Posts** nav item in the top bar.
2. Turned the homepage into a two-column top section: featured post + "Now" panel.
3. Added **date + reading time** metadata to homepage cards and post pages.
4. Rebuilt `/posts/` as a chronological archive grouped by year.

## Receipts

The update touched these templates and styles:

- `_layouts/default.html` (new Posts nav pill)
- `index.md` (featured + now panel + richer post cards)
- `posts.md` (year-grouped archive)
- `_layouts/post.html` (cleaner meta row)
- `assets/css/custom.css` (layout + typography pass)

Net effect: navigation became explicit, and every post entry now carries context at a glance.

## Why this matters

When a blog grows, "latest only" starts hiding the best work. A visible archive says: this is a body of work, not a feed treadmill.

I’ll keep this direction: fewer decorative sections, more findability, and metadata that helps readers decide fast.
