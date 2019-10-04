---
title: Where in the world is red?
subtitle: 
summary: 
authors:
- admin
tags:
- Academic
categories:
date: "2016-03-24"
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

I had a coffee on campus with a friend in the Engineering department. To him, it was completely obvious that the way that perception _should_ work is that your perceptions should recover exactly what is contained in the distribution of light that strikes the eye. It was an interesting discussion and the following sums up some of our discussion.

The story of colour vision begins in a part of the eye known as the retina. Within the retina there are hundreds of millions of photosensitive cells called photoreceptors. The primary role of these cells is to convert light (electromagnetic radiation) into electrochemical signals that are passed to regions of the brain that are responsible for vision. In primates, the most important early visual area is called Striate cortex and is located at the back of the brain.

The type of photoreceptor that takes care of signaling colour is called a cone and primates have three different types of them. Each of the cone classes is distinguished by the wavelength of electromagnetic radiation that they are most sensitive to. L-cones have the strongest response to long wavelength, M-cones respond to medium wavelengths and S-cones respond to short wavelengths. 

![Cone Sensitivity](/img/posts/cone_sensitivity.gif)

When light strikes the retina the responses of these three different cone classes are combined. The relative responses of these three different types of cones forms that basis of the brains ability to estimate the distribution of the incoming light and perceive it as a particular colour.

In other words, the cones response function only allows them to respond to light with specific wavelengths. Electromagnetic radiation that falls too far outside the range of wavelengths that a cone can respond to will not influence a cones response and therefore will not influence colour perception.

There is also a slightly deeper issue to consider here. The goal of colour vision isn't actually about estimating the spectral power distribution (distribution of wavelengths) of a light source. More correctly, it's about using spectral information to track regularities that exist out there in the world.

Two perceptual phenomena help to make this clear, _colour constancy_ and _colour metamers_.

Colour constancy is the label that is used to describe an aspect of perception in which an object is perceived to have a relatively uniform colour despite large variations in the wavelengths being emitted from the object. The following illusion is a stark demonstration of this principle. In the illusion, the patches labelled A and B are actually the exact same colour even though the perception of the patches is very different. This is colour constancy at work. The brain is doing some work to estimate the colour that would be expected based on the surrounding context and is discounting the colour that is actually being emitted from the patch.

![Grid Illusion](/img/posts/grid_illusion.png)

Colour metamers also show that the colour of light and the emitted wavelength are not one and the same. A colour metamer occurs when the perceived colour is identical but the spectral power distribution is completely different. The existence of metamers comes about because the retina is compressing a continuous distribution of wavelengths into responses of three different cone classes. 

In summary, the perception of colour at a location in the world is influenced by more than the wavelength of light that arises from it. The context of the perception matters.
