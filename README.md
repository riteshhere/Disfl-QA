
# Disfluency removal 

The goal of this project is to transform disfluent questions—those containing hesitations, repetitions, and grammatical inconsistencies—into fluent, coherent, and grammatically correct questions using natural language processing (NLP) models. By leveraging pre-trained transformer-based models such as BART and T5, this project explores data analysis, model training, and evaluation, with a focus on improving model performance through data augmentation and fine-tuning.

## DataSet
-------------------
Disfl-QA consists of ~12k disfluent questions with the following train/dev/test splits:
|File                  | Questions |
|----------------------|-----------|
|Questions train.json  |   7182    |
|dev.json              |   1000    |
|test.json             |   3643    |



## Evaluation
-------------------------------------------
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
├── Final_model/
│   ├── BART_Predication.csv     # Prediction on test set based on the selected model
│   ├── Training_Arguments.csv   # Main model-building script
│
├── augemented_dataset/
│   ├── DataAugmentation.ipynb   # Using data augemneation to increase the dataset
│   ├── test_augmeneted.csv      # Test dataset after adding augmented data
│   ├── train_augmeneted.csv     # Train dataset after adding augmented data
│   └── val_augmeneted.csv       # val dataset after adding augmented data

│
├── experimentations/
│   ├── Disfl-qa.ipynb                # Experimentation on T5 and BART fine tuning
│   └── Analysis_and_evalaution.ipynb # Analysis and eval of dataset and prediction 
│
├── README.md                    # Project overview and instructions for setup and usage
├── report.pdf                   # report on the projects(fine tuning, evaluation and analysis)
├── .gitignore                   # Specifies files and directories ignored by git
└── LICENSE                      # License file for the project
