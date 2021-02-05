---
title: Detection of camouflaged textures
summary: To study the importance of edges in detecting camouflaged objects.
tags:
- natural_systems_analysis
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption: Photo by rawpixel on Unsplash
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
slides: 
---

Occurrences of camouflage in nature evoke fascination and wonder in us. Less appreciated are the forces that shaped their evolution: the visual systems of their predators and prey. Indeed, having been filtered by them, camouflage specimens—no matter how ingenuous—are poised just at the edge of detectability, their inventiveness
only testifying to the sophistication of detection machinery that pruned even slightly less crafty variants.

Using theory, computation and experiment, we turn our inquiry to the visual resources and mechanisms that are harnessed for detecting camouflage in nature. In particular, we consider the scenario where the camouflaging animal has exactly mimicked its background texture. Any visual information usable for detection then lies only at its boundary. We begin therefore by defining the boundary mismatch: a computational measure of visual discontinuity at the boundary that putatively summarizes most of this available information. We then synthesize artificial stimuli using 1/f noise as the camouflage texture (this shares the same spatial frequency properties as natural images, but lacks further structure), and assess human performance on them with a
series of target-detection experiments. 

We find regular variation in the detectability of these stimuli as a function of their boundary mismatch, allowing us to measure boundary-mismatch thresholds against variations in task-relevant stimulus dimensions like luminance, contrast and duration. We shall extend this analysis to variations in the size, distance and shape of the target, and with naturalistic texture stimuli (see Portilla and Simoncelli, 2000). These ideas can also be brought to the question of engineering effective camouflage. The boundary mismatch measure allows us to computationally prescribe the best location on a background to hide against, and compare the effectiveness of different textures towards this goal. These computational results can be connected to actual detectability in such scenarios using the results of our psychophysical experiments.

Das, A., Walshe, R.C. and Geisler, W.S. (2018) Understanding camouflage detection. Presented at Computational and Systems Neuroscience (COSYNE) Annual Meeting.
