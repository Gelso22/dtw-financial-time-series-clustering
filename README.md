# Dynamic Time Warping for Financial Time Series

This repository contains an early exploratory project on the use of Dynamic Time Warping (DTW) to compare financial price paths with similar shapes.

The main idea is to transform price data into fixed time-window paths, normalize each path, compute pairwise DTW distances, and apply clustering methods to identify groups of similar market patterns.

## Notebooks

- `notebooks/dynamic_time_warping_bitcoin_intraday_weekly.ipynb`  
  Applies DTW and K-medoids clustering to Bitcoin intraday daily paths, then extends the same idea to weekly paths built from daily prices.

- `notebooks/dynamic_time_warping_spy_monthly.ipynb`  
  Applies DTW and K-medoids clustering to monthly SPY price paths, after normalizing each month by its first available price.

## Main methods

- Reshaping financial time series into daily, weekly, and monthly paths
- Path normalization by first-period price
- Dynamic Time Warping distance computation
- K-medoids clustering using a precomputed distance matrix
- Elbow and silhouette diagnostics for cluster selection
- Cluster-level inspection of future price performance

## Project goal

The objective was to explore whether similar historical price paths could be grouped together and then compared in terms of their subsequent performance.

This project should be interpreted as an exploratory analysis rather than a complete predictive trading model.

## Repository status

This is an old exploratory project. The notebooks have been lightly cleaned for readability while preserving the original structure and modelling logic.

Some notebooks depend on local CSV files that are not included in the repository, such as Binance historical data exports. To reproduce the analysis, place the required CSV files in the working directory or adapt the file paths.

## References

This exploratory project was inspired by research on using Dynamic Time Warping to compare indexed financial price paths:

- Nakagawa, K., Imamura, M., & Yoshida, K. (2019). *Stock price prediction using k-medoids clustering with indexing dynamic time warping*. Electronics and Communications in Japan, 102(2), 3–8.

The notebooks follow the same general idea of normalizing price paths and using DTW-based distances to compare their shapes.
