Here are the contents of Titanic EDA project.

```
# Titanic Dataset - Exploratory Data Analysis (EDA)

![Python](https://img.shields.io/badge/Python-3.8%2B-blue)
![Pandas](https://img.shields.io/badge/Pandas-1.3%2B-orange)
![Seaborn](https://img.shields.io/badge/Visualization-Seaborn%2FMatplotlib-red)
![Jupyter](https://img.shields.io/badge/Notebook-Jupyter-orange)
![License](https://img.shields.io/badge/License-MIT-green)

## 📖 Project Overview

This project is a comprehensive **Exploratory Data Analysis (EDA)** of the famous Titanic dataset. The goal is to uncover the factors that influenced a passenger's chance of survival using data cleaning, manipulation, and visualization techniques. This serves as a classic beginner project to demonstrate core data analysis skills.

**The central question guiding this analysis:** What helped someone survive the sinking of the Titanic?

## 📊 Dataset Description

The dataset contains information for 891 of the 2,224 passengers and crew on board the Titanic.

*   **Source:** The dataset is sourced from the Seaborn library's built-in datasets.
*   **URL:** `https://raw.githubusercontent.com/mwaskom/seaborn-data/master/titanic.csv`

**Key Features:**
*   `survived`: Survival (0 = No, 1 = Yes)
*   `pclass`: Ticket class (1 = 1st, 2 = 2nd, 3 = 3rd) - a proxy for socio-economic status
*   `sex`: Sex of the passenger
*   `age`: Age in years
*   `sibsp`: Number of siblings / spouses aboard
*   `parch`: Number of parents / children aboard
*   `fare`: Passenger fare
*   `embarked`: Port of Embarkation (C = Cherbourg, Q = Queenstown, S = Southampton)
*   `class`, `who`, `adult_male`, `deck`, `embark_town`, `alive`: Categorical derivatives of the above.

## 🎯 Business Questions / Objectives

The analysis seeks to answer the following key questions:

1.  What was the overall survival rate?
2.  Did gender influence survival? ("Women and children first")
3.  Did passenger class (socio-economic status) influence survival?
4.  How did the combination of class and gender affect survival rates?
5.  What was the age distribution of passengers, and did it affect survival?

## 🛠️ Tech Stack & Tools

*   **Programming Language:** Python 3
*   **Libraries:**
    *   `pandas` - Data manipulation and analysis
    *   `numpy` - Numerical operations
    *   `matplotlib` - Basic plotting and visualization
    *   `seaborn` - Advanced statistical visualizations
*   **Environment:** Jupyter Notebook

## 📈 Methodology & Workflow

1.  **Data Loading:** The dataset was loaded directly from its URL into a pandas DataFrame.
2.  **Data Assessment:** Used `.info()`, `.describe()`, and `.isnull().sum()` to understand the structure, summary statistics, and missing values.
3.  **Data Cleaning:**
    *   Handled missing values in the `age` column by imputing the median age.
    *   Handled missing values in the `embarked` column by imputing the mode (most frequent value).
    *   Dropped the `deck` column due to an excessive number of missing values.
    *   Converted data types for more intuitive analysis (`survived` to boolean, `pclass` to category).
4.  **Exploratory Data Analysis (EDA):**
    *   Performed univariate analysis (distribution of age, overall survival rate).
    *   Performed bivariate and multivariate analysis (survival by gender, by class, and by both).
    *   Created various visualizations (bar charts, histograms, point plots, heatmaps) to uncover patterns and relationships.
5.  **Conclusion:** Synthesized the findings to answer the initial questions.

## 🔍 Key Findings & Insights

| Question | Finding | Visualization |
| :--- | :--- | :--- |
| **Overall Survival Rate** | **38.38%** of passengers in the dataset survived. | ![Overall Survival](images/survival_count.png) |
| **Survival by Gender** | **74.2%** of females survived compared to only **18.9%** of males, strongly supporting the "women and children first" protocol. | ![Survival by Gender](images/survival_by_gender.png) |
| **Survival by Class** | A clear socio-economic divide: **63%** of 1st class passengers survived, vs. **47%** of 2nd class, and only **24%** of 3rd class. | ![Survival by Class](images/survival_by_class.png) |
| **Class & Gender Combined** | The interaction is striking. While gender was a powerful factor within each class, a 3rd-class female had a similar survival chance to a 1st-class male. Class privilege and gender norms combined to determine fate. | ![Survival by Class and Gender](images/survival_by_class_gender.png) |
| **Age Distribution** | The passenger base was relatively young, with a median age of 28. The distribution of age for survivors vs. non-survivors shows a slight tendency for younger children to have higher survival rates. | ![Age Distribution](images/age_distribution.png) |

## 📁 Project Structure

```
titanic-eda-project/
│
├── titanic_analysis.ipynb  # Main Jupyter Notebook with full analysis
├── README.md               # This file
├── requirements.txt        # List of dependencies (optional)
└── images/                 # Folder containing generated plots (for this README)
    ├── survival_count.png
    ├── survival_by_gender.png
    ├── survival_by_class.png
    └── survival_by_class_gender.png
```

## 🚀 How to Run This Project

1.  **Clone the repository** (or download the files):
    ```bash
    git clone <your-repo-url>
    cd titanic-eda-project
    ```
2.  **(Optional) Create a virtual environment:**
    ```bash
    python -m venv venv
    source venv/bin/activate  # On Windows: venv\Scripts\activate
    ```
3.  **Install the required dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *If you don't have a `requirements.txt`, install manually:*
    ```bash
    pip install pandas numpy matplotlib seaborn jupyter
    ```
4.  **Launch Jupyter Notebook:**
    ```bash
    jupyter notebook
    ```
5.  **Open the `titanic_analysis.ipynb`** notebook and run the cells sequentially.

## 📝 Future Work

*   Explore the `sibsp` and `parch` features to analyze survival rates for families.
*   Investigate the relationship between fare paid and survival within each passenger class.
*   Use the `embarked` feature to see if the point of departure had any correlation with survival.
*   Build a simple machine learning model to predict survival.

## 🔗 References

*   [Seaborn Datasets](https://github.com/mwaskom/seaborn-data)
*   [Pandas Documentation](https://pandas.pydata.org/docs/)
*   [Matplotlib Documentation](https://matplotlib.org/stable/contents.html)
*   [Seaborn Documentation](https://seaborn.pydata.org/)

## 📄 License

This project is licensed under the MIT License - see the LICENSE file for details.

---

**Author:** Bhanu Pratap Singh
**Date:** August 2025
```
