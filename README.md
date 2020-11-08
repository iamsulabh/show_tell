# show_tell
# Implementation of 'Show and Tell: A Neural Image Caption Generator' paper by [Vinyals et al.] at https://arxiv.org/abs/1411.4555

Note: This is a work in progress.

Here I am going to implement the popular image captioning approach proposed in the above mentioned paper.
However this will not be an exact implementation of the paper and differs in these following ways:
* The authors use an ensemble of models but we use only one model.
* The authors extract a single image feature vector from the penulimate layer of CNN but we extract a set of feature vectors from a lower layer. We have noticed that this allows us to acheive better performance. 
