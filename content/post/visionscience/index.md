---
title: '"Bringing machine learning to vision science before it was hot"'
subtitle: 
summary: 
authors:
- admin
math: true
tags:
- Academic
categories:
date: "2019-04-02"
lastmod:
featured: false
draft: false

# Featured image
# To use, add an image named `featured.jpg/png` to your page's folder.
# Placement options: 1 = Full column width, 2 = Out-set, 3 = Screen-width
# Focal point options: Smart, Center, TopLeft, Top, TopRight, Left, Right, BottomLeft, Bottom, BottomRight
image:
  placement: 2
  caption:
  focal_point: ""
  preview_only: false

# Projects (optional).
#   Associate this post with one or more of your projects.
#   Simply enter your project's folder or file name without extension.
#   E.g. `projects = ["internal-project"]` references `content/project/deep-learning/index.md`.
#   Otherwise, set `projects = []`.
projects: []
---
I probably should have seen this prior to now but there is a lot to read and even good stuff slips through the cracks. It was suggested to a colleague and he presented the work during a journal club. I was impressed by the work.

Visual salience has been a hot term in vision science since the 90s. The salience model identifies local regions in an image that have higher priority than other local regions. Sometimes it is used to mean areas of an image that will many fixations and sometimes it is used for properties of the image that attract attention without necessarily leading to an eye-movement.


The schematic shows the basic idea behind the salience model. These ideas were inspired by the understanding the authors had at the time of how visual information propagates through the primate visual system. These ideas are still influential today and even if researchers don't work on the salience model itself there are a lot of interest in the components of the salience model as individual research topics. The idea that the neural code expresses maps of one kind or another is probably the best hope we have of decoding the computations in the brain at a sufficiently rich level.

![Schematic-of-Itti-and-Koch-Saliency-Model-Itti-Koch-Neibur-1998.png](/img/posts/Schematic-of-Itti-and-Koch-Saliency-Model-Itti-Koch-Neibur-1998.png)

The schematic also shows that there are a lot of moving parts in the salience model. It is a complicated model and this has lead to many arguements. In my opinion, many of the debates over the salience model have been needlessly fussy.

This brings me to what I like about Kienzle et al. First of all, they attempt to do what the salience model does: predict eye-movements. While the salience model makes assumptions about image features the authors of this paper make minimal assumptions by taking a data-driven approach.

They collect many eye-movements in a generic task. By comparing regions that are fixated with regions not fixated they are able to learn a receptive field (filter) that characterizes image salience about as well as the salience model. 

The summary figure for the machine learnt salient shows how their setup works. They learn the kernels from the eye-movement data. Their model learned four kernels. Local image regions are filtered by the kernels, then passed through a point non-linearity and summed up. The resulting value is the salience. There are some additional analyses showing performs comparably to the salience model on several metrics.

![jov-9-5-7-fig004.jpeg](/img/posts//jov-9-5-7-fig004.jpeg)

This paper is not new, and since this there have been more applications of machine learning to salience. Their approach is simple and successful. As a technical advance there is clear progress. Like many approaches to studying biological vision with machine learning there is a tradeoff between opacity and predictability. Some models are hard to understand but predict well, while others perform conversely. The Kienzle et al. method is not as black box as some others but the connection to the underlying biology is less clear than in the salience model.
