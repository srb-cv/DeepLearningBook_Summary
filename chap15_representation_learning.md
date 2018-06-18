## 15 Represenatation Learning

Represenatation learning is useful to handle multiple modalities or domains, or to transfer learned knowledge to tasks where few or no examples are given but a task representation exists.

Both supervised and unsupervised deep learning algorithms have a main training objective but also learn a representation as a side effect. Difference is that in case of supervised learning we do not impose any condition on the learned intermediate feature.

### 15.1 Greedy Layer-wise Unsupervised Pretraining

* Enabled researchers for the first time to to train a deep supervised network.
* This appproach relies on single layer represenattaion learning algorithm.

  Each layer is pretrained using unsupervised learning, taking the output of previous layer as input and producing as output a new simpler representation

> * Greedy Layer-wise Unsupervised training is not required nowadays to train deep neural network architectures.
> * In context of  supervised learning task it can be viewed as a regularizer and a form of parameter initialization

### 15.1.1 When and why does unsupervised pretraining work ?

There exists different paradigms other than unsupervised pretraining for performing semi-supervised learning with the neural networks.
Example > Virtual Adversial Training mentioned in section 7.13.
Also Ladder networks(Rasmus et al. 2015) to combine both supervised and unsupervised losses

**why unsupervised pretraining works ?**

Two main ideas:
* Choice of initial parameters have a significant regularizing effect on the model
* Learning algorithm can use information learned in the unsupervised phase to peform better in the supervised learning stage


**when unsupervised pretraining works ?**
* From the point of view of unsupervised pretraining as **learning a representation**, it would be effective when the iniotial representation is poor.

   Example, use of word embeddings where one hot vectors are not very informative.

   Also such pretraining is less effective when processing images, perhaps because images already lie in a rich vector space.

* From the point of view of unsupervised pretraining as a **regularizer**, such prtraining is helpful when number of labelled data is very small and number of unlabelled examples is very large.

**Disadvantages of Unsupervised pretraining**
* The complete learning process involves operating with two trainig phases. So this strategy does not have a clear way 
