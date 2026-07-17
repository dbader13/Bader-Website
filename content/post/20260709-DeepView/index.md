---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Why Google AI Overviews expose AI's biggest problem"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2026-07-09T10:22:25-04:00
lastmod: 2026-07-09T10:22:25-04:00
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

{{<figure src="1763013acd09913d3778dbfc750c47249a5c30bb-1992x1120.jpg">}}

*By [Sabrina Ortiz](https://www.thedeepview.com/author/sabrina-ortiz)*

Google's AI Overviews now shape how millions of users find information, making the act of search practically synonymous with turning to AI.

The AI integration that Google has thrust upon users promises quicker, more conversational results, but what happens when you can’t trust the results being given?

Usually, I use Google in the same way that billions of people do every day: type a question into the search engine and trust whatever the AI tells me, my boyfriend's pleas to "actually Google it" notwithstanding. So, when [*The New York Times*](https://www.nytimes.com/2026/04/07/technology/google-ai-overviews-accuracy.html) published a report calling into question the accuracy of AI Overviews in April, I clicked immediately, curious as a reporter covering AI and invested as someone who often uses it without a second thought.

## The report and its findings ##

The New York Times commissioned an analysis by an AI start-up called Oumi, which found that AI Overviews were accurate approximately 90% of the time. While 10% inaccuracy may sound small, the sheer volume of Google searches makes it a massive concern.

As the report highlights, Google processes over five trillion searches annually. The Times claims that this translates to tens of millions of erroneous answers every hour or hundreds of thousands of inaccuracies every minute. Those figures are difficult to pin down precisely because not every search query triggers an AI Overview. Still, Google CEO Sundar Pichai disclosed last July that AI Overviews had surpassed two billion monthly users.

"The number that should concern everyone is not the accuracy rate, it is the scale," **David Bader**, distinguished professor and director of the Institute for Data Science at the New Jersey Institute of Technology, told The Deep View. "That is not a minor imperfection; that is misinformation operating at industrial scale, delivered with the visual authority of the world's most trusted search engine."

### Methodology ###

Oumi ran the first round of the study in October, when the most complex questions were answered by Gemini 2, and then in February, when it was upgraded to Gemini 3, which remained Google’s most capable mode until Google I/O in May, when Gemini 3.5 was launched. In both cases, the analysis focuses on 4,326 Google searches: Gemini 2 was accurate 85 percent of the time, and Gemini 3 was accurate 91 percent of the time. This was based on OpenAI's factuality benchmark, SimpleQA.

Google has since refuted the analysis’s results, claiming that the SimpleQA dataset included incorrect target answers and that it used one AI model, HallOumi, to assess the accuracy of another AI model, which could introduce errors.

"This study has serious holes. It uses one AI to grade another on an old benchmark that is known for being full of errors, and it doesn’t reflect what people are actually searching on Google," a Google spokesperson told The Deep View. "AI Overviews are built on our Gemini models, which lead the industry in accuracy, and they clear the same high-quality bar that we have for all our Search features."

Google also added that, because the dataset was artificially created, it does not accurately represent real-world human queries.

OpenAI created SimpleQA’s query dataset using AI trainers that browse the web to generate questions and corresponding answers. The questions had to meet the criterion of having a single "undisputable answer"; the answer couldn’t change over time; and they had to induce hallucinations from either GPT-4o or GPT-3.5. Beyond this, there were two more rounds of quality verification.

Google’s point that the benchmark queries are not entirely representative of an everyday user’s experience is "somewhat valid," according to Maarten Sap, assistant professor of natural language processing at Carnegie Mellon University. However, he said that third-party evaluations are crucial to avoid conflicts of interest and get truthful results.

"The methodology of probing these systems via the regular UI is good, and unfortunately, the only option we have since these products don't typically have a more controlled API endpoint that researchers can ping," Sap told The Deep View.

### The need for easier access to models ###

Both Google’s concerns and Sap’s insights highlight a major industry issue: the inability to get proper access to the models to accurately conduct the kinds of third-party evaluations necessary to hold companies accountable.

For instance, a [2024 report](https://www.adalovelaceinstitute.org/report/under-the-radar/) from the AI ethics nonprofit the Ada Lovelace Institute found that AI model evaluations are currently voluntary and subject to company discretion, leading to inconsistent quality and limited access for evaluators.

In 2023, the University of Oxford released a [paper](https://oms-www.files.svdcdn.com/production/downloads/academic/Investigating_Researchers%E2%80%99_Model_Access_Oct23-compressed_3.pdf) that examines the gated release of frontier artificial intelligence models, which prevents the conduct of important safety research.

"I would also argue that companies deploying AI at this scale have an obligation to fund independent auditing," said Bader. "Google disputed the Oumi study, but the company has not published its own comprehensive, independently verified accuracy data. If the product is as reliable as Google claims, they should welcome external scrutiny, not dismiss it."

## The underlying problem: hallucinations ##

The root cause of the AIO accuracy issue is hallucinations, which, while triggered by a number of factors, are inherent to how AI models work. These models are not actually thinking but rather regurgitating facts by predicting the next word in the sequence.

"These systems do not look up facts in a database. They predict the most statistically probable next word in a sequence based on patterns learned from training data. They are, at their core, sophisticated pattern-matching engines," said Bader.

This explains why models often show confidence or give outputs for their answers, even when they are not correct, he said: "They have no internal mechanism for distinguishing between what they 'know' and what they are guessing."

Olivier Toubia, Columbia University business school professor, told The Deep View that hallucinations can also be traced back to the training data itself, especially if models aren’t trained on an entirely accurate and labeled set of information. These models aren’t trained to sort out correct from incorrect. Instead, he said, they take in typically unlabeled training data and process answers based on it.

"Given all that, it’s very challenging for an AI model to capture uncertainty in the same way as humans think of it, and to model correctness," he added.

Toubia said that AI can "model uncertainty at the token level," referring to the model's probability distribution over every possible next word at each step. For example, if a user asks what the capital of France is, "Paris" would receive a higher probability than "Berlin."

However, that confidence score reflects statistical patterns in training data, not factual understanding. The model isn't verifying that Paris is correct; it's recognizing that "Paris" most commonly follows that prompt. That's why token-level confidence doesn't equate to certainty about factual correctness.

To exacerbate the problem even further, these models often express certainty despite not being explicitly trained to do so, a phenomenon [Apple Research](https://machinelearning.apple.com/research/trained-on-tokens) identified as resulting from popular training methods: Instruction tuning and RLHF (Reinforcement Learning from Human Feedback).

Instruction tuning trains the model to follow directions and give clear, direct answers. RLHF uses human ratings to reward responses that seem helpful, confident, and well-written. In both methods, the model is rewarded for sounding certain, which, of course, is harmful because it will continue to replicate this behavior.

"Hallucinations persist partly because of how these models are trained. During training, AI models are often rewarded for correct answers and for confident answers, which can incentivize them to guess even when they aren't certain," said Lewis.

He adds that it's not much different from how a human, under high pressure, answers a difficult question. We often perceive that it would be better to say something confidently that's not true than to admit uncertainty. And this is reinforced at a cultural level by messages like the "fake it till you make it" strategy.

## People’s predisposition to believing the models ##

The problem, however, is that these models *assert* that they are completely correct, giving people false confidence that the answers are true simply because they sound authoritative, as Sap’s [research](https://aclanthology.org/2024.acl-long.198/) found.

In one of the experiments, participants were shown trivia questions paired with just the beginning of a response, without ever seeing the actual answer. These response starters included epistemic markers, words or phrases that signal a speaker's confidence in what they are saying.

The responses came in three forms: a plain statement with no epistemic marker, one with a "strengthener" (language expressing certainty), and one with a "weakener" (language expressing uncertainty). Nearly 90% of users trusted the language when a strengthener was used. Conversely, approximately 90% chose to look up the answer themselves when a weakener was used.

Another [research paper](https://aclanthology.org/2025.naacl-long.556/) Sap worked on found that politeness can also increase trust and reliance. "Beyond whether the model is correct or not, how users interpret AI outputs and how they're packaged is also crucial," said Sap.

### The footnotes ###

Assertions of confidence and correctness aren’t the only factor that helps Google garner trust.

Another contributing factor to giving the false impression of accuracy is linking to footnotes, which makes outputs feel more believable, especially since it pulls information from Google’s AI search engine. Given that Google has spent its entire existence establishing authority, people may overlook the tiny disclosure on each output stating that it may hallucinate.

"When you position your AI system as the first and most prominent answer a user sees, you are implicitly telling people to trust it," said Bader. "A small disclaimer that says ‘AI responses may include mistakes’ does not absolve you when your system is producing tens of millions of wrong answers every hour."

Sap adds that it is a "huge liability" for Google to show these error-prone AI overviews above actual links to web pages, given the margin of error. Rather, he suggests that a different tab would be "slightly" better. In particular, he worries about the negative consequences related to sensitive matters such as health.

"I particularly worry about people entering health-related queries and the AI overview giving them incorrect information and that endangering them, but this is hard to study unless you know what queries people put into Google," said Sap.

## What can be done? ##

AI will only continue to be more deeply integrated into Google Search products over time, as seen most recently at Google I/O, the company’s annual developer conference, where it unveiled "[the biggest upgrade to our Search box in 25 years](https://www.thedeepview.com/articles/google-remakes-search-with-ai-once-again)." This includes AI-powered suggestions that go beyond autocomplete, a more seamless handoff between Search and AI Mode, and agents galore.

Nevertheless, hallucinations aren't going anywhere.

"The bottom line is this: hallucination is not a software bug that will be fixed in the next release. It is a fundamental property of large language models' text generation," said Bader. "The industry can and should continue driving error rates down, but users, policymakers, and organizations need to understand that some level of AI-generated misinformation is here to stay."

As a result, the best thing users can do is be aware of the issue and, as much as possible, double-check the response by visiting the provided links or doing their own research, especially when verifying critical topics such as health information. "To be fair, companies are already disclosing that their models might hallucinate, and they are already suggesting to users that they should check," said Toubia. "In a way, the problem also comes from the users."

Toubia explains that many people fall into the fallacy of convincing themselves that, although AI Overviews are only correct 90% of the time, every query they send will fall into that 90% and can be trusted.

"There seems to be a dose of wishful thinking in how people use LLMs, which leads them to outsource important human tasks to AI entirely, without spending the effort to check the output, even if they know it might be incorrect."





https://www.thedeepview.com/articles/why-google-ai-overviews-expose-ai-s-biggest-problem
