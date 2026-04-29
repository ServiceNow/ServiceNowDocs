---
title: Create a threshold for a metric definition
description: Evaluate the performance of your quantitative metric definition by defining a threshold for your metric definitions.
locale: en-US
release: australia
product: GRC: Risk Management Workspace
classification: grc-risk-management-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring metrics, GRC: Metrics in Integrated Risk Management, Risk Management, Governance, Risk, and Compliance]
---

# Create a threshold for a metric definition

Evaluate the performance of your quantitative metric definition by defining a threshold for your metric definitions.

## Before you begin

Role required: sn\_risk.admin or sn\_risk.manager

## About this task

Configure thresholds to define multiple performance levels, set specific ranges for each level, customize visual indicators, and configure automated actions that trigger when thresholds are breached. The threshold configuration supports both static values and dynamic percentage-based calculations.

## Procedure

1.  Navigate to **All** &gt; **Risk** &gt; **Risk Workspace** &gt; **Metrics** &gt; **Metrics**.

2.  Select and open the metric for which you want to define the threshold.

3.  Select the Thresholds related list.

4.  Select **New**.

5.  On the form, fill in the fields.

    For a description of the field values on the Metric Definition Threshold form, see [Metric Definition Threshold form](../reference/metric-definition-threshold-form-irm.md).

6.  Select **Submit**.

    The system automatically validates threshold configurations when you save. If validation errors occur, the system displays error messages indicating the specific field and recommended actions. Review these messages and correct the issues before resubmitting. 


## Result

The configured threshold is now active for the metric. The system monitors metric values and triggers the specified actions when threshold levels are exceeded. Metric values are displayed with the appropriate color indicators in dashboards, list pages, and record pages. When the Enable threshold breach monitoring check box is selected, the system prompts for justification when a threshold is breached. 

-   **[Metric Definition Threshold form](../reference/metric-definition-threshold-form-irm.md)**  
Use the Metric Definition Threshold form to define performance limits for a metric and control how the system responds when those limits are reached.

**Parent Topic:**[Configuring metrics](../concept/configuring-irm-metrics.md)

