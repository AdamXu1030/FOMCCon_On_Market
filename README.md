# Words That Move the Market: A Textual Analysis of Fed Chair Powell's Press Conferences and Next-Day S&P 500 Reactions

This repository contains the code, data, and final report for the project **"Words That Move the Market: A Textual Analysis of Fed Chair Powell's Press Conferences and Next-Day S&P 500 Reactions."** The project aims to quantify the impact of FOMC speeches on the S&P 500 index using text mining and machine learning.

## Project Overview

The goal of this project is to quantify the relationship between Federal Open Market Committee (FOMC) speeches and subsequent market movements. The analysis combines historical S&P 500 price data with FOMC speech transcripts to classify market responses into four categories: sharp drop, mild drop, mild rise, and sharp rise.

## Key Features

- **Data Collection**: Market data from the Wind Financial Terminal and speech transcripts scraped from the Federal Reserve website.
- **Text Preprocessing**: Tokenization, stopword removal, and TF-IDF vectorization for speech text.
- **Model Building**: Logistic Regression for baseline classification, XGBoost for improved accuracy.
- **Model Interpretation**: SHAP (SHapley Additive exPlanations) for identifying the most influential words in each market class.


## Setup Instructions

1. Clone the repository:
    ```bash
    git clone https://github.com/your-username/FOMC_Market_Analysis.git
    cd FOMC_Market_Analysis
    ```

2. Install the required packages:
    ```bash
    pip install -r requirements.txt
    ```

3. Run the Jupyter notebook:
    ```bash
    jupyter notebook notebooks/FOMC_Market_Analysis.ipynb
    ```

## Key Results

- **Top Predictive Words**:
    - Sharp Rise: "having", "meeting", "question"
    - Sharp Drop: "follow", "potentially", "addition"

- **Model Performance**:
    - XGBoost outperforms logistic regression but struggles with data imbalance.

- **SHAP Insights**:
    - SHAP values provide clear, interpretable insights into the most impactful words for each market class.

## Future Work

- Integrate additional data sources, such as macroeconomic indicators or social media sentiment.
- Apply more advanced NLP models like BERT or GPT for deeper contextual understanding.
- Explore ensemble learning or deep learning for enhanced classification performance.


## Contact

For questions or collaboration, please reach out to **Adam Xu** at tx543@example.com.


