---
title: Is there something so unbelievable that you would assign it probability 0?
subtitle: 
summary: 
authors:
- admin
math: true
tags:
- Academic
categories:
date: "2019-07-30"
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

How much evidence do you need to be convinced in something that is very implausible is actually the case? Or rather, if you really don't believe something to be true, how much evidence do you need to push you all the way to near certainty?

Of course, this is a question about probabilities so we aren't talking about any kind of knowledge that can be gained without evidence. The kind, for example, where we make definitions and then reason according to a set of rules to get some new knowledge. This kind of reasoning is common in mathematics or law. Most scientific laws, and especially in the rough and tumble world of knowledge in the real world (is this burger fully cooked, is Jones going to arrive late for the meeting again etc...) we are always working with probability and hence using some data to assign a definite number to a possible state of the world.

Let's think about an interesting case. You believe that something is very implausible but not all the way down at 0. For example, someone claims to have the miraculous ability to communicate with the deceased. For me, this is very unlikely but I'm willing to entertain at least the possibility that it could be true. How low is the probability? I think somewhere around -75 dB. How did I get that number? Basically, I asked myself how many yes/no questions would they have to get right about someone I knew who was deceased that only I would know the answer to. I found by introspecting that after 25 correct responses I would notice a change in my belief. Of course, this number depends on the conditions of the test. This would be 25 questions that I was pretty sure they simply could not know. That's pretty low, much lower than most Hollywood films where the clairvoyant hooks people in with a couple guesses but that's where I'm at.

But how many more guesses would be need to get to really make a big dent in my belief about their powers of clairvoyance? The answer is that with a prior that low more evidence will certainly result in a change in my beliefs but it will never approach certainty. There are always some alternative hypothesis that I would entertain that could explain the data I'm observing. These alternatives might also be extremely low, say down at around -50 dB but the important point is that there are competitor hypotheses that are at least more plausible to me than clairvoyance.

This kind of thinking comes from a straightforward application of Bayes' rule to combine evidence and prior beliefs to determine the probability of a hypothesis.

For the clairvoyance case: C is the proposition that the person has clairvoyance and D is the proposition that they got some number of guesses correct.

According to Bayes rule:

$$Pr(C \mid D) = Pr(D \mid C) * Pr(C) / Pr(D)$$

I found my prior is $Pr(D) = -75~\text{dB}$.

The part of this that makes it very difficult to get to near certainty in a case like this is that the value of the denominator $Pr(D)$ is formed by conditioning on a possibly large number of alternative hypothesis, in addition to the hypothesis that the person has clairvoyance: the person happened to actually know the person we are referring to, I'm a contestant on a twisted game show, there is a hidden microphone and they are getting answers from someone outside the room etc... These are all implausible, but less implausible than clairvoyance. To get the probability of the denominator we have by the law of total probability:

$$Pr(D) = Pr(D \mid C)  Pr(\text{C}) + \sum_{i=1}^{N} Pr(D \mid A_i) Pr(A_i)$$

If those alternative hypotheses stay more plausible than clairvoyance we are going to stay pretty close to the initially low prior belief.

Although this example is contrived it has relevance to the real world, especially if one believes that human reasoning is approximately rational. An important footnote here is that nowhere in this setup are we dealing with *true* probabilities. It's a statement about subjective states of affairs and how beliefs ought to change under those conditions.
