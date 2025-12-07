# A/B Testing & Hypothesis Prioritization

![Cumulative Conversion (Filtered)](cumulative_conversion_filtered.png)

This project analyzes a real e-commerce A/B test and compares multiple product-growth hypotheses using the ICE and RICE frameworks.  

**Goal:** identify the highest-impact hypothesis and determine whether Group A or Group B performs better based on conversion and revenue metrics.

## 🔍 Project Tasks
- Prioritize hypotheses using **ICE** and **RICE**; compare ranking differences.  
- Preprocess A/B-test datasets (date conversion, duplicate checks, cross-group user removal).  
- Analyze **cumulative revenue**, **AOV**, **conversion**, and their relative differences.  
- Detect anomalies using **P95/P99 thresholds** for orders per user and order price.  
- Run significance tests (Mann–Whitney) for **conversion** and **AOV** on raw & filtered data.  
- Make a final experiment decision and provide rollout recommendations.

## 📊 Key Findings
- **Group B** shows a statistically significant uplift in conversion (+13–16%).  
- Average order value shows **no significant difference** between groups.  
- After filtering anomalies, the uplift remains stable → results are robust.  
- **Decision:** stop the test; Group **B** is the winner. Gradual rollout recommended.

## 🛠 Tools & Methods
Python, pandas, numpy, scipy, plotly  
ICE / RICE frameworks, conversion rate, AOV, cumulative metrics, P95/P99 anomaly filtering, Mann–Whitney U-test.

## 📁 Project Structure
02_ab_test_hypothesis/  
│── README.md  
│── ab_test_analysis.ipynb  
│── cumulative_conversion_filtered.png  

> *This project was completed during the TripleTen Data Analysis Bootcamp.*
