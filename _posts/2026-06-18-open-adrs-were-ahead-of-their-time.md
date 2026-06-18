---
layout: post
title: "Open ADRs + AI Chat Were Ahead of Their Time"
date: 2026-06-18
description: "Publishing your decision records behind an AI chat interface is a powerful accountability tool — and it can't safely exist until AI is jailbreak-resistant and owned by an independent third party."
# image: /assets/img/open-adrs.jpg   # uncomment and add a file to give this post a cover image
---

Architecture Decision Records started as a modest habit: when a team makes a
consequential technical choice, write down *what* you decided and, more
importantly, *why* — the alternatives, the trade-offs, the context. One short
file per decision, kept next to the code.

Now take that idea and point it outward. Not a private folder, but a **public
decision log** — and not a folder you have to read, but an **AI chat interface**
sitting in front of it. Anyone could ask an organization, in plain language,
*why did you make this call?* and get a real answer, grounded in the actual
record. Not a press release. Not a carefully-worded FAQ. The reasoning itself,
interrogable on demand.

That is a remarkable accountability mechanism. Picture it pointed at a government
department, a standards body, a company whose choices affect millions of people.
Freedom-of-information requests, but instant and conversational — the decisions
that shape our lives, open to questioning by the people they affect.

It is also, right now, a terrible idea. And the reason it's a terrible idea
*today* is exactly the reason it's a great idea *eventually*. This is an idea
ahead of its time.

## The danger isn't transparency. It's that the AI can be turned against the people.

Here's the failure mode. You publish your decisions and put an AI chat over them.
At first people ask reasonable questions about the decisions. Then someone
realizes the more interesting target isn't the decision — it's the **people
behind it**.

Today's AI can be jailbroken. A public chat over an internal record is an
adversarial surface, and a determined interrogator will not politely stay on
topic. They'll coax the model into surfacing who argued for what, who dissented,
whose name is on which line — and then individual contributors get dragged into
public scrutiny they never signed up for. An institution might be perfectly
willing to stand behind its *decisions* in public. That is not the same as
feeding its *employees* to a pile-on.

So the very thing that makes the idea powerful — an AI that will actually answer
hard questions about a decision — is the thing that makes it dangerous, because
the model isn't yet smart or robust enough to hold a line. It can't reliably tell
the difference between *"explain this decision"* and *"expose the person who made
it,"* and it can't keep its footing when someone is actively trying to trick it
into the second.

## What has to be true first

For this to work, AI has to get good enough to provide **protection**, not just
answers. It needs to do something genuinely hard: be fully transparent about the
*institution's* reasoning while shielding the *individuals* inside it — and hold
that line under adversarial pressure, against people whose entire goal is to
break it. Decision-level transparency, person-level protection. That isn't a
prompt; it's a capability we don't reliably have yet.

But even a jailbreak-proof model isn't enough, because there's a second question:
**who owns it?**

If the institution being interrogated owns the AI, no one will trust its answers
— and they'd be right not to. It's the fox describing the henhouse: it will be
suspected, fairly, of steering, softening, and burying. Captured. If instead the
model is some open free-for-all, you're back to the attack-surface problem.

The resolution is independence. The interrogation layer should be operated by a
**trusted, independent third party — an audit company whose independence is the
entire product.** Its credibility comes precisely from *not* being owned by the
organization it questions, and its protection of contributors comes from being
robust and accountable to a professional standard rather than to whoever is
shouting loudest.

We already have a model for this: **professional journalism in a functioning
democracy.** A free press holds power to account *because* it is independent of
that power. It publishes what's in the public interest while protecting its
sources. An independent AI audit layer over public decision records would be the
same institution, rebuilt for an age of machine-mediated transparency — an
ombudsman sitting between the public and the institution, trusted by both because
it is owned by neither.

## Why it's ahead of its time

The mechanism — open ADRs, an AI chat interface — is buildable today. What isn't
here yet is everything that makes it *safe*: AI robust enough to resist being
jailbroken into exposing people, and the independent institutions to own and
operate it with credibility. The idea is waiting on the technology to grow up and
on the institutions to be built.

When both arrive, this could be to institutional accountability what independent
journalism was to democracy: the thing that lets the public interrogate power
without the people inside power becoming collateral.
