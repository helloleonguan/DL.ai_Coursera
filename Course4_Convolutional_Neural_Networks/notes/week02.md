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
	* you could also download pre-trained parameter values for transfer learning.  
