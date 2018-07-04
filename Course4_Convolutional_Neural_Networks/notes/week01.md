# Foundations of Convolutional Neural Networks

## Learning Objectives 
* Understand the convolution operation. 
* Understand the pooling operation. 
* Remember the vocabulary used in convolutional neural network (padding, stride, filter, ...). 
* Build a convolutional neural network for image multi-class classification. 

### 1. Computer Vision 
* computer vision problems 
![](./img/wk01_cv_problems.png) 
* DL challenges on CV
![](./img/wk01_cv_challenge.png)

### 2. Edge Detection Example  
![](./img/wk01_edge_problem.png)  

* computational details (convolution operation `*`) for vertical edge detaction.    
![](./img/wk01_vertical_edge.png)   
![](./img/wk01_vertical_edge2.png) 
![](./img/wk01_vertical_edge3.png)
![](./img/wk01_vertical_edge4.png)  
* different filters  
![](./img/wk01_filters.png)  
![](./img/wk01_filters1.png)  

### 3. Padding 
* issues with previous computation: 
	* pixels at the corners & edges are less frequently used than the ones in the middle. 
	* images shrink as more filters applied. 
* so we introduce the concept of padding around the original image.  
![](./img/wk01_padding.png) 
* valid & same convolutions 
![](./img/wk01_padding2.png) 

### 4. Strided Convolutions
* stride == number of steps when the filter moves horizontally and vertically.  
![](./img/wk01_stride.png) 
* by convention, if the filter is outside the image+padding, then do not perform any convolution operation on that. 
![](./img/wk01_stride2.png)
* note: the convolution operation is actually croass-correlation technically but we just simply call it convolution in ML literature. 

### 5. Convolution Over Volumes 
* the number of channels must match.  
![](./img/wk01_volume.png) 
![](./img/wk01_volume2.png)  
* multiple filters 
![](./img/wk01_volume3.png)

### 6. Convolutional Network 
* an example of a layer
![](./img/wk01_a_layer.png) 
* summary of notation
![](./img/wk01_cnn_notation.png) 
* a deeper ConvNet
![](./img/wk01_conv_net.png) 
* different types of layer in convolutional network:
	* convolution
	* pooling
	* fully connected 

