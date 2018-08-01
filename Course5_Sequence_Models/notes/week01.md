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

### 4. Different RNN Architectures 
* the reason why we need different types of RNNs due to the fact that Tx might not be equal to Ty. 
* __different types of RNN__
	* many-to-many (Tx = Ty)  
	![](./img/wk01_many_to_many.png)  
	* many-to-many (Tx != Ty)  
	![](./img/wk01_many_to_many2.png)  
	* many-to-one  
	![](./img/wk01_many_to_one.png)  
	* one-to-many  
	![](./img/wk01_one_to_many.png)  
	* one-to-one 
	![](./img/wk01_one_to_one.png)  
* summary of RNN types 
![](./img/wk01_RNN_types.png)  

### 5. Language Model and Sequence Generation 
* speech recognition: find the probability of that sentence out there.  
![](./img/wk01_speech_recognition.png)  
* Modelling an RNN
![](./img/wk01_language_model.png)  
![](./img/wk01_language_model2.png)  

### 6. Sampling Novel Sequences 
* sampling from y_hat prediction distributions and feeding it to the next node in the sequence. 
![](./img/wk01_sampling.png)  
* you could also build a character-level model  
![](./img/wk01_sampling2.png)  
_adv: handle Unknown words; disavd: much longer sequences, computational expensive, unable to capture sentence semantics._ 
* examples of sequence generation 
![](./img/wk01_sequence_generation.png)  

### 7. Vanishing Gradients with RNNs 
* challenge: language could potentially have long-term dependencies but RNN are not good at capturing this relation.  
![](./img/wk01_vanishing_gradients.png)  
_exploding gradients is handled by gradient clipping (i.e. rescaling some layers' gradients)._  
