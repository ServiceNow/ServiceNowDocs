---
title: Create an anomaly test rule
description: To use the anomaly model testing, create an anomaly test rule in which you specify up to 20 metric series to test anomaly detection for. Run the anomaly test, and after it completes, use the provided URL to open the Insights Explorer which is pre-loaded with the model testing results.
locale: en-US
release: zurich
product: Metric Intelligence
classification: metric-intelligence
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Optimizing Metric Intelligence, Metric Intelligence, IT Operations Management]
---

# Create an anomaly test rule

To use the anomaly model testing, create an anomaly test rule in which you specify up to 20 metric series to test anomaly detection for. Run the anomaly test, and after it completes, use the provided URL to open the Insights Explorer which is pre-loaded with the model testing results.

## Before you begin

Role required: evt\_mgmt\_user

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Anomaly Detection** &gt; **Anomaly Model Testing**.

2.  Select an existing anomaly test rule to edit and run again, or click **New** and fill out the Anomaly Test Rules form.

    |Field|Description|
    |-----|-----------|
    |Name|Name for the model test rule.|
    |Applies to|The table from which to select CI/metric pairs for the model test rule. The table used is Metric To CI Mapping \[sa\_metric\_map\].|
    |Rule|Filter conditions to specify pairs of CIs/metrics for the anomaly model testing. If the rule yields more than 20 pairs of CIs/metrics, then the list is truncated to 20.|
    |Start date/End data|The time period for which to apply the anomaly detection testing. The time period must be within the past 7 days.|
    |Status|Status of the test, automatically updated by the system during a test run. Status is initially Scheduled and eventually changes to Complete.|
    |URL|URL to the Insights Explorer in which the anomaly model test results are pre-loaded.|
    |Notes|Logging summary, automatically updated by the system with details of each test run of the anomaly test rule.|

3.  Click **Run Anomaly Test**.

    During the test run, the **Status**, **URL**, and **Notes** fields are automatically updated to reflect the progression of the job.

4.  After **Status** changes to Complete, click the **URL** link to open the Insights Explorer to see the results of the test.


## Result

The bounds and the chart for the anomaly model test, appear in faint colors in Insights Explorer. Also, the upper and lower bounds that are calculated by the test, use a line pattern that is different than line pattern used for actual anomaly detection results. These differences let you distinguish between actual anomaly detection and anomaly model test results, if both are selected in the chart settings. ![Anomaly Model Testing results, which appear in faint colors compared to results of actual anomaly detection.](../image/AnomalyModelTestResult.png)

## What to do next

-   Modify the date range for the test or choose different time series, and click **Run Anomaly Test** again to continue and fine-tune the model.
-   Click the **Chart Settings** icon for a chart to toggle the display of statistics and aggregations on the chart. Select **Show Bounds** and **Show Anomaly Scores** in the Anomaly Test Statistics and in the Anomaly Statistics sections, to display test results next to actual anomaly detection results.

    **Note:** Anomaly Model Testing results might be very similar to actual anomaly detection results. If you configure the chart to display both at the same time, as you move the mouse over the chart, it might be difficult to identify points of differences.

-   When you are satisfied with the anomaly test results, enable anomaly detection in the production environment, for the metrics and CIs specified in the test. See [Choose and configure metrics to monitor](configure-metric-monitors.md) for more details.

**Parent Topic:**[Optimizing Metric Intelligence](../../metric-intelligence/concept/optimizing-metric-intelligence.md)

**Related topics**  


[View metric values in the Insights Explorer](view-metrics-explorer.md)

