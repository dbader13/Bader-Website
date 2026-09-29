---
# Documentation: https://hugoblox.com/docs/managing-content/

title: "LOOM: A Team-of-Agents Architecture for High-Performance Graph Analytics Workflows with Arkouda and Arachne"
authors: [saxena-asha, admin]
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

abstract: "Teams of large language model (LLM) agents now plan, code, and verify their own work, yet nearly all agentic frameworks assume a dataset fits in the memory of one machine, excluding the billion-edge graphs that motivate high-performance computing and where a single poor analytical step can waste hours of supercomputer time. We present LOOM, a team-of­agents architecture for large-scale graph analytics on Arkouda and its graph extension Arachne. LOOM organizes role-specialized agents around a shared, typed artifact, and contributes five mechanisms that distinguish it from generic agentic pipelines: a Graph Workflow Intermediate Representation (GW-IR) that is statically checked so ill-typed workflows are rejected before any cluster cycles are spent; telemetry-grounded reflection that feeds per-locale load imbalance, communication volume, and time to solution from the Chapel-based server back to the agents; invariant-based verification against graph-theoretic identities that hold without ground truth; a Security and Access Control Agent that enforces resource quotas and audits data access before any cluster cycles are spent; and a Learning/Adaptation Agent that replaces the hand-crafted cost model with a data-driven predictor trained on accumulated provenance telemetry. LOOM is implemented as an open-source framework that runs end to end, available at https://github.com/Bader-Research/LOOM."

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
