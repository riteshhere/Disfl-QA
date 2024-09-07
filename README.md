
# Disfluency removal 

The goal of this project is to transform disfluent questions—those containing hesitations, repetitions, and grammatical inconsistencies—into fluent, coherent, and grammatically correct questions using natural language processing (NLP) models. By leveraging pre-trained transformer-based models such as BART and T5, this project explores data analysis, model training, and evaluation, with a focus on improving model performance through data augmentation and fine-tuning.

## DataSet

Disfl-QA consists of ~12k disfluent questions with the following train/dev/test splits.
Dataset can be downloaded from : [Disfl-QA dataset](https://github.com/google-research-datasets/Disfl-QA)

|File                  | Questions |
|----------------------|-----------|
|Questions train.json  |   7182    |
|dev.json              |   1000    |
|test.json             |   3643    |



## Evaluation

Evalautions are based on the BART model fine tuned on Disfl-QA dataset.

| Metric              | Score     |
|---------------------|-----------|
| ROUGE-1             | 0.953951  |
| ROUGE-2             | 0.911474  |
| ROUGE-L             | 0.943273  |
| BLEU                | 0.853771  |
| METEOR              | 0.932146  |
| BERTScore Precision | 0.98963   |
| BERTScore Recall    | 0.987921  |
| BERTScore F1        | 0.988741  |

## Directory Structure
--------------------------------------
The directory structure below outlines how the project is organized and what each file and folder contains:

├── Final_model/  
│   ├── BART_Predication.csv         # Prediction on test set based on the selected model  
│   ├── Training_Arguments.csv       # training arguments for replicating the results
├── augmented_dataset/  
│   ├── DataAugmentation.ipynb       # Using data augmentation to increase the dataset  
│   ├── test_augmeneted.csv          # Test dataset after adding augmented data  
│   ├── train_augmeneted.csv         # Train dataset after adding augmented data  
│   └── val_augmeneted.csv           # Validation dataset after adding augmented data  
├── experimentations/  
│   ├── Disfl-qa.ipynb               # Experimentation on T5 and BART fine-tuning  
│   ├── Analysis_and_evaluation.ipynb # Analysis and evaluation of dataset and prediction  
├── README.md                        # Project overview and instructions for setup and usage  
├── report.pdf                       # Report on the project (fine-tuning, evaluation, and analysis)  
├── .gitignore                       # Specifies files and directories ignored by Git  
└── LICENSE                          # License file for the project  

