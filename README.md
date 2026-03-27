[README (1).md](https://github.com/user-attachments/files/26302145/README.1.md)
# USER BEHAVIOR ANALYSIS WITH MACHINE LEARNING

This project analyzes user behavior data and applies machine learning techniques to identify meaningful user segments based on interaction patterns.

---

## 📌 Overview

This project applies exploratory data analysis and K-Means clustering to uncover hidden patterns in user behavior data. The goal is to segment users into meaningful groups that can be used for personalization, marketing strategies, or product improvements.

Developed in **Google Colab** using Python and standard data science libraries.

---

## 📁 Project Structure

```
├── data/
│   ├── raw/               # Original, unmodified datasets
│   └── processed/         # Cleaned and transformed datasets
├── notebooks/             # Jupyter notebooks with full analysis
└── src/                   # Source code and reusable functions (future extension)
```

---

## 🔬 Methodology

1. **Exploratory Data Analysis (EDA)**
   - Statistical summaries and distribution analysis
   - Detection of missing values and outliers
   - Correlation analysis between variables

2. **Feature Engineering**
   - Aggregation of raw events at the user level
   - Creation of behavioral metrics per user

3. **User Segmentation with K-Means**
   - Feature scaling and preprocessing
   - Optimal cluster selection using the Elbow method
   - Model training and cluster assignment

4. **Cluster Interpretation & Visualization**
   - Profile analysis per cluster
   - Visual representation using dimensionality reduction and plots

---

## 🛠️ Technologies Used

| Library | Purpose |
|---|---|
| Python | Core programming language |
| Pandas & NumPy | Data manipulation and numerical computing |
| Matplotlib & Seaborn | Data visualization |
| Scikit-learn | Machine learning (K-Means, preprocessing) |
| Jupyter Notebook | Interactive development environment |

---

## 🚀 Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/adrivargascouri/user-behavior-ml.git
cd user-behavior-ml
```

### 2. Install dependencies

```bash
pip install pandas numpy matplotlib seaborn scikit-learn notebook
```

### 3. Run the notebook

Open the project in **Google Colab** or locally:

```bash
jupyter notebook notebooks/
```

---

## 📊 Results

The analysis was performed on a dataset of **500 users** across **1,000 sessions**, with features including session length, pages viewed, actions count, device type, and time of day.

### Key EDA Findings

- **Session length is right-skewed**: most users have short sessions, with a mean of ~10 minutes and high variance.
- **Mobile is the most common device**, followed by desktop and tablet.
- **Session length is moderately correlated** with pages viewed and actions count.
- Some users show high actions count but low time per page, suggesting fast or automated navigation behavior.

### User Segmentation — 3 Clusters Identified

K-Means clustering (k=3) on 15 engineered features produced three distinct user profiles:

| Cluster | Label | Users | Avg. Session Length | Avg. Actions | Behavior Profile |
|---|---|---|---|---|---|
| 0 | 🔵 Low Engagement Users | 243 (57%) | ~6 min | Low | Short sessions, few pages, minimal interaction |
| 1 | 🟢 Highly Engaged Users | 65 (15%) | ~23 min | High | Long sessions, deep navigation, high engagement score |
| 2 | 🟠 Fast Browsers | 115 (26%) | ~12 min | Medium | Moderate session length, high pages-per-session ratio |

### Insights

- **57% of users are low-engagement** — the largest segment, representing users who visit briefly and don't interact deeply.
- **Highly Engaged Users (15%)** are the most valuable segment: longer sessions, more actions, and significantly higher engagement scores.
- **Fast Browsers (26%)** navigate quickly through many pages but don't dwell — potentially exploratory users or comparison shoppers.

---

## 📄 License

This project is open source and available under the [MIT License](LICENSE).
