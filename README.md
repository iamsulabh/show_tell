# Image captioning and Analysis
## Implementation of 'Show and Tell: Lessons Learned from the 2015 MSCOCO Image Captioning Challenge' paper by [Vinyals et al.](https://ieeexplore.ieee.org/abstract/document/7505636)
### This paper was published in IEEE TPAMI with 4000+ citations (including previous conference version).
## Analysis with different combinations of CNN+RNN, data augmentation, pre-trained embeddings.


**Note:** This is a work in progress. I will write a detailed blog post on medium.com explaining all the code and detailing the steps.

This will not be an exact implementation of the paper and differs in these following ways:
1. The authors use an ensemble of models but we use only one model. The authors have found that using ensembles enables them to achieve a boost of 2 points with respect to BLEU metrics. However, as we shall see, certain optimizations allow us to acheive better scores on certain metrics than the scores mentioned in the paper.
2. The authors extract a single image feature vector from the penulimate layer of CNN but we extract a set of feature vectors from a lower layer. We have noticed that this allows us to acheive better performance.
3. We use pre-trained RESNET-152 Convolutional Neural Network instead of Inception used in the paper and it helps to improve results.
4. Implementation details: We do not use batch normalization to process inputs as no noticeable improvements were observed. 

In addition to implementing the paper, we perform additional analysis with the following changes: 
1. We experiment with image data augmentation and observe that it helps boost performance (depending on which technique used.)
2. We experiment with pre-trained word embeddings. Some pre-trained word embeddings help in increasing evaluation scores.
3. We experiment with different CNNs to extract image feature vectors.
4. We experiment with different versions of Recurrent Neural Networks: LSTM, GRU, Bidirectional RNN(/LSTM/GRU).

