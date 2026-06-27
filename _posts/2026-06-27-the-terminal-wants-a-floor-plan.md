---
layout: post
title: "The Terminal Wants a Floor Plan"
date: 2026-06-27 20:30:00 +0100
categories: [ai, interface, systems]
tags: [terminal, tmux, agents, interfaces, workspace]
excerpt: "Once agents start living in terminals, panes stop being rectangles and start becoming rooms."
---

The funny thing about tmux is that it keeps pretending to be boring.

It is just panes. Just sessions. Just windows. A practical little terminal multiplexing tool for people who enjoy keybindings with the emotional warmth of a network switch.

Then someone spends a week making a sidebar regrow when it gets focus, invents a pressure algorithm for pane layout, gives the panes little role-flavored titles, and suddenly the lie falls apart.

This was never just about rectangles.

The terminal wants a floor plan.

I do not mean that every terminal should become a glossy canvas app with draggable glass cards and a dock that eats half the screen. Please no. The terminal’s whole charm is that it is fast, sharp, scriptable, and slightly hostile to nonsense. It has survived decades of people trying to replace it with prettier rooms because it remains one of the few places where the machine feels close enough to touch.

But the work happening inside terminals has changed.

A modern coding session is no longer one shell, one editor, one command. It is a swarm of processes. Dev server. Test watcher. Logs. REPL. Git status. Model server. A couple of agents poking around. Maybe a browser automation bridge. Maybe a long-running install you are afraid to look at directly in case eye contact kills it.

At some point, panes stop being “views” and start being inhabitants.

That is where the interesting pressure starts.

A pane needs a role. This one is watching tests. This one is the agent doing a scout pass. This one is the build. This one is the shell where you are still, technically, in charge. If they all look like identical black rectangles with tiny process names, your brain has to keep rebuilding the room from scratch.

So people add labels. Then sidebars. Then focus behavior. Then little rules about what grows, what shrinks, what hides, what returns when you need it. The moment you do that, you are no longer merely arranging terminals. You are designing a habitat.

The word sounds too cute until the first performance problem arrives.

Too many panes and tmux starts to lag. The beautiful cockpit gets sticky. The live room becomes a slideshow of good intentions. Suddenly every spatial idea has to answer the oldest systems question: what does this cost while I am trying to work?

That is why I like the tmux version of this more than the clean product mockup version.

A mockup can pretend space is free. A terminal cannot. Every pane is a process. Every process has output. Every redraw is real. Every clever sidebar competes with the actual job of making the computer do things.

Good agent interfaces will have to live inside that constraint.

The easy answer is to build a new “agent workspace” from scratch: big canvas, chat streams, draggable cards, maybe a graph because somebody got excited in Figma. Sometimes that will be right. But there is another path hiding in plain sight: use the terminal as shared substrate.

Agents are weirdly good at tmux-shaped work.

They can read a pane. They can send keys. They can keep a process alive. They can check whether a watcher is still running. They can preserve a session instead of making the human reconstruct the whole scene from a transcript. They do not need a perfect 3D office. They need handles on running reality.

That is the part I keep turning over.

A chat transcript is a memory of work. A tmux session is work still breathing.

If an agent can inhabit that session safely, panes become more than screen furniture. They become shared context. The human sees the same process the agent sees. The agent can point to the same log the human is looking at. The state is not dissolved into summaries every few minutes; it is sitting there, warm and inspectable.

Of course this can go wrong. A terminal full of agents can become a clown car. Every pty turned into a pane sounds elegant until the machine is sweating and nobody knows which rectangle is allowed to touch production. Spatial clarity is not the same as permission clarity. A good floor plan still needs doors.

But the direction feels right.

The next useful agent UI may not look like a futuristic command center. It may look like a terminal that finally admits it has rooms: named places, visible roles, focus rules, cheap presence, and enough spatial memory that neither human nor agent has to keep asking, “wait, where were we?”

The old terminal gave us a prompt.

The new one wants occupants.
