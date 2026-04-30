---
title: Detecting anomalies in MetricBase data using predictive models
description: MetricBase creates a model by training a representative sample of your time series data to determine the model parameters. The training process determines the model parameters that best fit your data, to distinguish normal data from anomalous data.
locale: en-US
release: xanadu
product: MetricBase
classification: metricbase
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Defining and collecting MetricBase data, MetricBase, Manage instance data sources, Extend ServiceNow AI Platform capabilities]
---

# Detecting anomalies in MetricBase data using predictive models

MetricBase creates a model by training a representative sample of your time series data to determine the model parameters. The training process determines the model parameters that best fit your data, to distinguish normal data from anomalous data.

MetricBase supports the following model types:

-   Probabilistic Exponentially Weighted Moving Average \(PEWMA\), a moving average algorithm that uses a probability factor to determine how it reacts to change in data
-   Autoregressive Integrated Moving Average \(ARIMA\), a moving average algorithm that factors in previous errors and values
-   Seasonal Trend decomposition using Loess \(STL\), a seasonal algorithm for decomposing time series data into seasonal and trend components
-   Holt-Winters \(HW\), a seasonal algorithm that decomposes the trend and seasonal components to determine the level

**Note:** MetricBase selects the most appropriate model type when you select **Find Best Fit Model** from the model class list.

After you have a model trained from your data, you can trigger flows when new data is significantly different than the trained data.

