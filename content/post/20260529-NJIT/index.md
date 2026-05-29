---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Q&A with David Bader, Recipient of Scientific Computing Honor"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2026-05-29T12:46:00-05:00
lastmod: 2026-05-29T12:46:00-05:00
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

*Written by: Evan Koblentz*

{{<figure src="databank-ribboncutting-8545.jpg" caption="A rack in the NJIT data center">}}

NJIT’s **David Bader**, distinguished professor and director of the Institute for Data Science, was recently named one of the industry’s [most influential researchers](https://www.scientific-computing.com/article/david-bader) by *Scientific Computing World*.

Scientific computing, also known as high-performance computing, refers to the hardware, software and networks that solve extreme math for the challenges of aerospace, defense, energy and healthcare, among other complex fields. It also tackles problems that undergird consumer-friendly artificial intelligence, and these are some of the same problems where Bader focuses his efforts.

Bader specializes in developing software that makes it easier and faster to find patterns in data, which is imperative to high-performance computing. He also works on ways to democratize access to that power and [answered big questions about AI in spring 2024](https://news.njit.edu/njits-david-bader-future-ai-silver-linings-touch-grey). Now, with the industry offering new features that did not exist two years ago, he’s providing another round of insights.

Large language models exploded in popularity four years ago due to their uncanny ability in responding to open-ended questions. But in the last two years they’ve gained the ability to reason rather than just predict, take actions rather than just write, and accept input through many means beyond typing — all of which require more advanced computing infrastructure.

**Q. These new abilities are spiking the demand for data centers that enable real-time computing, vs. traditional data centers that only spool up existing data. What does that mean for your research into faster, more accessible infrastructure?**

A. It changes the whole shape of the problem. The traditional data center was built around predictable, batch-style work. You knew roughly what was coming, you scheduled it, and you optimized for throughput. Real-time AI is the opposite. A user asks a question and expects an answer in the time it takes to blink, and the system has to marshal enormous computing power to deliver it, then release that power the instant the request is done. That kind of bursty, latency-sensitive workload is exactly where my research lives. I work on the irregular computations, the graph and data-intensive problems where the work does not divide neatly and the memory access patterns are unpredictable. Those are the hardest problems to make fast, and they are increasingly the ones sitting underneath modern AI.

**Q. Agentic AI is the ability for software to take actions on your behalf, not merely suggest what actions you should take. It’s one thing to use agents in a controlled development environment, but quite another to give agents deep and secure links into your personal life. How do you recommend that knowledge workers who aren’t coders safely go about dipping their toes into agentic waters?**

A. Start small, start reversible and keep yourself in the loop. The single best habit is to give an agent the narrowest permission it needs for the task in front of you, and nothing more. If you want it to draft replies, let it draft, but make sending a step you approve. If you want it to organize files, point it at one folder, not your entire drive. You are essentially hiring a very fast, very literal new assistant, and you would not hand a new assistant the keys to everything on day one. Second, favor tasks where mistakes are cheap and visible. Summarizing a document, comparing options, preparing a first draft. These let you build trust and learn how the agent thinks before you ever let it touch something irreversible like a payment, a calendar full of other people, or a published post. Third, watch the connections, not just the agent. The risk is rarely the model alone. It is the deep, standing link between the model and your email, your bank, your accounts. Grant those links deliberately, review what you have granted every so often, and revoke anything you are not actively using. You do not need to understand the code to be safe. You need to be the one deciding what the agent is allowed to reach.

**Q. Data centers seem to perpetually require more electricity and more water, while producing more sound and who knows what else — leading to nobody wanting a data center in their town. How can infrastructure research help make data center operators better citizens?**

A. The most powerful lever is doing more with less, and that is fundamentally an algorithms and infrastructure question. Every watt and every drop of water is spent computing something. If my research lets the same result be reached with a fraction of the operations, that is energy and cooling that simply never get consumed. People tend to think the answer is always more hardware. Often the better answer is smarter software running on the hardware we already have. Beyond efficiency, infrastructure research can make these facilities better neighbors in concrete ways. Smarter scheduling lets a center shift heavy work to hours when the grid is cleaner and demand is lower. Better thermal design turns waste heat into something useful, like warming nearby buildings, instead of dumping it. And better placement and monitoring can cut the water draw and the noise that understandably make communities wary. The honest path forward is to treat energy, water, and sound as first-class design constraints, not afterthoughts. The research community can give operators the tools to meet those constraints without giving up the capability everyone wants.

**Q. You wrote [a fascinating blog post](https://fastcode.substack.com/p/harnessing-the-power-of-llms-for) about how AI goes beyond finding software performance issues, to actually suggesting improvements, to hopefully someday soon even considering deeper, more nuanced developer concerns. How does your infrastructure research help get us there?**

A. Finding a bottleneck is the easy part. Plenty of tools can tell you a piece of code is slow. The harder and more valuable thing is understanding why it is slow on a particular machine, proposing a fix that actually respects the hardware, and eventually weighing the tradeoffs a thoughtful engineer would weigh. Is this change going to use too much memory, will it hurt readability, will it break on a different system. That is the nuance. My infrastructure research feeds directly into that, because to suggest a genuinely good improvement, an AI has to understand the machine the way an expert does. It has to know how memory hierarchies behave, how parallel work gets divided and synchronized, how irregular data access defeats naive optimizations. The performance knowledge I have spent a career building is exactly the knowledge these systems need to learn from. The goal is not an AI that hands you a faster snippet. It is an AI that reasons about performance the way a seasoned systems person does, and that frees human developers to focus on the problems that still need human judgment.

**Q. What’s next — what kind of high-performance computing research will people like you be able to do in a few years from now, that’s not possible today?**

A. I think we are heading toward a world where the scale of what one person can compute changes by orders of magnitude. Today, tackling a truly massive data or simulation problem still takes a team, specialized hardware and a long runway. In a few years I expect a single researcher to pose enormous questions and have the system itself figure out how to map them onto whatever computing resources are available, efficiently and almost conversationally. The deeper shift is that the infrastructure starts to disappear from view. The hardest part of high-performance computing has always been the gap between the problem in your head and the machine that runs it. As AI gets better at bridging that gap, the work I do on irregular and data-intensive computing becomes the engine underneath, letting people ask questions of data at a scale we cannot reach today, and getting answers fast enough to actually steer their thinking. That is the part I find most exciting. Not just faster machines, but a fundamentally wider door to who gets to use them.

https://news.njit.edu/david-bader-receives-scientific-computing-honor
