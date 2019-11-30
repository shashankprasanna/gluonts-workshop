---
title: "Deep Learning Based Time-Series Modeling Approaches"
weight: 5
katex: true
markup: "mmark"
---

Unlike classical approaches such as ARMIA, deep learning based approaches don't make any structural assumptions about your data.

Deep learning based approaches have the following benefits:
* Global models: identify patterns using all available time series
* Group-dependent seasonality and lifecycle
* Behavior in response to covariate inputs
* Weak structural assumptions
* Can be significantly more accurate than traditional methods
* Can easily incorporate and learn from rich metadata
* Support cold-start forecasts for new items

In this workshop we'll be using the [DeepAR](https://arxiv.org/abs/1704.04110) algorithm as an alternative to classical approaches such as ARIMA.
DeepAR is a deep learning based approach for producing accurate probabilistic forecasts, based on training an auto regressive recurrent network model on a large number of related time series.

* The DeepAR algorithm first tailors a Long Short-Term Memory (LSTM)-based recurrent neural network architecture to the data. DeepAR then produces probabilistic forecasts in the form of Monte Carlo simulation.
* Monte Carlo samples are empirically generated pseudo-observations that can be used to compute consistent quantile estimates for all sub-ranges in the prediction horizon.
* DeepAR also uses item-similarity to handle the Cold Start problem, which is to make predictions for items with little or no history at all.
