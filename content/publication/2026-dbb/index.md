---
# Documentation: https://hugoblox.com/docs/managing-content/

title: "Scaling Exact Substructure Extraction Beyond the Five-Vertex Graphlet Wall"
authors: [dindoost-mohammad, "Bartosz Bryg", admin]
date: 2026-09-01T10:27:03-04:00
doi: ""

# Schedule page publish date (NOT publication's date).
publishDate: 2026-09-01T10:27:03-04:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "30th Annual IEEE High Performance Extreme Computing Conference"
publication_short: "IEEE HPEC 2026"

abstract: "Exact substructure counts make graph neural networks (GNNs) provably more expressive than the first-order Weisfeiler–Leman (1-WL) limit on message passing, but two practical walls confine them to small graphs: combinatorial graphlet counters stop at a fixed catalog of patterns on at most five vertices, and exact extraction at scale was widely treated as too costly. We treat exact substructure-feature extraction as a parallel-systems problem. Using HiPerMotif, an edge-centric parallel subgraph-isomorphism engine in the open-source Arkouda/Arachne framework, we convert isomorphism mappings into per-vertex orbit features by normalizing with each pattern’s automorphism group. On a single 128-core shared-memory node, the extraction strong-scales with counts bit-identical across thread counts, reaches a multi-million-vertex, 10⁸-edge graph (a single-node capacity result), and passes the five-vertex graphlet wall by extracting patterns no fixed-catalog counter expresses, such as induced long cycles (C6–C8); we chart this coverage boundary against ORCA, ESCAPE, and PGD. Two reproducible constructs ground the expressivity payoff: the ten-class circulant skip-link (CSL) benchmark, whose 1-WL-identical classes cannot be fully separated by any size-≤ 5 graphlet system but can be separated by induced long cycles, and the cospectral Shrikhande/4×4-rook pair, which a single clique count distinguishes though 1-WL and the adjacency/Laplacian spectrum cannot. The two results demonstrate separate capabilities, each shown in its own regime, not their intersection: the size-4 orbit features give a capacity-independent accuracy benefit on structure-driven graph classification, validated against a dimension-matched random control, with strong native features able to mask this benefit, while HiPerMotif gives feasible at-scale extraction of the beyond-wall patterns. The size-4 orbit counts are verified against the ORCA oracle and the long cycles against an independent enumerator."

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
