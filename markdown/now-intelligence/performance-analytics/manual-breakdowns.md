---
title: Manual breakdowns
description: In a manual breakdown, you define the breakdown elements and the indicator scores for each element manually instead of using records from a breakdown source.Create a breakdown for an indicator where you add scores manually.Associate a manual indicator with a manual breakdown to enable users to enter broken-down scores for the indicator.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Indicator breakdowns, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Manual breakdowns

In a manual breakdown, you define the breakdown elements and the indicator scores for each element manually instead of using records from a breakdown source.

Unlike an automated breakdown, a manual breakdown does not map to any fields on the indicator source table. Instead, users must populate the broken-down scores manually.

**Parent Topic:**[Indicator breakdowns](c_CreatingBreakdowns.md)

## Create a manual breakdown

Create a breakdown for an indicator where you add scores manually.

### Before you begin

Roles required: pa\_data\_collector, pa\_power\_user, pa\_admin, or admin

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Manual Breakdowns**.

2.  Click **New**.

    The **Type** is set to **Manual** automatically.

3.  Enter a descriptive **Name**.

4.  Right-click the form header and select **Save**.

5.  In the **Manual** section, double-click **Insert a new row** to add a new breakdown element.

6.  Press Enter or click the green check mark to save the entry.

7.  Change the **Order** value.

    Elements with a lower **Order** value appear higher in the list of elements, such as on the Analytics Hub and dashboards.

8.  Repeat steps 5-7 to add additional breakdown elements.

9.  Click **Submit**.


### What to do next

Associate manual indicators with this breakdown and populate scores using the scoresheet.

## Assign a manual indicator to a manual breakdown

Associate a manual indicator with a manual breakdown to enable users to enter broken-down scores for the indicator.

### Before you begin

Role required: pa\_data\_collector, pa\_power\_user, pa\_admin, or admin

### About this task

**Note:** You can break down manual indicator scores by only one breakdown at a time. You cannot apply a 2nd-level breakdown to a manual indicator.

### Procedure

1.  Navigate to **All** &gt; **Performance Analytics** &gt; **Manual Breakdowns**.

2.  Select a breakdown record.

3.  In the **Indicators** related list, click **Edit**.

4.  Use the slushbucket to select the indicators you want to assign to this breakdown.

5.  Click **Save**.

6.  In the **Indicator Breakdowns** related list, set the **Display** value to false to hide the breakdown on the Analytics Hub and dashboard widgets.

    If the **Display** field is false, broken-down scores are still populated during data collection, but the breakdown is not selectable on the Analytics Hub or on dashboard widgets.


### What to do next

Populate broken-down scores for the indicators using the scoresheet.

