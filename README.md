# A/B Testing Analysis: Facebook Ads vs Google AdWords

## Business Problem

A digital marketing team is trying to determine the more effective advertising platform between **Facebook Ads** and **Google AdWords**. The primary business question is:

> **Which platform—Facebook or Google AdWords—yields better user conversion outcomes for similar levels of ad engagement?**

With limited marketing budgets, businesses must allocate spending to channels that maximize returns. This project uses A/B testing and statistical correlation analysis to compare user behavior metrics (clicks and conversions) on both platforms.

---

## Objectives

- Understand the relationship between **ad clicks** and **ad conversions** across platforms.
- Use **descriptive statistics**, **correlation coefficients**, and **visualizations** to explore performance.
- Support findings using **statistical significance testing**, including **Pearson correlation** and **hypothesis testing**.
- Provide business recommendations based on data-driven insights.

---

## Dataset Description

The dataset contains user-level interaction data across two platforms:

| Column                     | Description                                  |
|---------------------------|----------------------------------------------|
| Facebook Ad Clicks        | Number of clicks generated via Facebook Ads  |
| Facebook Ad Conversions   | Number of conversions from Facebook Ads      |
| AdWords Ad Clicks         | Number of clicks generated via Google Ads    |
| AdWords Ad Conversions    | Number of conversions from Google Ads        |

---

## Methodology

### 1. **Data Exploration**

- Used `pandas` to load and preview the dataset.
- Checked for missing or inconsistent data.
- Generated histograms to understand distribution of each metric.

### 2. **Descriptive Statistics**

- Computed mean, median, standard deviation, and range for each metric.
- Observed a relatively symmetric distribution for click and conversion data, validating use of Pearson correlation.

### 3. **Correlation Analysis**

- **Facebook Ads:**  
  Pearson correlation between clicks and conversions: **0.87**  
  → Indicates a strong positive relationship.

- **Google AdWords:**  
  Pearson correlation between clicks and conversions: **0.45**  
  → Indicates a moderate relationship.

### 4. **Statistical Tests**

- **Hypothesis Testing:**  
  - *Null Hypothesis (H₀):* There is no significant correlation between clicks and conversions.  
  - *Alternative Hypothesis (H₁):* There is a significant correlation between clicks and conversions.

- Applied Pearson correlation test via `pandas.DataFrame.corr()` and validated significance through visual inspection.

---

## Key Findings

- **Facebook Ads** demonstrate a stronger link between user clicks and conversions, suggesting more effective targeting or a more immediate funnel.
- **AdWords** shows a moderate correlation, possibly due to broader targeting or a delayed conversion pattern.

---

## Recommendations

- Consider prioritizing **Facebook Ads** for short-term conversion-focused campaigns.
- Use **Google AdWords** for brand awareness or top-of-funnel marketing, where direct conversions may not be immediate but contribute to longer-term goals.
- Further test additional factors like **cost-per-click (CPC)** or **return on ad spend (ROAS)** for deeper profitability insights.

---

## Technologies Used

- **Python 3.13**
- Jupyter Notebook
- Libraries:
  - `pandas`
  - `numpy`
  - `matplotlib`
  - `seaborn`

---

## How to Run the Notebook

1. Clone this repository:
   ```bash
   git clone https://github.com/yourusername/A-B-Testing-Analysis-of-Facebook-Ads-vs-Adwords.git
   ```

2. Navigate to the directory:
   ```bash
   cd A-B-Testing-Analysis-of-Facebook-Ads-vs-Adwords
   ```

3. Set up the virtual environment:
   ```bash
   python -m venv .venv
   source .venv/bin/activate  # On Windows: .venv\Scripts\activate
   pip install -r Requirements.txt
   ```

4. Launch Jupyter Notebook:
   ```bash
   jupyter notebook "AB Testing.ipynb"
   ```

---


## Future Improvements

- Include A/B test p-values and confidence intervals.
- Integrate cost-based metrics (CPC, CPA).
- Perform time-series analysis on campaign timelines.
