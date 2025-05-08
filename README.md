# Hospital Patient Outcome Analysis Using z-test and t-test

## Introduction

The **Hospital Patient Outcome Analysis Using z-test and t-test** project focuses on analyzing patient data to derive actionable insights for improving hospital performance and patient care. By leveraging statistical methods like z-tests and t-tests, the project evaluates key metrics such as recovery times, satisfaction levels, pain scores, and treatment effectiveness. 

The analysis is based on a simulated dataset of 50,000 patients, with a structured approach to data cleaning, exploration, and hypothesis testing. Insights derived from this study aim to guide hospital management in making data-driven decisions to enhance patient outcomes and operational efficiency.

## Project Overview

### 1. Data Cleaning & Exploration
- **Simulated Dataset**:  
    - 50,000 patients with the following columns:  
        `Patient_ID`, `Gender`, `Treatment_Type`, `Recovery_Days`, `Pain_Score_After`, `Satisfaction_Score`, `Vitals_Before`, `Vitals_After`.  
    - **Missing Values**:  
        - `Recovery_Days`: 3%  
        - `Pain_Score_After`: 7%  
        - `Satisfaction_Score`: 20%  
        - `Vitals_Before`: 5%  
        - `Vitals_After`: 5%  

- **Data Cleaning**:  
    Applied Rubin's missing data theory:  
    - <5% missing: Minimal concern.  
    - 5–20% missing: Requires careful analysis.  
    - 20–30% missing: Serious concern.  
    - 50% missing: Often unacceptable.  
    *(Reference: Jakobsen et al. (2017) - Guidelines for handling missing data)*  

- **Normality Check**:  
    - The QQ plot of the `Satisfaction_Score` column shows deviations from normality due to its bounded, discrete, and ordinal nature. Despite near-zero skewness, the data violates normality assumptions.  

- **Outcome**:  
    Cleaned data saved for further analysis.

---

### 2. Insights

#### 2.1. Is the hospital's average patient recovery time below the national average (10 days)?  
- **Insight**: The hospital's average recovery time is not below the national average.  
- **Business Implication**:  
    - No competitive advantage in recovery speed.  
    - Suggests the need to review treatment protocols.

#### 2.2. Do male patients recover slower than female patients?  
- **Insight**: Male patients recover slower than females.  
- **Business Implications**:  
    - Consider tailored rehab programs for male patients.  
    - Allocate more beds/resources for male patients.  
    - Investigate reasons for the gap (e.g., patient surveys, stratified analysis).

#### 2.3. Are >50% of discharged patients satisfied?  
- **Insight**: Only about 1 in 3 patients reach median satisfaction levels.  
- **Business Implication**:  
    - The hospital is underperforming in patient satisfaction.  
    - Requires immediate focus on improving patient experience.

#### 2.4. Is the average pain score after new treatment < standard (5)?  
- **Insight**: The new treatment effectively reduces the average pain score below 5.  
- **Business Implication**:  
    - Provides statistical support for the treatment’s effectiveness.  
    - Opportunity to promote the treatment as a viable pain management option.

#### 2.5. Compare pain scores between two treatments.  
- **Insight**: No significant difference in average pain scores between the two treatments.  
- **Business Implication**:  
    - Both treatments are equally effective in reducing pain.  
    - Focus on other factors (e.g., cost, side effects) for treatment selection.

#### 2.6. Compare patient vitals before and after treatment.  
- **Insight**: Treatment significantly reduces vital signs, indicating effectiveness.  
- **Business Implication**:  
    - Assess clinical significance of the reduction.  
    - Ensure alignment with expected treatment outcomes.

---

## Methodology

### Statistical Tests Used
- **z-test**: Used for large sample sizes to compare means and proportions.
- **t-test**: Applied for smaller sample sizes or when population variance is unknown.

### Tools & Libraries
- **Python**: Primary programming language.
- **Libraries**:  
    - `pandas` for data manipulation.  
    - `numpy` for numerical computations.  
    - `scipy.stats` for statistical tests.  
    - `matplotlib` and `seaborn` for data visualization.

---

## Results Summary
- **Recovery Time**: No significant improvement compared to the national average.  
- **Gender Disparity**: Male patients recover slower than females.  
- **Satisfaction Levels**: Below expectations, requiring immediate attention.  
- **Pain Management**: New treatment shows effectiveness in reducing pain scores.  
- **Treatment Comparison**: No significant difference in pain reduction between treatments.  
- **Vitals Improvement**: Significant reduction in vital signs post-treatment.

---

## Future Work
- Conduct further stratified analysis to identify subgroups with unique trends.
- Explore additional factors influencing patient satisfaction.
- Implement machine learning models to predict patient outcomes.
- Perform cost-benefit analysis for treatment protocols.

---

## References
- Jakobsen, J. C., Gluud, C., Wetterslev, J., & Winkel, P. (2017). Guidelines for handling missing data in randomized trials. *Journal of Biostatistics*.
- 'Practical Statistics for Data Scientists by Peter Bruce and Andrew Bruce' Copyright
© 2017 Peter Bruce and Andrew Bruce. All rights reserved.


---