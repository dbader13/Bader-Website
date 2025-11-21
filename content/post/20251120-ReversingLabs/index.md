---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "OWASP Top 10 tackles supply chain risk"
subtitle: "The Open Worldwide Application Security Project’s widely used AppSec priority list is expanding to cover systemic risk."
summary: ""
authors: []
tags: []
categories: []
date: 2025-11-20T10:27:31-05:00
lastmod: 2025-11-20T10:27:31-05:00
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

*By John P. Mello Jr., Freelance technology writer.*

{{<figure src="supply-chain-risk-1400x732.jpg">}}

A proposed [new version](https://owasp.org/Top10/2025/0x00_2025-Introduction/) of the global standard for application security — a key tool for raising awareness and educating developers about the most critical software risks — has been released by the Open Worldwide Application Security Project. 

One key change: OWASP is adding two key software supply chain security (SSCS) components to the update, with “Supply Chain Failures” coming in at No. 3 and “Mishandling of Exceptional Conditions” at No. 10.

Here’s what you need to know about the new OWASP Top 10 for Application Security — and why it matters.

## OWASP brings intellectual honesty to its list ##

As with every new Top OWASP 10 list, some risks move up, some down, some remain the same, some fall off — and new ones are added. In the latest proposal, “Cryptographic Failures,” “Injection,” and “Insecure Design” drop to Nos. 4, 5, and 6, respectively, while “Security Misconfiguration” climbs to No. 2. “Broken Access Control” remains No. 1, while “Authentication Failures,” “Software and Data Integrity Failures,” and “Logging and Alerting Failures” remain in the Nos. 2, 3, and 4 spots, respectively. 

But experts agree the key takeaway is the addition of SSCS. [Chris Hughes](https://www.linkedin.com/in/resilientcyber/), CEO of Aquia and chief security advisor for Endor Labs, in his [Resilient Cyber newsletter](https://www.resilientcyber.io/p/the-owasp-top-10-gets-modernized), noted that “the OWASP Top 10 has just received its most significant update since 2021.” 

Hughes explained the downgrading of “Insecure Design” as recognition by OWASP that  notable improvements have been made in that area, driven by the increased use of threat modeling and organizations’ new emphasis on the [Secure by Design initiative](https://www.reversinglabs.com/blog/how-legacy-app-sec-holds-back-securebydesign) of the U.S. Cybersecurity and Infrastructure Security Agency — demonstrating, he said, “that perhaps not all efforts are virtue-signaling pledges,” but rather real, proactive investments.

Gisela Hinojosa, a senior security consultant at the penetration-testing company Cobalt Labs, wrote in a company [blog post](https://www.cobalt.io/blog/comparing-the-owasp-top-10-2025-with-real-world-pentest-data) that, as a researcher, “I live and breathe this list.” 

> "It’s the standard we use to train pentesters, build test methodologies, and help organizations prioritize risk. And this year, the list signals a major, important evolution. The 2025 edition shows a clear shift away from individual, code-level bugs and toward broad, systemic risks."
> -- [Gisela Hinojosa](https://www.linkedin.com/in/gisela-hinojosa/)

**David Bader**, director of the Institute for Data Science at the New Jersey Institute of Technology, said that what he appreciates about this version “is that it’s more intellectually honest about how threats actually work.”

> "They’re analyzing 589 different vulnerability types across nearly three million applications now — the scale of data is impressive. And the decision to focus on root causes rather than symptoms? That’s the right approach. It’s more useful to tell developers ‘You have a configuration problem’ than to just say, ‘You’re leaking data.’"
> -- [David Bader](https://www.linkedin.com/in/dbader13)

Bader sees the fact that some categories have stayed stable for years  as evidence that “the community correctly identified the persistent problems.” For example, “Broken Access Control” remains at No. 1. 

> "Meanwhile, the movement we’re seeing with misconfigurations and supply chain failures validates the methodology of combining hard data with community surveys. These were emerging threats that traditional testing couldn't fully capture."
> -- David Bader

He said he also likes that OWASP is willing to expand and consolidate categories based on how threats actually manifest, rather than sticking with legacy classifications. 

> "Rolling ‘Server-side Request Forgery’ into ‘Broken Access Control,’ expanding ‘Vulnerable Components’ into the broader supply chain category — these reflect the reality of how attacks happen."
> -- David Bader

## Boundaries dissolve as supply chain attacks mature ##

Jagadeesh Kunda, chief product officer and co-founder of the identity and access management company Oleria, said the 2025 OWASP Top 10 contains a profound revelation about cybersecurity. 

> "The boundaries we’ve relied on for security are dissolving. The line between internal and external threats has blurred with supply chain attacks. The distinction between human and machine identities is vanishing with AI. The perimeter between ‘trusted’ and ‘untrusted’ no longer exists in zero-trust architectures."
> -- [Jagadeesh Kunda](https://www.linkedin.com/in/jagadeesh-kunda/)

Kunda said that every assumption on which security has been built is being challenged. “What’s striking is how toxic combinations emerge from these blurred boundaries.” A misconfigured service account (internal) gets exploited through a supply chain attack (external) during an exceptional condition (system overload), creating a perfect storm. “These aren't separate risks anymore. They’re interconnected vulnerabilities that compound each other.” 

> "The 2025 OWASP Top 10 isn’t just a vulnerability list. It’s a report card on our industry’s architectural debt."
> -- Jagadeesh Kunda

Kunda said organizations that continue to treat these as isolated security issues will keep playing Whac-a-Mole. “Those that recognize them as symptoms of systemic design failures will build the resilient, AI-ready platforms that define the next decade. Security can’t be a feature anymore. It has to be the foundation.”

## The AppSec mindset is maturing ##

Rosario Mastrogiacomo, chief strategy officer of Sphere Technology Solutions, said the OWASP Top 10 for 2025 reflects a maturing security mindset. 

> "Previous versions focused heavily on well-known issues like SQL injection and cross-site scripting. While those risks still exist, the new list recognizes that many of today’s most serious vulnerabilities aren’t tied to specific lines of code. They’re systemic."
> -- [Rosario Mastrogiacomo](https://www.linkedin.com/in/rmastrog)

The new version places much greater emphasis on ecosystem-level issues such as software supply chain risk, insecure design, and misconfiguration. It also brings attention to how failure handling and operational behavior contribute to security posture. “In short, the list has evolved from cataloging code flaws to addressing architectural and lifecycle risks,” Mastrogiacomo said.

> "This latest version is a clear call for organizations to expand their definition of application security. It’s not enough to scan for known vulnerabilities or sanitize input."
> -- Rosario Mastrogiacomo

Mastrogiacomo said AppSec today depends on understanding how systems behave in failure, how access is granted across services, and how deeply third-party dependencies are trusted. “The list encourages a shift from reactive testing to proactive design,” he said. “It asks development and security teams to think not just about what their code does, but also about how it fits into a much larger, risk-prone ecosystem.

## You’ve come a long way, AppSec teams ##

Shane Barney, CISO at Keeper Security, said the 2025 OWASP Top 10 highlights how far the industry has come in understanding the real nature of risk. 

> "It’s not just about patching bugs anymore. It’s about recognizing that vulnerabilities often stem from the complexity of our systems and the pace at which technology moves. Security teams are no longer chasing flaws. They’re managing the conditions that allow them to form in the first place."
> -- [Shane Barney](https://www.linkedin.com/in/shane-barney-69026528)

But Martin Jartelius, AI product director at the threat exposure management company firm Outpost24, said the new direction of the OWASP Top 10 list concerns him.

> "Web applications are becoming increasingly complex, with more and more types of vulnerabilities to address. This also makes creating a clear Top 10 list harder, and the attempt to fit more issues into the same number of entries can be seen in this new Top 10."
> -- [Martin Jartelius](https://www.linkedin.com/in/martinjartelius)

He said the list is starting to resemble the old Web Application Security Consortium (WASC) model, which had nearly 50 entries. “We are getting close to a similar situation by grouping issues that are only loosely related,” he said.

Still, he called the Top 10 a good initiative, adding that he understands why you would avoid turning the Top 10 into a Top 15. 

> "Having a shared term for the problems we describe and a standard understanding of what the problems mean and how to test for and prevent them gives us common ground. This is important because words matter, and this provides a shared terminology for developers, hackers, and security enthusiasts. The list serves its purpose, maybe not as a clean-cut top 10, but as a relevant way to describe the challenges we encounter and how we address them."
> -- Martin Jartelius

## In-production and AI attacks remain MIA ##

Jeff Williams, CTO and co-founder of Contrast Security and a former chairman of the OWASP board, said the main takeaway from the new list is that nothing has really changed about application and API vulnerabilities. “It’s Groundhog Day — again,” he said.

> "It’s too bad that the team didn’t consider attacks in production. That’s where the action is.  We — and others like Verizon and Mandiant — are seeing rapid increases in attacks on apps and APIs.  Unfortunately, the OWASP team didn’t take any of that data into account."
> -- [Jeff Williams](https://www.linkedin.com/in/planetlevel)

Williams said none of the changes are big enough to be called significant. “The addition of ‘Exceptional Conditions’ brings back a category that we had back in the 2000s called ‘Improper Error Handling.’ It only rarely leads to real security risk. The rest is just renaming and slight adjustments,” he said.

> "I do think it’s significant that nothing has changed. That sends a strong message that we need to stop hoping that current practices will work. We need to try new things."
> -- Jeff Williams

Jonathan Sander, field CTO of agentic AI security firm Astrix Security, noted that the only specific mention of AI in this new Top 10 is when OWASP calls it out as a possible aid in lowering false positives in logging and alerting failures.

Sander said concerns are shifting as we prepare for a world where a huge percentage of the code running in production is written, tested, and vetted by AI. “That amps up supply chain concerns, but it also means we need to define the playbook for best practices even more explicitly than before,” he said.

> "AI can only deal with what it’s told to do and the data we feed it. Do we think there’s more secure or insecure code out there it’s drinking in and using to model after? If we don’t tell it what ‘good’ looks like, it will do bad just because that’s all it sees. This new Top 10 feels like it’s bracing for that right now."
> -- [Jonathan Sander](https://www.linkedin.com/in/sanderiam/)

## Keep learning ##

* **Read** the [2025 Gartner® Market Guide to Software Supply Chain Security](https://www.reversinglabs.com/gartner-market-guide-to-software-supply-chain-security). Plus: See [RL's webinar](https://www.reversinglabs.com/webinar/2025-gartner-market-guide-sscs) for expert insights.

* **Get the report:** [Go Beyond the SBOM](https://www.reversinglabs.com/go-beyond-the-sbom). Plus: See the [CycloneDX xBOM](https://www.reversinglabs.com/webinar/beyond-the-sbom-welcome-cyclonedx-xbom) webinar.

* **Go big-picture** on the software risk landscape with [RL's 2025 Software Supply Chain Security Report](https://www.reversinglabs.com/sscs-report). Plus: See our [webinar for discussion about the findings](https://www.reversinglabs.com/webinar/the-year-in-software-supply-chain-threats).

* **Get up to speed on securing AI/ML** with our report: [AI Is the Supply Chain](https://www.reversinglabs.com/ai-is-the-supply-chain). Plus: See [RL's research on nullifAI](https://www.reversinglabs.com/blog/rl-identifies-malware-ml-model-hosted-on-hugging-face) and watch [how RL discovered the novel threat](https://www.reversinglabs.com/webinar/hugging-face-ml-malware-nullifai).

* **Learn how commercial software risk is under-addressed**: Download the [white paper](https://www.reversinglabs.com/manage-your-commercial-software-risk) — and see the [related webinar for more insights](https://www.reversinglabs.com/webinar/managing-your-commercial-software-risks).




https://www.reversinglabs.com/blog/owasp-top-10-supply-chain-risk
