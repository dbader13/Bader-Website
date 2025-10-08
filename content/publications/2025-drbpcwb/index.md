---
# Documentation: https://hugoblox.com/docs/managing-content/

title: "On the Optimization of Methods for Establishing Well-Connected Communities"
authors: [dindoost-mohammad, alvaradorodriguez-oliver, "Bartosz Bryg", "Minhyuk Park", "George Chacko", "Tandy Warnow", admin]
date: 2025-10-07T07:54:39-04:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2025-10-07T07:54:39-04:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "The 14th International Conference on Complex Networks and Their Applications"
publication_short: "CNA 2025"

abstract: "Community detection plays a central role in uncovering meso scale structures in networks. However, existing methods often suffer from disconnected or weakly connected clusters, undermining interpretability and robustness. Well-Connected Clusters (WCC) and Connectivity Modifier (CM) algorithms are post-processing techniques that improve the accuracy of many clustering methods. However, they are computationally prohibitive on massive graphs. In this work, we present optimized parallel implementations of WCC and CM using the HPE Chapel programming language. First, we design fast and efficient parallel algorithms that leverage Chapel's parallel constructs to achieve substantial performance improvements and scalability on modern multicore architectures. Second, we integrate this software into Arkouda/Arachne, an open-source, high-performance framework for large-scale graph analytics. Our implementations uniquely enable well-connected community detection on massive graphs with more than 2 billion edges, providing a practical solution for connectivity-preserving clustering at web scale. For example, our implementations of WCC and CM enable community detection of the over 2-billion edge Open-Alex dataset in minutes using 128 cores, a result infeasible to compute previously."

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
