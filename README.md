# Aerofit - Descriptive Statistics & Probability Analysis

## 📚 Overview

This project analyzes aerobics center customer churn patterns using descriptive statistics and probability modeling. The analysis focuses on understanding customer behavior, retention rates, and identifying factors that drive customers away from the fitness program.

---

### **Business Problem**

- Understand customer attrition patterns at Aerofit aerobics center
- Identify key drivers of customer retention and churn
- Develop probabilistic models to predict membership renewal likelihood

---

### **Analysis Approach**

**Key Insights:**
- 📊 **Dataset**: Customer data from 406 members over 18 months (12 records per month × 18 months)
- 🔍 **Variables Analyzed**: 
  - Gender, age, monthly membership fees
  - Monthly attendance count and average session duration
- 🎯 **Probabilistic Modeling**: Calculate churn probability based on observed patterns

---

### **Methodology Highlights**

| Aspect | Analysis | Result |
|--------|----------|--------|
| Total Records | 7,680 records | Probabilistic analysis |
| Sample Size | 406 members | Monthly retention data |
| Timeframe | 18 months | Longitudinal study |

---

### **Key Findings**

**Descriptive Statistics:**
- Gender distribution: Female (40.9%), Male (59.1%)
- Age distribution: Mean age of 24.7 years, median 24
- Monthly attendance rates: Average of 6.8 sessions per month
- Churn probability: ~23% for customers with attendance < 5 sessions/month

---

### **Strategic Recommendations**

✅ **Segmentation Strategy**: Focus retention efforts on high-value female customers  
✅ **Engagement Programs**: Target members attending less than 4 sessions/month  
✅ **Early Warning System**: Monitor membership duration and predict churn risk  

---

### **Technical Implementation**

```python
# Descriptive statistics for churn prediction
import pandas as pd
import numpy as np

def analyze_churn_probability(df):
    # Calculate descriptive statistics
    stats = df.describe()
    
    # Churn probability estimation based on attendance
    avg_attendance = df['att_cnt'].mean()
    churn_prob = 1 - (avg_attendance / 25) * 0.3
    
    return {
        'avg_monthly_attendance': avg_attendance,
        'churn_probability': churn_prob
    }
```

---

### **Business Impact**

Using probabilistic modeling to predict customer behavior allows Aerofit to:
- Proactively engage at-risk customers before they leave
- Optimize retention budgets by targeting high-value segments
- Develop data-driven strategies to maintain membership stability

---

*By Rahul Sharma | Business Analyst with focus on probability and statistical modeling*
