Words That Move the Market: A Textual Analysis of Fed Chair Powell’s Press Conferences and Next-Day S&P 500 Reactions

Overview

This repository contains the code and data for the project "Words That Move the Market: A Textual Analysis of Fed Chair Powell’s Press Conferences and Next-Day S&P 500 Reactions." This project aims to quantify the impact of Federal Open Market Committee (FOMC) speeches on the S&P 500 index, using text mining, machine learning, and interpretability techniques.

Authors

Junwen Fang

Adam Xu

Project Date

May 7, 2025

Project Structure

The repository is organized as follows:

data/ - Contains the S&P 500 market data and FOMC speech transcripts.

notebooks/ - Jupyter notebooks for data processing, text feature engineering, and model training.

src/ - Python scripts for data collection, preprocessing, model training, and SHAP analysis.

results/ - Model outputs, including feature importance scores, SHAP values, and visualizations.

figures/ - Summary plots and other project-related visuals.

README.md - Project documentation (this file).

requirements.txt - Required packages for the project.

Research Questions

How do FOMC speeches impact short-term market movements in the S&P 500 index?

What linguistic patterns in FOMC speeches are most strongly associated with significant market reactions, including sharp rises and sharp drops?

Can machine learning models, such as Logistic Regression and XGBoost, effectively capture the relationship between speech sentiment and subsequent market behavior?

How can SHAP (SHapley Additive exPlanations) analysis provide interpretability for these predictive models, revealing the most influential words for different market movements?

Data Sources

Market Data: S&P 500 market data from the Wind Financial Terminal (2015-2025)

FOMC Speech Data: Scraped directly from the official Federal Reserve website using a custom Python web scraper to ensure data authenticity.

Key Components

1. Data Collection and Preparation

Extracted S&P 500 market data, including date, open, high, low, close, and percentage change.

Scraped and cleaned FOMC speech transcripts from the Federal Reserve’s official website.

Aligned speech dates with corresponding market data to build a comprehensive dataset.

2. Text Feature Engineering

Text Cleaning: Removed non-alphabetic characters, excessive whitespace, and converted text to lowercase.

Tokenization and Stopword Removal: Standardized text for efficient processing.

TF-IDF Vectorization: Captured word importance by calculating term frequency-inverse document frequency scores.

3. Machine Learning Models

Logistic Regression: Baseline text classification model with multi-class support.

XGBoost: High-performance gradient boosting model for improved accuracy.

Model Comparison: Evaluated both models on precision, recall, and F1-score.

4. Model Interpretability (SHAP Analysis)

Calculated SHAP values to identify the most influential words driving market reactions.

Visualized SHAP summary plots to highlight critical features.

5. Results and Discussion

Identified key linguistic drivers of market sentiment, including terms strongly associated with sharp rises and sharp drops.

Discussed challenges like data imbalance and feature sparsity.

6. Conclusion and Future Work

Summarized key insights and potential future directions, including integrating macroeconomic indicators and more advanced NLP models.

Installation

To run the project, clone this repository and install the required packages:

git clone <REPO_URL>
cd <REPO_NAME>
pip install -r requirements.txt

Usage

Run the main analysis notebook:

jupyter notebook notebooks/FOMC_Speech_Analysis.ipynb

Or execute the preprocessing and model training scripts:

python src/data_preprocessing.py
python src/model_training.py

References

Federal Reserve Board. (2025). Federal Open Market Committee (FOMC) Speeches and Statements. Website

Wind Financial Terminal. (2025). S&P 500 Market Data. Website

Pedregosa, F. et al. (2011). Scikit-learn: Machine learning in Python. Journal of Machine Learning Research, 12, 2825-2830.

Lundberg, S. M., Lee, S.-I. (2017). A unified approach to interpreting model predictions. In Advances in Neural Information Processing Systems (pp. 4765-4774).

Mikolov, T. et al. (2013). Efficient estimation of word representations in vector space. arXiv preprint arXiv:1301.3781.

Contact

For questions or collaboration, please reach out to Adam Xu at tx543@nyu.edu.

