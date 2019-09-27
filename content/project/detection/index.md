---
title: Detecting objects in natural scenes
summary: We build a statistically near-optimum detector and compare this with human behavior.
tags:
- signal_detection
date: "2016-04-27T00:00:00Z"

# Optional external URL for project (replaces project detail page).
external_link: ""

image:
  caption:
  focal_point: Smart

links:
- icon: twitter
  icon_pack: fab
  name: Follow
  url: https://twitter.com/georgecushen
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

Nearly all biological visual systems have the ability to separate relevant signals from background clutter. The natural-signals hypothesis suggests that biological systems exploit regularities in the statistical structure of natural scenes to solve this problem. Here, we study optimal detection of target signals that occlude part of the natural backgrounds they are presented on. Occluding targets are the most common in natural vision, but most of the existing literature has focused on additive targets because they are easier to work with both mathematically and experimentally. We develop a Bayes optimal detector for occluding targets that is limited by only the approximate sampling density of the primate retina and the natural scene statistics after retinal sampling. The performance of the optimal model is then compared to data measured in a human psychophysical detection task. To represent the scene statistics used by the Bayes detector we first filter natural scene patches with and without the target by a modulation transfer function that approximates the optics of the human eye. Second, we simulate the output of RGCs by blurring and downsampling the optically filtered image to match the expected retinal response at a given eccentricity. Then, we decompose the information relevant for detection of occluding targets. Luminance, pattern and boundary signals are computed separately for each patch. The variances and covariances of the features are then measured for a large set of background conditions and retinal eccentricities. Finally, performance of the optimal detector is measured in a set of background and eccentricity conditions for which we have measured human psychophysical responses. Our results show that human performance is approximately proportional to optimal. We conclude that much of the variation in detecting occluding targets across the visual field arises from the statistical structure of natural scenes and the limitations of retinal sampling.

Walshe, R. C., Sebastian, S., & Geisler, W. (2018). Ideal observer for detection of occluding targets in natural scenes in the fovea and periphery. Journal of Vision, 18(10), 629-629. (Published abstract).