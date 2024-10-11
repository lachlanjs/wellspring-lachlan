---
description: 
draft: true
tags: 
date: 2024-10-05
---
*rant*

---

Federated Learning is about pooling the data of many clients to train a model, without actually ever pooling the *data*.
## problem: clients have different data distributions
There are different FL "settings". A common point of distinction between different FL settings is how the datasets of the clients are assumed to differ. In the easiest case, the clients share the same feature space, and their data is I.I.D (independent and identically distributed). This is to say that each client's data comes from the exact same underlying distribution.  

In practice, this can be close to true for certain applications, but there are many other cases to consider. By the fact of the clients being different entities in the first place, be they medical institutions, research labs, or users, the data is likely to be different in some way. 

Taking the scientific domain as an example, research labs may be taking the same measurements (same features) on different samples. One lab's instruments might be getting a bit old; another lab might not have followed proper temperature control procedures. This can shift and transform their underlying distributions away from each-other. It is not good practice to superimpose data from very different distributions if you set out to create a model of **one** distribution. 

The setting discussed so far has been "horizontal" FL. It is named this way because you can imagine taking a dataset, where rows -> samples and cols -> features, and slicing it horizontally. The resulting partitions represent the data belonging to the different clients.

Naturally, you could consider "vertical" FL, 

## how do you align client data?


## but does this actually align client data?

## okay so how do you actually align client data?

## but does THIS actually align client data?

