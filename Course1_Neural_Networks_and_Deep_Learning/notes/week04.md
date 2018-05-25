# Week 4: Deep Neural Network 

## Learning Objectives
* See deep neural networks as successive blocks put one after each other. 
* Build and train a deep L-layer Neural Network. 
* Analyze matrix and vector dimensions to check neural network implementations. 
* Understand how to use a cache to pass information from forward propagation to back propagation.
* Understand the role of hyperparameters in deep learning. 

### 1. Deep L-layer neural network 
* "deep" means many hidden layers. 
* __L__: number of layers.
* __n^[l]__: number of units in layer l.
* __a^[l]__: activations in layer l. 
* notes on notation: 
![](./img/wk04_DNN_notation.png)

### 2. Forward Propagation in DNN
* Forward propagation on DNN: 
![](./img/wk04_FW_notation.png)

### 3. Ensure Matrix Dimensions are right 
* General Rule for 1 example: 
![](./img/wk04_dim_1.png)
* General Rule for multi examples: 
![](./img/wk04_dim_multi.png)

### 4. Why Deep Network works 
* early layers learn the low-level, simple featiures and then they are put together in later layers to compose complex features. 
* __Circuit Theory__: (informally) small L-layer DNN requires shallower NN with _exponentially_ more hidden units to compute. 

### 5. Building Blocks of DNN
* Forward + Backward functions: 
![](./img/wk04_FW_BW_func.png)
* Whole Workflow: 
![](./img/wk04_workflow.png)
* Details of FW propagation function:
![](./img/wk04_FW_details.png)
* Details of BW propagation function: 
![](./img/wk04_BW_details.png) 
* __da^[l]__: is based on the cost function (often it is -y/a+(1-y)/(1-a) ). 

### 6. Parameters & Hyperparameters
* what are parameters & hyperparameters: 
![](./img/wk04_param.png)
* try out diff values for the hyperparameters and see which ones perform the best in terms of the cost function. 

