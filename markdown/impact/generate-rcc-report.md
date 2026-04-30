---
title: Generate RCC report
description: Generate a detailed Root Cause Correlation report that can be used to identify and narrow down underlying issues in your instance that caused a performance degradation and related alert.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Root Cause Correlation, Alerts in Instance Observer, Impact Instance Observer, Platform Health, Impact Delivery Instance \(formerly Impact Digital Experience\), Impact]
---

# Generate RCC report

Generate a detailed Root Cause Correlation report that can be used to identify and narrow down underlying issues in your instance that caused a performance degradation and related alert.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **Impact** &gt; **Platform Health** &gt; **Monitor** &gt; **Instance Observer**.

2.  From the **Performance** menu, select **Semaphores**.

    ![The Instance Observer Performance menu options.](../image/io-perf-rcc.png)

3.  Select the report options.

    ![RCC report options for selection.](../image/rcc-config-options.png)

    -   Instance: Only production instances are supported with the RCC feature.
    -   Metrics: Select from the available metrics for RCC report generation. Refer to the RCC symptom categories section in [Root Cause Correlation](root-cause-correlation.md) for the supported metrics.
    -   Date Range: Select a date range
    -   Options: Select the type of alert. For RCC, Self Service Alerts is supported.
    -   Select the Node type: Options are available in the list.
4.  Select **Get Snapshot** to generate the RCC report.

    ![Displays the RCC report for the selected parameters.](../image/io-rcc-semaphore-report.png)

5.  Select an alert icon from the report to review additional information about the issue.

    ![RCC report alert icons.6](../image/io-rcc-alert.png)

    **Note:** Options available on Report and Charts:

    -   Select a data point to view additional actions or remove the entry.
    -   Right-click to isolate a data point.
    -   Select and drag across the chart to drill down.
    -   Download to PNG, SVG, or CSV files or view transactions on the instance.
    -   Change the report type.
    The information for the RCC alert is displayed with the option to generate the root cause of the alert.

6.  Select **Generate Root Cause**.

    ![RCC details and option to select to Generate root cause.](../image/rcc-generate-rootcause.png)

    A status message displays with RCC generation information.

    ![RCC report generation status message.](../image/rcc-in-progress.png)


## What to do next

Check the RCC History page to further investigate the issues that caused the alert to trigger. See [Utilizing RCC history to perform root cause analysis](utilizing-rcc-reports-perform-root-cause-analysis.md) for more information.

