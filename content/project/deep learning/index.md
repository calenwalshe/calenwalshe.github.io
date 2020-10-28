---
title: Deep learning to predict human gaze and human actions in games. 
summary: Incorporating human gaze improves imitation learning of human actions in ATARI games.
tags:
- cognitive_science 
date: "2019-09-21"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption:
  focal_point: Smart

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/calenwalshe
url_code: ""
url_pdf: ""
url_slides: ""
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides: example
---

Large-scale public datasets have been shown to benefit research in multiple areas of modern artificial intelligence. For decision-making research that requires human data, high-quality datasets serve as important benchmarks to facilitate the development of new methods by providing a common reproducible standard. Many human decision-making tasks require visual attention to obtain high levels of performance. Therefore, measuring eye movements can provide a rich source of information about the strategies that humans use to solve decision-making tasks. Here, we provide a large-scale, high-quality dataset of human actions with simultaneously recorded eye movements while humans play Atari video games. The dataset consists of 117 hours of gameplay data from a diverse set of 20 games, with 8 million action demonstrations and 328 million gaze samples. We introduce a novel form of gameplay, in which the human plays in a semi-frame-by-frame manner. This leads to near-optimal game decisions and game scores that are comparable or better than known human records. We demonstrate the usefulness of the dataset through two simple applications: predicting human gaze and imitating human demonstrated actions. The quality of the data leads to promising results in both tasks. Moreover, using a learned human gaze model to inform imitation learning leads to an 115% increase in game performance. We interpret these results as highlighting the importance of incorporating human visual attention in models of decision making and demonstrating the value of the current dataset to the research community. We hope that the scale and quality of this dataset can provide more opportunities to researchers in the areas of visual attention, imitation learning, and reinforcement learning. 


Zhang, R., Walshe, R.C., Liu, Z., Guan, L., Muller, K.S., Whritner, J.A., Zhang, L., Hayhoe, M. & Ballard, D. (2019). Atari-HEAD: Atari Human Eye-Tracking and Demonstration Dataset. preprint arXiv. arXiv:1903.06754 (Under review at AAAI’20).
