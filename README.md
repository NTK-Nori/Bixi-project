# BIXI Montréal Analytics Project (2025)

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

## Key Insights (Phase 2 - EDA)
* **Peak Usage Hours:** Distinct dual-peak demand during weekday commuter rush hours (~8:00 AM and ~5:00 PM).
* **Popular Routes:** High-frequency trips heavily concentrate around major transit hubs, university campuses, and downtown corridors.
* **Trip Duration & Behavior:** Point-to-point commuting dominates total volume (>95%), whereas round trips (same start/end station) exhibit the longest average ride durations. Weekends show higher recreational usage with longer overall ride times.

* **Visualization / Reporting:** Matplotlib & Seaborn (`dark_background` theme), Tableau (Planned)

## Repository Structure
## Repository Structure

```text
.
├── data/
│   ├── raw/                # Original BIXI dataset
│   └── processed/          # Cleaned dataset (bixi_2025_cleaned.csv)
├── notebooks/
│   ├── 01_data_acquisition_and_profiling.ipynb
│   └── 02_exploratory_data_analysis.ipynb
├── CHANGELOG.md            # Version history & detailed updates
└── README.md               # Project overview
```
