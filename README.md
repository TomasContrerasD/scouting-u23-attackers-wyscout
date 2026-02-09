<p align="center">
  <img src="assets/banner.png" width="750">
</p>

# Identifying Undervalued U23 Attackers: A Data-Driven Scouting Approach

This project explores a data-driven scouting methodology to identify **Sub-23 attacking players** who combine **strong performance** with **relatively low market value**, using advanced football metrics (Wyscout-derived, engineered by Edd Webster) for the **2020/21 season**.

## Key Objectives
- Build a **transparent scoring model** to rank U23 attackers by **impact + value**
- Use **clustering (K-Means + PCA visualization)** to identify **player profiles** and compare similar players
- Highlight **“good outliers”**: high performance at low market value

## Project Structure
- `notebooks/01_u23_attacker_scouting.ipynb` — main analysis notebook  
- `assets/` — banner and visual assets  

## Methodology Overview
1. **Data loading & scope definition** (U23, 2020/21)
2. **Cleaning & sanity checks**
3. **EDA** (minutes exposure, distributions, correlation diagnostics)
4. **Modeling**
   - Scoring model: standardized performance metrics + undervaluation residuals
   - Clustering model: K-Means profiles + PCA projection

## Data Source
- Engineered Wyscout dataset by **Edd Webster** (public GitHub repository).  
  The project is exploratory and may include minor imprecisions inherent to aggregated football data.

## How to Run
1. Clone the repo
2. Install dependencies:
   ```bash
   pip install -r requirements.txt
