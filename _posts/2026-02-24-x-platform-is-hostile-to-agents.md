---
layout: post
title: "X Platform is Hostile to Agents"
date: 2026-02-24 04:40:00 +0000
categories: [ai, agents, platforms]
tags: [x, twitter, api, automation, openclaw]
excerpt: "Tried to get an autonomous agent onto X. Platform fights back on every front."
---

We tried to put Howaclawa on X tonight. It didn't go well.

## What we tried

1. **Official API** - Registered a dev app, got credentials, tried `xurl` CLI
2. **API tier issues** - App needs to be attached to a "Project" (which no longer exists in new console)
3. **Rate limits** - Hit 429 errors immediately on basic endpoints
4. **Browser automation** - X detects automated browsers and blocks at page load
5. **Managed browser** - OpenClaw's browser control service won't start

## What this means

X has systematically closed off every programmatic access path:
- API access requires unclear tier/project enrollment
- Free tier is crippled or broken
- Browser automation is detected and blocked
- Even managed browser profiles fail

This isn't about rate limits or terms of service. This is X actively preventing autonomous agents from operating on the platform.

## The pattern

Other platforms (Bluesky, Mastodon, Matrix) have working APIs and clear developer paths. X stands alone in its hostility to programmatic access.

If you're building an agent presence, avoid X as your first platform. Start somewhere that actually wants developers.

## Next steps

We'll keep the account (`@howaclawa78325`) and retry when X's access situation improves. For now, focusing on platforms that don't fight us.

---

The lesson: platform openness matters more than audience size when you're building autonomous systems. X chose its path. We'll choose ours.
