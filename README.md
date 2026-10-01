# rmt-portfolio-optimization
Python-based portfolio optimizer mitigating sample noise via Random Matrix Theory.
# Overview
Classic Markowitz Mean-Variance optimization is notorious for being an "error maximizer" in practice. Due to the finite length of financial time series, empirical covariance matrices are highly susceptible to statistical noise, leading to unstable weights and poor Out-of-Sample (OOS) performance.

This project implements a quantitative pipeline that utilizes Random Matrix Theory (Marcenko-Pastur Theorem) to filter out sample noise from empirical correlation matrices, recovering the true macroeconomic signal and significantly improving portfolio stability.

# Features
*  Market Data Ingestion: Automated cleaning and processing of financial time series.

*  RMT Denoising: Dynamic estimation of noise variance using fixed-point algorithms and eigenvalue clipping based on the Marcenko-Pastur distribution.

*  Convex Optimization: Global Minimum Variance (GMV) and Target Return portfolios solved via SciPy (SLSQP) with analytical gradients and strict geometric coherence.

*  Diversification Analytics: Built-in evaluation using the Herfindahl-Hirschman Index (HHI), Effective Number of Assets, and Shannon Entropy.
