# CharacterLevel_LanguageModeling_RNN
Character-level language modeling with LSTMs trained on old-English "Tragedy of Hamlet"

* TensorFlow version: 2.0.0-alpha
* Training data: "Tragedy of Hamlet" https://www.gutenberg.org/cache/epub/1787/pg1787.txt
* 1 custom layer converting the input uint8 type data into one-hot float32 type categorical data
* 1 LSTM layer with 1024 units with Stateful = True 
* 1 Dense layer with the number of units equal to the number of unique characters
* Number of time steps/Sequence Length: 100  
* Dropout: 0      
* Categorical Cross Entropy Loss function    
* Adam Optimizer(learning rate: .001)
* Batch size: 64
* Epochs: 100
* Categorical accuracy: 99.95%
* Prediction Function 1 uses tf.argmax for the next character
* Prediction Function 2 uses tf.random.categorical for the next character following the tensorflow "Text Generation" example
# Just change the input file to train any text
