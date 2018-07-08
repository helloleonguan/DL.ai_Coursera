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

### 7. Pooling Layers
* max pooling (it's a fixed computation, no parameter to learn)
![](./img/wk01_max_pooling.png)  
![](./img/wk01_max_pooling2.png)  
* average pooling 
![](./img/wk01_avg_pooling.png)  
* pooling applies to each of the channel individually. 
* max pooling is more common than average pooling in practice. 
* hyperparameters of pooling
![](./img/wk01_pooling_hyperparam.png)  

### 8. A CNN Example 
* usually, we only  count the layers with parameters to learn to be the total number of layers in a CNN. 
* __Fully Connected Layer__: it's just similar to a regular layer you would see in neural network with weights & bias to learn. 
* example: similar to [LeNet-5](http://yann.lecun.com/exdb/lenet/)  
![](./img/wk01_lenet5_eg.png)  
![](./img/wk01_lenet5_eg2.png)  
* __When calculating the number of parameters for a Conv layer with 1 filter, it should be fw[l] * fh[l] * nc[l-1] + 1. While, for multiple filters, it would then be (fw[l] * fh[l] * nc[l-1] + 1) * nc[l].__   
* _Notice that the number of parameters in this table are mostly are incorrect. The last 3 should be:_  
`FC3: 120 * 400 (W matrix) + 120 (bias) = 48,120`
`FC4: 84 * 120 (W matrix) + 84 (bias) = 10,164` 
`Softmax: 10 * 84 (W matrix) + 10 (bias) = 850`

### 9. Why to use convolution
* ConvNet generally have way fewer parameters to learn. 
* __advantages of ConvNet:__
	* parameter sharing  
	* sparsity of connections  
![](./img/wk01_adv_cnn.png)  
* It's common to use other researchers' well-tested architecture to the problem you have at hand. 

## Weekly Bio: Yann LeCun
* [OPTIMAL PERCEPTUAL INFERENCE](https://papers.cnl.salk.edu/PDFs/Optimal%20Perceptual%20Inference%201983-646.pdf)
* [Conditional random field](https://en.wikipedia.org/wiki/Conditional_random_field) 
* [DjVu](https://en.wikipedia.org/wiki/DjVu)
* Advice for entering AI: 
	* learn from the Internet 
	* make yourself valuable
	* contribute to the open source community 