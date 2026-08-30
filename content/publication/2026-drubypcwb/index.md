---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "Well-Connected Community Detection at Extreme Scale: Shared- and Distributed-Memory Parallel Algorithms"
authors: [dindoost-mohammad, alvaradorodriguez-oliver, "Asif Uddin", "Bartosz Bryg", "Haotian Yi", "Minhyuk Park", "George Chacko", "Tandy Warnow", admin]
date: 2026-08-29T19:57:00-04:00
doi: "10.1007/s41109-026-00818-y"

# Schedule page publish date (NOT publication's date).
publishDate: 2026-08-28T19:57:00-04:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["article-journal"]

# Publication name and optional abbreviated publication name.
publication: "Applied Network Science"
publication_short: "Appl. Netw. Sci."

abstract: "Community detection algorithms such as Louvain frequently produce clusters that are internally disconnected or poorly connected, limiting their utility in downstream network analysis. The Well-Connected Clusters (WCC) and Connectivity Modifier (CM) algorithms address this by post-processing any input clustering to enforce a user-defined edge connectivity criterion through recursive minimum cut bisection. While prior work demonstrated shared-memory parallel implementations of WCC and CM in Chapel on graphs with up to two billion edges, scalability remains constrained by single-node memory capacity and by the separate subgraph-construction preprocessing pass used in the original pipeline. This paper presents distributed-memory parallel implementations of WCC and CM in both C++ with MPI and Chapel with multi-locale execution. The central contribution is an architectural redesign that integrates subgraph generation into the Leiden clustering step, eliminating the separate WCC/CM subgraph preprocessing pass. Each compute node receives only its assigned subgraph files and executes a fully independent pipeline without ever loading the full graph. Connected component computation is parallelized within each node and distributed across nodes via round-robin assignment, and memory-mapped I/O accelerates file loading throughout. Experiments on ten real-world networks spanning up to 2.1 billion edges show that the C++ distributed implementation achieves up to 65× speedup over the original baseline on graphs where both complete successfully. The Chapel distributed implementation is integrated into Arachne, an open-source graph analytics framework built on the Arkouda platform, available at https://github.com/Bears-R-Us/arkouda-njit. It achieves broader graph coverage than the C++ distributed implementations, successfully processing billion-edge configurations including Open-Alex and Open-Citations on which all C++ distributed implementations fail, while Wikipedia-Links remains unsuccessful for both implementations. On successful configurations, Chapel distributed delivers speedups up to 19.7× at CPM 0.001 and up to 55.8× at CPM 0.01 over the Chapel shared-memory reference, with one reported slowdown on Livejournal WCC at CPM 0.001. Failures on a subset of large graphs are associated with memory leaks and data races in VieCut."

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
