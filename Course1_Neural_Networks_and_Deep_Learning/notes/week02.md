# Week 02: Neural Network Basics

## Learning Objectives 

* Build a logistic regression model, structured as a shallow neural network. 
* Implement the main steps of an ML algorithm, including making predictions, derivative computation, and gradient descent. 
* Implement computationally efficient, highly vectorized, versions of models.
* Understand how to compute derivatives for logistic regression, using a backpropagation mindset.
* Become familiar with Python and Numpy
Work with iPython Notebooks.
* Be able to implement vectorization across multiple training examples. 

<hr>

### 1. Binary Classification 
* Unrolling image RGB info: X = RGM channels of the image unrolled in a long vector. 
* __notations__:  
![](./img/wk02_BC_notation.png) 

### 2. Logistic Regression 
* __problem formulation__: the notation in red will not be used in this course.  
![](./img/wk02_LR_formulation.png)

### 3. Logistic Regression Cost Function
* If to use the squared error loss function, the optimasation problem becomes non-convex (i.e. has multiple local minima). 
* __loss function__: for a single training example. 
* __cost function__: for the entire training set. 
![](./img/wk02_cost.png)

### 4. Gradient Descent 
* __illustration__: 
![](./img/wk02_GD1.png)
* _alpha_: learning rate.
* _dw_: derivative term of w. 
* _db_: derivative term of b. 
* __gradient descent update__: 
![](./img/wk02_GD2.png)

### 5. Derivatives with Computation Graph
* one step of __backward__ propagation on a computation graph yields derivative of final output variable. 


