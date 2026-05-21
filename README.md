# Anxiety Level Prediction — Exploratory Data Analysis & Machine Learning

An end-to-end data science project analyzing the key drivers of anxiety across 12,000 individuals. The project combines in-depth Exploratory Data Analysis with a Machine Learning classification model and an interactive prediction system to determine an individual's anxiety level based on lifestyle and physiological indicators.

---

## Project Objective

Anxiety is influenced by a complex mix of lifestyle habits, biological factors, and external stressors. This project aims to:

- Identify the **lifestyle and physiological tipping points** where anxiety shifts from mild to severe
- Build a **predictive classification model** to accurately determine anxiety level (1–5)
- Provide an **interactive prediction system** for real-time anxiety level assessment

---

## Key Highlights

- 15+ visualizations covering lifestyle, biological, and psychological anxiety drivers
- 4 machine learning models evaluated — Logistic Regression, Decision Tree, Random Forest, XGBoost
- **84.01% classification accuracy** achieved with Random Forest (n_estimators=850)
- Live prediction system — input personal lifestyle data to receive an instant anxiety level prediction
- Tipping point analysis identifying where mild anxiety escalates to severe

---

## EDA — Key Findings

| Factor | Insight |
|---|---|
| Sleep Hours | Avg 8 hrs at Level 1, drops sharply to 4.5–5 hrs at Levels 4–5 |
| Caffeine Intake | Stable below 290 mg/day for Levels 1–3, spikes to ~430 mg/day at Level 4 |
| Physical Activity | Strong inverse relationship — declines significantly as anxiety increases |
| Stress Level | Scores remain below 6 for Levels 1–2, jump to 9–10 at Levels 4–5 |
| Heart Rate | 82–85 bpm at lower levels, exceeds 100 bpm at Levels 4–5 |
| Family History | Becomes the dominant differentiator at Levels 4–5 |
| Smoking | Probability of smoking exceeds non-smoking at Levels 4–5 |
| Diet Quality | Stable at 5.5 for Levels 1–3, drops to 2.5 at Level 5 |
| Occupation | Lawyers (3.16), Doctors (3.11), Engineers (3.10) show highest average anxiety |
| Gender | No meaningful impact — group means differ by less than 0.03 |

---

## Steps Performed

1. **Data Loading & Inspection** — Loaded dataset of 12,000 individuals, checked shape, data types, null values and class distribution
2. **Exploratory Data Analysis** — 15+ visualizations analyzing lifestyle, physiological, and psychological factors against anxiety levels
3. **Feature Encoding** — Binary mapped Yes/No columns,removed low-impact features, and performed One-Hot Encoding on categorical variables.
4. **Train-Test Split** — 80/20 split with random state for reproducibility
5. **Feature Scaling** — Applied StandardScaler on 11 numerical columns
6. **Model Training** — Trained and evaluated Logistic Regression, Decision Tree, Random Forest, and XGBoost
7. **Model Selection** — Random Forest selected as best model with 84.01% accuracy
8. **Prediction System** — Built an interactive input-based system for real-time anxiety level prediction

---

## Model Performance

| Model | Accuracy |
|---|---|
| Logistic Regression | 69.09% |
| Decision Tree | 72.47% |
| XGBoost | 83.73% |
| **Random Forest** | **84.01% — Best Model** |

Random Forest with 850 estimators outperformed all other models and was selected as the final classifier.

---

## Prediction System

The notebook includes an interactive input-based prediction system. Users provide:

- Demographic: Age, Occupation
- Lifestyle: Sleep Hours, Physical Activity, Caffeine Intake, Alcohol Consumption, Smoking, Diet Quality
- Clinical: Heart Rate, Breathing Rate, Sweating Level, Dizziness
- Behavioural: Stress Level, Therapy Sessions, Medication, Recent Major Life Event, Family History

The model returns a predicted **Anxiety Level (1–5)** with the following interpretation:

| Level | Classification | Recommendation |
|---|---|---|
| 1–2 | Low / Mild | Maintain current lifestyle and sleep habits |
| 3 | Moderate | Consider stress management and reducing caffeine |
| 4–5 | Severe | Consult a healthcare professional or counselor |

---

## Dataset

Data sourced from **Kaggle** — 12,000 individuals with lifestyle, physiological, and psychological attributes labelled with anxiety levels on a scale of 1 to 5.

---

## Getting Started

**Prerequisites**
```bash
pip install pandas numpy matplotlib seaborn xgboost
```

**Run**
1. Clone this repository
2. Place `anxiety_dataset.csv` in the same directory as the notebook
3. Open `anxiety_project.ipynb` in Jupyter Notebook or VS Code
4. Run all cells sequentially
5. Use the prediction system in the final cells to test with your own inputs

---

## Tech Stack

`Python` &nbsp;|&nbsp; `Pandas` &nbsp;|&nbsp; `NumPy` &nbsp;|&nbsp; `Matplotlib` &nbsp;|&nbsp; `Seaborn`  &nbsp;|&nbsp; `XGBoost`
