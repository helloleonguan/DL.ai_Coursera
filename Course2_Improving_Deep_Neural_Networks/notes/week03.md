# Hyperparameter tuning, Batch Normalization and Programming Frameworks

## Learning Objectives 
* Master the process of hyperparameter tuning. 

### 1. Hyperparameter Tuning 
* a list of hyperparameters to consider: 
	* learning rate: alpha
	* momentum term: beta
	* for adam: beta1, beta2, epsilon
	* num of layers 
	* num of hidden units 
	* choice of learning rate decay
	* mini-batch size 
* priorities for those hyperparameters:
![](./img/wk03_priorities_hyperparameters.png)
	* _red_: high
	* _yellow_: medium
	* _purple_: low
* How to find hyperparameter values: 
	* try random value combinations for the hyperparameters in certain ranges (definitely not uniform distribution on real numbers)
	* coarse to find scheme: sample more densely in a particularly promising region
* Pick the scale for hyperparameters 
	* for discrete hyperparameters (uniformly random): 
	![](./img/wk03_discrete_sampling.png)
	* for continuous hyperparameters (on a log scale): 
	![](./img/wk03_log_sampling.png)
	* for beta (on a minus log scale):
	![](./img/wk03_minus_log_sampling.png) 
	
### 2. Organization of Hyperparameter Tuning 
* Babysitting one model: patiently configuring the hyperparameter values as days go by if you do not have enough computational resource. 
* Training many models in parallel if you have many computational power.   
![](./img/wk03_tuning_in_practice.png) 

### 3. 