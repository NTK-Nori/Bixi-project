# Changelog

All notable changes to the BIXI Montréal Analytics project will be documented in this file.

## [0.1.0] - 2026-08-13

### Added
- **Notebook `01_data_acquisition_and_profiling.ipynb`**: Initial data pipeline for 2025 BIXI trip logs.
- **Feature Engineering**:
  - Derived `duration_sec` from epoch millisecond timestamps (`STARTTIMEMS`, `ENDTIMEMS`).
  - Converted timestamps into native Python datetime objects (`start_date`, `end_date`).
  - Extracted temporal dimensions for BI analysis: `start_hour`, `day_of_week`, and `month`.
  - Added boolean indicator `is_round_trip` (trips starting and ending at the same station).
- **Data Export**: Cleaned dataset saved locally to `data/processed/bixi_2025_cleaned.csv`.

### Changed / Cleaned
- Applied operational quality filters to remove 258,952 anomaly records (~1.8% of dataset):
  - Removed false starts (trips < 60 seconds).
  - Removed unreturned/abandoned bike rides (trips > 4 hours).
- Cleaned up output formatting and code cell organization.
