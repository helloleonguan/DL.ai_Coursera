# ML Strategy - 2

## Learning Objectives 
* Understand what multi-task learning and transfer learning are. 
* Recognize bias, variance and data-mismatch by looking at the performances of your algorithm on train/dev/test sets. 

### 1. Error Analysis 
* estimating the ceiling on different ideas
![](./img/wk02_ceiling.png)
![](./img/wk02_ceiling2.png) 
* cleaning up incorrectly labeled data
![](./img/wk02_incorrect_labeled.png)
_if it's systematic errors, then it will be an issue for the DL algorithm. e.g. consistently incorrectly label lions as cats._
* if the incorrectly labeled data are in dev set, add another colomn in the error analysis  
![](./img/wk02_incorrect_labeled2.png)
* advice on correcting incorrect samples
![](./img/wk02_advice_on_correcting.png)
* build your first system quickly, then iterate
![](./img/wk02_iterate.png)

### 2. Mismatched training and dev/test set
* Training and Testing on Different Distributions
![](./img/wk02_distribution.png)
![](./img/wk02_distribution2.png)
* Bias and Variance with mismatched data distributions
	* _issues: training data & dev + test data come from different distributions._
	* if the distributions of training data & dev data are different, it's no longer valid to draw conclusions about bias and variance. 
	![](./img/wk02_data_mismatch.png)
	![](./img/wk02_data_mismatch2.png)
	![](./img/wk02_data_mismatch3.png)
* addressing data mismatch - general guideline
![](./img/wk02_addr_data_mismatch.png)
* artificial data synthesis
![](./img/wk02_data_synthesis.png) 

### 3. Trabsfer Learning 
* initialize the weights for the last layer & re-train (_either re-train the last layer if you have a small dataset or the entire NN if you have a large dataset_) the NN on the new dataset. 
![](./img/wk02_transfer_learning.png)  
__Pre-training -> Fine Tuning__  

* Transfer Learning is commonly used from pre-training a large dataset and then move onto a smaller fina tuning dataset. It would not make sense / be meaningful if it's other way around. 
* When makes sense: 
![](./img/wk02_transfer_learning_useful.png)

### 4. Multi-task Learning 
* Simple auto-driving vehicle 
![](./img/wk02_multi_task_example.png)  
* __Good__:Performance is better than training each of the individual NNs. Even if some examples only have partial labels, it still can be trained (only consider label attributes in the loss function).  
![](./img/wk02_multi_task_imple.png)  
_one example can have multiple labels - [0 1 1 0 1].T_
* When makes sense: 
![](./img/wk02_multi_task_useful.png)
* Much less often used. Mostly used in computer vision - object detection. 

### 5. End-to-End Deep Learning
* replace multi-stage systems by a single NN.
* end-to-end approach requires a large amount of data to work well. 
![](./img/wk02_end_to_end_example.png)  
![](./img/wk02_end_to_end_example1.png)  
* end to end approach might not work well in the following example:  
![](./img/wk02_end_to_end_example2.png)
* pros & cons:  
![](./img/wk02_end_to_end_pros_cons.png)
* Applying end-to-end approach
![](./img/wk02_end_to_end_applying.png)
_the second example won't work well with end-to-end deep learning due to its complexity._


## Weekly Bio: Ruslan Salakhutdinov
* Director of Research in Apple
* [Restricted Boltzmann machine](https://en.wikipedia.org/wiki/Restricted_Boltzmann_machine)
* Unsupervised vs. Supervised: unsupervised pre-training models can help supervised learning. 
* Generative models: we haven't quite figure it out.
* How to utilise GPU? 
* Advice on entering DL: 
	* try different & new things; don't be afraid. 
	* code the low-level implementations
* Ph.D vs. Industry:	
	* in academia: you have more freedom;
	* in industry: affect more people; more resources; 
* Exciting frontier: __Deep Reinforcement learning, Reasoning NL understanding, Transfer Learning (on new tasks with small datatset).__
