## Trigger Word Detection 

### Objectives 
* Structure a speech recognition project. 
* Synthesize and process audio recordings to create train/dev datasets. 
* Train a trigger word detection model and make predictions. 

### Notes 
* Data synthesis is an effective way to create a large training set for speech problems, specifically trigger word detection.
* Using a spectrogram and optionally a 1D conv layer is a common pre-processing step prior to passing audio data to an RNN, GRU or LSTM.
* An end-to-end deep learning approach can be used to built a very effective trigger word detection system.

### Common Practice 