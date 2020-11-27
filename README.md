# TV_Script_Generation--Udacity

Deep learning Course Project 3 : Build a neural network to generate the next scene in a TV script. Using recurrent neural networks.

### Introduction
In this project, you'll generate your own Seinfeld TV scripts using RNNs. You'll be using a Seinfeld dataset of scripts from 9 seasons. The Neural Network you'll build will generate a new, "fake" TV script.

### Getting the project files
The project files can be found in our public [GitHub repo](https://github.com/udacity/deep-learning-v2-pytorch), in the project-tv-script-generation folder. You can download the files from there, but it's better to clone the repository to your computer using: git clone https://github.com/udacity/deep-learning-v2-pytorch.git
This way you can stay up to date with any changes we make by pulling the changes to your local repository with git pull.

### Submission
Process Step | Criteria
------------ | -------------
Pre-processing Data | The function create_lookup_tables create two dictionaries:
. | Dictionary to go from the words to an id, we'll call vocab_to_int
. | Dictionary to go from the id to word, we'll call int_to_vocab
. | The function create_lookup_tables return these dictionaries as a tuple (vocab_to_int, int_to_vocab)
. | The function token_lookup returns a dict that can correctly tokenizes the provided symbols.
Batching Data | The function batch_data breaks up word id's into the appropriate sequence lengths, such that only complete sequence lengths are constructed.
. | In the function batch_data, data is converted into Tensors and formatted with TensorDataset.
. | Finally, batch_data returns a DataLoader for the batched training data.
Build the RNN | The RNN class has complete __init__, forward , and init_hidden functions.
. | The RNN includes at least one LSTM (or GRU) and fully-connected layer.
. | The RNN must include an LSTM or GRU and at least one fully-connected layer. The LSTM/GRU should be correctly initialized, where relevant.
RNN Training | Enough epochs to get near a minimum in the training loss, no real upper limit on this. Just need to make sure the training loss is low and not improving much with more training.
. | Batch size is large enough to train efficiently, but small enough to fit the data in memory. No real “best” value here, depends on GPU memory usually.
. | Embedding dimension, significantly smaller than the size of the vocabulary, if you choose to use word embeddings
. | Hidden dimension (number of units in the hidden layers of the RNN) is large enough to fit the data well. Again, no real “best” value.
. | n_layers (number of layers in a GRU/LSTM) is between 1-3.
. | The sequence length (seq_length) here should be about the size of the length of sentences you want to look at before you generate the next word.
. | The learning rate shouldn’t be too large because the training algorithm won’t converge. But needs to be large enough that training doesn’t take forever.
. | The printed loss should decrease during training. The loss should reach a value lower than 3.5.
. | There is a provided answer that justifies choices about model size, sequence length, and other parameters.



### Advanced Projects
After completing this project, try applying what you learned to one of these problems.

Generate your own Bach music using like [DeepBach](https://arxiv.org/pdf/1612.01010.pdf).
Predict seizures in intracranial EEG recordings on [Kaggle](https://www.kaggle.com/c/seizure-prediction).
