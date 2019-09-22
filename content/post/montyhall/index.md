---
title: Did Monty consider that someone might want the goat?
subtitle: 
summary: 
authors:
- admin
math: true
tags:
- Academic
categories:
date: "2016-07-07"
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

The Monty Hall problem is a classic. I like it because it posed with simple language and hides it's complexity. The first time you hear the puzzle you have a good chance of answering correctly (50/50). However, once you start to think about the _reason_ for your answer you might need to grab a beer and get ready to think a little bit. [As the story goes](http://www.wired.com/2014/11/monty-hall-erdos-limited-minds/), one of the 20th centuries most famous mathematicians, Paul Erdos, needed several days before he was convinced by the truth of the proposed solution.

For a full description of the game check out the [wikipedia page](https://en.wikipedia.org/wiki/Monty_Hall_problem). The version I'm going to describe is stripped down.

There are three doors. Behind one of the doors there is a car and behind the other two doors there are goats. You player is invited to make a guess as to which door hides the car. After making a selection the host will open one of the doors that has a goat. Now, the player is given the opportunity to switch their choice to another door or to stick with their current selection. What would you do?

![smiley](https://upload.wikimedia.org/wikipedia/commons/3/3f/Monty_open_door.svg)

If you are like Paul Erdos you would initially think that it doesn't make any difference whether you switch or not. The probability of selecting the car on the first choice is 1/3. Swapping doesn't change this basic fact. This is the incorrect intuition that many people have for the problem. The correct solution is that one should always swap. 

The best way to show this is with conditional probabilities. In other words, you show that the probability that the car is behind door two given you initially selected door one and the host removed door three is higher than 1/3. This is done for us on the wikipedia page.

My own intuition for the problem goes as follows:

The probability of getting the car on the first try is 1/3 and the probability of not getting it is 2/3.

Now, break down the switching into these two cases:

If you happened to guess right the first time switching will be wrong. This happens 1/3 of the time.

On the other hand, if you happened to guess wrong on the first try then switching will always get you the correct door. This happens 2/3 of the time.

It's really as simple as this. Adopting a strategy of switching will result in getting the car 2/3 of the time. A big improvement over the 1/3 that we get from staying.

Another way to demonstrate this without going to conditional probabilities is run a simulation and see what probabilities come out. Run this code in R.

~~~ R
num_trials <- 100000 # number of trials

car     <- sample(1:3, num_trials,replace = T) # set the door with the car
choice  <- sample(1:3, num_trials, replace = T) # set the door choice of the contestant

remove_options <- apply(cbind(car,choice), 1, function (x) setdiff(c(1,2,3), x)) # the door(s) the host can choose to remove
remove         <- lapply(remove_options, function(x) ifelse(length(x) > 1, sample(x, 1), x)) # randomly select a door to remove

swap<- unlist(apply(cbind(choice, remove), 1, function(x) setdiff(c(1,2,3), x))) # always swap door
sum(swap == car)/length(car) # proportion of swapped choices that match the car door
~~~
