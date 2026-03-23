# ALY 6040 — Data Mining Applications: Yelp Dataset Pipeline

**Northeastern University · Roux Institute**  
**Course:** ALY 6040 Data Mining Applications  
**Language:** Python · scikit-learn · pandas · seaborn  
**Team:** Group 3 — Alva Ayitey-Adjin · Alexandra Offei · Akanah Semione Draper

---

## Overview

A complete end-to-end data mining pipeline on the **8.65 GB Yelp Academic Dataset**, progressing from large-scale EDA through predictive modelling, unsupervised clustering, and NLP text mining across six modules. The project focused on five industries: Restaurants · Food · Home Services · Automotive · Health & Medical.

---

## Pipeline

```
Raw Yelp Dataset (8.65 GB)
        ↓
Module 1: Dashboard & foot traffic analysis
        ↓
Module 2: Stratified sampling + EDA (150K+ businesses)
        ↓
Module 3: Predictive modelling (Random Forest F1 = 85.6%)
        ↓
Module 4: KNN + K-Means clustering (7 segments)
        ↓
Module 5: TF-IDF NLP text clustering
        ↓
Module 6: Combined structured + text features → Final model
```

---

## Modules

### Module 1 — Dashboard Prototype: Foot Traffic Analysis
- Random sample of 1,000 businesses across 13 U.S. states
- Expanded to 8,738 timestamped customer visits (2011–2020)
- Interactive dashboard: filter by category, city, state
- **Market gap analysis:** supply-demand imbalances across business categories
- Peak customer activity patterns by business type

---

### Module 2 — Exploratory Data Analysis (8.65 GB Dataset)
**Dataset:** 150,346 business entries · stratified to 11,341-business sample

- **Stratified sampling strategy:** proportional allocation by primary business category
- Data quality assessment: missing values, outlier detection, schema validation
- Business performance analysis: review counts, star ratings, open/closed status
- Advanced outlier detection using IQR and z-score methods
- Correlation analysis across numerical business attributes

---

### Module 3 — Predictive Modelling ⭐
**Target:** Binary classification (high/low rated) + star rating regression

- **Classification model:** Random Forest · **F1 score = 85.6%**
- **Regression model:** Random Forest regressor · R² = 0.29
- Feature engineering from structured review data (review count, check-ins, attributes)
- Train/test split · cross-validation · feature importance analysis
- Per-industry performance analysis across 5 sectors

---

### Module 4 — KNN & K-Means Clustering ⭐
**Dataset:** 6,200+ food and beverage establishments

**K-Means clustering (k=7) — segment profiles:**
| Cluster | Label | Key Characteristics |
|---|---|---|
| 0 | Struggling Establishments | Low engagement, few reviews |
| 1 | Social Community Hubs | High engagement (6.14 avg), social focus |
| 2 | Hidden Gems | High ratings, low visibility |
| 3 | High-Traffic Popular Spots | 716 avg reviews, 1,641 check-ins |
| 4 | Established Community Hubs | Mature, loyal customer base |
| 5 | Premium High-Volume | 11+ years operating, stable |
| 6 | Emerging Businesses | Recent openings, growing reviews |

- **KNN classification:** Predict business segment from operational features
- Elbow method and silhouette scoring for optimal k selection

---

### Module 5 — Text Mining & NLP Clustering ⭐
**Dataset:** Yelp reviews with text content for target businesses

- **TF-IDF vectorisation** (200 features) on review text
- Review-level text feature extraction aggregated to business level
- KMeans clustering on text features
- **Silhouette scoring** for cluster quality evaluation
- Category-level sentiment and topic scoring
- Combined text + structured features for enriched business profiles

---

### Module 6 — Final Predictive Model
- Combined TF-IDF text features with structured business data
- Comprehensive feature matrix: review counts · ratings · check-ins · text features · categories
- Random Forest classifier on enriched dataset
- Memory-optimised processing pipeline for large-scale data

---

## Skills Demonstrated

`Python` `scikit-learn` `pandas` `seaborn` `Random Forest` `K-Means` `KNN` `TF-IDF` `NLP` `Feature engineering` `Stratified sampling` `Large-scale EDA` `Clustering` `Text mining`
