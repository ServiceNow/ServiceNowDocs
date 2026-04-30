---
title: Create a configuration settings rule
description: Configuration settings affect how metric data is processed. Configuration settings rules override the default metric processing behavior to determine the system actions when an anomaly is detected.
locale: en-US
release: zurich
product: Agent Client Collector
classification: agent-client-collector
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 7
breadcrumb: [ACC deployment - endpoints, Agent Client Collector, IT Operations Management]
---

# Create a configuration settings rule

Configuration settings affect how metric data is processed. Configuration settings rules override the default metric processing behavior to determine the system actions when an anomaly is detected.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

A number of configuration settings determine the behavior of Metric Intelligence MID Servers. In the base system, these configuration settings are configured with default values, data types, and range of valid values. You cannot directly modify these configuration settings or add new ones. However, you can create a metric configuration rule with new configuration settings that override the default values on the MID Servers.

Then, manually apply these rules to all Metric Intelligence MID Servers in a single synchronization operation, or rely on an hourly system job to perform the synchronization.

To take effect, Metric Intelligence MID Servers must be synchronized with the updates to the configuration settings rules.

It is valid to have multiple rules for a setting that affect the same CIs, in which case:

-   Rules in which a filter is defined take precedence over a global rule in which no filter has been defined.
-   If multiple rules that affect the same set of CIs have the same priority, then only the latest rule to be defined is applied.
-   If multiple rules with different priorities affect the same set of CIs, then rules with the highest priority are applied.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Anomaly Detection** &gt; **Metric Config Rules**.

2.  On the Metric Configuration Rules pane, click **New**, and fill out the form.

<table id="table_lss_mpv_lz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Rule name.

</td></tr><tr><td>

Order

</td><td>

Rule priority within all other rules. Higher numbers represent higher priorities.

</td></tr><tr><td>

Filter by

</td><td>

Check box for displaying the **Rule** field, where you can specify conditions that CIs must meet for the rule to apply. For example, in the **choose field** list, select **Add Related Fields** and then add the filter **\[class\]\[is\]\[Linux Server\]**.

 If clear, the rule applies globally to all CIs in the Metric To CI Mapping \[sa\_metric\_map\] table.

</td></tr></tbody>
</table>3.  Right-click the form title, and click **Save**.

4.  In the Metric overridden configurations form section click **New**, fill out the form, and then click **Submit**.

<table id="table_ynj_bsv_lz"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Configuration setting for which to override its value. Click the ![Event Management icon](../image/LookupUsingList.png) icon to display the list of all configuration settings.

 Click the ![Event Management icon](../image/info.png) icon to display the **Metric Settings** dialog with details such as range of possible values.

 See the following tables \(Configuration Settings and Internal Configuration Settings\) for details about configuration settings.

</td></tr><tr><td>

Rule

</td><td>

Rule to which the created configuration setting applies.

</td></tr><tr><td>

Value

</td><td>

New value that overrides the default value for the specified configuration setting.

</td></tr></tbody>
</table>    You can modify the following configuration settings in the **Name** field.

    **Note:** The filter specified in the metric configuration rule does not apply to settings with a global scope.

<table id="table_nj5_tgl_pz"><thead><tr><th>

Name and Description

</th><th>

Values

</th><th>

Default

</th><th>

Data Type

</th><th>

Scope

</th></tr></thead><tbody><tr><td>

**anomaly\_detection\_enabled**

 Enable/disable anomaly detection.

 **Note:** If anomaly\_detection\_action\_level is set, then anomaly\_detection\_enabled is ignored.

</td><td>

N/A

</td><td>

true

</td><td>

boolean

</td><td>

CI/Metric

</td></tr><tr><td>

**anomaly\_detection\_action\_level**

 Action level of anomaly analysis and processing.

 For more information, see [Configure the action level for anomaly detection](../concept/configure-level-anomaly-detection.md).

</td><td>

choices:-   Metrics Only
-   Bounds
-   Anomaly Scores
-   Anomaly Alerts
-   IT Alerts


</td><td>

-   New records: Bounds
-   Upgraded records: Anomaly Alerts


</td><td>

choice

</td><td>

CI/Metric

</td></tr><tr><td>

**buffer\_anomaly\_eviction\_size**

 Maximum number of anomalies at individual metric level that can be stored in internal buffer before sending them to instance for every CI/Metric pair.

</td><td>

60–1440

</td><td>

60

</td><td>

integer

</td><td>

Global

</td></tr><tr><td>

**buffer\_ci\_score\_eviction\_size**

 Maximum number of anomalies at CI level that can be stored in internal buffer before sending them to instance \(Currently not being used\)

</td><td>

60–1440

</td><td>

60

</td><td>

integer

</td><td>

Global

</td></tr><tr><td>

**buffer\_metric\_eviction\_size**

 Maximum number of metrics that can be stored in internal buffer before sending them to instance for every CI/Metric pair.

</td><td>

60–1440

</td><td>

60

</td><td>

integer

</td><td>

Global

</td></tr><tr><td>

**connection\_login\_timeout\_secs**

 Maximum time in seconds to log in to the local database on MID Server.

</td><td>

30–60

</td><td>

30

</td><td>

integer

</td><td>

Global

</td></tr><tr><td>

**corrupt\_data\_count\_threshold**

 Minimum number of training points \(15-minute averages\) required to do any statistical analysis.

</td><td>

10–100

</td><td>

30

</td><td>

integer

</td><td>

Global

</td></tr><tr><td>

**deprioritize\_early\_batching\_of\_anomalous\_ci**

 Send anomalous CI information immediately or at regular interval.

</td><td>

N/A

</td><td>

false

</td><td>

boolean

</td><td>

Global

</td></tr><tr><td>

**mad\_model\_min\_days** Number of days for which data must be available to consider a Median Absolute Deviation based model.

</td><td>

10-120

</td><td>

10

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**max\_pool\_connections\_size** Maximum number of connections for local database pool.

</td><td>

10–50

</td><td>

25

</td><td>

integer

</td><td>

Global

</td></tr><tr><td>

**observation\_time\_min**

 Expected minimum metric observation interval.

</td><td>

1–1440

</td><td>

1

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**robust\_central\_percentage**

 Percentage of the residual data to compute the residual standard deviation, used for outlier detection. When set to 100 - uses the regular sample standard deviation.

</td><td>

50–100

</td><td>

90

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**sparse\_gap\_fraction\_threshold** If more than this percentage of data is missing and no other class has been identified, classify as SPARSE. Do not attempt to fit a WEEKLY model.

</td><td>

0–100

</td><td>

50

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**weekly\_model\_min\_days** Number of days for which data must be available in order to consider only a WEEKLY seasonality decomposition.

</td><td>

14-90

</td><td>

15

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**daily\_model\_min\_days** Number of days for which data must be available in order to consider only a DAILY seasonality decomposition.

</td><td>

2-90

</td><td>

3

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**build\_snpm\_model** Enable/disable building an SNPM data model.

</td><td>

N/A

</td><td>

true

</td><td>

boolean

</td><td>

CI/Metric

</td></tr><tr><td>

**snpm\_minimum\_data\_count**

 Minimum number of data points required for building a stationary nonparametric model.

</td><td>

0 – 1e9

</td><td>

5000

</td><td>

integer

</td><td>

CI/Metric

</td></tr></tbody>
</table>    The following configuration settings are for internal usage.

<table id="table_g4w_v3l_pz"><thead><tr><th>

Name and Description

</th><th>

Values

</th><th>

Default

</th><th>

Data Type

</th><th>

Scope

</th></tr></thead><tbody><tr><td>

**anomaly\_memory\_time\_min**

 Anomaly score calculator parameter: Memory time for abnormal situation.

</td><td>

1–600

</td><td>

45

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**excess\_z\_score**

 Anomaly score calculator parameter: Minimal anomalousness accumulated for outlier.

</td><td>

0–3

</td><td>

0.8

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**linear\_accumulator\_threshold**

 Decision Tree Threshold: ACCUMULATOR analysis

</td><td>

0.5–5

</td><td>

1

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

l**ow\_freq\_power\_threshold**

 Decision Tree Threshold: WEEKLY analysis

</td><td>

0–100

</td><td>

50

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**low\_variability\_threshold**

 Decision Tree Threshold: TRENDY analysis

</td><td>

0.0000000001–0.001

</td><td>

0.0001

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**mid\_freq\_power\_threshold**

 Decision Tree Threshold: WEEKLY analysis

</td><td>

0–100

</td><td>

33

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**multinomial\_count\_threshold**

 Decision Tree Threshold: MULTINOMIAL analysis

</td><td>

1–1000

</td><td>

40

</td><td>

integer

</td><td>

Global

</td></tr><tr><td>

**non\_zero\_diff\_threshold**

 Decision Tree Threshold: NEAR\_CONSTANT analysis

</td><td>

0–100

</td><td>

5

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**normal\_memory\_time\_min**

 Anomaly score calculator parameter: Memory time for normal situation.

</td><td>

1–600

</td><td>

1

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**normal\_probability\_ewma\_timescale\_min**

 Anomaly score calculator parameter: Normal assessment time-scale.

</td><td>

1–600

</td><td>

15

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**normal\_probability\_weight**

 Anomaly score calculator parameter: Normal assessment adjustment factor.

</td><td>

0–1

</td><td>

1

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**sigmoid\_offset**

 Anomaly score calculator parameter: Anomalousness to score conversion.

</td><td>

0–5

</td><td>

2.1

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**sigmoid\_weight**

 Anomaly score calculator parameter: Anomalousness to score conversion.

</td><td>

0–5

</td><td>

1.2

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**tiny\_variability\_threshold**

 Decision Tree Threshold: NEAR\_CONSTANT analysis

</td><td>

0–0.001

</td><td>

0.0000000001

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**weekly\_peak\_hi\_limit**

 Decision Tree Threshold: WEEKLY analysis.

</td><td>

7–14

</td><td>

10

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**weekly\_peak\_lo\_limit**

 Decision Tree Threshold: Weekly analysis.

</td><td>

0.5–7

</td><td>

0.7

</td><td>

double

</td><td>

Global

</td></tr><tr><td>

**weekly\_vs\_daily\_log\_likelihood\_threshold**

 By how much log likelihood of weekly needs to be larger than daily, to be the preferred statistical model.

</td><td>

100–1000

</td><td>

200

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**daily\_vs\_noisy\_log\_likelihood\_threshold**

 By how much log likelihood of daily needs to be larger than noisy, to be the preferred statistical model.

</td><td>

20–1000

</td><td>

200

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**weekly\_vs\_noisy\_log\_likelihood\_treshold**

 By how much log likelihood of weekly needs to be larger than noisy, to be the preferred statistical model.

</td><td>

100–1000

</td><td>

200

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**trendy\_vs\_noisy\_log\_likelihood\_threshold**

 By how much log likelihood of trendy needs to be larger than noisy, to be the preferred statistical model.

</td><td>

10–1000

</td><td>

50

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**seasonal\_loess\_width\_in\_hours**

 Applied to the seasonal component of a weekly or daily model before making a forecast of future behavior. If set to 0, each data point in the seasonal model becomes independent of the rest of the data points.

</td><td>

6–24

</td><td>

12

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**robustness**

 Affects how outliers contribute to seasonal and trend calculations.

</td><td>

N/A

</td><td>

true

</td><td>

boolean

</td><td>

CI/Metric

</td></tr><tr><td>

**snpm\_min\_value\_threshold**

 Minimum value of data required for building an SNPM model.

</td><td>

-1e9 – 1e9

</td><td>

0

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**snpm\_max\_observation\_interval\_in\_sec**

 Maximum expected observation interval required for building an SNPM model.

</td><td>

60 – 600000

</td><td>

120

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**min\_std\_jump\_fraction**

 Minimum ratio of locally calculated observation noise level to typical jump size that justifies recalculating a larger observation noise variance.

</td><td>

0.0 – 1.0

</td><td>

0.2

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**dynamic\_threshold\_error\_smoothing**

 Whether to use exponentially weighted moving average to smooth the residuals in the dynamic threshold analysis.

</td><td>

N/A

</td><td>

true

</td><td>

boolean

</td><td>

CI/Metric

</td></tr><tr><td>

**ewma\_alpha**

 The alpha value of the exponentially weighted moving average in dynamic threshold analysis.

</td><td>

1e-15 – 1.0

</td><td>

0.02739726027

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**dynamic\_threshold\_beginning\_smoothing\_length**

 Number of smoothed data points to set to the mean of double the smoothing length.

</td><td>

0 – 10000

</td><td>

250

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**dynamic\_threshold\_error\_buffer\_minutes**

 Number of data points around each outlier to group together.

</td><td>

1 – 1000

</td><td>

30

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**dynamic\_threshold\_search\_start**

 Start value at which the optimal control factor is looked for.

</td><td>

0.5 – 20.0

</td><td>

3.0

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**dynamic\_threshold\_search\_interval**

 Interval between search values of optimal control factor.

</td><td>

0.1 – 5.0

</td><td>

0.5

</td><td>

double

</td><td>

CI/Metric

</td></tr><tr><td>

**dynamic\_threshold\_search\_count**

 Number of values required for searching for optimal control factor.

</td><td>

1 – 50

</td><td>

19

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**dynamic\_threshold\_error\_sequence\_limit**

 Maximum number of error groups for a particular control factor value when searching.

</td><td>

1 – 20

</td><td>

5

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**dynamic\_threshold\_minimum\_data\_count**

 Minimum number of raw data points needed before attempting dynamic thresholding.

</td><td>

1 – 10000

</td><td>

5000

</td><td>

integer

</td><td>

CI/Metric

</td></tr><tr><td>

**linear\_seasonal\_log\_likelihood\_threshold**

 Threshold used in deciding whether to prefer a fitted model with linear seasonality over a model with a periodic component.

</td><td>

10-5000

</td><td>

1000

</td><td>

integer

</td><td>

CI/Metric

</td></tr></tbody>
</table>
**Related topics**  


[Configure multiple MID Servers to work with Agent Client Collector Monitoring](../../agent-client-collector/task/configure-multiple-mid-acc-monitoring.md)

