---
title: Add or edit indicator scores manually
description: You can manually enter score data for automated and manual indicators. Exercise care when editing scores for automated indicators.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Collecting indicator scores, Configure advanced features, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Add or edit indicator scores manually

You can manually enter score data for automated and manual indicators. Exercise care when editing scores for automated indicators.

## Before you begin

Role required: pa\_contributor, pa\_admin, pa\_power\_user, or admin

## About this task

You typically add scores manually for indicators that require an update only once a month or less often. In addition, if data cannot be collected automatically for some entities, like customers, you can manually enter or import data.

You can manually overwrite data that a job collected. However, the next time that a job is run that collects this data, the manually entered data is overwritten in turn.

**Note:**

-   Auditing does not track manual changes to the scoresheet. Manual inserts, updates, and deletions are not audited, even when auditing is enabled at the Dictionary level for all pa\_scores tables.
-   You cannot edit scores manually for formula indicators.

## Procedure

1.  Navigate to **Performance Analytics** &gt; **Scoresheet** &gt; ****.

2.  Select the indicator for which you want to enter manual scores.

3.  Change the selected date by clicking the left or right arrows around the date range, or click the date range to select a new range.

4.  Fill in the main scores for the indicator in the **Indicator Scores** row.

    Alternatively, if an indicator contains breakdowns, fill in the indicator scores per breakdown element.

    **Note:** A percentage bar above each column of scores indicates the percentage of breakdown elements that contain scores. A value of 0 counts as a score; only the absence of any value counts as empty.

    1.  Click **Aggregate scores**.

    2.  Choose whether you want to use the **Sum** or the **Average** of a specific breakdown to calculate the main scores for the indicator.

    3.  Select the breakdown to aggregate, such as **Priority**, and click **Apply**.

        All scores for that breakdown are totaled or the average is calculated for them.

        For automated indicators that collect a second-level breakdown and are based on two or more breakdown sources, multi-level breakdown scores can be entered in the scoresheet. For example, for Open incidents by workgroup by priority, you can enter both scores for the elements of workgroup \(first level\) and the elements of priority \(second level\). Aggregations for these indicators are calculated in the same way as other breakdowns.


**Parent Topic:**[Collecting indicator scores](../concept/c_ClctData.md)

**Related topics**  


[Manual indicators](t_CreateAManualIndicator.md)

