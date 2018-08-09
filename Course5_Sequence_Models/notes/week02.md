# Natural Language Processing & Word Embeddings 

## Learning Objectives 
* Natural language processing with deep learning is an important combination. Using word vector representations and embedding layers you can train recurrent neural networks with outstanding performances in a wide variety of industries. Examples of applications are sentiment analysis, named entity recognition and machine translation.

### 1. Word Representation
* 1-hot representation 
![](./img/wk02_one_hot.png)  
_disadv: treats each word as a thing onto itself and it doesn't allow algorithm to easily generalize across words. No idea how similar between words since the inner product is always 0._  
* Featurized representation: word embedding 
![](./img/wk02_word_embedding.png)  
* 	the feature vector learned might be hard to figure out the exact meaning, but will allow algorithm to determine the similarity between words. 
* visualizing feature vector on lower dimensions  
![](./img/wk02_vis_feature_vector.png)  

### 2. Word embeddings 
* name entity recognition  
![](./img/wk02_name_entity.png)  
* transfer learning for word embeddings 
![](./img/wk02_transfer_word_embeddings.png)  
* related to face encoding  
![](./img/wk02_face_encoding.png)  
_word embedding is mostly for a fixed set of words._  
* word embeddings can help figure out analogies as follows (i.e. analogy reasoning)  
![](./img/wk02_analogy.png)  
![](./img/wk02_analogy2.png)  
_note that sim calculation should be performed on the original multi-dimensional space._  
* common similarity functions 
![](./img/wk02_sim_function.png)  
* embedding matrix 
![](./img/wk02_embedding_matrix.png)  

### 3. Learning Word Embeddings 
* __neural language model: predicting missing words.__ 
![](./img/wk02_NL_model.png)  
![](./img/wk02_NL_model2.png)  
_If you want to build a language model then using last 4 words as context is a good approach. If you want to learn the word embeddings, all contexts suffice._  
* __Word2Vec: constructing context/target pairs within a window for supervised learning.__  
![](./img/wk02_word2vec.png)  
![](./img/wk02_word2vec2.png)  
_disadv: computational expensive when calculating the probability of p(t|c) - the softmax._  
![](./img/wk02_word2vec3.png)  
_when sampling context words, normally use a distribution with heuristics to avoid frequently sampling stopwords._  
* __Negative Sampling: given a pair of words, determine whether this is a pair of context-target (associating) pair as a supervised learning task.__ 
![](./img/wk02_negative_sampling.png)    
	* generating training examples:  
	* a) positive examples: pick a context word and then a target word within some range.
	* b) negative examples: pick the same context word and randomly pick words from the dictionary.  
![](./img/wk02_negative_sampling_model.png)  
* sampling distribution  
![](./img/wk02_sampling_distribution.png)  
_sampling distribution is between uniform and frequency._  
* __GloVe word vectors (global vectors for word representation): couting the number of time word t appears within the context of word c.__  
![](./img/wk02_glove.png)  
_note that depending on the definition of the context, X matrix might be symmetrical diagonally._  
![](./img/wk02_glove2.png)  
_the weighting term function has the following functionalities: a) eliminating 0-count terms, b) giving slightly less weights to stopwords pairs, c) moderating less frequent word pairs._
* axis might not be easily human-interpretable and might not be orthogonal.  
![](./img/wk02_axis.png)  

### 4. Sentiment Classification 
* classifying the emotion of a piece of text.  
![](./img/wk02_sentiment_classification.png)
* challenge: might not have a huge labelled training set. 
* __Simple Sentiment Classification Model__  
![](./img/wk02_simple_sentiment_classification_model.png)  
_disadv: the average function might turn bad reviews into good ones (indicated at the left-bottom corner)._ 
* __RNN for sentiment classification__  
![](./img/wk02_RNN_for_sentiment_classification.png)  

### 5. Debiasing Word Embeddings
* aim: free of all forms of bias (e.g. gender bias).  
![](./img/wk02_bias.png)  
* how to address bias?  
![](./img/wk02_address_bias.png)  


