# Ghost-BatchNormalisation-
This code contains 5 experiments with regularization including Ghost Batch Normalisation on the MNIST dataset.

## Aim : 
Create and build a model for MNIST dataset with less than 10,000 parameter and apply the following regularizations for 25 epochs and report findings:
with L1 + BN
with L2 + BN
with L1 and L2 with BN
with GBN
with L1 and L2 with GBN
## Ghost BatchNormalisation
Ghost Batch Normalization, a technique originally developed for trainingwith very large batch sizes across many accelerators. It consists of calculating normalization statistics on disjoint subsets of eachtraining batch.Why might Ghost Batch Normalization be useful? One reason is its power as a regularizer: due tothe stochasticity in normalization statistics caused by the random selection of mini-batches duringtraining, Batch Normalization causes the representation of a training example to randomly change
every time it appears in a different batch of data. Ghost Batch Normalization, by decreasing the number of examples that the normalization statistics are calculated over, increases the strength of this stochasticity, thereby increasing the amount of regularization. Refer https://arxiv.org/abs/1906.03548
## Results
Ghost batchNormalisation reduces training time significantly and helps the model to generalise better as we can see that accuracy is consistently grater than 99.4% in the last few epochs. But when used with other regularisation it does not do well.Other regularization's such as L1 and L2 do  not show a significant increase in accuracy which was expected as these regularization do not work well with CNN's
