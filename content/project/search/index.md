---
title: Optimal search for targets embedded in natural images. 
summary: We developed an approach to optimally search for objects in natural scenes. We tested humans against the optimal benchmark to see how well they can do.
tags:
- cognitive_science
- eye_movements
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
url_slides: search_presentation.pptx
url_video: ""

# Slides (optional).
#   Associate this project with Markdown slides.
#   Simply enter your slide deck's filename without extension.
#   E.g. `slides = "example-slides"` references `content/slides/example-slides.md`.
#   Otherwise, set `slides = ""`.
slides:
---

Searching the environment in a fast and efficient manner is a critical capability for humans and many other animals. Normally, multiple fixations
are used to identify and localize targets. However, in the special case of covert search the target must be identified and localized within a single
fixation. Here we present a theory of covert search that takes into account the statistical variation in background images, the falloff in resolution and
sampling with retinal eccentricity, the increase in intrinsic location uncertainty with retinal eccentricity, and the prior probability of target presence
and target location in the image. The computational steps of the theory are as follows. First, the effective prior probability distribution on target location
is computed from the prior and the intrinsic location uncertainty. Second, the effective amplitude of the target (also dependent on retinal eccentricity) is computed and the target (if present) is added to the background. Third, template responses are computed at each image location by taking the dot product of a template (having the shape of target) with the image and then adding a random sample of internal noise. Fourth, the responses are correctly normalized by the sum of the internal noise variance and the estimated variance due to external factors (the background statistics). Fifth, the normalized responses are summed with the log of the effective prior on target location to obtain values proportional to the posterior probability. If the maximum of these values exceeds a criterion, the response is that the target is present at the location of the maximum. The theory predicts that i) misses occur more often than false alarms, ii) misses occur further in the periphery than false alarms, and iii) these asymmetries decrease with increasing target amplitude. Preliminary results show that the theoretical and human spatial distribution of errors are similar. 

Walshe, R.C. & Geisler, W.S. (2019). Theory of Covert Search in Noise Backgrounds Correctly Predicts Asymmetrical Spatial Distributions of Misses and False Alarms. Annual meeting of the Vision Sciences Society. Poster available [here](https://calenwalshe.com/files/vss_2019_search_poster.pdf)

Technical Report (2019). A theory of visual search for foveated visual systems.  Report available [here](https://calenwalshe.com/files/tech_report_nov_1_2019.pdf)
