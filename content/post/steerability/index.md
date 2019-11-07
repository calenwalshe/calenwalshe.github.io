---
# Documentation: https://sourcethemes.com/academic/docs/managing-content/

title: "Steerability of the sum of Gaussians"
subtitle: ""
summary: ""
authors: []
tags: []
categories: []
date: 2019-11-06T20:32:30-06:00
lastmod: 2019-11-06T20:32:30-06:00
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Focal points: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight.
image:
  caption: ""
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---

For one of the projects I'm working on we use a Steerable filters to compute local image gradients at different parts of an image. Steerable filters are good because they are i) compact and simple ways to get the filter output from a family of filters from a small set of filters, ii) biologically plausible. Sparing the details it became important to figure out whether the derivative of the sum of two Gaussian functions with the same mean but different variance, is Steerable. It turns out they are, which is intuitive. [Here](https://calenwalshe.com/files/steerability.pdf)Here is a short description of the method used to prove this.  
