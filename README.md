# OneDayLLm: A Simple Character-Level Language Model

This project provides a fundamental introduction to building a character-level language model using a Recurrent Neural Network (RNN) with TensorFlow. It's designed to be a clear and accessible learning resource, demonstrating the core concepts of text generation with neural networks.

## Project Description

This project builds a simple language model that predicts the next character in a sequence based on the preceding characters. It uses a small, self-contained text dataset and a basic LSTM-based RNN to learn character dependencies. The primary goal is to illustrate the fundamental principles of language modeling, including data preprocessing, model architecture, training, and text generation.

We began with a very small text dataset, and built a simple RNN. We then trained the network, and used it to generate text. To improve the model, we then increased the number of epochs to 200, and added a loss plot to visualise the training process.

## Getting Started

1.  **Open the Colab Notebook:** Open the `OneDayLLm.ipynb` notebook in Google Colab.
2.  **Run the Notebook:** Execute the cells sequentially to train the model and generate text.

## Code Explanation

The notebook covers the following key steps:

1.  **Environment Setup:** Imports necessary libraries (TensorFlow and NumPy).
2.  **Data Preparation:**
    * Defines a small text dataset directly within the notebook.
    * Creates a vocabulary of unique characters.
    * Builds character-to-index and index-to-character mappings.
    * Generates input-output sequences of fixed length.
    * One-hot encodes the output characters.
3.  **Model Architecture:**
    * Constructs a sequential model with an LSTM layer and a dense output layer.
    * Compiles the model with categorical cross-entropy loss and the Adam optimizer.
4.  **Training:**
    * Trains the model on the prepared data for 200 epochs, with a batch size of 32.
    * A plot of the loss per epoch is generated.
5.  **Text Generation:**
    * Implements a function to generate text based on a seed sequence.
    * Iteratively predicts the next character using the trained model.

## Results

After training for 200 epochs, the model demonstrates the ability to generate text that resembles the patterns in the training data. The following loss plot illustrates the training progress:

![Loss Plot](https://github.com/user-attachments/assets/ec1e6211-f64b-4de7-b97f-96ce4fe9cc54)

Example generated text (using "The quick " as a seed):

"The quick brown fox jumps over the lazy frg.
A quick brown fox jumps over the lazy frg.
A" 

The results are not flawless but try to play with epochs number to see if it gets better or worse.

## Best Practices Implemented

* **Descriptive Variable Names:** Clear and meaningful variable names enhance code readability.
* **Modular Code:** The text generation logic is encapsulated in a reusable function.
* **Model Summary:** The `model.summary()` function provides a detailed overview of the model architecture.
* **Loss Visualization:** Adding a loss plot allows for visual monitoring of training progress.
* **Clear comments:** comments have been added to the code to explain each step.

## Author

Abdulrahman Aboluhom
