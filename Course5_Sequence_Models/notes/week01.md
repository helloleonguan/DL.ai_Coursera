# Recurrent Neural Networks 

## Learning Objectives 
* Learn about recurrent neural networks. This type of model has been proven to perform extremely well on temporal data. It has several variants including LSTMs, GRUs and Bidirectional RNNs, which you are going to learn about in this section. 

### 1. Sequence Models
* examples of sequence data 
![](./img/wk01_sequence_data_examples.png)    

### 2. Sequence Model Notation 
* motivating example: recognise name entities in the passage. 
![](./img/wk01_sequence_model_notation.png)  
_`<t>` means the t-th element in a sequence & `T` means the length of a sequence._
* build a vocabulary to represent words in a mapping  
![](./img/wk01_sequence_model_notation2.png)  
_one-hot representation_

### 3. Recurrent Neural Network Model 
* why a standard neural network did not work well? 
![](./img/wk01_disadv_std_network.png)  
_note that also RNN will reduce the number of parameters in the NN model._  
* a brief look into the RNN:  
![](./img/wk01_RNN_model.png)  
_limitation: only uses information from previous elements in the sequence but not  those subsequent elements._  
* calculations in forward propagation in the RNN model: 
![](./img/wk01_RNN_model2.png)  
![](./img/wk01_RNN_model3.png) 
_W & b parameters are shared in the RNN across different layers._ 
* Backpropagation through time: performs calculations in the opposite directions than forward propagation    
![](./img/wk01_back_prop.png)  
* loss function is similar to binary classification for logistic regression: cross-entropy loss. 

