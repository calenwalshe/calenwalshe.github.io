---
title: Accurate error rates for binary quadratic classifiers. 
summary:
tags:
- machine_learning 
date: "2019-09-24"

# Optional external URL for project (replaces project detail page).
external_link: ""

math: true

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

---

The classification accuracy between two general Gaussian distributions, and their discriminibality $d'$, are used ubiquitously to express the performance in binary classification and detection tasks. However, these quantities cannot in general be evaluated analytically from the Gaussian parameters. Standard numerical methods may require integration grids that are inefficiently large and fine, may converge slowly, yet miss relevant regions unless tailored case-by-case. We present a new calculation method, based on a transformation of the feature space, that is reliable and fast, and requires no hand-tailoring, for all cases up to 3 dimensions. [Our open-source MATLAB implementation of this method](https://github.com/abhranildas/classify) provides a suite of tools related to such classification.
