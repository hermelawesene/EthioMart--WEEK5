# Amharic Telegram E-commerce NER Project
========================================

## Table of Contents
1. [Overview](#overview)
2. [Introduction](#introduction)
3. [Dataset](#dataset)
4. [Methodology](#methodology)
5. [Model Details](#model-details)
6. [Evaluation Metrics](#evaluation-metrics)
7. [Installation and Usage](#installation-and-usage)
8. [Results](#results)
9. [Challenges and Future Work](#challenges-and-future-work)
10. [Acknowledgments](#acknowledgments)
11. [License](#license)

---

## Overview
The **Amharic Telegram E-commerce NER** project aims to develop a Named Entity Recognition (NER) system that extracts important business-related entities, such as product names, prices, and locations, from Amharic text data. The primary goal is to facilitate efficient extraction of relevant information from messages shared in Telegram e-commerce groups in Ethiopia.

---

## Introduction
The rise of e-commerce in Ethiopia, particularly on platforms like **Telegram**, has created a need for automated solutions to extract and organize key information from messages. Telegram channels such as [@nejashimarketingcenter](https://t.me/nejashimarketingcenter) contain thousands of messages about products and services, but finding specific details such as **product names**, **prices**, and **locations** can be time-consuming.

This project addresses this problem by developing a **Named Entity Recognition (NER)** system using **Amharic** text data. Our approach uses the **XLM-Roberta** model, a multilingual transformer-based model, to identify and extract critical business entities from Amharic Telegram messages. 

---

## Dataset
The dataset used in this project was collected from various **Telegram e-commerce channels**. Specifically, we scraped **6,268 messages** from channels such as [@nejashimarketingcenter](https://t.me/nejashimarketingcenter).

### Key Details:
- **Language**: Amharic
- **Format**: Text data converted to **CoNLL format** for NER tasks
- **Size**: Over **6500 messages** were labeled, focusing on entities like **product names**, **prices**, and **locations**.

### Entity Types:
1. **Product Names** – Extracting names of the items being sold.
2. **Prices** – Identifying the cost or price of the items.
3. **Locations** – Identifying geographical locations where the products are available or sold.

---

## Methodology
The project follows a structured pipeline that involves several stages:

1. **Data Collection**: Scraping text data from Telegram channels using Python-based web scraping tools.
2. **Preprocessing**: Cleaning the scraped text data, tokenizing Amharic text, and converting it into a format suitable for NER tasks (CoNLL format).
3. **Data Labeling**: Manual annotation of the dataset for training, validation, and testing, focusing on the relevant entities.
4. **Model Training**: Fine-tuning the **XLM-Roberta** model for the specific task of NER.
5. **Evaluation**: Evaluating model performance using standard metrics such as **Accuracy**, **Precision**, **Recall**, and **F1-score**.
6. **Model Interpretability**: Understanding model decisions using explainability tools.

---

## Model Details

### Model Architecture
We leveraged **XLM-Roberta**, a transformer-based multilingual model, pre-trained on 100 languages, including Amharic. This model is ideal for handling low-resource languages like Amharic due to its multilingual capabilities.

### Task: Named Entity Recognition (NER)
The NER task involved training the model to recognize and categorize entities from text into one of the following categories:
- **Products**
- **Prices**
- **Locations**

### Training Data
- **Input**: Text data in **CoNLL format** with labeled entities.
- **Output**: Tagged entities in the categories of interest.

---

## Evaluation Metrics

The model's performance was measured using the following metrics:

- **Accuracy**: The ratio of correctly predicted entities to the total number of entities.
- **Precision**: The proportion of predicted entities that were correctly identified.
- **Recall**: The proportion of actual entities that were correctly identified by the model.
- **F1-score**: The harmonic mean of Precision and Recall, providing a balanced measure of the model’s performance.

**Final Scores**:
- **Accuracy**: 100%
- **Precision**: 1.00
- **Recall**: 1.00
- **F1-score**: 1.00

---

## Installation and Usage

1. **Clone the Repository**:
    ```shell
    git clone https://github.com/hermelawesene/EthioMart--WEEK5.git
    ```

2. **Install the Required Libraries**:
    ```shell
    pip install -r requirements.txt
    ```

3. **Train the Model**:
    ```shell
    jupyter notebook FineTunning_model_evaluation.ipynb
    ```

---

## Results
The NER model performed exceptionally well on the task of identifying products, prices, and locations from Amharic e-commerce messages.

Evaluation Metrics:
- **Accuracy**: 100%
- **Precision**: 1.00
- **Recall**: 1.00
- **F1-score**: 1.00

---

## Challenges and Future Work

1. **Handling Out-of-Vocabulary (OOV) Words**: While the model performs well on known terms, it may struggle with new or unseen words.
2. **Multimodal NER**: Future improvements include expanding the model to handle images and documents.
3. **Domain Adaptation**: Further exploration can adapt this model for other sectors like healthcare or finance.

---

## Acknowledgments

Special thanks to the **Kifiya aim Team**, including:
- **Elias**
- **Kerod**
- **Mahlet**
- **Rediet**

---

## License
This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
