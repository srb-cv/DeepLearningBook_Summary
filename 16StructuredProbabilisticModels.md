## 16 Structured Probabilistic Models for Deep Learning

### Structurd Probabilistic Models -

* Structured Probabilistic Models are a way of describing a probability distribution using a graph.
* Describe which random variables in the probability distribution interact with each other.
* Since nides and edges are used to represent the data, these are also known as graphical models.


### Need for structured modelling 
* Modeling a distribution over thousands or millions of random variables is computationally and statistically challenging.
* If we want to model a vector X of R^n, each can take k discrete values each. P(X) would have k^n parameters.

### Using graphs to describe model structure
**Directed Models/Bayesian Network**

Models in which the edges are directed. 
![Directed graph Example](images/16/directed.png?raw=true)
Directed graphical model relay race example. Where finishing times of Carol depends on Bob and Bob's on Alice.

**Undirected graph/Markov Network** 
![Directed graph Example](images/16/undirected.png?raw=true)
Undirected graph representing how your roomates health h_r, your health h_y and your work colleague's health h_c affect each other.

### Factor graphs

Another way of drawing undirected graphs. It has two types of nodes -
* Variables
* Factors - Defining the relationship between the variables and comes with a factor function to describe their relationship.

### Use of probabilistic models

* Ask questions about how variables are related to each other.
* given the medical tests we might want to ask what disease a patient might have by using the principle of maximum likehood.

### Deep learning approach to structured probabilistic Models

**Restricted Boltzmann Machine**

* Single layer of latent variables and hidden variables. Both connected by a weight matrix W.
* v^T W h, W is a learnable parameter. The restrictions are there should not be any direct interaction between any two visible units or between two hidden units.

### Important questions from chapter
* In which case may a graphical model fail to encode and independence between variables?
* What do we do when we want to draw a sample from an undirected model?
* What properties of RBM are necessary for 16.11-12 to hold true?
