---
title: Predicting gaze with reinforcement learning
summary: 
tags:
- machine_learning 
- eye_movements
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
slides: ""
---

We developed an approach to predicting eye movements during category learning tasks. One of the central roles of eye movements is to sample information from the environment in a way that supports ongoing tasks and such that the information is sampled at the appropriate time.

During classification tasks information from different spatial locations must often be used to determine the specific features of an object that are relevant for placing it in the appropriate category. When categories and objects are well known to the object they will typically know where to look on the object to classify it appropriately. However, when encountering a new object, or a new *type* of object, it isn't clear which features are relevant. In this case, the observer must learn the features that should be used to classify the object correctly. 

In this work, we show that a reinforcement learning approach to learning which locations to look at in order to perform well in the classification task does a good job of predicting actual human learning in classification experiments. This work supports the idea that reinforcement learning provides a good model for how humans select actions.

Barnes, J. I., McColeman, C., Stepanova, E., Blair, M. R., & Walshe, R. C. (2014). RLAttn: An actor-critic model of eye movements during category learning. In Proceedings of the Annual Meeting of the Cognitive Science Society (Vol. 36, No. 36).
