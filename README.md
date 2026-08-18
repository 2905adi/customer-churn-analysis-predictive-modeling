# customer-churn-analysis-predictive-modeling
End-to-end Customer Churn Analysis project using SQL, Python, statistical analysis, A/B testing, and Logistic Regression to uncover churn drivers and build predictive models for customer retention.

# Customer Churn Analysis & Predictive Modeling

An end-to-end customer churn analytics project using **Python** and **SQLite** to identify churn drivers, generate business insights, evaluate retention strategies, and build a predictive churn model.

---

##  Project Overview

Customer churn is a major business challenge because acquiring a new customer is often more expensive than retaining an existing one.

This project analyzes customer, subscription, and support data to understand **why customers churn**, identify high-risk customer segments, evaluate potential retention strategies, and develop a **Logistic Regression model** for churn prediction.

The project follows an end-to-end analytics workflow covering **ETL, data cleaning, exploratory analysis, segmentation, statistical analysis, A/B testing, and predictive modeling**.

---

##  Business Problem

The objective is to answer key business questions such as:

* Which customer segments have the highest churn?
* Which subscription plans are most vulnerable to churn?
* Does contract type influence customer retention?
* Is customer support escalation associated with churn?
* Which states show relatively higher churn?
* Can a retention campaign potentially reduce churn?
* Can customer churn be predicted using available behavioral features?

---

##  Project Objectives

* Integrate multiple relational datasets into a unified analytical dataset.
* Clean and standardize customer, subscription, and support information.
* Identify major churn patterns through EDA.
* Segment customers based on relevant business attributes.
* Analyze relationships between support activity and churn.
* Test retention hypotheses statistically.
* Evaluate a simulated retention A/B test.
* Build a Logistic Regression model for churn prediction.
* Translate analytical findings into actionable retention recommendations.

---

##  Dataset & Data Architecture

The project integrates three relational datasets:

### 1. Customer Table

Contains customer-level information such as:

* Customer ID
* Customer Name
* Date of Birth
* State
* Customer attributes

### 2. Subscription Table

Contains subscription-related information such as:

* Customer ID
* Plan Type
* Contract Type
* Subscription attributes
* Churn Flag
* Churn-related metrics

### 3. Support Table

Contains customer support information such as:

* Customer ID
* Complaint information
* Escalation status
* Support-related attributes

The datasets are integrated using the common **Customer ID** to create a unified analytical dataset.

---

##  Tech Stack

### Programming & Data Analysis

* Python
* Pandas
* NumPy

### Database

* SQLite
* SQL

### Visualization

* Matplotlib
* Seaborn

### Statistics

* SciPy
* Chi-Square Test
* Correlation Analysis
* Hypothesis Testing

### Machine Learning

* Scikit-learn
* Logistic Regression

---

##  Project Workflow

```text
Raw Data
   ↓
Data Extraction
   ↓
Data Cleaning & Transformation
   ↓
ETL & Dataset Integration
   ↓
Feature Engineering
   ↓
Exploratory Data Analysis
   ↓
Customer Segmentation
   ↓
Revenue & Churn Analysis
   ↓
Correlation Analysis
   ↓
Hypothesis Testing
   ↓
Simulated A/B Testing
   ↓
Logistic Regression
   ↓
Model Evaluation
   ↓
Business Recommendations
```

---

##  Data Preparation & ETL

The raw datasets were processed through an ETL workflow involving:

* Loading relational data from SQLite.
* Inspecting dataset structure and data types.
* Handling missing values.
* Standardizing customer information.
* Cleaning date fields.
* Removing unnecessary columns.
* Validating categorical values.
* Creating derived analytical features.
* Joining customer, subscription, and support data.
* Validating the final analytical dataset.

The resulting dataset was used consistently across subsequent analysis and modeling stages.

---

##  Exploratory Data Analysis

EDA was performed to understand customer behavior and identify patterns associated with churn.

The analysis included:

* Overall churn distribution.
* Churn by subscription plan.
* Churn by contract type.
* Churn by state.
* Customer segmentation.
* Revenue analysis.
* Support escalation analysis.
* Distribution of churn-related features.

Visualizations were created using **Matplotlib** and **Seaborn**.

---

##  Key Business Insights

### Plan-Level Churn

The **Basic Plan** showed the highest churn rate at approximately **54.4%**, indicating a potentially vulnerable customer segment.

This suggests that retention initiatives could initially focus on Basic Plan customers.

### Support Escalations & Churn

Correlation analysis showed a **0.56 correlation** between support escalations and churn.

This indicates a meaningful positive relationship between escalation activity and customer churn, highlighting the importance of improving customer support experiences.

### Customer Segmentation

Customers were segmented across relevant dimensions such as:

* Plan type
* Contract type
* Churn risk
* Customer behavior

This helped identify groups requiring differentiated retention strategies.

---

##  Correlation Analysis

Correlation analysis was used to examine relationships between customer support activity and churn-related variables.

A correlation of approximately **0.56 between support escalations and churn** indicated a moderate positive relationship.

### Business Interpretation

Customers experiencing more support escalations may be more likely to churn.

However, correlation does **not imply causation**, so the result should be treated as a business signal rather than proof of a causal relationship.

---

##  Simulated A/B Testing

A simulated A/B test was designed to evaluate the potential impact of a customer retention campaign.

### Experimental Design

**Control Group**

Customers receive the existing customer experience.

**Treatment Group**

Customers receive a simulated retention intervention.

The resulting churn rates were compared between the two groups.

### Result

* Control churn: **33.8%**
* Treatment churn: **23.8%**

The observed difference was evaluated using a **Chi-Square Test**.

### Business Interpretation

The simulated treatment group showed lower churn than the control group.

The statistical test was used to determine whether the observed difference was statistically significant.

> **Note:** This is a simulated A/B test performed for analytical demonstration and does not represent a real-world randomized experiment.

---

##  Predictive Modeling

A **Logistic Regression** model was developed to predict whether a customer is likely to churn.

### Modeling Process

```text
Feature Selection
      ↓
Categorical Encoding
      ↓
Train-Test Split
      ↓
Logistic Regression
      ↓
Predictions
      ↓
Model Evaluation
```

The model uses customer and subscription-related features to estimate churn risk.

---

##  Model Evaluation

The Logistic Regression model was evaluated using:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-score**
* **Confusion Matrix**

### Why These Metrics?

**Accuracy** measures the overall proportion of correct predictions.

**Precision** measures how accurately the model identifies customers predicted to churn.

**Recall** measures how many actual churners are successfully identified.

**F1-score** provides a balance between precision and recall.

The **Confusion Matrix** provides a detailed view of correct and incorrect classifications.

---

##  Business Recommendations

Based on the analysis, potential retention strategies include:

### 1. Focus on High-Risk Plan Segments

Prioritize retention campaigns for customer segments showing consistently higher churn.

### 2. Improve Support Experience

Customers with repeated support escalations should be monitored more closely and prioritized for proactive resolution.

### 3. Use Predictive Churn Scores

Use model-generated churn predictions to identify customers who may require intervention.

### 4. Segment Retention Campaigns

Different customer groups can receive different retention strategies based on their plan, contract, behavior, and churn risk.

### 5. Measure Campaign Effectiveness

Retention initiatives should be continuously evaluated using controlled experiments rather than relying only on observed churn changes.

---

##  Project Structure

```text
customer-churn-analysis-predictive-modeling/
│
├── README.md
├── requirements.txt
│
├── data/
│   ├── customer_churn.db
│   └── exported_churn_data.csv
│
├── notebooks/
│   └── churn_analysis.ipynb
│
├── reports/
│   ├── churn_analysis.pdf
│   └── executive_kpi_summary.xlsx
│
├── outputs/
│   └── churn_analysis_WORKBOOK.html
│
└── images/
    ├── churn_by_state.png
    ├── churn_by_plan.png
    ├── churn_by_contract.png
    ├── correlation_analysis.png
    ├── ab_test.png
    └── model_evaluation.png
```

---

##  How to Run

### 1. Clone the repository

```bash
git clone https://github.com/2905adi/customer-churn-analysis-predictive-modeling.git
```

### 2. Navigate to the project

```bash
cd customer-churn-analysis-predictive-modeling
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Open the notebook

```bash
jupyter notebook
```

Open:

```text
notebooks/churn_analysis.ipynb
```

Run the notebook cells sequentially to reproduce the analysis.

---

##  Key Skills Demonstrated

* SQL
* Python
* Pandas
* NumPy
* SQLite
* Data Cleaning
* ETL
* Feature Engineering
* Exploratory Data Analysis
* Customer Segmentation
* Statistical Analysis
* Hypothesis Testing
* A/B Testing
* Data Visualization
* Logistic Regression
* Model Evaluation
* Business Analytics
* Data-Driven Decision Making

---

##  Future Enhancements

Potential future improvements include:

* Expanding the dataset for more robust modeling.
* Testing additional classification algorithms.
* Hyperparameter tuning and cross-validation.
* Building a real-time churn monitoring dashboard.
* Integrating Power BI for interactive business reporting.
* Implementing a production-ready retention recommendation system.

---

##  Disclaimer

This project is developed for **educational and portfolio purposes**.

The customer data and retention A/B test are simulated and should not be interpreted as results from an actual commercial customer experiment.

---


