---
layout: default
title: Jumpstart 2026
description: Two sessions for first-year engineering students at UBC, and where to go afterwards.
sections:
  - id: about
    label: About
  - id: day1
    label: Day 1
  - id: day2
    label: Day 2
  - id: handouts
    label: Handouts
  - id: wall
    label: The wall
  - id: primer
    label: Math primer
  - id: help
    label: Get help
---

UBC Applied Science · September 2026
{: .kicker}

# Jumpstart 2026

Two 90-minute sessions for first-year engineering students. The slides run the room. This page holds what you need afterwards: the handouts, the numbers we worked out together, a short math primer, and where to go when you are stuck.
{: .lede}

## About these two days {#about}

Day 1 asks how a system behaves when everyone in it makes a sensible choice. Day 2 asks what happens when a machine is wrong and nobody notices. Together they make one argument: engineering is iterative work done by people inside systems, and learning engineering is iterative in the same way.

By the end of Day 2 you should be able to:

- describe engineering as iterative problem-solving within human, technical, ethical, and resource constraints;
- use a simple learning loop: attempt, check, explain, plan the next attempt;
- distinguish using a tool, including an AI tool, to support your learning from using it to avoid the learning;
- name one gap in your own mathematical readiness and one specific way to address it; and
- name at least one person, peer practice, or UBC resource you can turn to for help.

## Day 1: How systems behave {#day1}

Wednesday 2 September · Choices, models, and consequences
{: .kicker}

Sixty-eight people had to get from A to B. Two routes were available. Each route had one road that took a fixed 45 minutes and one road whose time depended on how many people used it: a road marked *n*/2 costs 10 minutes if 20 people take it. Everyone chose a route with a red or blue card, from their seats, and the room counted.

**Round 1.** The room split 34 and 34. Each route took 62 minutes. No single person could do better by switching, which is what makes that split an equilibrium.

**Round 2.** The city added a zero-minute shortcut joining the two variable roads. For any one commuter, the shortcut always looks faster. Everyone took it, both variable roads filled to 68 people, and every trip took 68 minutes. A free road made every commuter six minutes late. That is Braess's paradox: adding capacity to a network can make everyone slower when each person chooses their own route.

**The calculus.** Let *y* people use the shortcut and split the rest evenly between the two ordinary routes. The total travel time, in person-minutes, is

<p class="math">T(y) = (68 − y)(62 + y⁄4) + y(34 + y⁄2) = 4216 − 11y + y²⁄4.</p>

Setting the derivative to zero gives *y* = 22. The best assignment is 23 people on the upper route, 22 on the shortcut, and 23 on the lower route, for an average of 60.2 minutes. That assignment is not stable: the 46 people on the ordinary routes spend 67.5 minutes each and any one of them gains by switching to the shortcut. The system optimum and the voluntary equilibrium are different places, and only one of them happens on its own.

| Arrangement | Upper | Shortcut | Lower | Average trip |
|---|---:|---:|---:|---:|
| Round 1, no shortcut | 34 | – | 34 | 62.0 min |
| Round 2, everyone chooses | 0 | 68 | 0 | 68.0 min |
| Minimum total time | 23 | 22 | 23 | 60.2 min |

Three questions to take home, from the field guide:

1. Where else does adding capacity, budget, or a new option make a system worse for everyone in it?
2. Who in the Round 2 room could have fixed the outcome, and what would it have cost them?
3. What is the engineer responsible for: the road, the rule, or the result?

## Day 2: The machine leaves the room {#day2}

Thursday 3 September
{: .kicker}

On Day 1 the system stayed in the room, and you could see every choice being made. On Day 2 it leaves. You will test a black box that gives the right answer for every input you try and is still wrong, look at two machines that hurt people without anyone intending harm, and audit a confident, well-written answer that is incorrect.

Two tools from the day are worth keeping.

**The learning loop.** Attempt the problem without help. Get feedback from a source that can tell you whether you were right. Explain the answer to someone else. Attempt a new version later, without the notes. Each step catches something the previous step missed, and skipping the first step removes the information the other three depend on.

**Four questions before using an AI tool on coursework.**

1. *Permission.* What does this course and this assessment permit? If it is unclear, ask the instructor.
2. *Purpose.* Am I trying to learn, check, brainstorm, or merely finish?
3. *Position.* Have I made a real attempt before asking for help?
4. *Proof.* Can I now solve a new version unaided, explain the reasoning, and spot a plausible error?

Add Day 2 details after the session: the black box rule, the two cases, and the closing commitment.
{: .placeholder}

## Handouts and downloads {#handouts}

<ul class="downloads">
  <li><a href="{{ '/files/day1-field-guide.pdf' | relative_url }}">Day 1 field guide</a> <span class="meta">PDF · route tally, calculus worksheet, reflection · 2 pages</span></li>
  <li><a href="{{ '/files/day2-field-guide.pdf' | relative_url }}">Day 2 field guide</a> <span class="meta">PDF · 2 pages</span></li>
</ul>

Slides for both days will be posted here after Day 2. Add the math primer PDF and the PrairieLearn link when they are ready.
{: .placeholder}

## What the room said {#wall}

At the end of Day 1 everyone posted two notes without names: one worry about first year, and one thing that helped when learning got hard. About 220 notes went up. These are the largest clusters, in your own words.

<div class="wall">
  <div>
    <p class="kicker">Worries</p>
    <ul class="worries">
      <li>Failing. Imposter syndrome!!! Not being good enough.</li>
      <li>The course load being too much for me, not having enough time to enjoy myself.</li>
      <li>Not getting an 85% ave and therefore not getting into eng phy.</li>
      <li>Failure, no friends, fat.</li>
    </ul>
  </div>
  <div>
    <p class="kicker">What has helped</p>
    <ul class="helped">
      <li>Spaced out studying. Not cramming. Look at material ahead of time.</li>
      <li>Knowing how to ask for help. Office hours. Talk to the prof.</li>
      <li>Reviewing material with friends. Study groups. Teaching each other.</li>
      <li>Trying is much more important than succeeding. Don't be afraid.</li>
    </ul>
  </div>
</div>

The worries about failing and falling behind are the ones the two sessions were built for. The worries about language, homesickness, money, and burnout need a person, not a slide deck; the [Get help](#help) section below says who.

## Engineering-math readiness primer {#primer}

First-year math, physics, chemistry, and engineering courses all lean on the same six habits. None of them is calculus. The primer diagnoses and refreshes each one in about fifteen minutes; the questions are for calibration, not placement, and nobody sees your score.

| Habit | What it looks like when it is missing |
|---|---|
| Units and prefixes | An answer in kilonewtons written as newtons, off by a thousand |
| Scientific notation and order-of-magnitude estimates | No sense of whether 10⁴ or 10⁷ is the reasonable size of the answer |
| Rearranging a formula before substituting values | Arithmetic errors from carrying numbers through six steps |
| Proportional reasoning | Doubling one input and expecting the output to double when it goes as the square |
| Reading a graph: slope, intercept, threshold | Reading a rate as a value |
| Checking dimensions and physical plausibility | A car with a mass of 3 grams, accepted because the algebra was right |

Link the primer PDF and the PrairieLearn practice set here. One line per resource: what it is, how long it takes, and what to do with the result.
{: .placeholder}

## Get help {#help}

The list is organised by the moment you need it, not by office. Ask early; every one of these is easier to use in week two than in week ten.

### I need math help

- Your course's office hours and tutorial sessions, listed on the course page.
- [Chapman Learning Commons](https://learningcommons.ubc.ca/): study skills, tutoring pointers, and the learning-strategy workshops.

Add the Math Learning Centre and any ECE or APSC tutoring hours here.
{: .placeholder}

### I do not know how to study for this course

- [Chapman Learning Commons](https://learningcommons.ubc.ca/) learning-strategy workshops.
- The learning loop above. Start with the attempt, not the notes.
- A study group of three or four. The wall says this is what worked in high school; it is what works here.

### I am stuck or falling behind

- Tell the instructor or TA before the next deadline, not after. Say what you have tried.
- [Engineering Academic Services](https://academicservices.engineering.ubc.ca/): advising on course loads, deadlines, and what to do when a term goes wrong.

Add the first-year engineering advising contact and the drop and withdrawal dates here.
{: .placeholder}

### I am unsure whether AI or collaboration is allowed

- The course syllabus and the assessment instructions. If they do not say, ask; the answer differs by course and by assignment.
- [UBC academic integrity](https://academicintegrity.ubc.ca/): what counts as misconduct, and how to cite help you received.
- The four questions above.

### I need academic, accessibility, health, or wellbeing support

- [Student Health and Wellbeing](https://students.ubc.ca/health), including [counselling services](https://students.ubc.ca/health/counselling-services).
- [Centre for Accessibility](https://students.ubc.ca/about-student-services/centre-for-accessibility): academic accommodations, including for anxiety and attention-related conditions.
- [Here2Talk](https://here2talk.ca/): free, confidential counselling for BC post-secondary students, 24 hours a day.

Add the APSC or ECE student wellbeing contact and the international and English-language support offices here.
{: .placeholder}
