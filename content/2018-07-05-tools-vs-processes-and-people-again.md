layout: post
title: Tools vs Processes and People (again)
author: devcurmudgeon
date: 2018/07/05

It's a year since I wrote the "People vs Processes and Tools" article. Apart
from being busy with other things, the main reason I don't write very much
here is that my criteria for a post are:

- cover something that I want (or need) to assert in public
- include something new/innovative/challenging, that isn't widely understood
- stand the test of time, i.e. hopefully still be valid in a decade

Suprisingly the main thing I feel compelled to write now is actually another
assault on the "People, Processes, Tools" dogma, which has been been lobbed
at me a lot, recently, as a magic spell to thwart my reasoning or
recommendation about a specific tool or set of tools.

In other words, the underlying message is...

"You're wrong to even be thinking about the tool(s) at this point. We need to
figure out the team and organisation first, then establish the processes that
matter... and then will be the time to choose the tools."

My internal monolog takes this further...

"...And by then, Paul, you'll no longer be one of the People involved. And in
any case we'll have established Processes that you would either refuse or fail
to follow. And just to completely box this off, we'll be choosing a **different
tool**, that you don't like, to demonstrate how wrong you were. And we'll make
sure you aren't even allowed to access it."

AFAIK the People>Processes>Tools ordering was originally cited as part of the
Six Sigma approach. It may well be fantastic in that context - I have no idea.
But for large scale software work, particularly in established organisations,
it seems largely irrelevant to me.

For a start, there aren't many effective levers we can pull with **People**:

- lead, manage
- incentive and environment factors
- educate/train
- hire
- fire
Without adequate leadership, management, incentives and environment the
remaining factors don't actually get us very far.

If we have the wrong people leading, no amount of education/training will
help. Inadequate managers will struggle to even **recognise**, let alone **hire** the
right people. And firing established staff is usually surprisingly stressful
and difficult.

Most of the **Processes** I've ever seen documented were at least in part

- unworkable in practice, and/or
- not relevant to the actual objectives

People who define processes without understanding both the details of the
actual work, and the stakeholder objectives and values, will usually produce
bad processes. Ironically, these documents are usually described as 
"Quality Processes".

**So what's the answer?**

Based on some decades of experience, and with a number of successful
(as well as unsuccessful) projects delivered in various scenarios,
I'd like to describe my alternative:

Philosophy => Key People => Tools and Environment => More People => Processes

**Philosophy:** let's make sure that we're as clear as we can be about what is
the best/right work to do, before we start. This is where our leadership needs
to get its principles, intentions and objectives straight. We may need to
adapt/improvise later but doing the thinking early can avoid a huge amount of
waste and grief later.

**Key People:** now onboard the (core, small) set of Key People, selected for
their knowledge and ability, to lead/drive/implement the initial phase,
which will be...

**Tools and Environment:** choose the best Tools for the work, and set them up
 in an Environment which

- is dogfooded (used and tested by the Key People)
- is reliable, reproducible, backed up etc
- causes minimal friction for the work
- is locked down so normal users working in good faith can't actually break anything
- has appropriate gates for review/quality/validation/signoff (but note that
  gates can cause bottlenecks and friction)
- is simple and obvious for users who are competent and experienced in the work
- is self-service (minimal handover/wait-steps) so users can get on with their jobs
- provides enough basic documentation for new users to get going quickly
- provides immediate and correct feedback from user actions so that problems
and documentation can be improved quickly and effectively
- collects and maintains evidence about the work done

**More People:** Onboard the rest of the team, preferably in phases, and:

- fix the problems they encounter
- document the things they find confusing or unclear
- measure the bottlenecks and do everything practical to reduce them and
increase overall throughput

Once this is working, the remaining step is...

**Process:** Now that everything is running, we can relatively easily document
what the actual processes are. However, this may not actually be worth doing:

- we already have the best tools for the job, in a low-friction environment
- we already have with evidence of appropriate reviews/approvals and outputs
- we are already measuring our throughput and reducing bottlenects

If you're still here, your internal alarm may be wailing

"Hah! He's hidden 'People, Processes, Tools' in his "Key People => Tools and
Environment' steps. The people chose tools to implement their implied processes."

Actually, that's true;

I work with the best **People** I can find, and I've learned a huge amount from
them. As a result I'm relatively experienced in both software engineering
(doing the work) and the business implications of software engineering
(stakeholder). As a result I'm relatively confident in what software enginering
**Processes** at scale need to involve; in my view they boil down to

"continous integration, automated test, and continous delivery... with
evidence of provenance, reviews and approvals.""

And so, in the end, I recommend specific **Tools** that help to achieve that.

