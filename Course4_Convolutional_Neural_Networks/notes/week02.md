# Deep convolutional models: case studies

## Learning Objectives 
* Understand multiple foundational papers of convolutional neural networks. 
* Analyze the dimensionality reduction of a volume in a very deep network. 
* Understand and Implement a Residual network
Build a deep neural network using Keras. 
* Implement a skip-connection in your network. 
* Clone a repository from github and use transfer learning. 

### 1. Classic Networks  
#### a) LeNet-5: identify hand-written digits on greyscale images  
![](./img/wk02_lenet_5.png)   

#### b) AlexNet: Large Scale Visual Recognition  
![](./img/wk02_alexnet.png)  

#### c) VGG - 16: Large Scale Visual Recognition  
![](./img/wk02_vgg_16.png)  

### 2. Residual Network 
* __Residual Block:__  
![](./img/wk02_resnet.png)  
![](./img/wk02_resnet2.png)  
* Why ResNet so well? 
	* ReLU = _/ to get back the original `a^[l]`.
	* identity function is easy for residual block to learn.   
	![](./img/wk02_resnet3.png)
	_Note that if the dimensions of Res Layer are not consistent, you could add another W matrix to adjust it._  
	![](./img/wk02_resnet4.png)   
	
### 3. Inception Neural Network 
* __1 x 1 convolution:__  
![](./img/wk02_1x1.png)  
![](./img/wk02_1x1_2.png)  
* __Inception Layer:__ perform all the operations you want altogether, though computational cost is high. 
![](./img/wk02_inception.png)  
* computational cost
![](./img/wk02_inception_comp_cost.png)  
* use a 1x1 convolution to reduce the computational cost 
![](./img/wk02_1x1_3.png)  
_It won't hurt the performance of the neural network._
* __inception network__
![](./img/wk02_inception2.png)  
![](./img/wk02_inception3.png)  
_Notice that there are some side-branches. Those are used for making early predictions in hidden layers._ 

### 4. Practical Advice on ConvNets
* using open-source implementation: 
	* look for online open-source implementation of a particular research paper. 
	* mostly on Github.  
* you could also download pre-trained parameter values for transfer learning (usually as intialization values).
* For a small dataset: 
![](./img/wk02_transfer_learning.png)  
_Note: a) freeze: do not train early parameters and only train the last few layers. b) save to disk: compute the previous layers result Z-n and save it to disk for re-use of multiple epochs._  
* For a large dataset (train more layer at the end):  
![](./img/wk02_transfer_learning2.png)  
* For an even larger dataset (use the parameters online as initialization): 
![](./img/wk02_transfer_learning3.png)  
* Data Augmentation (most CV projects need a lot of data): 
	* Mirroring 
	* Random Cropping 
	* Rotation 
	* Shearing 
	* Local warping   
	![](./img/wk02_data_augmentation.png) 
	* color shifting  
	![](./img/wk02_data_augmentation2.png)  
* run distortions in parallel with training. 
![](./img/wk02_data_augmentation3.png)  

### 5. State of Computer Vision 
* hand-engineering   
![](./img/wk02_cv_state.png)  
* benchmarks & competitions  
![](./img/wk02_cv_state2.png)   
* open-source code 
![](./img/wk02_cv_state3.png)  



 
