---
description: 
draft: true
tags:
  - research
date: 2024-10-07
---
*you're going to think I've bitten off more than I can chew but I don't care one bit*

---

Learning is the induction of changes in a computational model which steer its behaviour in the direction of some goal.

Genetic evolution has had a part to play in assigning the billions of parameters in our brains, but this is by no means an explanation for our intelligence[^1] - otherwise we might expect to be born more fully featured[^2]. What we should perhaps pay more attention to is that genetic evolution has had a large part to play in developing the actual learning process itself; the process which adds the complex features which allow us to survive and thrive in life. It makes a sculpture of the clay blob in our heads one deformation at a time.

In machine learning, there are two ways of challenging the state-of-the-art which are all the rage right now:
1. Come up with a new model to train (or maybe the same model, but bigger)
2. Train an existing model on new data (or maybe the same data, but bigger)

What is much rarer is a challenge to the training process itself.

There is **one agreed-upon** algorithm for machine learning and it is Backpropagation (BP). Backpropagation itself is really a necessary and obvious derivation from the **one agreed-upon** principle for optimising a continuously-differentiable mathematical model: Gradient Descent (GD). [^3]

GD and BP are so deeply ingrained in ML today for the following reasons:
- Extremely well justified mathematically
- Works surprisingly well
- Been the standard for years
- Beaten many alternatives
- The idea of descending down a high dimensional hill is intuitive at first to a moderately bright high-schooler who has just started to understand basic calculus.

If you thought that coming up with a new model, or application, or dataset, could get you laughed out of the room, imagine if your plan was to come up with a new learning algorithm.
## The most interesting failing of BP
BP is embarrassed by one thing in particular. It is not how biological brains learn! There is more to learning 



[^1]: Which is not to say that we are born featureless.
[^2]: I've recently come to the realisation that I have been acting in my research as though it were.
[^3]: By "agreed-upon", I mean that it is "what everyone uses" (by exhaustive majority) "in the field of ML" 
