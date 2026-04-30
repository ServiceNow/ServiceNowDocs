---
title: Compare scores
description: In the Analytics Hub Compare tab, compare scores on any two dates, or compare scores against linked benchmark scores.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Analytics Hub for a specific indicator, Analytics Hub, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Compare scores

In the Analytics Hub Compare tab, compare scores on any two dates, or compare scores against linked benchmark scores.

![The compare tab of the Analytics Hub showing the changes in scores between two dates](../image/detailed-scorecard-compare.png "Compare tab")

**Note:** The Compare tab is available only for automated indicators.

You can compare the scores of an automated indicator on two dates. Date selection works the same way as in the Overview tab. Furthermore, any dates selected on one tab persist when you change to another tab.

If the scores refer to a count, below the scores, you see the following information, from left to right:

-   The score on the earlier date
-   The number of records that have moved out, or left the indicator since the earlier date
-   The number of records that are shared by the indicator on both dates, meaning the records are in the indicator on both the earlier and later date
-   The number of records that moved in, or were added to the indicator on the later date
-   The number of records on the latest date

A list of records in the indicator is in the lower pane. If you are comparing dates, click the graph icon \(![](../image/ah-activity-stream-icon.png)\) to open the Activity Stream. The Activity Stream shows, for each record, the fields most relevant to the latest activity on the record and its current state. Hovering the cursor over the timestamp of an activity reveals the **Comment** link. This link opens a dialog where you can leave either an Additional Comment or a Work Note.

**Note:** If you apply a time series aggregation to the indicator, you cannot compare records. The scores are aggregated, but the underlying records are not. You can compare aggregated scores.

![The activity stream showing the Comment dialog](../image/ah-activity-stream-comment.gif "Activity stream")

If the indicator is linked to a benchmark indicator, select **Benchmarks** to compare the two indicators. Select a date range for comparing the indicators as you would in the **Overview** tab.

![If a benchmarked indicator is linked to the indicator of the Analytics Hub, click Benchmarks to compare the indicators](../image/detailed-scorecard-benchmarks.png "Comparing the indicator to a linked benchmark indicator")

**Related topics**  


[Link an automated indicator to a benchmark](../task/link-automated-indicator-benchmark.md)

