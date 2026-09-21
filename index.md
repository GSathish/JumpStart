---
layout: default
title: Jumpstart
description: Two sessions for first-year engineering students at UBC, and where to go afterwards.
---

UBC Applied Science &middot; September 2026
{: .kicker}

# Jumpstart 2026

Jumpstart consists of two 90-minute sessions for first-year engineering students at the University of British Columbia (UBC). Day 1 examines how individual choices affect a shared system. Day 2 examines failures in machines and the checks that can detect them.
{: .lede}

In both sessions, we attempt a problem, examine the result, and revise our reasoning. This process connects engineering work to the practice of learning it. The sessions have five learning objectives:

- Describe engineering as problem-solving within human, technical, ethical and resource constraints.
- Use a learning loop of attempt, feedback, explanation and a further attempt.
- Distinguish using a tool to support learning from using it to avoid an attempt.
- Identify a skill in your mathematical preparation that needs practice.
- Identify a person or resource to consult when you need help.

## What we worked out on Day 1

Sixty-eight people had to get from A to B. Two routes were available. Each route had one road that took a fixed 45 minutes and one road whose time depended on how many people used it: a road marked *n*/2 costs 10 minutes if 20 people take it. Everyone chose a route from their seats, and the room counted.

In the first round, 34 people chose each route, giving a travel time of 62 minutes on both. No individual could reduce their travel time by switching routes. This is an **equilibrium**: each person has chosen a route they have no incentive to leave while the others keep their choices.

In the second round, we added a zero-minute shortcut between the two roads whose travel times depended on traffic. Each commuter could reduce their own travel time by choosing the shortcut. Once everyone chose it, however, both roads carried 68 people and every trip took 68 minutes. Adding the shortcut increased the equilibrium travel time by six minutes.

We then used calculus to find the assignment that minimises total travel time. Let *y* people use the shortcut and divide the remaining people equally between the two ordinary routes. Under this assignment, total travel time in person-minutes is

<p class="math">T(y) = (68 &minus; y)(62 + y&frasl;4) + y(34 + y&frasl;2) = 4216 &minus; 11y + y&sup2;&frasl;4.</p>

Setting the derivative to zero gives *y* = 22: twenty-three people on the upper route, twenty-two on the shortcut, twenty-three on the lower, for an average of 60.2 minutes. This assignment is not an equilibrium because the 46 people on the ordinary routes each spend 67.5 minutes travelling and could shorten their trips by switching to the shortcut.

<div class="table-wrap" markdown="1">

| Arrangement | Upper | Shortcut | Lower | Average trip |
|---|---:|---:|---:|---:|
| Round 1, no shortcut | 34 | – | 34 | 62.0 min |
| Round 2, everyone chooses | 0 | 68 | 0 | 68.0 min |
| Minimum total time | 23 | 22 | 23 | 60.2 min |

</div>

The calculation identifies an assignment with a lower total travel time than either equilibrium. Maintaining it would require a way to influence route choices, because some commuters would otherwise benefit from switching. The choice to minimise total travel time is also a modelling decision: it gives equal weight to each minute travelled without limiting how much time any particular commuter spends.

Use the route example to consider the following questions about design responsibility:

1. Where else does adding capacity, budget, or a new option make a system worse for everyone in it?
2. Who in the Round 2 room could have fixed the outcome, and what would it have cost them?
3. What is the engineer responsible for: the road, the rule, or the result?

## Where to go next

<div class="cards">
  <a class="card" href="{{ '/going-further/' | relative_url }}">
    <h2>Going further</h2>
    <p>Explore a choice of specialisation, examine engineering failures, and follow the route problem to further results.</p>
  </a>
  <a class="card" href="{{ '/how-to-study/' | relative_url }}">
    <h2>How to study</h2>
    <p>Use practice and feedback to assess your learning, with research on study methods, attention and sleep.</p>
  </a>
</div>

For course questions and student support, [get help]({{ '/help/' | relative_url }}). The page groups resources by the kind of help you need.

## Slides

<ul class="downloads">
  <li><a href="{{ '/files/jumpstart-2026-day1-slides.pdf' | relative_url }}">Day 1 slides: How systems behave</a><span class="meta">PDF, 34 pages, 1.4&nbsp;MB</span></li>
  <li><a href="{{ '/files/jumpstart-2026-day2-slides.pdf' | relative_url }}">Day 2 slides: When systems go wrong</a><span class="meta">PDF, 50 pages, 0.9&nbsp;MB</span></li>
  <li><a href="{{ '/files/jumpstart-2026-neural-networks-slides.pdf' | relative_url }}">Extra deck: How a neural network learns</a><span class="meta">PDF, 23 pages, 88&nbsp;KB</span></li>
</ul>
