---
title: "Long Time No Blog"
date: 2023-03-13T17:38:23-06:00
draft: false
toc: true
keywords: ["blawx", "openfisca", "csps", "video"]
---

Wow, it's been nearly a year since I updated the blog? Wild.

First thing to note, the address has changed. Now that I understand better how to use multiple email addresses with
the same GitHub account, I've moved this blog to my personal GitHub account, so you will now find it at [https://gauntlet173.github.io/](https://gauntlet173.github.io/).
Assuming Microsoft doesn't become some sort of evil overlord, it should be able to live here for a while. Fingers crossed.

Quick catch-up in case you're interested...

### New Home Department

Since last time I blogged, I have moved inside the Government of Canada. I'm now the Director of Rules as Code at the Public Health Agency of Canada,
working under their Chief Data Officer, Chris Allison. My work is mostly the same, except that I am working on Blawx with new target use-cases in mind, and will be encoding some
different source texts.

### Lots of Work on Blawx

When I last posted, Blawx was on version 1.3.15-alpha. That's about 30 releases ago. Blawx is now at v1.5.1-alpha.  The major changes...

* User registration, authentication and authorization for projects
* Import/Export features
* Replacement of BlawxBot with new Scenario Editor
* New Time, Date, Datetime datatypes
* Lists, and Aggregation
* New natural-language explanation display
* A major change to how booleans are dealt with that simplified the code language
* A complete overhaul of defaults and exceptions
* The ability to specify when rules do not apply

Here's a video demo of the version that went live last Friday:

<iframe width="560" height="315" src="https://www.youtube.com/embed/jJnR5mrNfu8" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

### Lots of Work With Blawx

In addition to working ON Blawx, we have been working *with* Blawx. In fact, I took a few months at the end of last year
to step back from adding features in order to eat my own dogfood, and learn more from how Blawx was actually being used by the Canada School
of Public Service and its clients throughout the government.

That was an extremely valuable exercise. As a result of that learning, I have a much clearer idea of
what features it would be worth adding once the language itself settles down.

We have legitimately done some stuff at CSPS that I think are world firsts, and it sounds like the client department
would be open to spending some time bragging about them, so look for more on that in the coming months.

### Development Goals

The language is getting closer to settling down. I am currently prioritizing adding all the reasoning features to
the language that are required for the use cases coming from PHAC and CSPS's clients. At the moment, there is only
one such feature about which I harbour doubt, and that's temporal reasoning with event calculus. I know it can be
done with s(CASP), and I have played with small versions of it myself. I do not know whether it can be done in a
computationally-efficient way on top of all the other features Blawx already has.

But the fact is that I run into temporal reasoning tasks in legislation all the time. So we have to try it and see.

I'm also continuing to work on Scenario Editor, which provides a much cleaner interface for non-programmers to build
fact scenarios, ask questions, and get natural language explanations for the results. The more shiny I can make it,
the easier it will be to communicate the value of Rules as Code going forward, and that's Blawx's primary purpose.

April 15 will be the third anniversary since I published [my LLM thesis](https://papers.ssrn.com/sol3/papers.cfm?abstract_id=3577239), which set out a list of things that I
would want out of a declarative logic tool for legal knowledge representation. That thesis has been sort of a
recipe book for development of Blawx, and temporal reasoning is the last thing in that list that I still want.

Three years doing the LLM part time, followed by three years working full-time in computational law, and I will soon have
a fully-featured prototype designed in collaboration with users inside the Government of Canada.

If you had told me that's how it was going to go down when I started the degree, I would have said you were being
insanely optimistic. Pretty good for 6 years work.

### Notable Stuff

There was a [very cool report out of Japan](https://www.digital.go.jp/assets/contents/node/basic_page/field_ref_resources/b51af10d-39ff-44bf-9e1c-6a332e6bf4ea/9dc06578/20230123_meeting_administrative_research_working_group_en_01.pdf) on Legislative Affairs that discussed Rules as Code as basically the
ultimate stage in the digitalization of laws.

The OpenFisca people went to the World Governance Summit and won an innovation prize for their work. They also have [a cool video describing Rules as Code](https://youtu.be/gx6SDXe-E74). I can't say that I agree with Matti that you can't
encode criminal laws in Rules as Code. You can, and there may be good reasons to. You ought not use them to calculate the
outcomes of criminal cases, but that is a very different thing. I understand the motivation to avoid scaring people,
but without nuance I think there is a risk of convincing people that their fears are well-founded, when they are not,
and their reinforced fears may pose a hurdle elsewhere.

### Future Plans

* My [sprint for this week](https://github.com/orgs/Lexpedite/projects/3/views/7) is mostly cleaning up how 
  explanations appear in the new defaults and exceptions system, and in particular fixing 
  how logical and numerical constraints are displayed in the answers and explanations. That should give me what I need to
  start work on the temporal reasoning features next week, which are based on numerical constraints applied to timestamps.
* A paper I co-authored has been submitted to a peer review process, so there's some possibility of good news soon on that front.🤞🏻
* [LitCon](https://suffolklitlab.org/LITCon/2023/about/) is happening April 3 at Suffolk Law, I will be attending virtually.
* [CodeX FutureLaw](https://conferences.law.stanford.edu/futurelaw2023/) is happening April 13 at Stanford CodeX, I will also be attending that virtually.



