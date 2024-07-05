# Next-Word-Predictor

## Objective
The goal of this project is to develop a text generation model using TensorFlow and Keras. The model is trained on a dataset containing information about the Data Science Mentorship Program (DSMP 2023) and aims to predict the next word in a sequence given the preceding words. This project demonstrates the use of LSTM (Long Short-Term Memory) networks for sequential data modeling and text generation.

## Methodology

### 1. Data Preprocessing:


Text Tokenization: The input text data is tokenized into words using TensorFlow's Tokenizer class. Each word is assigned a unique integer identifier.

Sequence Generation: The tokenized text is split into sequences where each sequence is an incremental list of tokens from the text.

Padding: All sequences are padded to ensure uniform length, which is necessary for training the LSTM model.


### 2. Model Architecture:


Embedding Layer: An Embedding layer is used to convert the integer tokens into dense vectors of fixed size.

LSTM Layers: Two LSTM layers are stacked. The first LSTM layer is configured to return sequences (return_sequences=True), providing a 3D output which is suitable input for the second LSTM layer.

Dense Layer: A Dense layer with a softmax activation function is used as the output layer to predict the next word in the sequence.


### 3. Training:


Input and Output Preparation: The input sequences (X) and the corresponding next word (y) are prepared. The y labels are one-hot encoded to match the output shape of the Dense layer.

Model Compilation: The model is compiled using the categorical cross-entropy loss function and the Adam optimizer.

Model Training: The model is trained on the prepared sequences using the fit method.


### 4. Evaluation and Prediction:

Model Evaluation: The model’s performance is evaluated using the loss and accuracy metrics.

Text Generation: Given a seed text, the trained model is used to generate the next word iteratively to create a sequence of words.


### 5. Results:

The trained model's predictions are analyzed to evaluate the quality of the generated text. The results demonstrate the model's ability to understand and generate coherent text based on the training data.
