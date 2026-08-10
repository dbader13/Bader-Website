---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "How the creator of the first Linux supercomputer built a second brain for his research lab"
subtitle: "David Bader used Adapter Mind to give Claude persistent cognition and power a proactive dashboard for his NJIT research group."
summary: ""
authors: []
tags: []
categories: []
date: 2026-08-05T13:02:48-04:00
lastmod: 2026-08-05T13:02:48-04:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

*By **David Bader**, Co-Founder, Chief Knowledge Officer*

{{<figure src="adapter.jpg">}}

## The same problem at every scale ##

The challenges I have worked on all share a shape. The graph is too large to hold in memory, too irregular to partition cleanly, and changing too fast to rebuild from scratch. A coordinated intrusion hiding in billions of network events an hour. Evolutionary history read across whole genomes, not single genes. The handful of accounts laundering money through a financial system that clears tens of millions of transactions a day. A pathogen crossing an entire country's contact network. Coordination across a social graph with hundreds of millions of actors. In every one, the answer you need is a global property of the structure, so sampling will not save you, and by the time a batch computation finishes the graph has already moved.

That is the real difficulty, and it is why this class of problem resisted progress for so long. Not scale by itself, but scale combined with irregularity and constant change, on machines architected for dense regular work. Getting these computations onto hundreds of thousands of cores, and getting answers back in seconds rather than days, is the work of my career.

My research lab poses the same problem in miniature. Too large to hold in my head, too irregular to partition, because one decision leaves fragments in four systems, and moving faster than I can rebuild my picture of it. Who needs my attention and why is a global property too. Reading my last twenty emails is sampling.

## The silent student ##

I run [a research lab](https://datascience.njit.edu/about) at the New Jersey Institute of Technology. Students who are stuck on a problem often let me know with a 2am email or by showing up to office hours with their issue. They are hard to miss, and once I know there’s a problem, I can usually help.

But I worry more about the students I don’t hear from. They might have gotten tripped up on something small, like losing access to a computing cluster or a software library that refuses to build properly. But often they feel embarrassed about making no progress, so they don’t ask for help. By the time the problem surfaces, half the semester is gone.

Silence can also be difficult to interpret. Three weeks with no update from a doctoral student might be normal as they write a chapter, but for an undergrad, that’s a red alert. Silence means nothing without context.

Communication (or a lack of it) is just one among dozens of signals that I need to follow. At any given time, our lab has papers under revision, proposals in progress, experiments running, code waiting for review, and grant deadlines looming. Context is spread across documents, email, calendars, Slack, GitHub, and more.

I have spent over thirty years designing systems to find patterns in enormous, fast-changing datasets. Yet, like most managers, I had no reliable way to see what was happening across my own research lab, and spent much my of my day trying to answer: ***who in my group needs my attention, and why?***

I can’t keep it all in my head, so with the help of AI, I set out to build a system that could.

## Giving Claude understanding of my lab ##

I connected Claude to my Gmail and Calendar, which gave it access to much of the information flowing through my research group. When Claude uses a connector, it can retrieve relevant emails, events, and documents and bring that information into its context window to produce a better answer.

I then asked Claude (Opus 5, on high-reasoning mode): ***What should my research group focus on during the next week?***

{{<figure src="claude1.jpg">}}

Claude told *me* it didn’t have enough context to give an answer and instead asked me to explain our projects and priorities to *it*. While that answer is honest, it’s not helpful. In this case, it seems as though Claude failed to call the tools that would help it find the evidence.

As a user, I should not need to diagnose why I got an unsatisfactory answer, or really even understand how these systems work at all. I asked a reasonable question about my own work — the product should know how to investigate it.

Even when the AI calls tools correctly, a deeper problem remains: the process of creating understanding starts with my prompt. The moment I hit enter, Claude’s work begins. It interprets my question, decides where to search, retrieves the relevant information, and places that data into its context window. It works out what that information means while generating the answer.

This works well for many questions and tasks about ***the world***— for general knowledge or a few relevant records. But when it comes to reasoning about ***your world*** — your team, your business, your life — this approach falls short.

A single event in my lab may leave fragments across four systems. Let’s say a student decides to restructure a benchmark during a one-on-one with me. They articulated their reasoning prior to the meeting in Slack, they publish the updated code to GitHub over the weekend, and my co-reviewer’s feedback arrives by email the following week. Answering “*what is happening with the benchmark?*” requires the system to recognize one student, project, and decision, and understand how each fragment relates to the next through time.

**Adapter Mind does exactly that:** ***it builds the understanding you need before you ask a question.***

Adapter Mind continuously processes new information from the systems where my group works. It resolves people and projects across those systems, connects new activity to the history behind it, and maintains an up-to-date picture of my lab.

I made my Adapter Mind available to Claude and asked the same question again:

{{<figure src="claude2.jpg">}}

Now Claude can reason over a current, accurate, and persistent understanding of my lab — and provide a far better answer. I can finally ask complex and abstract questions to my model without first reconstructing the context.

A system cannot become truly “superintelligent” if I have to first explain my world well enough to answer the question myself. Models will keep getting more powerful, but bigger context windows and greater reasoning power cannot compensate for a lack of fundamental understanding. This is what Adapter supplies.

## From reactive to proactive ##

Remember my worry about the student who goes quiet? A chat interface is perfect for questions on my mind, but won’t flag the student I forget to ask about.

So in an afternoon, I built a proactive system with a dashboard powered by the same Adapter mind:

{{<figure src="radar.jpg">}}

This app runs on Cloudflare Workers and queries the same Adapter Mind every thirty minutes. Each pass looks at one of my students and asks a narrow set of questions: *What has moved since our last check-in? Is something waiting on me? Is the work blocked? Is a deadline approaching? Has the thread gone quiet?*

Adapter returns facts with evidence. I wrote a deterministic function in my own code to turn those facts into a priority score. The board above shows me who may need attention and why, while a separate brief tool flags blockers, deadlines, and progress for me every morning.

Claude helped me write the application, while Adapter supplied the cognition harness.

In the past, building a comparable cognition layer would have required a small army of engineers to build the data ingestion and processing pipelines and maintain the infrastructure to keep everything in the graph current. I should know, because I have spent my career building these complex graphs systems and managing those teams of engineers!

With Adapter, that complexity is simplified behind one API and cognition can be accessed for pennies.

## Working from one mind ##

I now use the same Adapter Mind in two ways: Claude with Adapter connected answers the questions on my mind, while my dashboard app keeps watch 24/7 and brings important updates to me. Together, they help me make decisions faster, unblock work, and focus my attention where I can make the greatest difference. Now, I have a better chance of helping a silent student while their problem is still small.

The afternoon was the easy part. Every other system like this that I've built throughout my career came with a funded team and years on real machines. The build was never the cost. A graph of a living organization is only worth having if it is current, so someone has to keep it current, and the obligation never ends. Which is why this has only ever existed inside organizations that could staff it. I was not going to hire a team to find out which of my students is quietly stuck.

With Adapter, that obligation sits behind one API, and it stays current whether or not I am paying attention to it.

That’s what I need from AI: an understanding of what is happening in my world, and the ability to help me act in time.

## About David Bader ##

David A. Bader is Co-Founder and Chief Knowledge Officer at Adapter, a Distinguished Professor of Data Science at NJIT, and Director of its Institute for Data Science. A pioneer in high-performance computing and large-scale graph analytics, he is a Fellow of the ACM, IEEE, AAAS, and SIAM and a recipient of the IEEE Sidney Fernbach Award.

For more than thirty years, David has built systems to find patterns and relationships across enormous, constantly changing datasets. He has applied this work to detecting coordinated intrusions across billions of network events, tracing financial crime through tens of millions of transactions, and modeling how disease spreads through an entire country. His career has been focused on making complex, fast-moving systems understandable, so people get answers that matter and act on them in time.

https://www.adapter.com/blog/building-a-second-brain-for-university-research-lab


