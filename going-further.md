---
layout: default
title: Going further
description: Exploring your interests before committing to a path, engineering failures, extensions of the route problem, and further reading.
permalink: /going-further/
sections:
  - id: identity
    label: Choosing a path
  - id: practice
    label: Practice and direction
  - id: communication
    label: Writing and speaking
  - id: braess
    label: The route problem
  - id: failures
    label: Engineering failures
  - id: asides
    label: Three asides
  - id: reading
    label: Reading
---

Beyond the two sessions
{: .kicker}

# Going further

First year gives you experience to draw on when choosing what to study next. The discussion below starts with how to use that experience, including what happens when you commit to a path before exploring it. It also extends the route-choice problem and examines engineering failures and near misses.
{: .lede}

## Choosing a path before you have explored it {#identity}

You may arrive at university already saying that you will be a mechanical engineer, work in software, or go to graduate school. A plan gives you something to work towards. But you may know much more about the title than about the work, especially when the plan comes from family expectations or what your friends want to do.

James Marcia called commitment without exploring alternatives **identity foreclosure**. His framework distinguishes commitment from the process of examining possible choices. You can sound certain about a career without having considered what attracts you to it. You can also be uncertain while actively learning enough to make a choice.

The four categories describe different relationships between exploration and commitment:

<div class="table-wrap" markdown="1">

| Identity status | Exploration and commitment |
|---|---|
| Diffusion | No settled commitment and no active effort to resolve the choice; some exploration may have happened earlier. |
| Foreclosure | Commitment without seriously considering alternatives. |
| Moratorium | Active exploration, with commitment still unsettled. |
| Achievement | Commitment after considering meaningful alternatives. |

</div>

Marcia's original study involved 86 male college students. Use the categories here to reflect on a decision; they are not a test of which specialisation suits you or a timetable for deciding your future.

James E. Marcia, [*Development and validation of ego-identity status*](https://doi.org/10.1037/h0023281), Journal of Personality and Social Psychology 3(5), 1966, 551 to 558.
{: .source}

### Try the work before choosing a specialisation

Suppose you want to study mechanical engineering because you like cars. Working on a design team's suspension assembly might confirm that interest. You might instead discover that you prefer writing the software that reads the sensors. Either experience gives you a more specific reason for your next choice than liking the finished car does.

Choose a manageable way to investigate an interest this term. Attend a team meeting and ask about a beginner task, or ask an upper-year student to walk you through a recent project, including the routine work and the parts that went badly. Afterwards, write down what you enjoyed doing and what you would like to try again. A department's name tells you less than an account of how someone spent their week.

You may finish this process wanting exactly what you wanted at the start. That is a reasonable outcome: you now have experience behind the choice. Family advice and concerns about earning a living also deserve consideration. Exploring means examining those reasons alongside your own experience.

## Early frustration and changing direction {#practice}

A first programming assignment can take hours because you are still learning how to read an error message. That experience alone tells you little about whether you will enjoy programming once you can debug a small program. The **frustration barrier** is this early stretch when you cannot yet do enough of an activity to judge what it offers.

Before drawing a conclusion about your ability, identify one part you cannot do and practise it with feedback. For debugging, that might mean predicting the value of a variable, running the program, and explaining why the value differed. Ask someone more experienced to show you how they investigate a mistake. The [learning loop]({{ '/how-to-study/' | relative_url }}#loop) gives you a sequence to follow.

After some practice and help, you may find that you can do the work but have little interest in continuing it. You may also discover an interest that your original plan leaves no room for. Those are reasons to reconsider the plan. An early setback and a sustained dislike of the work give you different information.

Changing direction can have costs. Before changing your course load or taking time away, talk with [Engineering Academic Services]({{ '/help/' | relative_url }}#behind) about how the options affect your degree. You can take your current work seriously while reconsidering where it leads.

## Practise explaining your work {#communication}

When a teammate uses your calculation, they need to know what you assumed and when the result applies. An answer without that explanation is difficult to check. Writing and speaking give other people enough information to question your reasoning or use it in their own work.

After solving a problem, write a short explanation for someone who missed the class. State the problem and the assumptions, then explain why you chose the method. Include a check, such as the units or the behaviour in a limiting case. Read it aloud to a classmate and ask them to identify a step they could not follow. Revise that step before adding more detail elsewhere.

You can practise within a lab report or a design-team update. Both give you a reader who needs to understand the explanation and can tell you where it falls short.

## Where the route problem goes next {#braess}

In the session you found the equilibrium of a two-route network by voting, then added a road that cost nothing and made everybody slower. You used a derivative to find the assignment that minimised total travel time. That assignment differed from the one people chose for themselves.

Related effects occur in physical systems. In an electrical network, adding a wire can raise the total power dissipated. In a mechanical version built from two springs and two strings, cutting a supporting string makes the load rise rather than fall. These examples show why adding a connection requires checking how the whole system responds.

The ratio between the cost of the worst equilibrium and the cost of the optimum is called the **price of anarchy**. In the standard model, which treats traffic as a continuous flow, selfish routing costs at most 4/3 of the minimum possible total when each road's travel time is a nonnegative constant plus a nonnegative multiple of its traffic. The bound is tight: some networks attain it. It gives a limit under those assumptions, rather than a guarantee for every real road network.

Tim Roughgarden and Éva Tardos, [*How bad is selfish routing?*](https://doi.org/10.1145/506147.506153), Journal of the ACM 49(2), 2002, 236 to 259.
{: .source}

Reports about road closures need more care. Seoul demolished the Cheonggye elevated expressway in 2003 and restored the stream beneath it; Stuttgart reopened a section of new road only after closing it improved conditions. Both are often cited as examples of the paradox. Each city changed several things at once, so these observations cannot isolate the paradox from transit investment and induced demand.

## Engineering failures and a near miss {#failures}

These cases include fatal accidents, the loss of a spacecraft, and a building repaired before it failed. In each case, examine the design assumptions and how people responded to evidence of a problem. The sources below give more detail; the Citicorp account is journalism, while several others are investigation reports.

### Therac-25, 1985 to 1987

A radiation therapy machine delivered massive overdoses to six patients in the United States and Canada. Several died. Earlier models had hardware interlocks that physically prevented the beam from firing at full power without a target in place; the Therac-25 removed them and relied on software to enforce the same condition. A race condition let a fast, practised operator edit the treatment screen faster than the software could reconcile it, and the machine fired in the wrong mode. The manufacturer had no adequate mechanism for investigating reported accidents and did not believe the operators' reports.

Nancy Leveson and Clark Turner, *An Investigation of the Therac-25 Accidents*, IEEE Computer 26(7), July 1993, 18 to 41. doi:10.1109/MC.1993.274940
{: .source}

### Ariane 5 Flight 501, 4 June 1996

Thirty-seven seconds after the start of the main engine ignition sequence, the launcher lost all guidance and attitude information and destroyed itself. The inertial reference system had converted a 64-bit floating-point value, the horizontal bias, into a 16-bit signed integer. The value did not fit. The conversion had been left unprotected because an analysis showed the overflow could not occur, and that analysis was correct for the Ariane 4 trajectory. Ariane 5 flew a different trajectory. The code was correct against the assumptions it was written under, and nobody re-checked those assumptions when the launcher changed.

*Ariane 5: Flight 501 Failure*, Report by the Inquiry Board, Paris, 19 July 1996.
{: .source}

### Hyatt Regency walkways, Kansas City, 17 July 1981

Two suspended walkways in the hotel atrium collapsed during a crowded tea dance, killing 114 people and injuring more than 200. The original design hung both walkways from a single continuous set of rods. During fabrication that was changed to two shorter rods, one from the ceiling to the upper walkway and a second from the upper walkway to the lower. On a drawing the change is almost invisible, and it doubled the load carried by the upper walkway's box beam connection, which had not been designed to take it. The change was made for ease of fabrication, and the review that should have caught it did not.

Marshall et al., *Investigation of the Kansas City Hyatt Regency Walkways Collapse*, NBS Building Science Series 143, National Bureau of Standards, 1982.
{: .source}

### Lac-Mégantic, Quebec, 6 July 2013

An unattended freight train carrying petroleum crude oil rolled downgrade into the centre of town. Sixty-three tank cars derailed, the oil ignited, and 47 people died. No single person caused it. The Transportation Safety Board identified eighteen contributing factors: too few handbrakes applied and no effective test of whether they held, a locomotive shut down after a fire left no air brakes, tank cars that breached readily, a safety management system the regulator had not adequately audited, and a company operating with thin margins on a line it had bought cheaply. Each of those defences was present in some form and each was thin enough to fail.

Transportation Safety Board of Canada, Railway Investigation Report R13D0054, 2014.
{: .source}

### Citicorp Center, New York, 1978

A year after the tower opened, its structural engineer, William LeMessurier, was asked by an undergraduate writing a thesis, Diane Hartley, about the building's behaviour under winds striking it at an angle. Checking, he found that a change made during construction, bolted rather than welded joints, left the tower vulnerable to a quartering wind of a kind expected roughly once every sixteen years if its tuned mass damper lost power. The joints were welded, at night, while the building stayed open. A newspaper strike meant almost nobody heard about it, and the episode stayed quiet for seventeen years. A question from outside the project prompted the engineer to re-examine the design.

Joe Morgenstern, *The Fifty-Nine-Story Crisis*, The New Yorker, 29 May 1995.
{: .source}

### Tacoma Narrows Bridge, 7 November 1940

The bridge twisted itself apart in a 68 km/h wind four months after opening. Physics textbooks still describe this as forced resonance, wind supplying a periodic push that matched the structure's natural frequency. It was not. The failure was aerodynamically induced self-excitation in torsion, a negative-damping instability now called flutter, in which the motion of the deck generates the very forces that amplify it. Resonance and self-excitation are different phenomena with different mathematics. Aeronautical engineers already understood flutter in 1940, but bridge engineers were not reading the aeronautical literature.

K. Yusuf Billah and Robert Scanlan, *Resonance, Tacoma Narrows bridge failure, and undergraduate physics textbooks*, American Journal of Physics 59(2), 1991, 118 to 124.
{: .source}

### Quebec Bridge, 29 August 1907

The south cantilever of what would have been the world's longest bridge span buckled and fell into the St Lawrence. Seventy-five of the 86 workers on the span died, 33 of them Mohawk ironworkers from Kahnawake. The Royal Commission found that the consulting engineer, Theodore Cooper, had underestimated the structure's dead weight and never corrected it, and that he supervised from New York and visited rarely. The compression chords had been visibly bending for days. Nobody on site had both the authority and the standing to stop the work.

This is the failure behind the Iron Ring, worn by Canadian engineers since the Ritual of the Calling of an Engineer began in 1925. You will be told at some point that the rings were forged from the wreckage. They were not. The first ones were made by veterans at the Christie Street Military Hospital in Toronto.

Royal Commission on the Quebec Bridge Inquiry, Report, 1908. On the ring itself, see ironring.ca.
{: .source}

## Three asides {#asides}

### Mariner 1 and the missing overbar

Mariner 1 left Cape Canaveral for Venus on 22 July 1962, veered off course, and was destroyed by the range safety officer 293 seconds after launch. The cause is usually given as a missing hyphen, but it was a missing overbar. Someone transcribing the handwritten guidance equations dropped the bar above an R, and the software used the raw radar value where it should have used the smoothed one, so ordinary noise read as urgent course error. Arthur C. Clarke called it the most expensive hyphen in history, and his phrase has outlived the correction to it. The familiar retelling obscures the distinction between a punctuation error in code and a missing mathematical symbol in the guidance specification.

### The Harvard Mark II moth

On 9 September 1947 an operator of the Harvard Mark II taped a moth into the logbook with the note "First actual case of bug being found." The entry is usually offered as the origin of the word, which the wording itself rules out. You do not write *actual* unless *bug* already means something else, and it did: engineers had been calling faults bugs since at least Edison. The joke in the logbook is that this time there was a literal one. The moth is therefore evidence that the term was already in use rather than the origin of it.

### What computing is for

Richard Hamming opened *Numerical Methods for Scientists and Engineers* with a line that applies directly to your first programming course: "The purpose of computing is insight, not numbers." A correct number that nobody understands has not yet been checked.

## Reading {#reading}

<ul class="reading">
  <li>
    <a href="https://doi.org/10.1109/MC.1993.274940">An Investigation of the Therac-25 Accidents</a>
    <span class="src">Nancy Leveson and Clark Turner &middot; IEEE Computer, July 1993</span>
    <p>This investigation covers the software defect, the missing hardware interlock, and the reporting process that let the same accident happen six times.</p>
  </li>
  <li>
    <a href="https://doi.org/10.1017/S0140525X00005756">Minds, Brains, and Programs</a>
    <span class="src">John Searle &middot; Behavioral and Brain Sciences, 1980</span>
    <p>The Chinese Room argument, that running the right program is not the same as understanding it. The article sets out the thought experiment without requiring a programming background.</p>
  </li>
  <li>
    The Milk of Human Intentionality
    <span class="src">Daniel Dennett &middot; open peer commentary printed with Searle's paper, 1980</span>
    <p>The reply, printed in the same issue. Searle's article was published with about two dozen commentaries and his answers to them, so the argument and its opposition are in one place.</p>
  </li>
  <li>
    <a href="https://archive.org/details/whatengineerskno0000vinc">What Engineers Know and How They Know It</a>
    <span class="src">Walter Vincenti &middot; Johns Hopkins University Press, 1990</span>
    <p>Vincenti argues that engineering knowledge is not applied science, and works through five cases from aeronautical history to show what it is instead. Useful if you have wondered what your degree is actually teaching you.</p>
  </li>
  <li>
    <a href="https://archive.org/details/toengineerishuma00petr">To Engineer Is Human</a>
    <span class="src">Henry Petroski &middot; St Martin's Press, 1985</span>
    <p>Petroski's case that design advances by failure, argued through bridges, roofs and everyday objects. The case histories provide an introduction without assuming specialist engineering knowledge.</p>
  </li>
  <li>
    <a href="https://archive.org/details/computerpowerhum0000weiz_v0i3">Computer Power and Human Reason</a>
    <span class="src">Joseph Weizenbaum &middot; W. H. Freeman, 1976</span>
    <p>Weizenbaum wrote it after watching people confide in ELIZA, the chatbot he had built. It is about the difference between what a computer can be made to do and what it should be asked to decide.</p>
  </li>
  <li>
    <a href="https://doi.org/10.1145/506147.506153">How Bad Is Selfish Routing?</a>
    <span class="src">Tim Roughgarden and Éva Tardos &middot; Journal of the ACM, 2002</span>
    <p>The mathematical treatment of selfish routing, including the 4/3 bound discussed above. It requires more mathematical background than the other readings.</p>
  </li>
</ul>
