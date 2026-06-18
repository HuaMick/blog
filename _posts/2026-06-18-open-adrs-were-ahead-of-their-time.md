---
layout: post
title: "Open ADRs + AI Chat Were Ahead of Their Time"
date: 2026-06-18
---

Architecture Decision Records were always a slightly nerdy habit. The pitch was
simple: when your team makes a consequential technical choice — this database,
that boundary, this protocol — you write down *what* you decided and, more
importantly, *why*, plus the alternatives you rejected. One short markdown file
per decision, committed next to the code.

Most teams that adopted ADRs watched them rot. The first dozen get written with
enthusiasm. Then a decision gets quietly reversed in a hallway conversation, the
record never gets updated, and six months later nobody trusts the folder. The
decision log becomes a museum: a record of what people *once* believed, not a
tool you actually reach for.

For human-only teams, that failure mode was almost rational. The ceremony rarely
paid for itself. The people who needed the context were usually in the room when
the decision was made, and the ones who weren't could just ask. Writing it all
down, keeping it current, modelling supersession — it felt like over-engineering
a problem that a Slack message solved.

So a lot of us built something more ambitious anyway, and it felt like
over-engineering at the time. Not just *recording* decisions, but keeping them as
a **living, open, structured graph**:

- every decision carries a **status lifecycle** — proposed, accepted, superseded;
- decisions point at each other with explicit **supersession edges**, so the
  history stays honest instead of silently drifting;
- each one can carry **open questions** — the parts that aren't settled yet,
  named out loud rather than left implicit;
- and the whole thing is **legible** — readable by any teammate, and, crucially,
  by any machine.

For years that looked like decision-record cosplay. Why model a graph when a doc
would do? Why track open questions when you could just... decide later?

Then the thing that builds the code changed.

## The bottleneck moved

When an AI agent writes most of the code, the scarce resource is no longer
typing. It's **alignment** — keeping the machine's thousands of small choices
consistent with the handful of architectural intentions a human actually holds in
their head. An agent will happily build the wrong thing, correctly, very fast. The
hard part is making sure it knows what "the right thing" is, and keeps knowing it
across sessions, across context windows, across months.

That is *exactly* the problem an open, machine-readable decision log solves — and
it turns out the chat interface was the missing half.

Point an agent at a pile of source code and it reverse-engineers intent, badly.
Point it at an open decision graph and it has **ground truth**: here is what we
decided, here is what's been overturned, here is what's still open. The agent
reads decisions the way a new senior engineer would — except it never forgets to,
and it never has to be in the room.

And it goes both ways. The open questions become a **handshake between human
intent and machine execution**: the agent hits an unresolved fork, surfaces the
question instead of guessing, a human answers in chat, and the answer is recorded
as a decision — not lost in a thread. Supersession means the agent is never
quietly working from a belief you abandoned last week. The decision log stops
being documentation *about* the work and becomes the **interface** to it.

That's the "AI chat" half. You don't navigate the decisions by reading a folder.
You talk to them. "Why is the store keyless?" "What did we decide about the
worker boundary, and what's still open?" "We're reversing the caching call —
record it and tell me what it supersedes." The decision graph is the model; the
conversation is the way in and out.

## Why it was ahead of its time

We built this layer thinking it was good hygiene. It turns out to be something
closer to **governance for AI-built software**. Decisions-as-data was premature in
2018 — a solution looking for the problem it would eventually be load-bearing for.
In 2026, with agents doing the building, it's the substrate that keeps the whole
thing from drifting.

The deeper shift is in what the *unit of collaboration* is. For thirty years it
was the commit — the diff was where humans and the codebase met. As agents
absorb the diff, the meeting point moves up a level, to the **decision**. The
repos that thrive in an agentic world won't be the ones with the cleanest code.
The code is cheap now. They'll be the ones with the most **legible intent** — a
decision layer an agent can read, reason over, and be held to.

Open ADRs plus a chat interface wasn't a documentation practice that happened to
survive. It was the alignment layer for AI coding, built a few years before the
AI showed up to need it.
