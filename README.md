# 🚲 BIXI Montréal Analytics Project (2025)

## Project Overview
This project analyzes the 2025 BIXI trip dataset to understand urban mobility trends, peak rental hours, and user behavior across Montréal's bike-sharing network. The goal is to extract actionable insights for fleet optimization and business intelligence reporting.

## Tech Stack & Tools
* **Language:** Python (Pandas, NumPy)
* **Environment:** Jupyter Notebooks, Linux Mint
* **Version Control:** Git & GitHub
* **Visualization / Reporting:** [e.g., Matplotlib / Seaborn / Tableau]

## Data Cleaning & Quality Control
Out of **14,386,222 raw trip records** in the 2025 dataset, **258,952 trips** were identified and removed as operational anomalies:
* **False Starts:** Trips under 60 seconds (accidental rentals or system glitches).
* **Unreturned Bikes:** Trips exceeding 4 hours (abandoned or unreturned bikes).

This left **14,127,270 cleaned records** for analysis. Derived new fields (`duration_sec`, `start_hour`, `day_of_week`, `month`, and `is_round_trip`) to prepare the dataset for exploratory analysis.

## Key Insights (In Progress)
* *Peak Usage Hours:* [To be added after Exploratory Data Analysis]
* *Popular Routes / Stations:* [To be added after EDA]
* *Average Trip Duration:* [To be added after EDA]

## Repository Structure
## 📁 Repository Structure

```text
.
├── data/
│   ├── raw/                # Original BIXI dataset
│   └── processed/          # Cleaned dataset (bixi_2025_cleaned.csv)
├── notebooks/
│   └── 01_data_acquisition_and_profiling.ipynb
├── CHANGELOG.md            # Version history & detailed updates
└── README.md               # Project overview
```
