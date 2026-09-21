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

Choosing a specialisation requires some knowledge of the work it involves. First-year courses and projects can help you acquire that knowledge, provided you examine what you have learned from them. We begin with this choice, then return to the engineering problems and case histories introduced in the sessions.
{: .lede}

## Exploring before committing to a path {#identity}

Suppose you arrive at university intending to study mechanical engineering because you like cars. You know which vehicles interest you, but you have not yet worked on a mechanical design. Your interest gives you a reason to investigate the field. It gives you less information about whether you would enjoy the work involved.

A design project can make that distinction clearer. Working on a suspension assembly might confirm your interest in mechanical design. You might instead find that you prefer writing the software that reads the sensors. In either case, you have examined a part of the work and can use that experience when deciding what to study next.

James Marcia distinguished two aspects of such decisions: **exploration**, the consideration of meaningful alternatives, and **commitment**, the investment in a choice. He used **identity foreclosure** to describe commitment without exploration. For example, a student might rule out other specialisations because they have always described themselves as a future mechanical engineer, without examining what that choice involves.

Marcia's framework distinguishes four identity statuses by how exploration and commitment relate:

<div class="table-wrap" markdown="1">

| Identity status | Exploration and commitment |
|---|---|
| Diffusion | No settled commitment and no active effort to resolve the choice; some exploration may have happened earlier. |
| Foreclosure | Commitment without seriously considering alternatives. |
| Moratorium | Active exploration, with commitment still unsettled. |
| Achievement | Commitment after considering meaningful alternatives. |

</div>

These categories distinguish uncertainty during exploration from a decision that has received little consideration. They do not identify which specialisation suits a student. Marcia's original study involved 86 male college students; it does not establish a timetable by which you should decide your future.

James E. Marcia, [*Development and validation of ego-identity status*](https://doi.org/10.1037/h0023281), Journal of Personality and Social Psychology 3(5), 1966, 551 to 558.
{: .source}

For a choice you are considering, identify something you still need to learn about the work. You could ask a design team about a beginner task or ask an upper-year student to describe a recent project. Include the routine work in that conversation: an account of debugging a sensor may tell you more about the project than a demonstration of the finished vehicle. Afterwards, record which activities you would like to try again and why.

Exploration need not lead to a different choice. You may retain your original plan because experience has confirmed your interest. Family advice and the need to earn a living can also inform the decision. The purpose is to examine those reasons alongside what you have learned about the work.

## Early frustration and changing direction {#practice}

Trying unfamiliar work creates a difficulty of its own: your first experience may consist mostly of mistakes. A programming assignment can take hours because you are still learning to interpret error messages. That experience shows what you cannot yet do, but it provides limited evidence about whether you will enjoy programming with more experience. We use **frustration barrier** here to describe this early difficulty.

To investigate the difficulty, choose a specific task and practise it with feedback. For debugging, ask someone more experienced to explain how they locate an error. Then use that method on another problem and explain why the program behaved differently from your prediction. This gives you a way to assess progress: you can check whether you now solve a problem that previously stopped you. The [learning loop]({{ '/how-to-study/' | relative_url }}#loop) describes this process in more detail.

Practice also gives you better information about your interests. You may become able to do the work and still have little interest in continuing it, or find that another part of the project interests you more. These are reasons to reconsider your plan. An initial difficulty is less informative because it is hard to separate your response to the work from your response to being unfamiliar with it.

A change of direction may affect your course sequence or the time needed to complete your degree. Before changing your course load or taking time away, discuss the options with [Engineering Academic Services]({{ '/help/' | relative_url }}#behind). That conversation can help you assess the consequences of a change alongside your reasons for making it.

## Explaining assumptions and results {#communication}

The route-choice calculation gives us an example of why an engineering result needs an explanation. We found that assigning 22 people to the shortcut minimises total travel time. A reader given only that number would not know that the remaining 46 people must split evenly between the other routes, or that those people could shorten their own trips by switching. The proposed assignment therefore needs both a calculation and an account of how it would be maintained.

When you explain a solution, state the problem and the assumptions before describing the method. Then interpret the result: say what it establishes and what remains unresolved. For the route problem, minimising total travel time establishes an assignment under the model's assumptions. It leaves open how to persuade people to follow that assignment.

You can practise this explanation in a lab report or a design-team update. Ask a classmate to read it and identify a step they cannot follow. Revise that step, then ask them to explain the result back to you. Their explanation gives you evidence about what your writing communicated and which assumptions you still need to make explicit.

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

Thirty-seven seconds after the start of the main engine ignition sequence, the launcher lost all guidance and attitude information and destroyed itself. The inertial reference system had converted a 64-bit floating-point value, the horizontal bias, into a 16-bit signed integer. The value exceeded the integer range. Engineers had left the conversion unprotected because their analysis of the Ariane 4 trajectory ruled out an overflow. Ariane 5 flew a different trajectory, so that analysis no longer justified the decision. The failure followed from reusing the code without re-examining the assumption that made the conversion safe.

*Ariane 5: Flight 501 Failure*, Report by the Inquiry Board, Paris, 19 July 1996.
{: .source}

### Hyatt Regency walkways, Kansas City, 17 July 1981

Two suspended walkways in the hotel atrium collapsed during a crowded tea dance, killing 114 people and injuring more than 200. The original design hung both walkways from a single continuous set of rods. During fabrication that was changed to two shorter rods, one from the ceiling to the upper walkway and a second from the upper walkway to the lower. This change doubled the load on the upper walkway's box beam connection, which had not been designed to carry it. The change simplified fabrication, but the review did not identify its effect on the load.

Marshall et al., *Investigation of the Kansas City Hyatt Regency Walkways Collapse*, NBS Building Science Series 143, National Bureau of Standards, 1982.
{: .source}

### Lac-Mégantic, Quebec, 6 July 2013

An unattended freight train carrying petroleum crude oil rolled downgrade into the centre of town. Sixty-three tank cars derailed, the oil ignited, and 47 people died. The Transportation Safety Board identified eighteen contributing factors, including too few handbrakes applied and no effective test of whether they held, a locomotive shut down after a fire left no air brakes, tank cars that breached readily, a safety management system the regulator had not adequately audited, and a company operating with thin margins on a line it had bought cheaply. The report examines how failures in securing the train combined with equipment limitations and inadequate oversight.

Transportation Safety Board of Canada, Railway Investigation Report R13D0054, 2014.
{: .source}

### Citicorp Center, New York, 1978

A year after the tower opened, its structural engineer, William LeMessurier, was asked by an undergraduate writing a thesis, Diane Hartley, about the building's behaviour under winds striking it at an angle. His check found that the use of bolted joints in place of the specified welded joints left the tower vulnerable to a quartering wind of a kind expected roughly once every sixteen years if its tuned mass damper lost power. Crews welded the joints at night while the building stayed open. A newspaper strike meant almost nobody heard about it, and the episode stayed quiet for seventeen years. A question from outside the project prompted the engineer to re-examine the design.

Joe Morgenstern, *The Fifty-Nine-Story Crisis*, The New Yorker, 29 May 1995.
{: .source}

### Tacoma Narrows Bridge, 7 November 1940

The bridge twisted itself apart in a 68 km/h wind four months after opening. Billah and Scanlan examine textbook accounts that attribute the failure to forced resonance: a periodic force matching the structure's natural frequency. They explain the failure as **flutter**, an instability in which the deck's twisting motion changes the aerodynamic forces in a way that increases the motion. This mechanism differs from an external periodic force driving the bridge at its natural frequency. Aeronautical engineers already understood flutter in 1940, but bridge engineers were not reading the aeronautical literature.

K. Yusuf Billah and Robert Scanlan, *Resonance, Tacoma Narrows bridge failure, and undergraduate physics textbooks*, American Journal of Physics 59(2), 1991, 118 to 124.
{: .source}

### Quebec Bridge, 29 August 1907

The south cantilever of what would have been the world's longest bridge span buckled and fell into the St Lawrence. Seventy-five of the 86 workers on the span died, 33 of them Mohawk ironworkers from Kahnawake. The Royal Commission found that the consulting engineer, Theodore Cooper, had underestimated the structure's dead weight and never corrected it, and that he supervised from New York and visited rarely. The compression chords had been visibly bending for days. Nobody on site had both the authority and the standing to stop the work.

This is the failure behind the Iron Ring, worn by Canadian engineers since the Ritual of the Calling of an Engineer began in 1925. The first rings were made by veterans at the Christie Street Military Hospital in Toronto, rather than forged from the bridge wreckage as a common account claims.

Royal Commission on the Quebec Bridge Inquiry, Report, 1908. On the ring itself, see ironring.ca.
{: .source}

## Three asides {#asides}

### Mariner 1 and the missing overbar

Mariner 1 left Cape Canaveral for Venus on 22 July 1962, veered off course, and was destroyed by the range safety officer 293 seconds after launch. The cause is usually given as a missing hyphen, but it was a missing overbar. Someone transcribing the handwritten guidance equations dropped the bar above an R, and the software used the raw radar value where it should have used the smoothed one, so ordinary noise read as urgent course error. Arthur C. Clarke called it the most expensive hyphen in history, and his phrase has outlived the correction to it. The familiar retelling obscures the distinction between a punctuation error in code and a missing mathematical symbol in the guidance specification.

### The Harvard Mark II moth

On 9 September 1947 an operator of the Harvard Mark II taped a moth into the logbook with the note "First actual case of bug being found." Engineers had used *bug* to mean a fault since at least Edison. The logbook entry plays on that established meaning: this fault involved an insect. It records an example of the term in use, although later accounts often cite it as the term's origin.

### What computing is for

Richard Hamming opened *Numerical Methods for Scientists and Engineers* with a line that applies directly to your first programming course: "The purpose of computing is insight, not numbers." For a calculated result, explain what the number measures and check its units and physical plausibility. Those checks connect the calculation to the problem it was intended to solve.

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
    <p>Searle uses the Chinese Room thought experiment to argue that running a program does not by itself establish understanding. The explanation does not require a programming background.</p>
  </li>
  <li>
    The Milk of Human Intentionality
    <span class="src">Daniel Dennett &middot; open peer commentary printed with Searle's paper, 1980</span>
    <p>Dennett responds to Searle in the commentaries published with the article. The issue includes about two dozen commentaries and Searle's replies, allowing you to compare the argument with objections to it.</p>
  </li>
  <li>
    <a href="https://archive.org/details/whatengineerskno0000vinc">What Engineers Know and How They Know It</a>
    <span class="src">Walter Vincenti &middot; Johns Hopkins University Press, 1990</span>
    <p>Vincenti examines five cases from aeronautical history to explain how engineers develop knowledge through design. His account distinguishes that knowledge from the application of scientific results.</p>
  </li>
  <li>
    <a href="https://archive.org/details/toengineerishuma00petr">To Engineer Is Human</a>
    <span class="src">Henry Petroski &middot; St Martin's Press, 1985</span>
    <p>Petroski examines failures in bridges, roofs and everyday objects to explain how engineers revise designs. The case histories do not assume specialist engineering knowledge.</p>
  </li>
  <li>
    <a href="https://archive.org/details/computerpowerhum0000weiz_v0i3">Computer Power and Human Reason</a>
    <span class="src">Joseph Weizenbaum &middot; W. H. Freeman, 1976</span>
    <p>Weizenbaum wrote it after watching people confide in ELIZA, the chatbot he had built. It is about the difference between what a computer can be made to do and what it should be asked to decide.</p>
  </li>
  <li>
    <a href="https://doi.org/10.1145/506147.506153">How Bad Is Selfish Routing?</a>
    <span class="src">Tim Roughgarden and Éva Tardos &middot; Journal of the ACM, 2002</span>
    <p>Roughgarden and Tardos derive bounds on the cost of selfish routing, including the 4/3 bound discussed above. The proofs require more mathematical background than the other readings.</p>
  </li>
</ul>
