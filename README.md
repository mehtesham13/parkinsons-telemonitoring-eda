# Parkinson's Disease Telemonitoring: Exploratory Data Analysis

This project performs an in-depth Exploratory Data Analysis (EDA) on the **Parkinson's Telemonitoring Dataset**. The goal is to understand the relationships between various biomedical voice measurements and the clinical assessment of Parkinson's disease severity using the Unified Parkinson's Disease Rating Scale (UPDRS).

##  Project Overview

The dataset contains a range of biomedical voice measurements from 42 people with early-stage Parkinson's disease. This analysis focuses on:

* **Target Variables:** Predicting `motor_UPDRS` and `total_UPDRS`.
* **Feature Analysis:** Identifying which vocal characteristics (Jitter, Shimmer, HNR, etc.) correlate most strongly with disease progression.
* **Multicollinearity:** Assessing the high degree of redundancy across telemonitoring features.

##  Key Findings

### 1. Target Distributions

The UPDRS scores show a wide range of severity across the patient group.

* **Motor UPDRS:** Primarily reflects physical movement symptoms.
* **Total UPDRS:** A broader measure of the disease's overall impact.

### 2. Feature Importance & Correlation

Through the correlation analysis, several key insights were uncovered:

* **Top Predictors:** `age`, `HNR` (Harmonics-to-Noise Ratio), and `PPE` (Pitch Period Entropy) emerged as some of the most significant indicators for UPDRS scores.
* **Multicollinearity:** The analysis identified **29 highly correlated feature pairs** ($r > 0.8$). For example, `Shimmer:APQ3` and `Shimmer:DDA` have a perfect correlation ($r = 1.0$), suggesting that feature reduction (like PCA) would be beneficial for future modeling.

### 3. Voice Measurement Insights

* **Jitter & Shimmer:** These measures of frequency and amplitude instability show moderate correlations with disease severity.
* **HNR:** Showed a consistent negative correlation with UPDRS, indicating that lower voice quality (more noise) is associated with higher disease severity.

##  Tech Stack

* **Language:** Python
* **Libraries:** `Pandas`, `NumPy`, `Matplotlib`, `Seaborn`
* **Tools:** Jupyter Notebook / Google Colab

##  Project Structure

* `parkinsons_eda_project.ipynb`: The main notebook containing data cleaning, visualization, and statistical analysis.
* `parkinsons_telemonitoring.csv`: The raw dataset used for analysis.
* `correlation_matrix.csv`: Exported data showing the relationship between all features.
* `Visuals/`: Folder containing generated heatmaps, distributions, and feature importance plots.

##  How to Run

1. Clone this repository:
```bash
git clone https://github.com/your-username/parkinsons-telemonitoring-eda.git

```


2. Install the required dependencies:
```bash
pip install pandas numpy matplotlib seaborn

```


3. Open `parkinsons_eda_project.ipynb` in Jupyter Notebook or Google Colab to view the analysis.

---

**Author:** Muhammad Ehtesham

**LinkedIn:** [(https://www.linkedin.com/in/muhammad-ehtesham-dsa)]

---
