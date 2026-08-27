# Changelog

All notable changes to the BIXI Montréal Analytics project will be documented in this file.

## [0.1.0] - 2026-08-13

### New
- **Notebook `01_data_acquisition_and_profiling.ipynb`**: Initial data pipeline for 2025 BIXI trip logs.
- **Creating new metrics / Calculating extra information**:
  - Derived `duration_sec` from epoch millisecond timestamps (`STARTTIMEMS`, `ENDTIMEMS`).
  - Converted timestamps into native Python datetime objects (`start_date`, `end_date`).
  - Extracted temporal dimensions for analysis: `start_hour`, `day_of_week`, and `month`.
  - Added boolean indicator `is_round_trip` (trips starting and ending at the same station).
- **Data Export**: Cleaned dataset saved locally to `data/processed/bixi_2025_cleaned.csv`.

### Changes and cleaning
- Applied operational quality filters to remove 258,952 anomaly records:
  - Removed false starts (trips < 60 seconds).
  - Removed unreturned/abandoned bike rides (trips > 4 hours).
- Cleaned up output layout and organized code blocks for clarity.

## [0.2.0] - 2026-08-19

### Added
- **Notebook `02_exploratory_data_analysis.ipynb`**: Comprehensive EDA for 2025 BIXI trip logs.
- **Time & Location Patterns**:
  - Aggregated trip volumes by hour of day, identifying dual peak demand periods (morning and evening commuter rush hours).
  - Calculated weekday vs. weekend distribution and average ride durations.
  - Identified top 10 most frequent origin-to-destination route corridors across Montréal.
  - Analyzed round-trip vs. point-to-point ride ratios and corresponding duration distributions.

### Key Insights
- **Commuter Demand:** Weekday usage peaks sharply during standard commuting hours, whereas weekend rides exhibit longer average durations.
- **Trip Types:** Point-to-point transit dominates overall volume, while round trips account for longer leisure/recreational ride durations.

### Added
- Created `notebooks/03_tableau_data_prep.ipynb` to transform the 14.1M raw records into smaller Tableau files.
- Generated `tableau_station_summary.csv` with station locations (latitude, longitude, and borough) for mapping.
- Generated `tableau_hourly_summary.csv` to track ride volumes and average trip lengths by hour of the day and day of the week.
- Generated `tableau_bixi_2025_sample10pct.csv` using a fixed random seed (`random_state=404`) for consistent sampling.

## [1.2.0] - 2026-08-26

### Added
- Created `03_tableau_data_prep.ipynb` to generate a 10% representative sample (~1M records) from the cleaned 2025 BIXI dataset.
- Built and published an interactive 3 panel dashboard on Tableau Public covering station density, peak 24-hour demand, and top station volumes.
- Implemented sorting by trip count on the station activity map to prevent high-volume hub occlusion.
- Updated `README.md` with Tableau Public dashboard link, feature breakdown, and updated repository structure.
