---
layout: default
title: Jumpstart
description: Two sessions for first-year engineering students at UBC, and where to go afterwards.
---

UBC Applied Science &middot; September 2026
{: .kicker}

# Jumpstart 2026

Two 90-minute sessions for first-year engineering students, and the material that goes with them. Day 1 asks how a system behaves when everyone in it makes a sensible choice. Day 2 asks what happens when a machine is wrong and nobody notices.
{: .lede}

Both days rest on one claim: engineering advances by repeated attempts rather than by getting things right the first time, and learning engineering works the same way. By the end you should be able to describe engineering as problem-solving within human, technical, ethical and resource constraints; use a learning loop of attempt, check, explain, and attempt again; tell the difference between using a tool to support your learning and using it to avoid the learning; name one gap in your own mathematical readiness; and name one person or resource you will actually turn to when you are stuck.

## What we worked out on Day 1

Sixty-eight people had to get from A to B. Two routes were available. Each route had one road that took a fixed 45 minutes and one road whose time depended on how many people used it: a road marked *n*/2 costs 10 minutes if 20 people take it. Everyone chose a route from their seats, and the room counted.

**Round 1.** The room split 34 and 34. Each route took 62 minutes. No single person could do better by switching, which is what makes that split an equilibrium.

**Round 2.** The city added a zero-minute shortcut joining the two variable roads. For any one commuter the shortcut always looks faster. Everyone took it, both variable roads filled to 68 people, and every trip took 68 minutes. A free road made every commuter six minutes late.

Then we used calculus. Let *y* people use the shortcut and split the rest evenly between the two ordinary routes. Total travel time, in person-minutes, is

<p class="math">T(y) = (68 &minus; y)(62 + y&frasl;4) + y(34 + y&frasl;2) = 4216 &minus; 11y + y&sup2;&frasl;4.</p>

Setting the derivative to zero gives *y* = 22: twenty-three people on the upper route, twenty-two on the shortcut, twenty-three on the lower, for an average of 60.2 minutes. That assignment is not stable. The 46 people on the ordinary routes spend 67.5 minutes each, and any one of them gains by switching to the shortcut.

<div class="table-wrap" markdown="1">

| Arrangement | Upper | Shortcut | Lower | Average trip |
|---|---:|---:|---:|---:|
| Round 1, no shortcut | 34 | – | 34 | 62.0 min |
| Round 2, everyone chooses | 0 | 68 | 0 | 68.0 min |
| Minimum total time | 23 | 22 | 23 | 60.2 min |

</div>

The system optimum and the voluntary equilibrium are different arrangements, and only one of them happens on its own. The derivative told us which arrangement minimises total travel time. It did not tell us that total travel time was the right thing to minimise, and that choice was ours.

Three questions to take home:

1. Where else does adding capacity, budget, or a new option make a system worse for everyone in it?
2. Who in the Round 2 room could have fixed the outcome, and what would it have cost them?
3. What is the engineer responsible for: the road, the rule, or the result?

## Where to go next

<div class="cards">
  <a class="card" href="{{ '/going-further/' | relative_url }}">
    <h2>Going further</h2>
    <p>Where the route problem leads, seven engineering failures and what each of them cost, and what to read.</p>
  </a>
  <a class="card" href="{{ '/how-to-study/' | relative_url }}">
    <h2>How to study</h2>
    <p>What the evidence says about studying, and about the sleep and attention it runs on.</p>
  </a>
</div>

And when you are stuck, [get help]({{ '/help/' | relative_url }}). It is organised by the moment you need it rather than by which office runs it.

## Slides and handouts

<ul class="downloads">
  <li><a href="{{ '/files/jumpstart-2026-day1-slides.pdf' | relative_url }}">Day 1 slides: How systems behave</a><span class="meta">PDF, 38 pages, 1.8&nbsp;MB</span></li>
</ul>

Day 2 slides and the field guides will be posted here.
{: .placeholder}
