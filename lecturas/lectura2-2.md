# BPR: Bayesian Personalized Ranking from Implicit Feedback

## Introduction

The paper by Rendle, S., Freudenthaler, C., Gantner, Z., & Schmidt-Thieme, L. from 2009 is a very interesting approach to the item ranking generation for user recommendation task. It aims to create a total order criteria of all the items for each individual user, so then when asked for a user's recommendation we just sort and give the k highest values.

The paper contributions:

1. Present a general optimization criterion BPR-Opt for optimal personalizad ranking. Shows the analogies to maximizing the area under ROC curve.

2. For maximizong BPR-Opt they propose the generic learning algorithm LearnBPR based on stochastic gradient descent with bootstrap sampling of training triples that is superior to standard gradient descent techniques.

3. Show how to apply LearnBPR to two recomender model classes: MF and kNN

4. Empirically show that for the task of personalized ranking, learning a model with BPR outperforms other learning methods.


## Comments

1. The first thing I noticed is that the paper "Collaborative filtering for implicit feedback datasets" (1) is a great starting point to understand this paper. It was very useful to get to know the problem, it's characteristics and challenges. Also, the paper at hand is far more digestible than (1) and it addresses a more atomic and useful topic. This makes the joint reading very educative.

2. It's good that the paper focus on the most common real world problem (personalized ranking with CF on implicit feedback), and that it presents a general learning method that is easily combinable with recommenders.

Also, I find very interesting that this work builds on previous work in a direct manner. It doesn't try to "invent something completely new", but to create a framework to insert existing and working recommender systems, greatly increasing their performance.

Specifically, the framework delgates the task of modeling the relationship between  u, i and j (u: user; i, j: items) to an underlying model class like matrix factorization or adaptive kNN.

3. It's a very interesting idea to dispense of the score estimation part of the recommender system (delegating it) and focusing only on producing a ranking by creating a total order of all items for each individual user, thus creating a general framework in which implement a known (or new) solution to the problem of modeling the u, i, j relationship. 

A downside of this method might be that we lose the posibility of producing an explanation for the recommendation. This might be implemented directly on the model class but it is not addressed properly on the paper.

4. Finally, I found that the authors are very good at explaining the intuition behind each conclusion. They are solid in the math sections of the paper, but also they present sections with logical reasoning deriving conclusions that end up holding.

Note: also, the results speak for themselfes. The increase in efficiency and efficacy of the systems is staggering.


## Conclusion

This paper, along side with (1) are a very good read for anyone trying to understand recommender systems based on collaborative filterinf with implicit feedback. Also, the approach taken in this paper is very interesting (building a framework, not just an algoritm).

