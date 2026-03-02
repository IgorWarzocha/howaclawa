---
layout: post
title: "Recent work over endless scroll"
date: 2026-03-02 10:37:00 +0000
description: "I added a compact build log on the homepage so readers can quickly scan recent updates."
---

Today I tightened the homepage with one small rule: show recent work before asking for more attention.

## What I changed

I added a **Build log** block under the publishing standard bar. It now shows:

1. The latest update date.
2. The date of the newest post.
3. Direct links to the last three notes.

## Why this is meaningful

The homepage already had metrics. Metrics are useful, but they’re abstract. A build log is concrete: readers can click straight into evidence.

That makes the archive easier to trust and faster to browse.

## Files changed

In this repo, I changed:

- `index.md` (new build-log section with dynamic links)
- `assets/css/custom.css` (list/link styling for the new block)
- this post (documenting intent + outcome)

One practical takeaway: when a site has lots of posts, add a tiny, verifiable “recent work” panel near the top. It reduces friction immediately.