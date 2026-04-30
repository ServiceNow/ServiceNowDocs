---
title: Understanding Metric Intelligence
description: Use Metric Intelligence to identify and prevent potential service outages. Metric Intelligence, based on historical metric data, indicates anomalous behavior of CIs which events might not capture. Anomaly alerts can be promoted to regular IT alerts and appear on the Service Operations Workspace and service health dashboard for preventive actions.
locale: en-US
release: yokohama
product: Metric Intelligence
classification: metric-intelligence
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [Exploring Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Understanding Metric Intelligence

Use Metric Intelligence to identify and prevent potential service outages. Metric Intelligence, based on historical metric data, indicates anomalous behavior of CIs which events might not capture. Anomaly alerts can be promoted to regular IT alerts and appear on the Service Operations Workspace and service health dashboard for preventive actions.

## Anomaly detection

Metric data is collected by various data sources such as SCOM, SolarWinds monitoring system, or Nagios XI server \(some partially configured for metric collection by default\). These monitoring systems collect metric data from the source environment regularly. Metric Intelligence captures the raw data from these monitoring systems, and uses event rules and the CMDB identification engine to map data to existing CIs and their resources. The data is then analyzed to detect anomalies and to provide other statistical scores.

Metric Intelligence uses historical metric data to build statistical models. These models facilitate projection of expected metric values along with upper and lower bounds. Metric Intelligence then uses these projections to detect statistical outliers and to calculate anomaly scores. Anomalies are scored on a range of 0-10. High anomaly scores for CI metrics can indicate that a CI is at risk of causing a service outage.

After processing, the [Insights Explorer](../task/view-metrics-explorer.md) shows metric statistics and charts, and the [Anomaly Map](../task/view-metrics-anomaly-alerts.md) shows correlated scores for CIs with the highest anomaly scores, across a timeline.

You may want to disable anomaly detection during system maintenance, as anomalies may be irrelevant when detected while maintenance is in progress. To do so, set the **mid.mi.anomaly\_detection.disable** property to **true**.

To customize displaying anomalies for metrics classified as near-constant, contact customer support.

Metric Intelligence is available when you activate the Metric Intelligence \(com.snc.sa.metric\) plugin.

## Terms used with Metric Intelligence

-   **Source metric type**

    A metric such as '% Free Space' or 'Current Bandwidth' that can be measured by a data source for a CI. For each data source, you can choose which of all possible source metric types are processed. For example, there are about 380 source metric types that are active by default for the SCOM data source.

-   **Anomaly**

    Data that is outside the control bounds is considered a statistical outlier. These outliers are used to compute an anomaly score, which is a value between 0–10 that indicates the degree to which the metric appears unlikely. When an anomaly score is above a threshold, an anomaly alert is generated. Anomaly alerts are reported separately from regular IT alerts.

-   **Resource**

    A component of a CI that consists of multiple individual components of similar type, where each subcomponent can be monitored separately. For example, individual Web pages, or specific disks such as 'Disk C:' and 'Disk D:'.

-   **Time series**

    A series of values \(such as metric values\) over a time range, associated with a CI and a metric type. Because an anomaly score is evaluated for each metric, the series of anomaly scores over a period of time are also a time series. Time series are computed by the statistical model built for a metric data series, and are used with metric data values, anomaly scores, and upper and lower control bounds.


## Statistical models

Metric Intelligence jobs learn from past metric data \(up to 32 days old\). A model training process analyzes historical data to construct a model that projects future values. Typically, models are in effect until the next time the model learning process runs. These models are used to calculate upper and lower bounds. Incoming values that are beyond those bounds, and that deviate with statistical significance from expected values, generate anomalies. Each model is uniquely patterned and is labeled with a classifier that illustrates the general behavior of the model. This classification determines if anomaly detection can be applied. For most models, it is possible to project which future values deviate from expected values. Such models are associated with control bounds and anomaly detection can be applied \(if enabled\).

However, for some models, there is insufficient data to determine which values are anomalous and anomaly detection cannot be applied without additional information \(even if anomaly detection is enabled\).

The learned data models are stored in the Metric Time Series Models \[sa\_time\_series\] table.

The following statistical models and classifiers are used in anomaly detection:

-   **Time Series statistical model**

    After it is established, a time series model does not adjust to changes in the incoming metric data. Therefore, if the pattern of incoming data changes, those changes are likely to be identified as anomalous. Upper and lower control bounds, after they are learned, persist until the next time the learning process runs \(data is learned every day\).

    -   **Weekly**

        Data with a pattern that repeats itself over weekly intervals \(seasonal model\).

        Requires a minimum of 15 days of data in the series, as set by the [weekly\_model\_min\_days](../task/create-config-overriding-rule.md) configuration setting.

        ![Weekly classifier](../image/WeeklyDataModel.png)

    -   **Daily**

        Data with a pattern that repeats itself over a daily interval \(seasonal model\).

        Requires a minimum of 3 days of data in the series, as set by the [daily\_model\_min\_days](../task/create-config-overriding-rule.md) configuration setting.

        ![Daily classifier](../image/DailyDataModel.png)

    -   **Trendy**

        Data that has a linear trend with some slope and with some noise.

        Requires a minimum of 30 data points in the series, as set by the [corrupt\_data\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting.

        ![Trendy classifier](../image/TrendyDataModel.png)

    -   **Noisy**

        Typical noisy data that is a basic pattern classification in a data model. The pattern cannot be identified with a specific trend or seasonality.

        Requires a minimum of 30 data points in the series, as set by the [corrupt\_data\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting.

        ![Noisy classifier](../image/NoisyDataModel.png)

    -   **Positive clipped noisy**

        Similar to the noisy classifier other than the lower bound that is fixed on 0.

        Requires a minimum of 30 data points in the series, as set by the [corrupt\_data\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting.

        ![Positive clipped noisy classifier](../image/PositiveClippedNoisyDataModel.png)

    -   **Centered noisy**

        Noisy data that typically spreads symmetrically between user-specified upper and lower bounds. The formula that is used to set bounds and width values, ignores the statistical data, and the lower and the upper widths have an identical value.

        Requires that the number of data points in the series is zero.

        See [Specify custom upper and lower metric bounds](../task/override-metric-bounds.md) for more information.

        ![Centered noisy classifier](../image/CenteredNoisyDataModel.png)

    -   **Skewed noisy**

        Noisy data that is not evenly spread between user-specified upper and lower bounds, but instead tends to concentrate closer to one of the bounds. The median of the data is used to separately compute an upper width and a lower width.

        Requires a minimum of one data point in the series.

        See [Specify custom upper and lower metric bounds](../task/override-metric-bounds.md) for more information.

        ![Skewed noisy classifier](../image/SkewedNoisyDataModel.png)

    -   **Skewed noisy - Generalized Extreme Value \(GEV\) Distribution**

        Noisy data that is spread unevenly between user-specified upper and lower bounds, and concentrates closer to one of the bounds. In addition, the data distribution demonstrates a long or heavy tail. The median of data derived from the tail of the distribution is used to separately compute an upper width and a lower width. There must be at least one data point in the series.

    -   **Accumulator**

        Data pattern similar to the trendy classifier but with a monotonous increase and without noise. For this classifier, there is no data model and no anomaly detection.

        Requires a minimum of 30 data points in the series, as set by the [corrupt\_data\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting.

        ![Diagram of the Accumulator classifier.](../image/AccumulatorDataModel.png)

    -   **Near Constant**

        Nearly constant data, in which most values are a specific constant value. For this classifier, there is no data model and no anomaly detection.

        Requires a minimum of 30 data points in the series, as set by the [corrupt\_data\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting.

        ![Diagram of the Near Constant classifier.](../image/NearConstantDataModel.png)

    -   **Detected Constant**

        Enables checking near-constant metrics for anomalies. To do so, you must move the metrics to the detected-constant model, via a system token. To add tokens to the token list and enable more metrics to be measured for anomalies, contact customer support.

        Requires a minimum of 30 data points in the series, as set by the [corrupt\_data\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting.

        Enabled when the `metric_name_analysis.add_detected_constant_candidate` system property is set to **true**. To overwrite the value of this property for a specific metric type, update the **Detected Constant Candidate** field in the Metric Types table by doing the following:

        1.  Enter `sa_metric_type.list` in the instance navigation field.
        2.  In the **Detected Constant Candidate** column, select the relevant value for the entry you want to update.

<table id="table_vzz_wdz_wcc"><thead><tr><th>

Value

</th><th>

Description

</th></tr></thead><tbody><tr><td>

&lt;empty&gt;

</td><td>

An algorithm automatically decided whether the metric is to be considered for the detected constant model.This is the default value.

</td></tr><tr><td>

Yes

</td><td>

The metric is considered for the detected constant model.

</td></tr><tr><td>

No

</td><td>

The metric is not considered for the detected constant model.

</td></tr></tbody>
</table>    -   **Multinomial**

        Data pattern in which all values are one of a relatively small number of values. For example, values are always 100 or 99.9. For this classifier, there is no data model and no anomaly detection.

        Requires a minimum of 400 data points in the series, calculated as 10 times the value of the [multinomial\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting.

        ![Multinomial classifier](../image/MultinomialDataModel.png)

    -   **Corrupt**

        Data has insufficient data points to identify a pattern. For this classifier, there is no data model and no anomaly detection.

        Requires that the number of data points in the series is less than the value of the [corrupt\_data\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting \(30 by default\).

-   **Kalman Filter statistical model**

    Add on to the time series statistical model and applicable only to the noisy and positive noisy classifiers. This model is a general method of estimating model parameters from a stream of data where level is the only parameter in the model. The Kalman Filter model can adjust to new values in incoming metric data. When there are no clear patterns in the noise or if there is too much noise, the Kalman Filter model is not used.

    -   **Local level**

        When incoming data clusters around a new value according to the current control bounds, the Learner adjusts the data model to accommodate a permanent change. This clustering is detected as a new value in the data model so that most incoming data is again within the control bounds rather than anomalous. Such change detection is useful when for example, cores or memory are added to a server, which impact the baselines.

        Requires a minimum of 30 data points in the series, as set by the [corrupt\_data\_count\_threshold](../task/create-config-overriding-rule.md) configuration setting.

        ![Diagram of the Kalman Filter Local Level classifier.](../image/KalmanFilterLocalLevelDataModel.png)

    -   **Unrecognized**

        When data does not fit the local level classifier, time series classifiers are used. This happens when it is not possible to adjust the variance ratio in a learned local level model to reasonable values.

-   **Non-Parametric statistical model**

    Add on to the positive noisy classifier. In the nonparametric model, noise distribution is not symmetrical and does not fit any seasonal pattern. The nonparametric model creates control bounds that better fit the actual data, and once learned, the control bounds persist until the next learning cycle. This model does not adjust itself to changes in the data, and it takes longer for a deviation to be identified as an anomaly.

    -   **Stationary Non-Parametric**

        Data that is not time-dependent meaning that there is no significant shift in parameters such as mean and variance when shifting data in time.

        Requires a minimum of 5000 data points in the series, as set by the [snpm\_minimum\_data\_count](../task/create-config-overriding-rule.md) configuration setting.

        ![Diagram of the Non-Parametric Stationary classifier.](../image/NonParametricStationaryDataModel.png)

    -   **Unrecognized**

        When data does not fit the stationary classifier, time series classifiers are used.

-   **Median Absolute Deviation \(MAD\) statistical model**

    An add-on to the skewed noisy classifier. In this type of data, noise distribution is not symmetrical and does not fit any seasonal pattern. In addition, data reflects a heavy or long-tailed distribution. The MAD statistical model creates control bounds that better fit the data, and once learned, the control bounds persist until the next learning cycle. Using this model enhances the deciphering of data collection with approximately 30% greater efficiency.


