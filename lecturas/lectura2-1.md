# Collaborative Filtering for Implicit Feedback Datasets

## Intoduction

This paper by Hu, Y., Koren, Y., and Volinsky, C. from the year 2008 presents a theorical approach with experimental results to the collaborative filtering (CF) recommenter system based on implicit feedback. It places this problem in the context of other CF with explicit feedback and other content based approaches, briefly describing their differences in terms of requirements and advantages.

It also outlines the general characteristics for any implicit feedback recommender system:

- No negative feedback
- Implicit feedback is noisy
- The numerical value on explicit feedback indicates preference, whereas the numerical value of implicit feedback indicates confidence
- Evaluation of implicit feedback recommenders requires appropriate measures.

After that, the authors present a theoretical model for generating predictions and its explanations, followed by an experiment performed in the TV consumption industry.


## Comments

1. It would be interesting to see how explicit and implicit feedback can be combined to form a mix sytsem.

The problem of implicit feedback that a user's favorite movie will be wathched only once but a show that the user finds "ok" will be viewed multiple times, working together with explicit feedback could help to partly solve the sparcity problem by finding correlation between frequently viewed shows an movies.

Users probably don't leave explicit feedback on every item they consume, just on the ones that cause an extreme impresion, either good or bad. But they do leave implicit feedback on every item they interact with, so one could build a system that models a user using explicit and implicit feedback and using the recurrent events of the implicit feedback one to fill the gaps of the explicit feedback (as those are more likely to reflect the user's opinion).


2. The optimization algorithm design is very smart and interesting. As a normal stocaic decent would have to much computational requirements the authors choose to implement  an "alternating leas squares" to compute loss on the items and optimize in that direction and then alternate to the users.


3. Related with the previous comment, the explanation generation from the alternating least squares is a great idea. It asumes though, precomputed values that in a large enough system could be very difficult to achieve.


4. Again related with the previous comment, there is a flaw that I couldn't help but to notice in the method described by the authors. This is that here is too much precomputing to do. They put emphasis in that the system  is supposed to be scalable, and maybe the computational requirements do scale sinearly, but in a large enough system the precomputed values may be to big to hold. I felt that that issue was not addressed properly.

On the other hand it is remarcable that the authors achieved a systems that scales linearly with the data, and there are parts of the paper that are very well designed. For example, when they present a few variants for the variable definition proces, and then outline the underlying process that needs to ocurr in order for the system to work.


## Conclusion

This paper was very interesting to read, although not very friendly. It's outline is on point and almost all issues were addressed.


