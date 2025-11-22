---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Hammerspace Breaks IO500 Barriers: First Standards-Based Linux + NFS System To Achieve True HPC-Class Performance"
subtitle: "Fastest 10-node production result in IO500 history achieved using standard Linux, NFSv4.2 and off-the-shelf NVMe"
summary: ""
authors: []
tags: []
categories: []
date: 2025-11-20T14:27:54-05:00
lastmod: 2025-11-20T14:27:54-05:00
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

ST. LOUIS--([BUSINESS WIRE](https://www.businesswire.com/))--Supercomputing 2025 — [Hammerspace](https://hammerspace.com/), the high-performance data platform for AI Anywhere, today announced a breakthrough IO500 10-Node Production result that establishes a new era for high-performance data infrastructure. For the first time, a fully standards-based architecture — standard Linux, the upstream NFSv4.2 client, and commodity NVMe flash — has delivered a [10-node Production fully reproducible IO500](https://io500.org/list/isc25/ten-production) result traditionally achievable only by proprietary parallel filesystems.

This result is the first IO500 Production benchmark demonstrating indisputable proof that standards-based Linux and NFS can meet the extreme performance requirements of high-performance computing (HPC) and artificial intelligence (AI) workloads — without proprietary client software, specialized networking stacks or complex parallel filesystem infrastructure.

## A Milestone Moment for Data Platforms — As Transformative as Linux Was for Compute ##

In the late 1990s, researchers like **Dr. David Bader**, Distinguished Professor and founder of the Department of Data Science in the Ying Wu College of Computing and Director of the Institute for Data Science at New Jersey Institute of Technology, transformed the HPC world by proving that Linux-based clusters, built on Linux and on commodity components, could rival proprietary supercomputers. That work transformed HPC architecture then, and machine learning (ML) and AI architectures of the future, ultimately making Linux the standard powering nearly every powerful compute environment on Earth.

This vision laid the foundations for the AI architectures that are emerging even today. [Hyperion Research](https://hyperionresearch.com/) estimates that “over $300 billion in revenue has been generated from selling supercomputers. This represents a sizable economic gain, especially since the use of these systems generated research valued at least ten times over the purchase price. While it is difficult to fully measure the value that supercomputers have generated, even looking at just automotive, aircraft, and pharmaceuticals, supercomputers have contributed to products valued at more than $100 trillion over the last 25 years.”

Hammerspace’s IO500 achievement represents the next chapter of that evolution, this time in the data layer.

Just as Linux revolutionized compute architecture, the combination of standards-based Linux and pNFS is now proving it can revolutionize high-performance data architecture for HPC and AI.

## The First Architecture That Meets the Demands of Both HPC and AI ##

This achievement marks the industry’s proof that open, interoperable infrastructure can deliver the performance required by AI and HPC workloads without proprietary lock-in.

HPC environments have traditionally relied on deep institutional expertise to operate complex proprietary filesystems, but the rapid rise of AI has changed the landscape. AI is scaling far faster — across enterprises, cloud providers, sovereign AI platforms, service providers and thousands of new data-intensive applications — and it is impossible to meet this demand with architectures that require niche expertise to deploy and maintain. Every systems administrator already knows how to operate Linux and NFS; however, very few have the specialized knowledge required for legacy parallel file systems. As AI infrastructure becomes mainstream, organizations need HPC-class performance delivered through tools and protocols familiar to the broader IT community. This IO500 result proves that the performance required for both HPC and AI can now be achieved using standard Linux, standard NFS and widely understood operational models, finally aligning extreme performance with the scale and accessibility the AI industry demands.

## Standards-Based Architecture, Industry-Leading Performance ##

The submission by Samsung, leveraging the Hammerspace Data Platform, achieved the fastest standards-based IO500 10-Node Production result ever recorded. Hammerspace not only contributes a substantial number of the capabilities into Linux for pNFS workloads, but its Data Platform is engineered and designed from the ground up to capitalize on these upstream performance enhancements in the Linux kernel.

Unlike traditional storage platforms and legacy parallel file systems that treat Linux as a compatibility layer or pNFS as an added-on interface, Hammerspace’s architecture is built directly on top of — and actively contributes to — the same NFSv4.2 and pNFS innovations driving modern HPC and AI performance. This deep alignment uniquely allows Hammerspace to take immediate advantage of new capabilities such as lower-latency I/O paths, advanced client-side parallelism and improved failover logic, translating Linux’s ongoing advancements directly into real-world application speedups. As a result, organizations can benefit from cutting-edge performance improvements in standard Linux distributions without deploying proprietary clients or rearchitecting their infrastructure.

Unlike legacy parallel file systems that rely on complex, vendor-specific clients, the Samsung’s Hammerspace submission used:

* Standard RHEL/Ubuntu Linux
* Standard upstream NFSv4.2 (pNFS) client
* Standard NVMe SSDs from Samsung
* Standard IP-over-InfiniBand
* Standard server platforms
* Hammerspace’s standards-based parallel global file system leveraging the pNFS client

In the submission, there was no proprietary client, no custom kernel modules and no exotic parallel file system used.

Modern HPC and AI workloads can now run at elite speeds using standards-based infrastructure and data architectures.

## Upstream Linux Innovation Unlocks New Performance ##

The step-function improvement achieved during the time between the ISC25 and SC25 events is the result of:

* Enhanced pNFS Flexible File layout parallelism
* Upstream NFS client improvements contributed by Hammerspace
* Upstream NFS server improvements that avoid page cache contention, allowing improved sustained performance and reduced resource utilization, contributed by Hammerspace
* File-level objective-based policy optimizations
* Latency reductions and throughput gains in metadata access
* High-performance NVMe data placement managed through the Hammerspace global file system

These enhancements strengthen the entire Linux ecosystem — echoing the transformative Linux HPC contributions of the late 1990s and early 2000s.

“This IO500 result rewrites long-standing assumptions about what standards-based Linux and NFS are capable of,” said Trond Myklebust, Hammerspace CTO and Linux NFS client kernel maintainer. “Achieving a leading 10-Node Production score with the Hammerspace parallel global file system using upstream Linux, pNFS and NVMe hardware demonstrates that HPC-class performance no longer requires proprietary clients or specialized file systems. This achievement is a significant moment for the Linux performance community.”

“The next era of AI and HPC will be defined by platforms that combine extreme performance with open, standards-based interoperability,” said David Flynn, Hammerspace founder and CEO. “Just as Linux transformed supercomputing a generation ago, standards-based data infrastructure will transform high-performance data processing today. This IO500 milestone proves that the future belongs to architectures that deliver both openness and performance at scale.”

Hammerspace’s Top-10 IO500 performance is more than a benchmark victory. It is the first empirical proof that standards-based Linux and NFS can power high-performance data systems at the top of the HPC and AI stack.

Linux democratized supercomputing and now standards-based data infrastructure is positioned to democratize high-performance storage — and reshape the future of global-scale computing.

## Learn More ##

* Read the blog post, “[Samsung and Hammerspace Go To The Next Level in the IO500 Benchmark](https://hammerspace.com/samsung-and-hammerspace-go-to-the-next-level-in-the-io500-benchmark/)”
* Listen to the Data Unchained podcast, "[First Standards-Based Linux + NFS System to Achieve True HPC-Class Performance: Jonathan Flynn](https://hammerspace.com/first-standards-based-linux-nfs-system-to-achieve-true-hpc-class-performance/)"
* Read the press release, “[Hammerspace Announces Latest Version of its Data Platform Software, with Significant Performance, Security & Ecosystem Enhancements](https://hammerspace.com/hammerspace-announces-latest-version-of-its-data-platform/)”
* Visit the Parallel NFS [Resource Center](https://hammerspace.com/parallel-nfs/)

## About Hammerspace ##

Hammerspace is the high-performance data platform built to simplify AI infrastructure at scale. It makes all your data immediately accessible—anywhere across on-premises and cloud environments—without copying or migrating data. By integrating with existing storage, networking, and applications, Hammerspace creates a unified, high-speed data backbone for AI, enabling organizations to accelerate every stage of the AI pipeline while eliminating data silos. Learn more at https://hammerspace.com.

Hammerspace and the Hammerspace logo are trademarks of Hammerspace, Inc. All other trademarks used herein are the property of their respective owners.
©2025 Hammerspace, Inc. All rights reserved.


## Contacts ##

**Press Contact**:  
IGNITE Consulting, on behalf of Hammerspace  
Kim Pegnato, +1 781-835-7118  
Hammerspace@igniteconsultinginc.com


https://www.businesswire.com/news/home/20251120823774/en/Hammerspace-Breaks-IO500-Barriers-First-Standards-Based-Linux-NFS-System-To-Achieve-True-HPC-Class-Performance
