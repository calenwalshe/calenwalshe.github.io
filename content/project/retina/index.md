---
title: A model of the retina
summary: We built a model of the retina and then use it to estimate fundamental limits of human visual capabilities.
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

Many of the projects that I work on involve understanding the earliest stage of visual processing, the retina. There is a critical factor the take into account when building models of visual sensory processing which is the substantial loss in resolution that occurs in the periphery. In other words, when images on the retina fall at positions away from the center of the retina they are transmitted to the brain in a lower quality format.  This has major implications for perception and behavior. For example, doing basic signal detection is going to be negatively impacted when the images are presented in the periphery. Without taking the retinal factors into account predicting how humans detect signals is not likely to be successful. Retinal factors also play a major role in how well  we can search and located objects in scenes. Intuitively, finding objects that are very close to where you are currently looking is relatively easy compared to objects that are located far away. Part of this phenomenon is simply that the image of the object you are looking from the perspective of your brain is blurry and low-quality!

The model of the retina that we developed recently has helped us ask concrete questions about basic signal processing capabilities of humans and machines. You can download a demo [here](https://github.com/calenwalshe/retina_model) and filter any image you like at a specific location on the retina. See what the image looks like to your visual system!
