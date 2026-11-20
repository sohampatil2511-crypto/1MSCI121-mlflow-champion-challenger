# Champion–Challenger Model Comparison Using Hugging Face and MLflow

**Student Name:** Soham Patil  
**USN:** 1MS25CI121  
**Section:** B

## Project Overview

This project implements a Champion–Challenger approach for comparing two pre-trained sentiment analysis models using Hugging Face and MLflow. The objective is to evaluate model performance, identify the better-performing model, and manage model versions through MLflow Model Registry.

## Technologies Used

- Python
- Hugging Face Transformers
- PyTorch
- MLflow
- Pandas and Scikit-learn

## Models Used

1. DistilBERT – `distilbert-base-uncased-finetuned-sst-2-english`
2. BERT-base – `textattack/bert-base-uncased-SST-2`

Both models were evaluated on 200 balanced SST-2 validation sentences containing positive and negative reviews.

## Methodology

The project evaluates both models using accuracy, precision, recall, Macro-F1 score, and inference latency. MLflow is used to track experiments, compare performance, register model versions, and assign Champion and Challenger aliases.

The selection criteria prioritize Macro-F1 score, with a minimum improvement margin of 0.01 and a maximum allowed latency of five times the existing Champion.

## Results

DistilBERT achieved a Macro-F1 score of 0.8948, while BERT-base achieved 0.9250. Although BERT-base has slightly higher inference latency, it satisfies the predefined latency constraint.

Therefore, BERT-base was selected as the new Champion model, and DistilBERT was retained as the Challenger.

## Conclusion

This project demonstrates model evaluation, experiment tracking, performance comparison, and model registration using MLflow. It provides practical experience in managing machine learning models and selecting the most suitable model based on performance and latency.
