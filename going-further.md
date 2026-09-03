---
layout: default
title: Going further
description: The topics the Jumpstart sessions point at but do not have time to reach, and an annotated reading list.
permalink: /going-further/
sections:
  - id: braess
    label: The route problem
  - id: failures
    label: Seven failures
  - id: asides
    label: Three asides
  - id: reading
    label: Reading
---

Beyond the two sessions
{: .kicker}

# Going further

Each session runs for ninety minutes and covers a single idea. This page holds the material those ideas point at: where the route-choice problem leads, seven engineering failures and what each of them cost, and what to read next.
{: .lede}

## Where the route problem goes next {#braess}

In the session you found the equilibrium of a two-route network by voting, then added a road that cost nothing and made everybody slower. Then you minimised total travel time with a derivative and found that the best assignment is not the one people choose. Three directions lead out of that.

**The paradox is not about traffic.** The same structure appears wherever elements optimise locally inside a shared network. In an electrical network, adding a wire can raise the total power dissipated. In a mechanical version built from two springs and two strings, cutting a supporting string makes the load rise rather than fall. The effect does not depend on roads: it appears whenever each element responds to its own cost and nothing responds to the total.

**The gap you measured has a name.** The ratio between the cost of the equilibrium and the cost of the optimum is called the price of anarchy, and it is bounded. When every road's travel time is a linear function of how many people use it, as in the network you voted on, selfish routing costs at most 4/3 of the minimum possible total, and that bound is tight. So the damage a network can do to itself through individual choice is limited, and the limit is computable before the road is built.

Tim Roughgarden and Éva Tardos, *How bad is selfish routing?*, Journal of the ACM 49(2), 2002, 236 to 259.
{: .source}

**Roads have been removed on this reasoning.** Seoul demolished the Cheonggye elevated expressway in 2003 and restored the stream beneath it; Stuttgart reopened a section of new road only after closing it improved conditions. Both are cited often and both deserve more scepticism than they usually get. Each is an observation of a city that changed several things at once rather than a controlled experiment, and the effect attributed to the paradox is entangled with transit investment and induced demand. The mechanism is not in doubt, only the claim that these two cities are clean demonstrations of it.

## Seven failures worth knowing {#failures}

In each of these cases competent people, following the practice of their time, built something that killed people. Read the primary source rather than a retelling: the secondary accounts disagree with each other and often with the report.

### Therac-25, 1985 to 1987

A radiation therapy machine delivered massive overdoses to six patients in the United States and Canada. Several died. Earlier models had hardware interlocks that physically prevented the beam from firing at full power without a target in place; the Therac-25 removed them and relied on software to enforce the same condition. A race condition let a fast, practised operator edit the treatment screen faster than the software could reconcile it, and the machine fired in the wrong mode. The deeper failure was organisational: the manufacturer had no adequate mechanism for investigating reported accidents, and the operators' reports were not believed.

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

A year after the tower opened, its structural engineer, William LeMessurier, was asked by an undergraduate writing a thesis, Diane Hartley, about the building's behaviour under winds striking it at an angle. Checking, he found that a change made during construction, bolted rather than welded joints, left the tower vulnerable to a quartering wind of a kind expected roughly once every sixteen years if its tuned mass damper lost power. The joints were welded, at night, while the building stayed open. A newspaper strike meant almost nobody heard about it, and the episode stayed quiet for seventeen years. The part that matters is that the check happened only because someone outside the project asked a question.

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

Mariner 1 left Cape Canaveral for Venus on 22 July 1962, veered off course, and was destroyed by the range safety officer 293 seconds after launch. The cause is usually given as a missing hyphen, but it was a missing overbar. Someone transcribing the handwritten guidance equations dropped the bar above an R, and the software used the raw radar value where it should have used the smoothed one, so ordinary noise read as urgent course error. Arthur C. Clarke called it the most expensive hyphen in history, and his phrase has outlived the correction to it. Wrong details survive a long time when the story they are attached to is broadly right.

### The Harvard Mark II moth

On 9 September 1947 an operator of the Harvard Mark II taped a moth into the logbook with the note "First actual case of bug being found." The entry is usually offered as the origin of the word, which the wording itself rules out. You do not write *actual* unless *bug* already means something else, and it did: engineers had been calling faults bugs since at least Edison. The joke in the logbook is that this time there was a literal one. The moth is therefore evidence that the term was already in use rather than the origin of it.

### What computing is for

Richard Hamming opened *Numerical Methods for Scientists and Engineers* with a line that applies directly to your first programming course: "The purpose of computing is insight, not numbers." A correct number that nobody understands has not yet been checked.

## Reading {#reading}

<ul class="reading">
  <li>
    <a href="https://doi.org/10.1109/MC.1993.274940">An Investigation of the Therac-25 Accidents</a>
    <span class="src">Nancy Leveson and Clark Turner &middot; IEEE Computer, July 1993</span>
    <p>The primary source, and about forty pages. It covers the software defect, the missing hardware interlock, and the reporting process that let the same accident happen six times.</p>
  </li>
  <li>
    <a href="https://doi.org/10.1017/S0140525X00005756">Minds, Brains, and Programs</a>
    <span class="src">John Searle &middot; Behavioral and Brain Sciences, 1980</span>
    <p>The Chinese Room argument, that running the right program is not the same as understanding it. Twelve pages, no technical background needed, and still under argument.</p>
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
    <p>Petroski's case that design advances by failure, argued through bridges, roofs and everyday objects. The most readable book on this list, and a reasonable place to begin.</p>
  </li>
  <li>
    <a href="https://archive.org/details/computerpowerhum0000weiz_v0i3">Computer Power and Human Reason</a>
    <span class="src">Joseph Weizenbaum &middot; W. H. Freeman, 1976</span>
    <p>Weizenbaum wrote it after watching people confide in ELIZA, the chatbot he had built. It is about the difference between what a computer can be made to do and what it should be asked to decide, and it has aged unusually well.</p>
  </li>
  <li>
    <a href="https://doi.org/10.1145/506147.506153">How Bad Is Selfish Routing?</a>
    <span class="src">Tim Roughgarden and Éva Tardos &middot; Journal of the ACM, 2002</span>
    <p>Where the route-choice session leads if you follow the mathematics. Harder going than the rest of this list, and the result it builds to is the 4/3 bound.</p>
  </li>
</ul>
