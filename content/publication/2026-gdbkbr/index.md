---
# Documentation: https://docs.hugoblox.com/managing-content/

title: "CoBLOC-Continuous Block Level Fairness on Data Streams"
authors: ["Subhodeep Ghosh", du-zhihui, "Angela Bonifati", "Manish Kumar", admin, "Senjuti Basu Roy"]
date: 2026-09-04T11:44:19-04:00
doi: "10.14778/3827998.3828091"

# Schedule page publish date (NOT publication's date).
publishDate: 2026-09-04T11:44:19-04:00

# Publication type.
# Legend: 0 = Uncategorized; 1 = Conference paper; 2 = Journal article;
# 3 = Preprint / Working Paper; 4 = Report; 5 = Book; 6 = Book section;
# 7 = Thesis; 8 = Patent
publication_types: ["paper-conference"]

# Publication name and optional abbreviated publication name.
publication: "Proceedings of the VLDB Endowment"
publication_short: "VLDB 2026"

abstract: "We present `CoBLOC`, the first interactive system for enforcing *continuous group fairness* over sliding windows in data streams. `CoBLOC` introduces *block-level fairness*, a fine-grained fairness model that exposes short-term disparities missed by window-level guarantees, and supports efficient real-time monitoring using compact sketch-based summaries. When violations occur, `CoBLOC` applies theoretically grounded stream reordering algorithms to restore fairness within the current window, while maintaining low-latency, high-throughput performance suitable for real-world streaming analytics. Through interactive demonstrations, `CoBLOC` also surfaces serendipitous moments where fairness adjustments become critical, provides intuitive explanations of its decisions, and recommends landmark sizes that best balance reordering cost and fairness in dynamic streaming settings."

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
