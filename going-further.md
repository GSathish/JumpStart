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

Ninety minutes holds one idea properly. It does not hold the things that idea points at. This page is the rest of it: where the route-choice problem goes next, seven failures worth knowing, and what to read.
{: .lede}

## Where the route problem goes next {#braess}

In the session you found the equilibrium of a two-route network by voting, then added a road that cost nothing and made everybody slower. Then you minimised total travel time with a derivative and found that the best assignment is not the one people choose. Three directions lead out of that.

**The paradox is not about traffic.** The same structure appears wherever elements optimise locally inside a shared network. In an electrical network, adding a wire can raise the total power dissipated. In a mechanical version built from two springs and two strings, cutting a supporting string makes the load rise rather than fall. Nothing about roads is doing the work; what does the work is that each element responds to its own cost and none of them responds to the total.

**The gap you measured has a name.** The ratio between the cost of the equilibrium and the cost of the optimum is called the price of anarchy. It is not unbounded. When every road's travel time is a linear function of how many people use it, as in the network you voted on, selfish routing costs at most 4/3 of the minimum possible total, and that bound is tight. So the damage a network can do to itself through individual choice is limited, and the limit is computable before the road is built.

Tim Roughgarden and Éva Tardos, *How bad is selfish routing?*, Journal of the ACM 49(2), 2002, 236 to 259.
{: .source}

**Roads have been removed on this reasoning.** Seoul demolished the Cheonggye elevated expressway in 2003 and restored the stream beneath it; Stuttgart reopened a section of new road only after closing it improved conditions. Both are cited constantly and both are worth reading sceptically. They are observations of cities that changed several things at once, not controlled experiments, and the effect attributed to the paradox is entangled with transit investment and induced demand. The theory is solid. The field evidence is suggestive.

## Seven failures worth knowing {#failures}

Engineering is taught through its successes and learned through its failures. Each of these is a case where competent people, following the practice of their time, produced something that killed. Read the primary source rather than the retelling; the secondary accounts disagree with each other and often with the report.

### Therac-25, 1985 to 1987

A radiation therapy machine delivered massive overdoses to six patients in the United States and Canada. Several died. Earlier models had hardware interlocks that physically prevented the beam from firing at full power without a target in place; the Therac-25 removed them and relied on software to enforce the same condition. A race condition let a fast, practised operator edit the treatment screen faster than the software could reconcile it, and the machine fired in the wrong mode. The deeper failure was organisational: the manufacturer had no adequate mechanism for investigating reported accidents, and the operators' reports were not believed.

Nancy Leveson and Clark Turner, *An Investigation of the Therac-25 Accidents*, IEEE Computer 26(7), July 1993, 18 to 41. doi:10.1109/MC.1993.274940
{: .source}

### Ariane 5 Flight 501, 4 June 1996

Thirty-seven seconds after the start of the main engine ignition sequence, the launcher lost all guidance and attitude information and destroyed itself. The inertial reference system had converted a 64-bit floating-point value, the horizontal bias, into a 16-bit signed integer. The value did not fit. The conversion was left unprotected because an analysis had shown the overflow could not occur, and that analysis was correct: for the Ariane 4 trajectory. Ariane 5 flew a different trajectory. The code was not wrong. The code plus its assumed context was wrong, and only one of those two things had been reviewed.

*Ariane 5: Flight 501 Failure*, Report by the Inquiry Board, Paris, 19 July 1996.
{: .source}

### Hyatt Regency walkways, Kansas City, 17 July 1981

Two suspended walkways in the hotel atrium collapsed during a crowded tea dance, killing 114 people and injuring more than 200. The original design hung both walkways from a single continuous set of rods. During fabrication that was changed to two shorter rods, one from the ceiling to the upper walkway and a second from the upper walkway to the lower. The change looks like nothing on a drawing. It doubled the load carried by the upper walkway's box beam connection, which had not been designed for it. The detail was a shop convenience, and the review that should have caught it did not.

Marshall et al., *Investigation of the Kansas City Hyatt Regency Walkways Collapse*, NBS Building Science Series 143, National Bureau of Standards, 1982.
{: .source}

### Lac-Mégantic, Quebec, 6 July 2013

An unattended freight train carrying petroleum crude oil rolled downgrade into the centre of town. Sixty-three tank cars derailed, the oil ignited, and 47 people died. No single person caused it. The Transportation Safety Board identified eighteen contributing factors: too few handbrakes applied and no effective test of whether they held, a locomotive shut down after a fire left no air brakes, tank cars that breached readily, a safety management system the regulator had not adequately audited, and a company operating with thin margins on a line it had bought cheaply. Every defence was present in some form. Every one of them was thin.

Transportation Safety Board of Canada, Railway Investigation Report R13D0054, 2014.
{: .source}

### Citicorp Center, New York, 1978

A year after the tower opened, its structural engineer, William LeMessurier, was asked by an undergraduate writing a thesis, Diane Hartley, about the building's behaviour under winds striking it at an angle. Checking, he found that a change made during construction, bolted rather than welded joints, left the tower vulnerable to a quartering wind of a kind expected roughly once every sixteen years if its tuned mass damper lost power. The joints were welded, at night, while the building stayed open. A newspaper strike meant almost nobody heard about it, and the episode stayed quiet for seventeen years. The question worth sitting with is not whether he did the right thing. It is that the check happened only because someone outside the project asked.

Joe Morgenstern, *The Fifty-Nine-Story Crisis*, The New Yorker, 29 May 1995.
{: .source}

### Tacoma Narrows Bridge, 7 November 1940

The bridge twisted itself apart in a 68 km/h wind four months after opening. Physics textbooks still describe this as forced resonance, wind supplying a periodic push that matched the structure's natural frequency. It was not. The failure was aerodynamically induced self-excitation in torsion, a negative-damping instability now called flutter, in which the motion of the deck generates the very forces that amplify it. Resonance and self-excitation are different phenomena with different mathematics. Aeronautical engineers already understood flutter in 1940; bridge engineers were not reading their literature.

K. Yusuf Billah and Robert Scanlan, *Resonance, Tacoma Narrows bridge failure, and undergraduate physics textbooks*, American Journal of Physics 59(2), 1991, 118 to 124.
{: .source}

### Quebec Bridge, 29 August 1907

The south cantilever of what would have been the world's longest bridge span buckled and fell into the St Lawrence. Seventy-five of the 86 workers on the span died; 33 were Mohawk ironworkers from Kahnawake. The Royal Commission found that the consulting engineer, Theodore Cooper, had underestimated the structure's dead weight and never corrected it, and that he supervised from New York and visited rarely. The compression chords had been visibly bending for days. Nobody on site had both the authority and the standing to stop the work.

This is the failure behind the Iron Ring, worn by Canadian engineers since the Ritual of the Calling of an Engineer began in 1925. One thing to get right when you are told the story: the first rings were not forged from the wreckage. They were made by veterans at the Christie Street Military Hospital in Toronto. The obligation is real; the relic is a myth.

Royal Commission on the Quebec Bridge Inquiry, Report, 1908. On the ring itself, see ironring.ca.
{: .source}

## Three asides {#asides}

### The most expensive hyphen in history was not a hyphen

Mariner 1 left Cape Canaveral for Venus on 22 July 1962, veered off course, and was destroyed by the range safety officer 293 seconds after launch. The cause is usually given as a missing hyphen. It was a missing overbar. Someone transcribing the handwritten guidance equations dropped the bar above an R, and the software used the raw radar value where it should have used the smoothed one, so ordinary noise read as urgent course error. Arthur C. Clarke's line stuck because it is better than the truth. Notice how comfortably a wrong detail travels when the story it supports is right.

### Why "actual"?

On 9 September 1947 an operator of the Harvard Mark II taped a moth into the logbook with the note "First actual case of bug being found." The entry is usually offered as the origin of the word. Read it again. You do not write *actual* unless *bug* already means something else, and it did: engineers had been calling faults bugs since at least Edison. The joke in the logbook is that this time there was a literal one. The moth is not the origin of the term. It is evidence that the term was already old.

### What computing is for

Richard Hamming opened *Numerical Methods for Scientists and Engineers* with a line worth keeping near your first programming course: "The purpose of computing is insight, not numbers." A correct number that nobody understands is not a finished piece of engineering. It is a result waiting to be checked.

## Reading {#reading}

<ul class="reading">
  <li>
    <a href="https://doi.org/10.1109/MC.1993.274940">An Investigation of the Therac-25 Accidents</a>
    <span class="src">Nancy Leveson and Clark Turner &middot; IEEE Computer, July 1993</span>
    <p>The primary source, and the best forty pages you can read on how software kills people. Read it before any retelling.</p>
  </li>
  <li>
    <a href="https://doi.org/10.1017/S0140525X00005756">Minds, Brains, and Programs</a>
    <span class="src">John Searle &middot; Behavioral and Brain Sciences, 1980</span>
    <p>The Chinese Room argument: that running the right program is not the same as understanding. Twelve pages, no jargon, and still argued about.</p>
  </li>
  <li>
    The Milk of Human Intentionality
    <span class="src">Daniel Dennett &middot; open peer commentary printed with Searle's paper, 1980</span>
    <p>The reply, and it is in the same journal issue: Searle's article was published with two dozen commentaries and his response to them. Read the argument and its opposition in one sitting.</p>
  </li>
  <li>
    <a href="https://archive.org/details/whatengineerskno0000vinc">What Engineers Know and How They Know It</a>
    <span class="src">Walter Vincenti &middot; Johns Hopkins University Press, 1990</span>
    <p>Engineering knowledge is not applied science, and this book shows why through five cases from aeronautics. The one to read if you ever wonder what your degree is actually teaching you.</p>
  </li>
  <li>
    <a href="https://archive.org/details/toengineerishuma00petr">To Engineer Is Human</a>
    <span class="src">Henry Petroski &middot; St Martin's Press, 1985</span>
    <p>The case that design advances by failure. The most readable book on this list; start here if you start anywhere.</p>
  </li>
  <li>
    <a href="https://archive.org/details/computerpowerhum0000weiz_v0i3">Computer Power and Human Reason</a>
    <span class="src">Joseph Weizenbaum &middot; W. H. Freeman, 1976</span>
    <p>Written by the author of ELIZA after watching people confide in it. On the difference between what a computer can be made to do and what it should be asked to decide. Fifty years old and about this week.</p>
  </li>
  <li>
    <a href="https://doi.org/10.1145/506147.506153">How Bad Is Selfish Routing?</a>
    <span class="src">Tim Roughgarden and Éva Tardos &middot; Journal of the ACM, 2002</span>
    <p>Where the route-choice session goes if you follow the mathematics. Harder than the rest of this list, and the payoff is the 4/3 bound.</p>
  </li>
</ul>
