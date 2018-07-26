# Special applications: Face recognition & Neural style transfer 

## Learning Objectives 
* Discover how CNNs can be applied to multiple fields, including art generation and face recognition. Implement your own algorithm to generate art and recognize faces!

### 1. Face Recognition 
* face verification vs. face recognition
![](./img/wk04_face_verification_and_recognition.png)  
* __One-shot Learning__: predicting from 1 person's image/face. 
![](./img/wk04_one_shot.png) 
* challenges: 
	* a) training set is extremely small
	* b) not very extendable
* __similarity function__  
![](./img/wk04_similarity_function.png) 

### 2. Siamese Network 
* feed both pictures to the same neural network and produce the final "feature vector" (i.e. the encoding of the input image)  
![](./img/wk04_siamese_network.png)  
* training:  
![](./img/wk04_siamese_network2.png) 
* triplet loss function: 
	* you will need 3 images: anchor, positive, negative  
	![](./img/wk04_triplet_loss.png) 
	* definition of triplet loss: 
	![](./img/wk04_triplet_loss2.png)  
* choosing the triplets 
![](./img/wk04_triplet_loss3.png)  

### 3. Face Verification and Binary Classification
* uses siamese netwrok on 2 images (i.e. pairs) and add a logitsic unit at the end to predict 0/1. 
![](./img/wk04_sim_bin_classification.png)  
![](./img/wk04_sim_bin_classification2.png)  
* pre-compute the encodings of images in the database for prediction 

### 4. What are deep ConvNets learning? 
* as the neural network goes deeper, neurons tend to learn more complex patterns. 
![](./img/wk04_visualizing_learning.png)  
![](./img/wk04_visualizing_learning2.png)  

### 5. Neural Style Transfer 
* examples:  
![](./img/wk04_neural_style.png) 
[A neural Algorithm of Artistic Style](./A neural_Algorithm_of_Artistic_Style.pdf)  
* __cost function__  
![](./img/wk04_style_transfer_cost.png) 
	* content cost function  
	![](./img/wk04_style_transfer_content_cost.png)  
	_note that `l` is chosen to be neither too small nor too big._
	* style cost function  
	![](./img/wk04_style_transfer_style_cost.png) 
	![](./img/wk04_style_transfer_style_cost2.png)
	_patterns across different channels_
	![](./img/wk04_style_transfer_style_cost3.png)  
	_go from 1 layer to multiple layers_
	![](./img/wk04_style_transfer_style_cost4.png)  
	_gram matrix_
* __learning__  
![](./img/wk04_style_transfer_learning.png)  

### 6. 1D & 3D Generalizations
* 1D generalization
![](./img/wk04_1D_generalization.png)  
* 3D generalization  
![](./img/wk04_3D_generalization.png)  

