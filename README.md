# RNN-Based SMS Spam Classification

## Overview

This project implements an **RNN/LSTM-based SMS spam classification model using PyTorch**. The objective is to classify SMS messages into two categories: **Spam** and **Ham**.

The SMS Spam Collection Dataset contains **5,572 classified SMS messages**. SMS classification is treated as a sequence problem because the meaning of text depends on the order and context of words.

## Methodology

The project follows these steps:

1. Dataset loading and exploration
2. Text preprocessing and tokenization
3. 80/20 train-test split
4. Vocabulary construction
5. Sequence preparation with padding and unknown-word handling
6. Embedding layer
7. LSTM model
8. Linear classification layer
9. Model training using BCEWithLogitsLoss and Adam optimizer
10. Final test evaluation
11. Confusion matrix and prediction analysis

The model was trained **from scratch without pretrained models**, using an 80/20 train-test split.

## Model Architecture

**Embedding → LSTM → Linear**

The Embedding layer converts word IDs into learnable vectors. The LSTM processes the word sequence and captures relevant information from previous words. The Linear layer produces the final binary classification output.

## Results

| Metric              |   Accuracy |
| ------------------- | ---------: |
| Hackathon Baseline  |      86.6% |
| Hackathon Target    |        96% |
| Final Test Accuracy | **98.57%** |

The model achieved **98.57% test accuracy**, exceeding both the 86.6% baseline and the 96% target.

## Evaluation

The model was evaluated using the held-out test set. The project also includes:

* Accuracy
* Precision
* Recall
* F1-score
* Confusion matrix
* Training loss curve
* Prediction examples
* Misclassified SMS analysis

## Conclusion

The LSTM model successfully learned patterns from SMS text sequences and achieved **98.57% test accuracy**. This exceeded the hackathon target of 96%, demonstrating that the model was effective for SMS spam classification.

## Project File

* `RNN_Hackathon.ipynb` — Complete implementation, training, evaluation, visualizations, and results.

## How to Run

1. Clone this repository.
2. Open `RNN_Hackathon.ipynb` in Jupyter Notebook or VS Code.
3. Install the required Python libraries.
4. Run the notebook cells from beginning to end.
