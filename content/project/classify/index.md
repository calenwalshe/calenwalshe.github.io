---
title: A new method to calculate classification accuracy
summary:
tags:
- machine_learning 
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
  url: 
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


The classification accuracy between two general Gaussian distributions, and their discriminibality $d'$, are used ubiquitously to express the performance in binary classification and detection tasks. However, these quantities cannot in general be evaluated analytically from the Gaussian parameters. Standard numerical methods may require integration grids that are inefficiently large and fine, may converge slowly, yet miss relevant regions unless tailored case-by-case. We present a new calculation method, based on a transformation of the feature space, that is reliable and fast, and requires no hand-tailoring, for all cases up to 3 dimensions. \href{https://github.com/abhranildas/classify}{Our open-source MATLAB implementation of this method} provides a suite of tools related to such classification.
