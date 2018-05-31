## Deep Neural Network Application 

### Objectives
* Build and apply a deep neural network to supervised learning.  

### Notes
1. In the next course on "Improving deep neural networks" you will learn how to obtain even higher accuracy by systematically searching for better hyperparameters (learning_rate, layers_dims, num_iterations, and others you'll also learn in the next course).

### Common Practice 
* General methodology (As usual you will follow the Deep Learning methodology to build the model):
	1. Initialize parameters / Define hyperparameters
	2. Loop for num_iterations:
		* Forward propagation
		* Compute cost function
     * Backward propagation
     * Update parameters (using parameters, and grads from backprop)
	3. Use trained parameters to predict labels