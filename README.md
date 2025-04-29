# Integrating Regression and LSTM Models for Accurate Stock Price Prediction Using Yahoo Finance Data

## Project Overview

This repository contains the code, data processing steps, and analysis for the MSc Data Science final project titled **"Integrating Regression and LSTM Models for Accurate Stock Price Prediction Using Yahoo Finance Data"**. The project investigates whether a hybrid model combining linear regression and LSTM neural networks can outperform standalone models in forecasting Apple Inc. (AAPL) stock prices.

- **Student Name:** Vishal Ramdayal Garg  
- **Student SRN:** 23020991  
- **Supervisor:** Dr. Martin Bourne  
- **Course:** MSc Data Science, University of Hertfordshire  
- **Module:** 7PAM2002  
- **Submission Date:** 29/04/2025  
- **GitHub:** [Project Repository](https://github.com/vishalgarg99/-IntegratingRegression-and-LSTM-Models-for-Accurate-Stock-Price-Prediction-Using-Yahoo-Finance-Data-.git)

---

## Table of Contents

- [Abstract](#abstract)
- [Project Motivation](#project-motivation)
- [Aims and Objectives](#aims-and-objectives)
- [Data Source and Preprocessing](#data-source-and-preprocessing)
- [Model Architectures](#model-architectures)
- [Evaluation Metrics](#evaluation-metrics)
- [Results Summary](#results-summary)
- [How to Run](#how-to-run)
- [Key Files](#key-files)
- [Ethical Considerations](#ethical-considerations)
- [References](#references)

---

## Abstract

This project examines the performance of a hybrid model integrating linear regression and Long Short-Term Memory (LSTM) neural networks for stock price forecasting, using Apple Inc. (AAPL) historical data from 2015 to 2025. The research question is:  
**"Will a hybrid model integrating regression analysis and LSTM neural networks enhance accuracy in forecasting the stock price over using single methods?"**

Three predictive models were implemented:
- A linear regression model using technical indicators,
- An LSTM model with regularization,
- A hybrid model integrating both approaches.

Comparative analysis demonstrates that the linear regression model achieves an RMSE of \$2.67 and an R² of 0.99, highlighting strong linear relationships in this dataset. The best hybrid model, after architectural improvements, achieved an RMSE of \$4.35 and a MAPE of 1.52%. The results show that while simple linear models can be highly effective for specific stocks and timeframes, properly tuned hybrid architectures can achieve comparable performance with better generalization.

---

## Project Motivation

Stock price forecasting is a critical challenge in financial analysis and machine learning, impacting investment decisions, risk management, and trading strategies. Traditional statistical methods are interpretable but limited in capturing temporal dependencies, while deep learning models like LSTM excel at modeling sequences but may miss immediate market signals. This project aims to leverage the strengths of both approaches for robust and accurate stock price prediction.

---

## Aims and Objectives

- Analyze Apple Inc. (AAPL) historical stock data with exploratory data analysis.
- Develop a linear regression model using technical indicators.
- Implement a deep LSTM model to capture temporal dependencies.
- Design and construct a hybrid model integrating both approaches.
- Evaluate and compare all models using RMSE, MAE, R², and directional accuracy.
- Assess practical utility for trading strategies.
- Analyze strengths and limitations of each approach.

---

## Data Source and Preprocessing

- **Source:** Yahoo Finance (AAPL, 2015–2025)
- **Features:** Open, High, Low, Close, Volume, moving averages (MA5, MA20, MA50), volatility, price/volume changes
- **Preprocessing:**  
  - Imputation of missing values (forward/backward fill)
  - Feature scaling (MinMaxScaler for LSTM)
  - Exploratory data analysis (see Appendix in `FPR.pdf`)

---

## Model Architectures

| Model                | Description                                                                                  |
|----------------------|---------------------------------------------------------------------------------------------|
| Linear Regression    | Uses engineered technical indicators as features. Implemented with scikit-learn.             |
| LSTM Neural Network  | Sequence modeling with LSTM layers. Input: sequences of scaled historical features.          |
| Hybrid Model         | Integrates outputs of linear regression and LSTM before final prediction layer.               |

---

## Evaluation Metrics

- **RMSE (Root Mean Squared Error)**
- **MAE (Mean Absolute Error)**
- **R² (Coefficient of Determination)**
- **MAPE (Mean Absolute Percentage Error)**
- **Directional Accuracy** (up/down prediction correctness)

---

## Results Summary

| Model                | RMSE ($) | R²    | Direction Accuracy (%) |
|----------------------|----------|-------|-----------------------|
| Linear Regression    | 2.67     | 0.99  | 80.3                  |
| LSTM                 | 10.17    | 0.83  | 53.0                  |
| Hybrid (final)       | 4.35     | 0.72  | 50.6                  |

- **Linear Regression**: Strongest overall for this dataset.
- **LSTM**: Captures temporal patterns but underperforms in this case.
- **Hybrid**: After improvements, RMSE and MAPE improved significantly.

See `FPR.pdf` for detailed error analysis, training curves, and visual comparisons.

---

## How to Run

1. **Clone the repository:**
