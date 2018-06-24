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
	* _Hopefully, tune distinctive features of the ML system under each assumption._
	* _Normally, don't consider early stopping because it affects training set and dev set performance at the same time._

### 2. Single Number Evaluation Metric
* To combine Precision & Recall, one can use F1 score. 
![](./img/wk01_F1_score.png)
* The other option is the average. 

### 3. Satisficing and Optimizing metric
* _examples:_ maximise accuracy subject to runningTime <= 100ms
![](./img/wk01_SO_metric.png) 

### 4. Train/Dev/Test Sets
* Randomly shuffle data coming from different distributions into dev/test sets. 
* __Guideline__
![](./img/wk01_set_guideline.png) 
* Splitting Data
![](./img/wk01_splitting_data.png)  
_Depending on the size of the data._
* Size of Test Set
![](./img/wk01_test_size.png)  

### 5. When to change dev/test sets & metrics
* Situation arises when metric + dev performance favors 1 algorithm while the users/company prefers another algorithm. 
![](./img/wk01_metric_change.png)
![](./img/wk01_ortho_metric_change.png)
* If doing well on your metric + dev/test set does not correspond to doing well on your application, change your metric and/or dev & test set. _Example:_ high resolution cat images while training but users upload blurry, distorted cat images. 
