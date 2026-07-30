---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "An Agent That Reads the Federal Register So You Don't Have To"
subtitle: "How a weekend project became a research-alert system for the Ying Wu College of Computing"
summary: ""
authors: []
tags: []
categories: []
date: 2026-07-30T13:09:24-04:00
lastmod: 2026-07-30T13:09:24-04:00
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

There is a particular kind of email that arrives too late. A colleague forwards a solicitation with three weeks to the deadline, and it is a perfect fit for work you have been doing for years, and three weeks is not enough time to write a competitive proposal. You file it away for next cycle, and next cycle you are busy, and the cycle after that the program has changed.

The information was public the whole time. It was sitting on grants.gov the day it posted. Nobody read it, because reading all of it is nobody's job.

That is the problem I set out to solve this month, and the solution turned out to be smaller than I expected.

## The shape of the problem ##

As Associate Dean for Research, part of my charge is making sure our faculty know about funding opportunities that fit their work. In principle this is simple: watch the agencies, match calls to people, send an email. In practice it fails at the matching step. NSF alone posts more than a hundred active opportunities. Add NASA, DoD, DOE and HHS and the volume is well past what anyone will read weekly, and the fraction relevant to any one faculty member is small enough that a broadcast-to-all approach trains people to ignore you.

The obvious fix is a keyword alert. I have tried keyword alerts. They fail in both directions at once: "graph" matches a call about graphical user interfaces, and misses one about combinatorial scientific computing. Research areas are not keywords, and the gap between what a solicitation says and what it means is exactly the gap a person spends years of training learning to read.

That gap is where a language model earns its keep.

## What I built ##

The system runs every Monday morning. It queries grants.gov for newly posted opportunities from five agencies, applies a cheap keyword filter to discard the obviously irrelevant, and for each survivor asks Claude a single question: given this call and this roster of sixty-six faculty, who does this genuinely fit?

The model is instructed to be strict, and told explicitly that returning nobody is the correct and common answer. For each real match it drafts an email in my voice, referencing that person's actual research rather than generic praise. The drafts land in my Gmail Drafts folder. I read them, edit or discard, and press send.

Nothing goes out automatically. That was the first design decision and the one I would defend hardest.

## Why HHS was the hardest one to add ##

The first four agencies were the same problem five times over. HHS, which is how NIH reaches grants.gov, was different in kind.

Volume was the obvious issue: HHS posts more than the other four combined, and the overwhelming majority is clinical work with no computational component at all. But the subtler issue was that the naive filter fails in both directions here. Screen too hard on computing vocabulary and you drop the biomedical informatics calls that several of our faculty are among the best-positioned people in the country to answer. Screen too softly and you match a computer scientist to a clinical trial because the abstract used the word "data."

The fix was two-sided. The keyword gate learned a biomedical vocabulary: bioinformatics, ontologies and terminologies, medical imaging, genomics, clinical decision support. And the model was given an explicit instruction that NIH calls usually presume a clinical or biological research program, and that a computing faculty member should be matched only where the call genuinely wants methods and would support a computational lead or co-investigator.

That instruction is doing real work. Without it the system is enthusiastic in exactly the way that makes people stop opening your email.

## Three things I got wrong ##

*I over-engineered it.* My first architecture ran on Cloudflare Workers with a vector database for semantic retrieval, a SQL store for state, and a scheduled Durable Object to coordinate it all. It was a defensible design for a roster of a thousand. For sixty-six faculty, the entire roster is about three thousand tokens and fits in a single prompt. The vector database solved a problem I did not have.

The version now running is one file of Google Apps Script, pasted into a browser. No servers, no deployment, no build step. It took an afternoon.

*I assumed the wrong email stack.* I designed around Microsoft Graph before remembering that our shop is Google. This mattered more than it sounds: the Graph route needed an Entra application registration and IT approval for mailbox permissions, a conversation measured in weeks. Apps Script runs as me, so it needs no permission grant at all. The infrastructure question and the organizational question turned out to be the same question.

*I trusted the model to follow a format.* Early runs failed because I asked for JSON and received a thoughtful paragraph of reasoning followed by JSON. The fix is tool use: define a schema, force the call, receive a parsed object. There is no text to parse and therefore nothing to parse wrongly. If you are building anything that consumes model output programmatically, start there rather than arriving there.

## What the roster exercise turned up ##

Building the faculty roster was supposed to be the boring part. It was the most useful part.

I extracted sixty-five profiles from our research report, then gathered email addresses from our own public pages. The addresses follow at least three different conventions, which is worth knowing if you have ever guessed at a colleague's address and wondered why it bounced.

More interesting was what the data itself revealed. One faculty member's entry listed a title that conflicted with a current appointment. Another had no publications recorded at all. A third was on record with grant history that substantially understated what he actually holds, which I only learned because he wrote back to correct it.

None of this was hidden. It was simply never assembled in one place where the inconsistencies would be visible next to each other. The agent needed a clean roster, and needing one is what produced one.

Jim Geller, reviewing his own entry, made the obvious suggestion: every faculty member should verify their own. He is right, and that is coming.

## What it does not do ##

The system reads grants.gov. Grants.gov does not carry everything. NSF Dear Colleague Letters, most DARPA BAAs, some DOE Office of Science announcements, and NIH notices that never become full funding opportunity announcements appear only on agency sites. DCLs are often the most time-sensitive thing CISE issues, so their absence is a real gap rather than a rounding error. I still check those by hand.

It also cannot know things that are not written down: who is already over the two-proposal limit, who is on leave, who tried this program in 2023 and got reviews that would take a year to address. That context lives with the people, not the data, which is one reason a human still presses send.

## The general lesson ##

The interesting part of this project was not the AI. It was discovering how much of the work was organizational rather than technical: whose email system, whose permissions, whose data was stale and in what direction.

The model did one thing well, which was reading a solicitation and telling me which of sixty-six researchers it actually fit. That is real judgment, applied at a volume no person will sustain. Everything else was plumbing, and the plumbing was where the surprises lived.

If you want the code, ask me. It is short enough to read in one sitting, which was also a design goal.

---

***David A. Bader** is Distinguished Professor in the Department of Data Science, Director of the Institute for Data Science, and Associate Dean for Research in the Ying Wu College of Computing.*
