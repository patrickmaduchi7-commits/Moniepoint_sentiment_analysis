# Nigerian Fintech Sentiment Intelligence
### What Moniepoint Users Are Really Saying — A Sentiment-Driven Competitive Intelligence Analysis

![Python](https://img.shields.io/badge/Python-3.10-blue)
![VADER](https://img.shields.io/badge/NLP-VADER-green)
![SciPy](https://img.shields.io/badge/Stats-SciPy-orange)
![Status](https://img.shields.io/badge/Status-Complete-brightgreen)

---

## Overview

This project presents an independent sentiment and competitive intelligence 
analysis of three Nigerian fintech applications — Moniepoint, Opay, and 
Palmpay — using publicly available Google Play Store review data.

75,000 reviews were scraped, processed through VADER NLP sentiment scoring, 
and validated through Mann-Whitney U statistical testing. The findings were 
packaged into an executive-level competitive intelligence report tailored for 
three separate audiences: CEO, Product Manager, and Data Lead.

---

## Key Findings

- Moniepoint matches Opay in positive sentiment (82.5% vs 82.7%) but trails 
  in negative sentiment containment (5.7% vs 4.1%) — the gap is operational, 
  not product quality
- Moniepoint's October 2025 rating dip to 4.33 was caused by a broken app 
  update — confirmed through thematic clustering of 3,212 negative reviews
- Zero switching behavior from Moniepoint to Opay was detected across 25,000 
  Opay reviews — reframing the competitive battlefield as both platforms vs 
  traditional banks
- Palmpay trails significantly with 10% negative sentiment and ethical 
  concerns around loan harassment
- All pairwise sentiment differences are statistically significant (p < 0.001, 
  Mann-Whitney U)

---

## Tools & Methods

| Category | Tools |
|---|---|
| Data Collection | google-play-scraper |
| Sentiment Analysis | VADER (vaderSentiment) |
| Data Manipulation | Pandas |
| Statistical Testing | SciPy (Mann-Whitney U, Pearson Correlation) |
| Visualization | Matplotlib, WordCloud |
| Report Generation | ReportLab |

---


## Statistical Analysis

**Descriptive Statistics**

| Metric | Moniepoint | Opay | Palmpay |
|---|---|---|---|
| Mean Sentiment | 0.445 | 0.466 | 0.381 |
| Median | 0.493 | 0.493 | 0.440 |
| Std Deviation | 0.331 | 0.320 | 0.386 |

**Mann-Whitney U Test**

| Comparison | U-Statistic | P-Value | Significant? |
|---|---|---|---|
| Moniepoint vs Opay | 300,092,972 | < 0.001 | Yes |
| Moniepoint vs Palmpay | 340,771,666 | < 0.001 | Yes |

**Pearson Correlation (Star Rating vs Sentiment Score)**

| Platform | r | P-Value |
|---|---|---|
| Moniepoint | 0.400 | < 0.001 |
| Opay | 0.293 | < 0.001 |
| Palmpay | 0.534 | < 0.001 |

---

## Sentiment Classification

Reviews were classified using VADER compound scores:

- **Positive** — score >= 0.05
- **Neutral** — -0.05 < score < 0.05  
- **Negative** — score <= -0.05

---

## Platform Comparison

| Metric | Moniepoint | Opay | Palmpay |
|---|---|---|---|
| Average Rating | 4.44 | 4.61 | 4.21 |
| Positive Sentiment | 82.5% | 82.7% | 77.9% |
| Negative Sentiment | 5.7% | 4.1% | 10.0% |
| Statistical Rank | 2nd | 1st | 3rd |

---

## How to Run

```bash
# Clone the repo
git clone https://github.com/patrickmaduchi7-commits/moniepoint-sentiment-analysis

# Install dependencies
pip install google-play-scraper vaderSentiment pandas scipy matplotlib wordcloud reportlab

# Open the notebook
jupyter notebook notebooks/moniepoint code.ipynb
```

---

## Author

**Patrick Maduchi** — Data Analyst

- Email: patrickmaduchi7@gmail.com
- LinkedIn: linkedin.com/in/maduchi-patrick-90ba27336
- Kaggle: kaggle.com/maduchipatrick

---

## License

This project is for portfolio and research purposes. 
All data sourced from publicly available Google Play Store reviews.
