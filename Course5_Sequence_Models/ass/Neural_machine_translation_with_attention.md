## Neural machine translation with attention 

### Objectives 
* You will build a Neural Machine Translation (NMT) model to translate human readable dates ("25th of June, 2009") into machine readable dates ("2009-06-25") 
* You will do this using an attention model, one of the most sophisticated sequence to sequence models.

### Notes  
* Machine translation models can be used to map from one sequence to another. They are useful not just for translating human languages (like French->English) but also for tasks like date format translation.
* An attention mechanism allows a network to focus on the most relevant parts of the input when producing a specific part of the output.
* A network using an attention mechanism can translate from inputs of length  Tx to outputs of length Ty, where  Tx and Ty can be different.
* You can visualize attention weights  α⟨t,t′⟩   to see what the network is paying attention to while generating each output.

### Common Practice 
* Attention Model Details 
![](./img/attn_model.png)  
