# Practical aspects of Deep Learning

## Learning Objectives 
* Recall that different types of initializations lead to different results. 
* Recognize the importance of initialization in complex neural networks.
* Recognize the difference between train/dev/test sets.
* Diagnose the bias and variance issues in your model.
* Learn when and how to use regularization methods such as dropout or L2 regularization.
* Understand experimental issues in deep learning such as Vanishing or Exploding gradients and learn how to deal with them. 
* Use gradient checking to verify the correctness of your backpropagation implementation. 

### 1. Train / Dev / Test sets 
* ML is a highly iterative process. 
* Intuition from one specific area (e.g. NLP, CV, and etc) often does not transfer very well to another field. 
* common splits for train/dev/test: 
	* for data size 100 to 10000: 70/30% (train/test) or 60/20/20%
	* for data size around 1000000 or above: 98/1/1%
* Mismatched train/test distribution: make sure dev & test sets come from the same distribution.
* Might be okay to not have a test set. (only dev set to choose the best model)

### 2. Bias / Variance 
* high bias == underfitting 
* high variance == overfitting 
* examples: 
![](./img/wk01_bias_variance.png)
![](./img/wk01_bias_variance2.png)
_based on the assumption that optimal error is nearly to 0%_ 
* training error indicates high bias 
* dev (i.e. CV set) error indicates high variance
* high bias and high variance == in some regions it's high variance and in other regions it's high bias. 
![](./img/wk01_high_bias_variance.png)

### 3. Basic Recipe for ML
* In modern DL era, there is probably no trade-off between variance and bias, since you would have specific methods that only reduce one of them. 
* training a bigger neural network alomst never hurts. 
* the recipe for resolving high bias/variance issues: 
![](./img/wk01_recipe.png)

