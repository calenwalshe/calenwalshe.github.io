---
title: The Princess Bride does game theory.
subtitle: The Princess Bride does game theory.
summary: 
authors:
- admin
tags:
- Academic
categories:
date: "2016-02-20"
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

The Alamo Draft House is a local theatre company here in Austin. Their bread and butter is putting on the current hits but they also make a solid focus on showing cult hits. Over at the Ritz yesterday they put on the Princess Bride (1987) a love story staring a young Claire Underwood (Robin Wright) in the innocent days before being corrupted by Frank and the dirty lies of the US Senate. 

One of the great scenes in this film is when the masked hero, Wesley, challenges Vizzini, one of the villians, to a battle of wits. The scene is humourous, but it has some underlying lessons for students of game theory and the psychology of human decision making. The scene begins as Vizzini clutches the Princess Buttercup (aka Claire Underwood/Robin Wright) and theatens to kill her if the hero Wesley steps any closer. Vizzini has cause to be worried, Wesley has just won a duel with a master swordsman and rendered a Giant unconscious in hand to hand combat. Vizzini does not possess any physical strength, but he does proclaim himself to have a massive intellect. Here is what Vizzini has to say about himself:

----

Hero: You're that smart?

Vizzini: Let me put it this way: have you ever heard of Plato, Aristotle, Socrates?

Hero: Yes.

Vizzini: Morons. 

----

So Vizzini is smart. Therefore, the only way for our hero to overcome Vizzini is to challenge him to a game of wits and this is exactly what he does. Being über confident in his abundant intellect Vizzini accepts the challenge.

Here is the game they play:

There are two cups of wine on the table. The masekd hero hides the two cups of wine and informs Vizzini that he has placed a powerful poison, Iocane, in one of the cups. Each contestant will drink from one of the cups with Vizzini getting to chose who drinks which cup. The stakes are that whoever drinks from the poised cup will presumably die.

So why is this game wits? At first blush, it might seem like this is more a game of pure chance. Sort of like playing Russian Roulette with an equal number of blanks and bullets. What makes this into a game of wits is when we consider the possibility that Vizzini could have a reasonably good model of the Hero's psychological processes that went into choosing which cup to place the poison in. In other words, Vizzini could attempt to read the Hero's mind.

Vizzini is, "like, a really smart person" and he verbalises his reasoning process:

---- 

Hero: All right: where is the poison? The battle of wits has begun. It ends when you decide and we both drink, and find out who is right and who is dead.

Vizzini: But it's so simple. All I have to do is divine from what I know of you. Are you the sort of man who would put the poison into his own goblet, or his enemy's? [pauses to study the Hero] Now, a clever man would put the poison into his own goblet, because he would know that only a great fool would reach for what he was given. I'm not a great fool, so I can clearly not choose the wine in front of you. But you must have known I was not a great fool; you would have counted on it, so I can clearly not choose the wine in front of me.

Hero: You've made your decision then?

Vizzini: Not remotely. Because iocaine comes from Australia, as everyone knows. And Australia is entirely peopled with criminals. And criminals are used to having people not trust them, as you are not trusted by me. So I can clearly not choose the wine in front of you.

Hero: Truly, you have a dizzying intellect.

Vizzini: Wait till I get going! Where was I?

Hero: Australia.

Vizzini: Yes -- Australia, and you must have suspected I would have known the powder's origin, so I can clearly not choose the wine in front of me.

Hero: [beginning nervousness] You're just stalling now.

Vizzini: You'd like to think that, wouldn't you? You've beaten my giant, which means you're exceptionally strong. So, you could have put the poison in your own goblet, trusting on your strength to save you. So I can clearly not choose the wine in front of you. But, you've also bested my Spaniard which means you must have studied. And in studying, you must have learned that man is mortal so you would have put the poison as far from yourself as possible, so I can clearly not choose the wine in front of me.

Hero: [nervously] You're trying to trick me into giving away something -- it won't work --

Vizzini: [triumphant] It has worked -- you've given everything away -- I know where the poison is.

Hero: [fool's courage] Then make your choice.

Vizzini: I will. And I choose [stops suddenly and points at something behind the Man in Black] what in the world can that be?

Hero: [Turns, looks] What? Where? I don't see anything.

Vizzini quickly switches the goblets while the Hero has his head turned.

Vizzini: Oh, well, I-I could have sworn I saw something. No matter.

The Hero turns to face him again. Vizzini starts to laugh.

Hero: What's so funny?

Vizzini: I'll tell you in a minute. First, let's drink -- me from my glass, and you from yours.

And he picks up his goblet. The Hero picks up the one in front of him. As they both start to drink, Vizzini hesitates a moment. Allowing the MAN IN BLACK to drink first, he swallows his wine.

Hero: You guessed wrong.

Vizzini: [roaring with laughter] You only think I guessed wrong... [louder now] ...that's what's so funny! I switched glasses when your back was turned. Ha-ha, you fool.

The Hero sits silently.

Vizzini: You fell victim to one of the classic blunders. The most famous is "Never get involved in a land war in Asia." But only slightly less well known is this: "Never go in against a Sicilian when death is on the line!Ahahahaha, ahahahaha, ahahaha--

----

Game theory is one of the jewels of 20th century intellectual achievements. It gives us a way to understand games such as the one that is played here by provided a framework for understanding how certain games 'ought' to be played when the players are making choices that are in their best interests. In game theory, you will often see the term rationality being bandied about. In many game theoretic settings the goal is determine what a rational decision maker would do given the available information and a certain goal. Rational typically means self interested because a rational decision is one that maximizes the payoff for individual and does not consider the harm to the competitor.

So let's assume that Vizzini is a rational decision maker. In a two player game such as we have in the film the information that he gets from the arrangement of the cups is nil. Instead, Vizzini must try and determine whether he can exploit any hidden patterns in the Hero's reasoning and exploit this pattern to gain information about which cup has the poison. In this case, Vizzini is assuming that the Hero is not a _fully rational agent_, if he was then there would be no way to get better than a 50/50 chance at determining which cup has the poison.

In reality, it would probably be impossible for Vizzini to make use of any such reasoning to any effect. Firstly, he doesn't know the Hero which means he doesn't have much input to calculate the Hero's decision making biases. Secondly, even if he did know the Hero very well it is likely to be well beyond the capability of human reasoning to determine the role of decision making biases in such a case as there are non-linearities in the way that multiple sources of information are combined to make a decision. The result is that any signal will be almostly completely obscured by the background noise.

However, in simpler games that are actually quite similar to Wesley's game we can actually obtain solutions. Consider the game of buying a car. The game is to get the best price you can on the car that you want. In other words, you want to beat the car sellers market. You might discover that during Winter there are the greatest number of cars put up on the market. Being smart, like Vizzini, you might think that this will lead you to get a deal. Not so fast, this is a bit too easy. Other buyers probably are able to figure this out as well and there might very well be a glut of _buyers_ in the market and thus lead to inflated sales prices. So know you need to ask yourself, how far is the average car buyer likely to take this? If other car buyers know that other car buyers know that spring is a good time to buy a car maybe they'll buy a car in the Fall instead, which is the period of the year during which the second highest volume of cars is available. Buyers might take this even one step further and realize that other car buyers might have access to the same information. This might bias them to pick another time of the year to buy. In other words, the real challenge here is figuring out how deep the other buyers estimates go and what information that have access to. If all buyers had access to the same information and were equally rational there would be no gaming the system. However, in human systems this is patently not the case and opportunities for advantage can emerge. 

The New York Times has an [interactive example](http://www.nytimes.com/interactive/2015/08/13/upshot/are-you-smarter-than-other-new-york-times-readers.html) of a variant of the Princess Bride game. See how you do!
