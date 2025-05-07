# FOMC Market Analysis - Predicting Market Movements from Fed Speeches

This repository contains the code and report for the project **"FOMC Market Analysis - Predicting Market Movements from Fed Speeches"**, which analyzes the impact of FOMC speech content on S&P 500 market movements using machine learning techniques.

## Project Overview

The goal of this project is to quantify the relationship between Federal Open Market Committee (FOMC) speeches and subsequent market movements. The analysis combines historical S&P 500 price data with FOMC speech transcripts to classify market responses into four categories: sharp drop, mild drop, mild rise, and sharp rise.

### Key Features

- **Data Collection**:
  - Market data from the **Wind Financial Terminal**.
  - Speech transcripts scraped from the **Federal Reserve** website.

- **Text Preprocessing**:
  - Tokenization, stopword removal, and TF-IDF vectorization for speech text.

- **Model Building**:
  - Logistic Regression for baseline classification.
  - XGBoost for improved accuracy and non-linear feature capture.

- **Model Interpretation**:
  - SHAP (SHapley Additive exPlanations) for identifying the most influential words in each market class.

- **Results and Insights**:
  - Analysis of top predictive words for sharp rises and sharp drops.
  - Discussion of model performance, limitations, and future work.

## Directory Structure

📂 FOMC_Market_Analysis/
├── data/
│ ├── SPX.xlsx # S&P 500 market data
│ └── FOMC_Txt/ # Raw FOMC speech transcripts
├── notebooks/
│ └── FOMC_Market_Analysis.ipynb # Jupyter notebook with full analysis
├── src/
│ ├── data_preprocessing.py # Data cleaning and preparation scripts
│ ├── text_vectorization.py # TF-IDF vectorization
│ ├── model_training.py # Logistic Regression and XGBoost training
│ └── shap_analysis.py # SHAP interpretation
├── results/
│ ├── figures/
│ │ ├── shap_class3.png # SHAP summary for sharp rise
│ │ └── shap_class0.png # SHAP summary for sharp drop
│ └── performance_metrics.csv # Model evaluation results
├── report/
│ └── main.tex # Full LaTeX report
└── README.md # Project documentation (this file)


## Setup Instructions

1. Clone the repository:

```bash
git clone https://github.com/your-username/FOMC_Market_Analysis.git
cd FOMC_Market_Analysis


2. Install the required packages:
pip install -r requirements.txt



3. Run the Jupyter notebook:
jupyter notebook notebooks/FOMC_Market_Analysis.ipynb

Key Dependencies

Python 3.11+
numpy
pandas
scikit-learn
xgboost
shap
matplotlib
Key Results

Top Predictive Words:
Sharp Rise: "having", "meeting", "question"
Sharp Drop: "follow", "potentially", "addition"
Model Performance:
XGBoost outperforms logistic regression but struggles with data imbalance.
SHAP Insights:
SHAP values provide clear, interpretable insights into the most impactful words for each market class.
Future Work

Integrate additional data sources, such as macroeconomic indicators or social media sentiment.
Apply more advanced NLP models like BERT or GPT for deeper contextual understanding.
Explore ensemble learning or deep learning for enhanced classification performance.
License

This project is licensed under the MIT License - see the LICENSE file for details.

Contact

For questions or collaboration, please reach out to Adam Xu at tx543@nyu.edu.
