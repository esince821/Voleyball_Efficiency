# AI and the Future of Entry-Level Jobs: Are Recent Graduates at Risk?


## Motivation
We are entering the workforce during a period of rapid growth in artificial intelligence and automation. Unlike previous generations, who often had clearer and more stable career paths, recent graduates face increasing uncertainty in the job market. In this era of digital transformation, there is a growing concern that automation may reduce the availability of entry-level positions. This project aims to analyze whether this concern is supported by data, and to examine the extent to which AI is affecting employment opportunities for recent graduates. 

---

## Hypotheses
This project investigates how artificial intelligence is reshaping entry-level job opportunities through three key dimensions: job accessibility, economic impact, and educational requirements.

---

### Hypothesis 1: Demand vs Entry-Level Access
**Question:** Do high-demand AI jobs offer fewer entry-level opportunities?

- **H0:** Demand score is not related to experience level  
- **H1:** High-demand jobs are less likely to be entry-level  

---

### Hypothesis 2: Salary Inequality
**Question:** Does AI increase salary differences between entry-level and senior roles?

- **H0:** AI salary premium is similar across experience levels  
- **H1:** Senior roles benefit more from AI salary premiums  

---

### Hypothesis 3: Education Requirements
**Question:** Do entry-level AI jobs still require formal degrees?

- **H0:** Education requirements are independent of experience level  
- **H1:** Entry-level jobs still require formal degrees  

---

### Columns Used

| Hypothesis                                      | Columns                                                                 |
|------------------------------------------------|-------------------------------------------------------------------------|
| H1: Demand vs Entry-Level Accessibility         | demand_score, experience_level                                          |
| H2: Salary Premium Inequality                  | ai_salary_premium_pct, experience_level, annual_salary_usd              |
| H3: Education Requirements                     | education_required, experience_level, required_skills                   |

---

## Dataset

This project uses a cleaned AI job market dataset stored in the `data` folder.

The original data was collected from Kaggle and cleaned for this project. After preprocessing and selecting relevant variables, the final analysis uses one cleaned dataset:

- `data/ai_jobs_market_cleaned.csv`

The main columns used in the analysis are:

- `demand_score`
- `experience_level`
- `annual_salary_usd`
- `ai_salary_premium_pct`
- `education_required`
- `required_skills`

---

### Dataset: AI Jobs Market (2025–2026)

This dataset focuses on the **AI job market**, including salary trends, demand, and job requirements.

**Key features used:**
- demand_score → measures how in-demand a role is  
- experience_level → identifies entry-level vs senior roles  
- annual_salary_usd → salary analysis  
- ai_salary_premium_pct → additional salary advantage in AI roles  
- education_required → degree requirements  
- required_skills → skills expected from candidates  

**Purpose:**  
Used to analyze how AI demand and salary dynamics vary across experience levels.

---

## Project Timeline

| Date              | Task                                                   |
|------------------|--------------------------------------------------------|
| 17 March, 22:00  | Create a GitHub repository and submit the URL          |
| 31 March, 22:00  | Submit the project proposal                            |
| 14 April, 22:00  | Data collection, EDA, and hypothesis testing           |
| 5 May, 22:00     | Apply machine learning methods                         |
| 18 May, 22:00    | Final report and code submission                       |

---

## Methodology

### 1. Data Preparation
- Selected relevant columns related to demand, salary, experience, and education  
- Cleaned missing and inconsistent values  
- Standardized categorical variables (e.g., experience_level, education_required)  

### 2. Exploratory Data Analysis (EDA)
- Analyzed distribution of experience levels across jobs  
- Examined salary trends and AI salary premiums  
- Explored education and skill requirements  
- Used visualizations (bar charts, boxplots) to identify patterns  

### 3. Hypothesis Testing
- Compared experience levels across different demand_score ranges  
- Analyzed salary differences using ai_salary_premium_pct  
- Examined relationship between education_required and experience_level  
- Applied statistical tests and group comparisons  

### 4. Interpretation
- Interpreted results to evaluate accessibility of entry-level jobs  
- Assessed whether AI creates barriers for recent graduates  
- Connected findings to broader job market trends  

### 5. Machine Learning 
- Apply classification/regression models to predict:
  - experience_level  
  - salary trends  
- Evaluate model performance and feature importance

---

Additionally, I made a website to present main findings of my project. Here is the link for the website: 
https://entry-level-jobs-with-ai.vercel.app/#hypotheses

---


