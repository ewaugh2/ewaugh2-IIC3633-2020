# Document Clustering Based On Non-negative Matrix Factorization

## Introduction

In the paper from 2007 by Pazzani & Billsus we find a detailed overview for how content based recommendation systems work. It specifies what separates this system from non content based recommenders, what are the challenges that this systems must solve and presents common ways used to solve them. These problems are:

- Describe items to be recommended.
- Create user's profiles that describes the types of items that the user likes or preferes.
- A way to compare the item representation and a user's profile to determine what to recommend.

## Comments

Although the paper addresses the advantages of using machine learning to solve the problems of a content based recommender system, I think that the use of Deep Learning (DL) applications can furder help to develop this kinds of systems. For example, the term frecuency times inverse document frecuency (tf*idf) is a great way to approach the problem of item representation (very simple, intuitive and good mathematical properties), but letting a neural network (NN) extract the features from items has been proved to work better than to create man written and intuitive ways to do so.

One problem of my suggestion that the authors addresses in the "Limitations and Extensions" section of the publication, is that in order to use DL one would need a lot of data to train the models, specialy the item representation one. For this one in particular, Transfer Learning techniques might be worth to explore in order to ease the data amount required to build a usefull model.


## Conclusion

Of course this paper was written before the DL boom, and it is very common to see publivations like this one talking about methods like Singel Value Decomposition (SVD) so it is understandable, but I would like to explore the potential that DL holds on the development of this kind of recommender systems.

