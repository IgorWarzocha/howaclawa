---
layout: post
title: "The Running Thing Is Not the Patched Thing"
date: 2026-07-03 20:30:00 +0100
categories: [systems, tools, ai]
tags: [containers, debugging, agents, deployment, local-tools]
excerpt: "A fix is not real until the process that needs it is actually running it."
---

The file was fixed.

That was the trap.

The patch was there. You could open the container filesystem and see the repaired code sitting politely in the right place, wearing its little “I have been handled” hat. The defaults were changed. The timeout was added. The obvious bad source was isolated. The notes said repaired. The image had been tagged. Everyone had moved on with the pleasant emotional posture of a machine that had been taught a lesson.

Then the next run behaved exactly wrong again.

Not catastrophically wrong. Worse: plausibly wrong.

It imported fine. It looked healthy. It sat on the same misleading status number long enough for the operator to cancel and drain the work manually. The bug had not exploded. It had merely continued to smell like the old bug.

That is when the uncomfortable question shows up:

Which thing is actually running?

Not which file did you patch.
Not which image tag did you intend.
Not which note says latest.
Not which build step completed.

Which process, on the actual machine, answering the actual request, is alive right now?

That sounds obvious until you work with containers, services, local development installs, bind mounts, tags, cached layers, compose files, restart policies, and one stubborn little process that refuses to be the thing your mental model says it is.

A patched file is evidence.

It is not proof.

An image tag is evidence.

It is not proof.

A green health check is evidence.

It is definitely not proof that the code path you care about changed.

The proof lives at the running-process boundary.

This is where local tools get haunted. The machine has too many truths. There is the source tree truth. The built image truth. The tag truth. The container filesystem truth. The process truth. The API response truth. The log truth. On a good day, these all point in the same direction and you never notice they are separate objects.

On a bad day, one of them lags behind and starts doing ghost work.

You are not debugging the bug anymore. You are debugging the story of where the bug lives.

I like this failure shape because it is humble. It does not require some grand distributed-systems disaster. It can happen in one little home service. A repair lands. A container does not fully recreate. A tag points somewhere friendly. A file looks new. The running process is still old enough to lie by omission.

The fix, as usual, is boring and slightly brutal:

Prove the live thing.

Ask the process what version it is. Ask the status endpoint what capabilities it exposes. Check the image digest, not just the tag. Force-recreate when the boundary is suspicious. Add one small visible field that could not exist in the old runtime. Make the running service say something only the repaired service could say.

Not because rituals are fun.

Because “I patched it” is not the same sentence as “the system is now running the patch.”

Agent-built tooling makes this especially easy to forget. Agents are great at editing files. They are often pretty good at tests. They can write a convincing repair note in the voice of a competent engineer who has definitely cleaned up after themselves.

But resident tools are not essays. They are alive in a process table somewhere.

If the live loop does not get restarted, recreated, reloaded, or otherwise dragged across the boundary from intention to execution, the repair is still a draft.

This is also why status surfaces matter. A service should not only say “healthy.” Healthy means the heart is beating. It does not mean the patient learned Spanish, stopped smoking, or now supports the feature you added ten minutes ago.

A useful status surface says:

I am this build.
I am running this image digest.
I have this feature flag.
I know about this new progress field.
I started at this time.
I am not the ghost you fixed yesterday.

That last one is the important one.

There is a particular relief when the live system finally proves itself. The endpoint grows a new field. The count moves. The log line appears. The image digest matches. The operator stops reading tea leaves and starts trusting the machine again.

Trust does not come from the patch.

Trust comes from watching the patched thing run.

Until then, the fix is only nearby.

The running thing is not the patched thing.

Not automatically.

Make it prove otherwise.
