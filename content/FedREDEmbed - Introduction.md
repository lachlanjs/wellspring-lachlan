---
description: 
draft: false
tags:
  - research
date: ""
---
*introduction to an ongoing research project*

---
I've got a ML problem that I am working on and I thought it would be a fun experiment to document some thoughts here

The problem has to do with Federated Learning. In essence, as far as I am concerned right now, Federated Learning is about training a series of $N$ models on $N$ different datasets belonging to $N$ different clients as well as possible [^1] 

The premise is usually that those $N$ datasets have something in common that would make you want to combine all of them together by instinct and train one monolithic model. The model would be better for having been trained on data of higher quality, quantity and diversity. In practice, there is some reason that this cannot occur. You are forced to find a way to train $N$ models in a way that benefits from the $N$ different datasets without ever actually sharing the data explicitly.

Federated Learning solves this problem by executing training epochs for the $N$ different models only on their respective datasets, interrupting this process at regular intervals to **aggregate** and **redistribute** the **models**. In unrigorous terms, this ensures that each model is *influenced by* the $N-1$ datasets that it does not belong to, without any data-sharing explicitly taking place. This technique is known as FedAvg.

What makes the problem interesting at its core, to me, is that these datasets *can* be very different. They may:
- Originate from different distributions
- Vary in their number of samples
- Contain different features entirely
- Have different labels or different tasks associated with them (classification vs regression)

There are many cases where FL can be applied where the data belonging to each client is the same, or belongs to the same underlying distribution, but I am interested in the adaptations that need to be made when these significant differences *do* arise; what do they tell us about FL in general? can we create something that works better in all cases by exploring what happens in these more extreme settings?

Take, for example, the possibility that the client datasets have different feature sets. One client might have 10 features, the next 20. This is going to alter the parameter structure of the model. We cannot simply average models that don't have the same structure; it doesn't make sense. How do we overcome this?

A possible answer, and main interest of my investigation, is the use of a data preprocessing step prior to model input. If successful, this step should serve the function of aligning these different datasets in a way that assists the federated model's training. 

*more to follow in another page*

[^1]: Federated Learning is much more than that in reality. I am completely ignoring issues such as encryption and adversarial attacks. I am also ignoring the lineage of Federated Learning techniques predating FedAvg.