---
title: "On news addiction and reading good things not more things."
subtitle: 
summary: 
authors:
- admin
math: true
markup: mmark
tags:
- Academic
categories:
date: "2019-03-26"
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


Patterns that reduce uncertainty about some aspect of the world are called information. Open your curtains in the morning, see a certain amount of light. Opening your window gives you some information about what time of the morning it is. More light is a pretty reliable way of approximating the time during sunrise. 

Speaking generally, it always seems right that more information is a good thing. If getting more information reduces our uncertainty and we want to be more certain, then collect as much information as possible. This feels right. In fact, it feels so right that it is the default operating mode for most people. Reading news daily or watching news hourly is a pretty common pasttime. The goal here must be to reduce the uncertainty we have about the world. When the news isn't out with a straighforward mission to decieve us we'll be getting some good nuggets of information that we can store away for later use in our quest to understand the world. Sure, some of those nuggets will be worse than others but we believe that information accumulates so we'll take what we can get.

Is more information always a good thing? In some circumstances it surely is. Here is a common scenario. There is a fixed pool of information sources that vary in their quality. If we sample them all and then combine them in a rational way then the total information will always be greater with more sources. So that is +1 for the more information camp. The cable news addicts.

Change the setup a little bit. I'm going to change it in a way that is a little more realistic (not much) for how we actually use information.

Let's say that there is fixed pool of information bearing samples. The samples vary in their quality, some are low information some are high. Then let's say that we can't sample all the sources -- we can only sample a fixed subset of those samples. Think of this like having a large collection of memories about the world but only a couple of them can be recalled in a given instant while we're thinking about something. Furthermore, for simplicity, assume that which samples form the subset are random. This is also kind of consistent with how memory works. There is obviously some structure to which events appear in memory, but there is also a arbitrary random quality to them as well. Now, once this subset of samples has been encoded we combine them in a rational way. This is a case where more information is not always better.

If the low quality samples increase in proportion to the high quality samples then the probability of selecting a high quality information sample goes down. The result is that the overall information is lower. If all you have access to is good information then total information will be good.

We can compare these two situations exactly using a simple simulation. The code is at the bottom of the page.

For situation 1 set n.good equal to total.samples. Set p.bad to 0. This means there are only good samples. Information increases.

Information is not clearly defined here. It is not in "bits" or "nats" -- units that result from a typical definition of information. The units here are related to how well a binary stimulus can be classified. Larger numbers mean we have more information to classify with. These units could be converted into Shannon information and we would get the same result.

For situation 2 set n.good to some number and set total.samples to some value lower than that. Then increase p.bad and see what happens. What this does is increase the proportion of low information samples relative to high information samples. The figures show what happens.



In the following, the proportion of bad samples increases and information goes down.
![a](/img/posts/info.sample_bad.png)

Next, the total number of samples increase and all are sampled, and the information goes up. 
![b](/img/posts/info.sample_good.png)


~~~ R
g <- function(n.good, p.bad, total.samples) {
  n.good <- n.good
  n.bad <- p.bad * n.good
  
  mu.snr.bad <- -log2(.99)
  mu.snr.good <- 1/sqrt(10)
  
  snr.vector <- c(rep(mu.snr.bad, times = round(n.bad)), rep(mu.snr.good, round(n.good)))
  
  f <- function(n.samples) {
    info.sample <- sample(snr.vector, n.samples, replace = F)
  }
  
  info.samples <- replicate(1000, f(total.samples))
  
  mean(sqrt(colSums(info.samples^2)))
}

out.vals <- lapply(seq(0, 1, .01), FUN = function(x) g(100, x, 10))

snr.frame <- data.frame(x = seq(0, 1, .01), y = unlist(out.vals))
~~~
