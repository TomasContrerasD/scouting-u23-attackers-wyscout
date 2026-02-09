# Identifying Undervalued U23 Attackers: A Data-Driven Scouting Approach

<p align="center">
  <img src="assets/banner.png" width="750">
</p>

This project presents a **data-driven scouting framework** designed to identify **Sub-23 attacking players** who combine **strong on-field performance** with **relatively low market value**, using advanced football metrics derived from Wyscout data for the **2020/21 season**.

The objective is not to predict future performance, but to **support scouting decision-making** by structuring performance data, reducing noise, and highlighting players who may be **undervalued by the market** given their contribution and playing style.

This work is exploratory in nature. The dataset contains aggregated and engineered metrics, which may include minor imprecisions typical of football data. These limitations are handled through filtering, normalization, and comparative analysis, with the primary goal of showcasing a **scalable scouting methodology** rather than producing definitive rankings.

---

## Project Objectives

- Build a **transparent scoring model** that combines performance and market value into a single ranking
- Identify **market inefficiencies** (high performance, low price)
- Use **unsupervised learning (clustering)** to group attackers by playing style
- Enable fair comparisons between **similar player profiles**
- Demonstrate a practical application of data science to football scouting

---

## Dataset

- Engineered Wyscout dataset created by **Edd Webster**
- Covers selected European leagues during the **2020/21 season**
- Includes per-90 performance metrics, duels, passing, finishing, and progression statistics

This project focuses on:
- **Sub-23 players**
- **Attacking positions**
- Separate analysis by **minutes played buckets** to control for exposure

---

## Methodology Overview

### 1. Data Cleaning
- Filtering by age, season, and minutes played
- Handling missing values and categorical inconsistencies
- Creation of macro positions (GK / DEF / MID / ATT)

### 2. Exploratory Data Analysis (EDA)
- Distribution of minutes played to avoid modeling noise
- Identification of:
  - variables with many zeros
  - strong skewness
  - near-zero variance features
  - incompatible scales
- Correlation analysis to detect redundant metrics
- Performance vs market value exploration
- Detection of “good outliers” (high performance, low price)

### 3. Scoring Model (Main Model)
- Feature selection based on EDA
- Standardization (z-scores)
- Construction of a **performance score**
- Transformation of market value into a **value inefficiency score**
- Minutes-based weighting
- Final ranking combining **impact + value**

### 4. Clustering Model (Complementary)
- K-Means clustering on standardized performance features
- Silhouette-based selection of number of clusters
- PCA projection for visualization
- Identification of **playing styles and profiles**
- Ranking players **within clusters** to ensure fair comparisons

---

## Repository Structure
scouting-u23-attackers-wyscout/
│
├── notebooks/
│ └── scouting_u23_attackers.ipynb
│
├── assets/
│ └── banner.png
│
├── requirements.txt
└── README.md

---
## Key Takeaways:
* Raw football statistics are noisy; minutes played and context matter
* Many commonly used metrics are highly redundant
* Combining performance with market value reveals hidden scouting opportunities
* Clustering adds interpretability by distinguishing player styles, not just levels
* Simple, interpretable models can be more useful than complex black boxes in scouting contexts

---
## Conclusion

This project demonstrates how a structured, data-driven approach can support football scouting by identifying young attacking players who offer strong performance at a reasonable cost. By combining careful exploratory analysis, a transparent scoring model, and unsupervised clustering, the framework balances interpretability, practicality, and analytical rigor.

Rather than relying on a single metric or opaque model, the methodology emphasizes comparison within context: similar minutes, similar roles, and similar playing styles. While the results are exploratory and subject to data limitations, the approach itself is scalable and adaptable to other leagues, seasons, and positions.

Ultimately, this work highlights how data science can complement traditional scouting by narrowing the search space, revealing market inefficiencies, and providing objective support to football decision-making.

---
## Author
**Tomás Contreras**  
GitHub: https://github.com/TomasContrerasD<br>
LinkedIn: www.linkedin.com/in/tomas-contreras-delporte<br>
Email: tomascontrerasipd@gmail.com
