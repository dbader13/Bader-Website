---
# Documentation: https://hugoblox.com/docs/managing-content/

title: "Agentic Algorithm Engineering: Improving Shared-Memory Exact Minimum Cuts"
authors: [admin, "Adil Chhabra", "Ernestine Großmann", "Monika Henzinger", "Alexander Noe", "Christian Schulz"]
date: 2026-09-08T09:58:52-04:00
doi: "10.48550/arXiv.2609.07204"

# Schedule page publish date (NOT publication's date).
publishDate: 2026-09-08T09:58:52-04:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["Preprint"]

# Publication name and optional abbreviated publication name.
publication: "arXiv"
publication_short: "arXiv"

abstract: "The minimum cut problem for an undirected edge-weighted graph asks us to divide its set of nodes into two blocks while minimizing the weighted sum of the cut edges. Over the last years, we engineered a range of fast algorithms for this problem. Our fastest exact algorithm uses an inexact algorithm to obtain a better bound for the problem, reductions that depend on this bound, improved data structures and parallel contraction routines. It is available in the open-source package VieCut and, on real-world instances, outperformed the previously fastest solvers by a factor of up to 2.5 sequentially and up to 12.9 when run in parallel. We improve this algorithm using agentic algorithm engineering (AAE), a methodology that we introduce here, in which autonomous large language model agents run the algorithm engineering cycle on an existing code base: they form hypotheses about where running time is lost, implement them, benchmark the result on a fixed instance set and keep or discard the change. Even though we had already tuned our algorithm by hand extensively, the agent finds significant optimizations, in particular on the DIMACS core instances: factors of 1.28 (sequential) and 1.63 (32 threads) on real-world k-cores, and 6.26 and 127 on the DIMACS core instances."

# Summary. An optional shortened abstract.
summary: ""

tags: []
categories: []
featured: false

# Custom links (optional).
#   Uncomment and edit lines below to show custom links.
# links:
# - name: Follow
#   url: https://twitter.com
#   icon_pack: fab
#   icon: twitter

url_pdf:
url_code:
url_dataset:
url_poster:
url_project:
url_slides:
url_source:
url_video:

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder. 
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Associated Projects (optional).
#   Associate this publication with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `internal-project` references `content/project/internal-project/index.md`.
#   Otherwise, set `projects: []`.
projects: []

# Slides (optional).
#   Associate this publication with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides: "example"` references `content/slides/example/index.md`.
#   Otherwise, set `slides: ""`.
slides: ""
---
