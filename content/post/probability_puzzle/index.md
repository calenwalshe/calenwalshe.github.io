---
title: "When playing Magnus Carlsen, play him twice."
subtitle: 
summary: 
authors:
- admin
math: true
markup: mmark
tags:
- Academic
categories:
date: "2019-03-10"
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

The Monty Hall puzzle is entertaining because the result turns out to be counter to intuition. Those are the most entertaining puzzles. The family of puzzles like Monty Hall are so contrived that they don't resemble reality. Reality, especially when chance and probability is involved is not expected to be _more_ intuitive than these puzzles. I like them because they are fun to think about but they also remind me how easy it for intuition to lead to wrong conclusions when not applied under the right circumstances.

Here is another puzzle that resembles the Monty Hall in this regard.

You are entered in a chess tournament. To win the big prize you have to win two matches in a row out of three matches that you will played. You will have two opponents, Magnus Carlsen and the local chess pro. Of course, the probability of beating Carlsen is lower than beating the pro. What you get to choose is the order you play them in. You can either choose to play Magnus, the pro, then Magnus or play the pro, Magnus, then the pro again. Which sequence would you choose?

The obvious choice is to select the sequence in which you play the pro twice and Magnus once, since Magnus is the better player. But we only suspect that is right, how do we justify our choice? Here is a simple argument by reasoning via probability: 

Let the probability of beating Magnus be $$Pr(Carlsen) = c$$ and the probability of beating the pro, $$Pr(Pro) = p$$ and let $$c < p$$.

The union of independent events is $$Pr(\bigcup\limits_{i=1}^N A_i) = \sum\limits_{i = 1}^N Pr(A_i)$$.

If we enumerate all the independent ways to win the contest under the first sequence it looks like this:

$$Pr(CPC) = cpc + cp(1 - c) + (1-c)pc$$

The first case is winning all three matches, the second is winning the first two and losing the second and the third is losing the first match and winning the second and third. $$1 - c$$ expresses the probability of losing to Magnus.

Likewise, the enumeration of the second sequence is as follows:

$$Pr(PCP) = pcp + pc(1 - p) + (1 - p)cp$$

Rearrange the terms in these sums and we get $$cp(2 - c)$$ for the first sequence and $$cp(2 - p)$$ for the second.

Now it's easy to see that since $$c < p$$ then $$cp(2 - c) > cp(2 - p)$$. Which is surprising because it is not as I would have thought prior running through this argument. Even though Magnus is a better player, it is still worthwhile playing him twice under these conditions. With this sequence the worse player is in the middle of the sequence and that gives a higher probability of getting two wins in a row.
