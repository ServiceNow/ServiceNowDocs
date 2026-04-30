---
title: Preview weight map - Legacy
description: You can preview a weight map to give you visibility of the generated metric weight map because it displays the accounts for the selected metric and the selected fiscal period with the percentage split for each account.
locale: en-US
release: yokohama
product: Financial Management
classification: financial-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Allocation metrics - Legacy, Financial Modeling - Legacy, Financial Management - Legacy, Project Portfolio Management, Strategic Portfolio Management]
---

# Preview weight map - Legacy

You can preview a weight map to give you visibility of the generated metric weight map because it displays the accounts for the selected metric and the selected fiscal period with the percentage split for each account.

## Before you begin

Role required: cost\_transparency\_admin or cost\_transparency\_analyst

## About this task

The Allocation workbench displays the expense summary for all months, quarters, or periods when you run the allocation and the window becomes cluttered with data for all quarters. To overcome the UI page clutter, you can preview the weight map in its own page.

## Procedure

1.  Navigate to **All** &gt; **Financial Modeling** &gt; **Consumption Metrics** &gt; **Preview Weight Maps**.

    1.  Alternatively, you can navigate to **Financial Modeling** &gt; **Consumption Metrics** &gt; **All Metrics**.
    2.  Click a cost allocation metric to open the Weighted Metric Builder.
    3.  Click **Preview Weight Map** .
2.  Select a metric from the **Metric** list in the left pane.

3.  Select a fiscal periodfrom the **Fiscal Period** list.

4.  Click **Generate**.

    The right pane displays the generated date and time details, the accounts, their respective weights, the total weight, and the percentage split. You can regenerate the weight map to preview each month or a quarter of a fiscal period.

5.  Click **Generate** or **Generate All** based on the metric that you have selected:

    -   Click **Generate** to roll up an account of a segment to a segment above in the hierarchy. Based on the metric that you have selected the amount is divided between the accounts of that rolled up segment.

    -   The **Generate All** button is enabled if you select a metric that defines rolling up of all the accounts individually in a segment using the **Enforce Relationships** option in the metric definition to one or more accounts of a segment above in the hierarchy.


**Parent Topic:**[Allocation metrics - Legacy](../concept/c_AllocationMetrics.md)

