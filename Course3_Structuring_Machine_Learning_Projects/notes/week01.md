# ML Strategy - 1  

## Learning Objectives
* Understand why Machine Learning strategy is important. 
* Apply satisficing and optimizing metrics to set up your goal for ML projects. 
* Choose a correct train/dev/test split of your dataset. 
* Understand how to define human-level performance. 
* Use human-level perform to define your key priorities in ML projects. 
* Take the correct ML Strategic decision based on observations of performances and dataset. 

### 0. Motivation
* When improving a ML system, you might have a lot of ideas/directions. 

### 1. Orthogonalization
* Orthogonal controlling makes it easier to tune things to the way you wanted. 
* Chain of Assumptions in ML  
![](./img/wk01_chain_of_ass.png)  
	* _Hopefully, tune distinctive features of the ML system in under each assumption._
	* _Normally, don't consider early stopping because it affects training set and dev set performance at the same time._
 
