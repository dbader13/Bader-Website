---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "TU Wien Lecture: High-Performance Parallel Graph Analytics: Scalable Algorithms and Frameworks for Discovering Structure in Massive Networks"
event:
event_url:
location: "Technische Universität Wien, Vienna, Austria"
address:
  street:
  city:
  region:
  postcode:
  country:
summary:
abstract: "Graphs are the natural representation for data in domains from neuroscience and genomics to cybersecurity, finance, and social networks, yet they are among the hardest workloads to parallelize. They are sparse, irregular, and exhibit little of the spatial locality that conventional parallel architectures reward. This talk presents two decades of work attacking that grand challenge, spanning foundational parallel graph kernels and a modern open-source framework for interactive analytics at massive scale.

The talk traces a line of high-performance parallel algorithms for breadth-first search, betweenness centrality, connected components, community detection, and subgraph and motif discovery. For each, it highlights the parallelization strategies that make them perform on graphs with billions of edges, including fine-grained shared-memory parallelism, lightweight synchronization, GPU acceleration, and distributed-memory scaling. It then turns to Arkouda and Arachne, an open-source framework that pairs a Python and Jupyter front-end with a high-performance back-end written in Chapel, giving data scientists supercomputer-scale graph analytics without leaving the interactive environment they already use.

A deeper example comes from scalable motif finding in neuroscience connectome graphs. A connectome is a complete wiring diagram of a nervous system, modeled as a graph in which neurons or brain regions are vertices and synapses or fiber tracts are edges. Recurring connection patterns, or network motifs, are believed to be the functional building blocks of neural circuits, but modern connectomes contain hundreds of thousands of neurons and tens of millions of synapses, making motif enumeration combinatorially explosive and far beyond the reach of serial tools. The talk shows how careful algorithm and architecture co-design within Arachne turns this previously intractable analysis into an interactive one, and how the same techniques transfer to anomaly and pattern detection in cybersecurity and financial networks.

The talk closes by connecting this work to the broader arc of parallel computing, from architecting the first Linux supercomputer and co-founding the Graph500 benchmark to the road toward exascale and emerging accelerator architectures, and to the open problems likely to define the next decade of the field."

# Talk start and end times.
#   End time can optionally be hidden by prefixing the line with `#`.
date: 2026-06-29T14:00:00-04:00
date_end: 2026-06-29T15:30:00-04:00
all_day: false

# Schedule page publish date (NOT event date).
publishDate: 2026-06-17T11:25:34+02:00

authors: []
tags: []

# Is this a featured event? (true/false)
featured: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

# Optional filename of your slides within your event's folder or a URL.
url_slides:

url_code:
url_pdf:
url_video:

# Markdown Slides (optional).
#   Associate this event with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: ""

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

## Brief Biography: ##

David A. Bader is a Distinguished Professor and the founding Director of the Institute for Data Science at the New Jersey Institute of Technology, where he also founded the Department of Data Science. He previously founded the School of Computational Science and Engineering at Georgia Tech. He earned his Ph.D. at the University of Maryland. A Fellow of the IEEE, ACM, AAAS, and SIAM, Bader received the 2021 IEEE Computer Society Sidney Fernbach Award for his work in parallel algorithms and high-performance computing. He architected the first Linux supercomputer, the architecture now underlying essentially all of the world's Top500 systems, and co-founded the Graph500 benchmark. His research spans parallel algorithms, massive-scale graph analytics, and HPC, supported by more than $190M in funding from NSF, NIH, DARPA, and DOE. He served as Editor-in-Chief of ACM Transactions on Parallel Computing and IEEE Transactions on Parallel and Distributed Systems. Bader holds dual U.S. and Austrian citizenship and maintains longstanding family and cultural ties to Vienna.