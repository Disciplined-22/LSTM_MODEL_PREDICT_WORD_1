# Text Generation using LSTM
## Overview
This project focuses on leveraging Long Short-Term Memory (LSTM) networks to generate coherent and contextually relevant text. The model is trained on a dataset containing the writings of Jim Rohn. The project is divided into several sections: data preprocessing, model development, and text generation.

## Sections
### 1. Data Preprocessing
The dataset, sourced from the writings of Jim Rohn, is tokenized and converted to lowercase. The Tokenizer class from Keras is utilized to prepare the text for use in neural network models. The total number of unique words in the corpus is determined, and the word index provides a dictionary of words and their assigned indices.

### 2. Sequence Generation
Input sequences are generated by creating n-gram sequences from the tokenized data. These sequences are then padded to ensure uniform length. The predictors and labels are extracted from the input sequences, with labels further converted to one-hot encoding to facilitate model training.

### 3. Model Development
In this section, a sequential model is constructed using the Keras library to facilitate text generation. The architecture comprises an Embedding layer, a unidirectional LSTM layer with 200 units, and a Dense output layer with softmax activation. The model is compiled using the Adam optimizer with a learning rate of 0.01, and categorical crossentropy is employed as the loss function. The training process spans 100 epochs, during which accuracy is monitored.

![Screenshot (1917)](https://github.com/Disciplined-22/LSTM_MODEL_PREDICT_WORD_1/assets/129745308/4164e1f1-5643-4885-9f42-7077dce06299)


Note: The architecture can be customized and fine-tuned for optimal performance. In this particular scenario, a unidirectional LSTM has been chosen for its effectiveness in capturing sequential dependencies. Depending on the nature of the data and specific requirements, the use of Bidirectional LSTMs or adjustments to the number of units may further enhance the model's capabilities.

### 4. Text Generation
The trained model is used to generate text based on an initial seed phrase. The provided seed text, "History is the proof the more you give," is used to predict the next 10 words in the sequence. The generated text showcases the model's ability to continue a coherent thought based on the training data.

## Usage
Ensure the necessary libraries are installed using pip install -r requirements.txt.
Execute the provided Jupyter notebook or run the Python script to train the model.
Modify the seed text in the text generation section to experiment with different starting points.
Explore the generated text to observe the model's ability to extend the given context.
Results
The model demonstrates the potential of LSTM networks in capturing patterns and generating contextually relevant text. Further experimentation with hyperparameters and model architecture could enhance performance.

## Future Improvements
1. Fine-tune hyperparameters for better model convergence.
2. Experiment with different LSTM architectures, such as Bidirectional LSTMs.
3. Implement regularization techniques to prevent overfitting.
4. Evaluate performance on a diverse range of texts to enhance generalization.


