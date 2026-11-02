# Machine Learning Fundamentals: Two Regression Projects

Two beginner-friendly regression projects in Python and Scikit-Learn, built while working through Chapter 1 (*The Machine Learning Landscape*) of *Hands-On Machine Learning with Scikit-Learn, Keras & TensorFlow* (3rd ed., Aurélien Géron).

## 🎯 Goal of this repository

To learn and demonstrate the **complete basic workflow of Machine Learning** — from raw data to a tested model — and the **most important pitfalls** every ML practitioner must understand: non-representative data, overfitting, and how regularization helps.

The two projects build on each other:

1. **[Life satisfaction](life-satisfaction-prediction/)** — a guided walkthrough of the book's introductory example, to understand the concepts step by step.
2. **[Car fuel consumption](car-fuel-consumption-prediction/)** — the same concepts applied to **my own question and current real-world data** (all 2026 car models), with a proper train/test evaluation and my own experiments.

## ✅ Overview of results

| | [Car fuel consumption](car-fuel-consumption-prediction/) | [Life satisfaction](life-satisfaction-prediction/) |
|---|---|---|
| **Question** | How much fuel (L/100 km) does a new car need, given its engine size? | Does a country's GDP per capita predict its people's life satisfaction? |
| **Data** | 613 car models (2026) + 10,060 (2015–2024), Natural Resources Canada | 36 countries, OECD + World Bank (2020) |
| **Models** | Linear Regression, k-NN (k = 5), Polynomial, Ridge | Linear Regression, k-NN (k = 3), Polynomial, Ridge |
| **Main result** | Test error of **1.18 L/100 km** (k-NN) on unseen cars | Prediction for Cyprus: **6.3 / 10** (both models agree) |
| **Key experiment** | Ridge cuts the test error of an overfitting model from **9.22 to 1.42** | Adding missing countries makes the trend **3× flatter** |

![Overfitting vs. regularization](car-fuel-consumption-prediction/images/06_regularization.png)

## 🧠 Concepts covered

| Concept | Where |
|---|---|
| Supervised learning, regression | both |
| Model-based (Linear Regression) vs. instance-based learning (k-NN) | both |
| Training set vs. test set, Mean Absolute Error (MAE) | car project |
| Non-representative training data | both (hybrid cars / missing countries) |
| Overfitting | both |
| Regularization (Ridge) | both |
| Combining datasets, trend analysis | car project |

## 📁 Repository structure

```
├── car-fuel-consumption-prediction/   # Project 1: own question and dataset
│   ├── fuel_consumption_prediction.ipynb
│   ├── data/
│   └── images/
├── life-satisfaction-prediction/      # Project 2: walkthrough of the book's example
│   ├── life_satisfaction_prediction.ipynb
│   └── images/
├── requirements.txt                   # shared Python packages
└── README.md
```

Each project folder has its own README with goal, approach, results and limitations.

## ▶️ Setup

```bash
git clone https://github.com/AT3060/car-fuel-consumption-prediction---life-satisfaction-prediction.git
cd car-fuel-consumption-prediction---life-satisfaction-prediction
pip install -r requirements.txt
jupyter notebook
```

## 🧰 Tools

Python · pandas · NumPy · Matplotlib · Scikit-Learn · Jupyter · Git
