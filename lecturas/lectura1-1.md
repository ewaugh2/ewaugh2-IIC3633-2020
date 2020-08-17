# Item-based Collaborative Filtering Recomendation Algorithms

This paper displays the importance of implementing recomender systems and  reviews the challenges that the traditional algorithms to do so are facing. These are:

- Producing many high quality recomendations per second to millions of users and items (the scalability problem).
- Achive high coverage in the face of data sparcity (the sparcity problem).

Then it goes to explore the posibility that in order to surpass this challenges we could make a transition from traditional or user-based collaborative filtering to item-based collaborative filtering, to better perform the tasks of a recomender system: prediction and recomendation.

After this introduction, the paper describes how the traditional or user-based collaborative filtering algorithms (also called memory-based) work and how they differ from the item-based (also called model-based) algorithms. Then the authors explain how the later can solve the tasks of a recomender system.

#### Similarity Computation

The autors describe three methods:

- Cosine-based Similarity: calculates the cosine of the angle of the item's vectorial representation.
- Correlation-based Similarity: computes the Pearson-r correlation between the item's vectorial representation.
- Adjusted Cosine Similarity: this takes into account the different scales of user ratings. 

In the experimental section of the paper the authors conclude that for the experiment being done this is the best option.
 

#### Prediction Computation

The authors discuss two methods.

- Weightd Sum: ranking times similarity.
- Regression

In the experimental section the authors conclude that the weighted sum is better for the task they have at hand.


### Comments

In my opinion this paper was very helpfull to understand both the topic of recomender systems and its challenges. It shows the intuition behind recomendation and also shows (although not explicitly) that testing is required to determine the best combination of choices that will maximize the output of a system, impplicating that there is no "magic formula".

Specifically it's interesting that they tested for the "x" parameter (training-testing dataset ratio), the "k" parameter (amount of neighbours) and all combination of item-based choices, and compared it to the user-based and the non-personalized algorithms.


