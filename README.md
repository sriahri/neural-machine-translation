# Neural Machine Translation
In Machine Translation, our goal is to convert a sentence from the source language to the target language. We will implement a sequence-to-sequence  network with attention, to build a Neural Machine Translation (NMT) system.
We will implement a sequence-to-sequence
 (Seq2Seq) network with attention, to build a Neural Machine Translation (NMT) system. In this section,
 we describe the training procedure for the proposed NMT system, which uses a Bidirectional LSTM
 Encoder and a Unidirectional LSTM Decoder.

## Model Architecture
Encoder: The encoder is a Bidirectional LSTM that processes the input sentence from both directions (forward and backward) to capture context. It generates hidden states and cell states for each word in the input sentence.

Decoder: The decoder is a Unidirectional LSTM that generates the translated sentence one word at a time. It uses the final hidden and cell states from the encoder as its initial states.

## Training Procedure
Embedding: The input sentence is converted into embeddings, which are then fed into the encoder.

Convolutional Layer: The embeddings are passed through a convolutional layer to maintain their shapes.

Encoder: The encoder processes the embeddings to produce hidden and cell states.

Decoder Initialization: The decoder’s initial hidden and cell states are set using a linear projection of the encoder’s final states.

Decoder: At each step, the decoder generates a word in the target language using the attention mechanism to focus on relevant parts of the input sentence.

Loss Calculation: The model’s output is compared to the target sentence using cross-entropy loss, and the model parameters are updated to minimize this loss.

## Implementation Steps
Padding: Sentences in a batch are padded to the same length to apply tensor operations.

Embedding Initialization: Source and target embeddings are initialized.

Model Layers Initialization: LSTM, CNN, projection, and dropout layers are initialized.

Encoding and Decoding: Functions to encode the input sentence and decode the target sentence are implemented.

Attention Computation: The attention scores, distribution, and output are computed during decoding.

## Practical Considerations
Google Colab Setup: Instructions for running the assignment in Google Colab, including mounting Google Drive, enabling GPU, and best practices for GPU usage.

Training and Testing: Steps to train the model, monitor training using TensorBoard, and test the model to report its performance.

All the details about the mathematical computations are provided in the ([Assignment_4.pdf](https://github.com/sriahri/neural-machine-translation/blob/main/Assignment_4.pdf)).

