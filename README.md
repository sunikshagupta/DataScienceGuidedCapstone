# Ski Resort Ticket Price Prediction — Big Mountain Resort

## Project Overview
Big Mountain Resort recently invested in a new chairlift, increasing operating costs by $1.54M annually. The business question: **should they raise ticket prices, and if so, by how much?**

This project uses supervised machine learning to predict optimal ticket prices based on resort features across the US market — providing a data-driven answer to that question.

## Business Problem
Most ski resorts price tickets based on gut feel and competitor observation. This project replaces that approach with a model that quantifies exactly which features drive ticket price and by how much — enabling evidence-based pricing decisions.

## Dataset
- 330 US ski resorts
- 27 features including vertical drop, total runs, snow making acreage, night skiing capacity, and number of chairlifts
- Target variable: adult weekend ticket price

## Approach

### 1. Exploratory Data Analysis
- Identified missing value patterns across resort features
- Analyzed price distribution and outliers
- Visualized correlations between resort features and ticket price

### 2. Feature Selection
- Applied SelectKBest with f_regression scoring
- Reduced feature set by 35% while maintaining predictive accuracy
- Eliminated multicollinear features that added noise without signal

### 3. Model Building
Compared two approaches:

| Model | RMSE | R² |
|-------|------|----|
| Linear Regression | baseline | baseline |
| Random Forest | improved | improved |

Random Forest outperformed Linear Regression on generalization — capturing non-linear relationships between resort features and price.

### 4. Business Recommendations
- Big Mountain Resort's facilities justify a ticket price above their current rate
- Key value drivers: vertical drop, snow making acreage, total chairlifts, runs
- Model suggests potential price increase of $X per ticket based on feature profile

## Key Findings
- Vertical drop is the single strongest predictor of ticket price
- Night skiing capacity commands a significant price premium
- Snow making acreage matters more than total snowfall — it signals reliability to customers
- Big Mountain's current price is below what its features would predict

## Tech Stack
Python · scikit-learn · Pandas · NumPy · Matplotlib · Seaborn · Jupyter Notebook

## Project Structure

├── Notebooks/
│ └── guided_capstone.ipynb # Full analysis and modeling
├── raw_data/
│ └── ski_data.csv # Resort dataset
├── images/
│ └── visualizations # EDA and model plots
└── README.md


## How to Run
```bash
git clone https://github.com/sunikshagupta/ski-resort-ticket-price-prediction
cd ski-resort-ticket-price-prediction
pip install -r requirements.txt
jupyter notebook Notebooks/guided_capstone.ipynb
```

## Author
**Suniksha Gupta, PhD**
Data Scientist | Seattle, WA
[LinkedIn](https://www.linkedin.com/in/suniksha-gupta) | [GitHub](https://github.com/sunikshagupta)
