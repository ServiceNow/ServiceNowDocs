---
title: Create a threshold for a metric
description: Create thresholds for metrics and metric definitions to monitor performance. Thresholds serve as reference points based on specific criteria. Each threshold can be assigned a unique color and configured with conditions and subsequent actions.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Configuring GRC: Metrics, GRC: Metrics, Operational Sustainability Management \(formerly Environmental, Social, and Governance\)]
---

# Create a threshold for a metric

Create thresholds for metrics and metric definitions to monitor performance. Thresholds serve as reference points based on specific criteria. Each threshold can be assigned a unique color and configured with conditions and subsequent actions.

## Before you begin

Role required: sn\_esg.admin, sn\_esg.program\_manager, or sn\_esg.metrics\_manager

**Note:** Thresholds can only be applied to quantitative metric definitions. 

## About this task

Configure thresholds to define multiple performance levels, set specific ranges for each level, customize visual indicators, and configure automated actions that trigger when thresholds are breached. The threshold configuration supports both static values and dynamic percentage-based calculations.

## Procedure

1.  Navigate to **All** &gt; **Operational Sustainability Management** &gt; **Operational Sustainability Workspace** &gt; **Metrics**.

2.  Open the quantitative metric definition for which you want to add thresholds.

3.  Select the Thresholds related list.

4.  Select **New**.

5.  On the form, fill in the fields.

    For a description of the field values, see [Metric Threshold form fields](../../esg-management-reporting/reference/metric-threshold-form-fields.md).

6.  Select **Submit**.

    -   If the threshold configuration validation is successful, the threshold is saved and becomes active based on the configured settings.
    -   If validation errors occur, the system displays error messages indicating the specific field and recommended actions. Review these messages and correct the issues before resubmitting.
    The configured threshold is now active for the metric. When the Enable threshold breach monitoring check box is selected, the system monitors metric values and immediately triggers the specified actions when threshold levels are exceeded. Metric values are displayed with the appropriate color indicators in dashboards and reports.


**Parent Topic:**[Configuring GRC: Metrics](../concept/configuring-grc-metrics.md)

