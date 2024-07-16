# Sentence Reordering with Transformers

This repository contains the implementation of a sentence reordering model using the Transformer architecture, inspired by the "Attention Is All You Need" paper. The notebook documents the process of developing, training, and evaluating the model.

## Table of Contents
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Dataset](#dataset)
- [Notebook Structure](#notebook-structure)
- [Custom Callback](#custom-callback)
- [Cosine Decay Restart](#cosine-decay-restart)
- [Usage](#usage)
- [Results](#results)
- [Conclusion](#conclusion)
- [References](#references)

## Introduction
The goal of this project is to develop a model that can reorder sentences to form coherent paragraphs. This task is crucial for applications such as text summarization and generation. The primary architecture used in this project is the Transformer model, known for its effectiveness in natural language processing tasks.

## Requirements
To run this notebook, you'll need the following packages:
- Python 3.7+
- TensorFlow
- Keras
- NumPy
- Pandas
- Matplotlib
- Scikit-learn

You can install the required packages using the following command:
```bash
pip install tensorflow keras numpy pandas matplotlib scikit-learn
```

## Dataset

The dataset used in this project consists of text data where each instance contains sentences in a shuffled order. The goal is to reorder these sentences to their original, coherent order. The dataset is split into training, validation, and test sets to evaluate the model’s performance effectively.

## Notebook Structure

The notebook is divided into several sections:

1. **Introduction**: An overview of the project and its objectives.
2. **Data Loading and Preprocessing**: Loading the dataset and preprocessing steps, including tokenization and padding.
3. **Model Development**: Implementation of the Transformer model for sentence reordering.
4. **Training and Evaluation**: Training the model and evaluating its performance on the validation set.
5. **Experiments**: Various experiments conducted to fine-tune the model, including different architectures and hyperparameters.
6. **Conclusion**: Summary of the results and final thoughts.

## Custom Callback

A custom validation callback is implemented to monitor the model’s performance in real-time during training. This callback allows for dynamic adjustments and early stopping based on validation performance, helping to prevent overfitting and improve generalization.

## Cosine Decay Restart

The learning rate schedule used in this project is the Cosine Decay with Restarts. This schedule helps in improving the convergence of the model by periodically reducing the learning rate and then increasing it again, which can help the model escape local minima and continue learning effectively.


## Usage

1. Clone this repository:
```bash
git clone https://github.com/your_username/sentence-reordering-transformers.git
```
2. Navigate to the project directory:
```bash
cd sentence-reordering-transformers
```
3. Open the notebook:
```bash
jupyter notebook francesco_baiocchi_Sentence_Reordering.ipynb
```
4. Run the cells in the notebook to execute the code.
   





## Results

The model’s performance is evaluated using a custom validation callback to monitor real-time performance on the validation set. The best model achieved an average score of 0.573 on the test set using 20 milions of lernable parameters.

## Conclusion

After numerous experiments and iterations, the Transformer model demonstrated average performance in the task of sentence reordering. The aim was to diminishing the number of parameters while keeping a good score, i have obtained a score of 0.54 with just 6 millions of parameters.

## References

This project was inspired by the following papers:

- [A Comprehensive Study on Sentence Reordering](https://aclanthology.org/2021.naacl-main.134.pdf)
- [Attention Is All You Need](https://arxiv.org/pdf/1706.03762.pdf)
