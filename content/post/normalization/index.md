---
title: "Nature is pretty good at building machines."
subtitle: 
summary: 
authors:
- admin
math: true
markup: mmark
tags:
- Academic
categories:
date: "2019-04-01"
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

I think a lot about detection and estimation problems. A detection problem is one in which it pays off to identify the presence or absence of a signal amongst some background noise. This is a problem that has applications all over the place. Transmission of data over the internet relies on detection of discrete pulses encoded in an analog signal. Doctors "detect" cancerous masses in images taken with an x-ray or other technology. Estimation is a different but related problem. In an estimation problem the challenge is to figure out which state the world is in when we only receive some noisy corrupted sample from the world. It is like detection but with estimation we want more than "yes" or "no" we want to know the value behind the noisy samples.

I think about detection and estimation because they are problems that visual systems are confronted with all the time. They are both problems that biology has solved over and over again to allow organisms to use sense data (signals encoded by the sense organs like the eyes and ears) to understand the environment they are in.

They are also well posed computation problems. When the setup is simple enough there are ways to characterize exactly how biological systems "should" do detection and estimation. In these cases we don't have to settle just for "how" detection and estimation comes about.

The concept of normalization has been an important principle in sensory neuroscience for a number of decades. There are several distinct ideas that the term can refer to but generally speaking it refers to a variety of computations that take the sensory inputs and divide (normalize) them by some other quantity. There are at least two good reasons why normalization occurs in these circuits. One reason is that it provides a mechanism for response gain. Neurons have physical limits on their minimum and maximum activity. Normalization helps expand the range over which neurons take inputs and improves sensitivity of the response.

Another interesting and subtle role for normalization is that it provides improved statistical power for systems, like neural networks, that are responsible for detection and estimation and that have large variations in how reliable the units of the system (neurons) are. Improving the statistical power yeilds higher signal to noise, better estimation (accuracy) and lower error rates (detection). All of those things are complimentary ways of saying that normalization is necessary to perform well under conditions of large and portentially varying uncertainty.

There are some good ways to argue for the inferential benefits of normalization, but not many are simpler than simulation.

The figures below are the result of a toy simulation estimating the mean from noisy samples with and without normalization. The trick here is that while 100 samples are drawn, each of those 100 samples is drawn from a distribution with a different variance but the same mean. The differing variance means that each of the 100 samples differs in the amount of information that they give about the population mean. However, they all contribute something and they also should be combined to come up with an estimate that uses all available information. In this example, normalization is used to weight each sample by an _estimate_ of its reliability. With normalization the population mean is estimated as a weighted mean of the samples where the weights are the reliability. Without normalization we simply compute the unweighted mean. This results in all samples contributing to the estimated mean in an equal manner. Keeping with the analogy to neurons, even if a neuron is very noisy (has responses that are high or low to the same stimulus) and is known to be noisy the rest of the brain would still listen to that neuron just as closely as a neuron that was very reliable and consistent. With the described normalization setup this noisy neuron would be downweighted and its contribution minimized.

The left panel has the results of the no normalization experiment and the right panel has the normalized results. The different coloured lines show what happens when we try and combine different numbers of samples. When averaging things we generally expected the estimate to get better with more samples, normalization or not. The x axis is the way I set the range of noisy units (neurons) in this experiment. The range of variances in the sample range from 0 to an upper limit. The x axis shows that upper limit. A value of 20 here means that the variances of the sample population are from 1 to 20. The values on the y axis is the measure of error. Larger values mean worse estimation performance.

![normalization](/img/posts/normalization.png)

To reiterate the analogy to neurons: a single sample is a hypothetical response of a single neuron; all of the samples form a population of neurons. The samples are combined either in a normalized or unnormalized way; the same problem would be true for the population of neurons as well. Neurons differ in how noisy they are, so any rule that combines them would need to take the variation in reliability into account.

The results of the toy simulation show in a straightforward way how the biological rule of cortical normalization can lead to computational benefits for detection and estimation. 




~~~ R
library(purrr)

true.mu    <- 20
sigma.var <- seq(1, 20, length.out = 5)
n.samples  <- seq(10, 100, 10)
b.norm     <- c(0,1)

param.frame <- expand.grid(true.mu = true.mu, sigma.var = sigma.var, n.samples = n.samples, b.norm = b.norm)

param.frame.data <- by_row(param.frame, function(x) {
  n.rms <- 1000

  noise.fixed <- seq(1,x$sigma.var,length.out = x$n.samples)
  obs.sample <- replicate(n.rms, rnorm(x$n.samples, x$true.mu, noise.fixed))
  
  if(x$b.norm) {
    sigma_hat <- apply(obs.sample, 1, var)
    
    
    norm.val <- (1/sigma_hat) / sum(1/sigma_hat)
    
    obs.sample.1 <- sweep(obs.sample, 1, norm.val, "*")
    
    obs.sample.2 <- colSums(obs.sample.1)
    
    error <- mean((obs.sample.2 - true.mu)^2)
  
    }else{
      
      obs.sample.1 <- sweep(obs.sample, 1, 1/x$n.samples, "*")
      
      obs.sample.2 <- colSums(obs.sample.1)
      
      error <- mean((obs.sample.2 - true.mu)^2)
  }
  data.frame(error = error)
}, .to = "simulate_col")

param.frame.data.unnest <- param.frame.data %>%
  unnest()

~~~
