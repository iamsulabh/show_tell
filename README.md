# Show Tell Image captioning
# Implementation of 'Show and Tell: A Neural Image Caption Generator' paper by [Vinyals et al.] at https://arxiv.org/abs/1411.4555

Note: This is a work in progress.

Here I am going to implement the popular image captioning approach proposed in the above mentioned paper.
However this will not be an exact implementation of the paper and differs in these following ways:
* The authors use an ensemble of models but we use only one model. The authors have found that using ensembles of models enables them to achieve a performance boost of 2 points with respect to BLEU metrics. However, as we shall see, certain optimizations allow us to acheive better scores on certain metrics than the scores mentioned in the paper. I will explain the optimizations used and the scores that we acheive. 
* The authors extract a single image feature vector from the penulimate layer of CNN but we extract a set of feature vectors from a lower layer. We have noticed that this allows us to acheive better performance. 
