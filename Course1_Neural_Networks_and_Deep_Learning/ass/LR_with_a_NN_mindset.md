## Logistic Regression with a Neural Network Mindset 

### Objectives
* Build the general architecture of a learning algorithm, including:
	* Initializing parameters
	* Calculating the cost function and its gradient
	* Using an optimization algorithm (gradient descent)
* Gather all three functions above into a main model function, in the right order.

<hr>

### Notes
1. A trick when you want to flatten a matrix X of shape (a,b,c,d) to a matrix X_flatten of shape (b ∗∗ c ∗∗ d, a) is to use: ```X_flatten = X.reshape(X.shape[0], -1).T # X.T is the transpose of X```  
2. One common preprocessing step in machine learning is to center and standardize your dataset, meaning that you substract the mean of the whole numpy array from each example, and then divide each example by the standard deviation of the whole numpy array. But for picture datasets, it is simpler and more convenient and works almost as well to just divide every row of the dataset by 255 (the maximum value of a pixel channel).  
3. Preprocessing the dataset is important.
4. You implemented each function separately: initialize(), propagate(), optimize(). Then you built a model().
5. Tuning the learning rate (which is an example of a "hyperparameter") can make a big difference to the algorithm. 

### Common Practices 
* Useful Packages:
	1. `numpy` is the fundamental package for scientific computing with Python.
	2. `h5py` is a common package to interact with a dataset that is stored on an H5 file.
	3. `matplotlib` is a famous library to plot graphs in Python.
	4. `PIL` and `scipy` are used here to test your model with your own picture at the end.
* Common steps for pre-processing a new dataset are:
	1. Figure out the dimensions and shapes of the problem (m_train, m_test, num_px, ...)
	2. Reshape the datasets such that each example is now a vector of size (num_px * num_px * 3, 1)
	3. "Standardize" the data 
* General Architecture of a Learning Algorithm
	1. Initialize the parameters of the model
	2. Learn the parameters for the model by minimizing the cost  
	3. Use the learned parameters to make predictions (on the test set)
	4. Analyse the results and conclude
* The main steps for building a Neural Network are:
	1. Define the model structure (such as number of input features)
	2. Initialize the model's parameters
	3. Loop:
		* Calculate current loss (forward propagation)
		* Calculate current gradient (backward propagation)
		* Update parameters (gradient descent)  
__You often build 1-3 separately and integrate them into one function we call model().__
* Interpretation of different Learning Rates
	* Different learning rates give different costs and thus different predictions results.
	* If the learning rate is too large, the cost may oscillate up and down. It may even diverge.
	* A lower cost doesn't mean a better model. You have to check if there is possibly overfitting. It happens when the training accuracy is a lot higher than the test accuracy.
	* In deep learning, we usually recommend that you:
		* Choose the learning rate that better minimizes the cost function.
		* If your model overfits, use other techniques to reduce overfitting.
