![image alt](https://github.com/PyInsightHub/student-mental-health-prediction/blob/bcaf95ead3b17b7c5380250b5ba6587fb05f4c69/student-mental-health-banner.png)

>An end-to-end data science project analyzing the impact of daily digital habits (social media exposure and generative AI tool usage) and lifestyle markers (sleep duration and physical exercise) on the mental and physical well-being of **16,000 students**.

[![Python](https://img.shields.io/badge/Python-3.9%2B-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Pandas](https://img.shields.io/badge/Pandas-2.0%2B-150458?logo=pandas&logoColor=white)](https://pandas.pydata.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-1.2%2B-F7931E?logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-F37626?logo=jupyter&logoColor=white)](https://jupyter.org/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)



---

## 📌 Project Overview

With the rapid adoption of generative AI tools and increasing screen times, understanding student digital well-being is critical. This project explores:
* How daily **Social Media Hours** and **AI Tool Usage** correlate with self-reported health indices.
* Whether **Sleep** and **Physical Activity** serve as protective buffers against digital fatigue.
* Whether health differences across academic tiers (**High School**, **College**, **University**) are statistically significant using **One-Way ANOVA**.
* Predictive modeling to estimate **Mental Health Scores** using Ridge Regression and Random Forest Regressor.

---

## 📂 Dataset Architecture

The dataset contains **16,000 student records** across 10 attributes with **0 missing values** and **0 duplicate rows**[span_0](start_span)[span_0](end_span).

| Feature | Data Type | Description | Summary Stats / Categories |
| :--- | :--- | :--- | :--- |
| `Student_ID` | String | Unique student identifier | `STU_00001` – `STU_16000`[span_1](start_span)[span_1](end_span) |
| `Age` | Integer | Student age | 13 – 25 years (Mean: 19.04)[span_2](start_span)[span_2](end_span) |
| `Gender` | String | Gender identity | Male (48.4%), Female (47.7%), Non-binary (3.9%)[span_3](start_span)[span_3](end_span) |
| `Education_Level` | String | Current academic tier | High School (38.0%), University (31.4%), College (30.6%)[span_4](start_span)[span_4](end_span) |
| `Daily_Social_Media_Hours` | Float | Daily time spent on social platforms | 0.00 – 14.00 hrs (Mean: 4.54 hrs)[span_5](start_span)[span_5](end_span) |
| `Daily_AI_Tool_Usage_Hours` | Float | Daily time utilizing AI assistants | 0.00 – 9.50 hrs (Mean: 2.59 hrs)[span_6](start_span)[span_6](end_span) |
| `Sleep_Hours` | Float | Daily duration of sleep | 2.00 – 11.15 hrs (Mean: 6.55 hrs)[span_7](start_span)[span_7](end_span) |
| `Physical_Activity_Hours` | Float | Daily duration of physical exercise | 0.00 – 5.00 hrs (Mean: 1.25 hrs)[span_8](start_span)[span_8](end_span) |
| `Mental_Health_Score` | Float | Composite mental well-being index | 32.56 – 91.76 (Mean: 72.49)[span_9](start_span)[span_9](end_span) |
| `Physical_Health_Score` | Float | Composite physical health index | 48.03 – 99.98 (Mean: 88.02)[span_10](start_span)[span_10](end_span) |

---

## 🔍 Key Findings & Statistical Insights

* **Total Screen Exposure**: Students spend an average of **7.13 hours/day** in front of screens across social media (4.54 hrs) and AI utilities (2.59 hrs)[span_11](start_span)[span_11](end_span).
* **Negative Impact of Social Media**: Daily social media usage exhibits a strong inverse correlation with `Mental_Health_Score` ($r = -0.404$) and `Physical_Health_Score` ($r = -0.308$).
* **Protective Lifestyle Factors**:
  * **Physical Activity**: The strongest positive contributor to physical health ($r = +0.421$) and mental well-being ($r = +0.245$).
  * **Sleep**: Exhibits a strong positive correlation with mental health ($r = +0.313$) and physical health ($r = +0.270$).
* **Academic Tier Parity (ANOVA Test)**[span_12](start_span)[span_12](end_span):
  * $F\text{-statistic} = 1.7559$, $p\text{-value} = 0.1728$[span_13](start_span)[span_13](end_span).
  * Since $p > 0.05$, there is **no statistically significant difference** in mental health scores between High School, College, and University students[span_14](start_span)[span_14](end_span). Screen fatigue affects students uniformly across all educational tiers.

---

## 🛠️ Project Structure

```text
student-mental-health-prediction/
│
├── AI_SocialMedia_Student_Dataset.csv   # Raw dataset (16,000 records)
├── AI Social Media Student Data.ipynb   # Complete pipeline notebook
├── README.md                            # Project documentation
└── requirements.txt                     # Dependencies for reproduction

