# Week 01: Intro to Deep Learning

## Learning Objectives 
* Understand the major trends driving the rise of deep learning.
* Be able to explain how deep learning is applied to supervised learning.
* Understand what are the major categories of models (such as CNNs and RNNs), and when they should be applied.
* Be able to recognize the basics of when deep learning will (or will not) work well.

<hr>

## 0. Course Outline
1. Intro 
2. Basics of NN programming 
3. 1 hidden layer NN
4. Deep NN
 
### 1. What is Neural Network
* Figuring out a mapping between X & y. Mostly used in supervised learning. 
* Deep learning == training large neural network
* Single Neuron: applying linear function or non-linear function (a transformation)
* __ReLU__: Rectified Linear Unit - function that looks like _/.
* __Density Connected__: take all ouputs from the previous layer as inputs for this neuron. 

### 2. Supervised Learning with Neural Network
Examples: ![](./img/wk01_SL_examples.png) 

* Common Choices of NN: Standard NN (data science), __CNN__ (computer vision), __RNN__ (speech recognition, machine translation), or custom/hybrid NN (auto-driving cars).
![](./img/wk01_NN_examples.png)

* Structured Data: tabular databases 
* Unstructured Data: audio, image, text 

### 3. Drivers behind Deep Learning 
1. Large amount of labeled data. 
2. The ability to train large NN. (a.k.a. computional power) 
3. New Algorithms

![](./img/wk01_NN_vs_data.png)

* With a small amount of data, the order of performances of diff learning algorithms are not well-defined. 
* Activation function: move from sigmoid to ReLU because sigmoid function have extremely small slope on both ends -> learning to be slow but ReLU has a constant slope on the right half -> gradient constant -> learning more quickly converges. 
* Iterative Process: Idea -> Code -> Experiement -> Idea ...

## Weekly Bio: Geoffrey Hinton
* The "Godfather" of DL - a legend. 
* Backprop algorithms can learn wording connections - semantic meanings. 
* A.I. perspective Knowledge: how it relates to other concepts. 
* 