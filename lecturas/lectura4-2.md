# Document Clustering Based On Non-negative Matrix Factorization

## Introduction

In the paper from 2003 by W Xu, X Liu & Y Gong, the authors present a novel document partitioning method based on the non-negative factorization
of the term-document matrix of the given document corpus. The method differs from the latent semantic indexing method based on SVD and the related spectral clustering methods in that the latent semantic space derived by NMF does not need to be orthogonal, and that each document is guaranteed to take only non-negative values in all the latent semantic directions.

Later, by experimenting, the authors show that these two differences bring about an important benefit that each axis in the space derived by the NMF has a much more straightforward correspondence with each document cluster than in the space derived by the SVD, and thereby document clustering results can be directly derived without additional clustering operations. These experiment show that this mew method surpasses SVD and the eigen decomposition clustering methods not only in the easy and reliable derivation of document clustering results, but also in document clustering accuracies.

## Comments

I find that the idea of deriving a semantic space where the axies do not have to be ortogonal, a very smart one. At first it comes to mind as a counter intuitive, hard to visualize way to complicate the porblem, but together with the guarantee that each documet will take only non-negative values in all the latent directions it becomes an even more intuitive way to look at the latent space representation than other methods, where the documents representation are closer to its tags (axis).

The experimentation only confirms the intuitive potential that this method holds. It would be very interesting to apply this methods to different problems and to study the posibility of building a hierarchical tree-like visual representation of the diferent category clasifications for each document to furder unterstand how intuition can help us understand this method.

## Conclusion

The bigest takeaway from this work for me is that thinking outside the box can lead to staggering results. The at first counter intuitive (and off putting) approach taken by the authors to build a latent representation space in which the axis do not have to be ortogonal turned out to be a great solution for the problem, and with the propper explanation it comes back as a very logical approach, leaving me (the reader) with the thought "why didn't anyone thought about that before".

