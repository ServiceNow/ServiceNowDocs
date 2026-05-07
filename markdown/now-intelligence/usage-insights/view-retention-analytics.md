---
title: User retention
description: User retention reports help you understand how often your users visit your application to better understand if it meets your users' needs and expectations.Understand how Usage Insights calculates user and action retention.
locale: en-US
release: australia
product: Usage Insights
classification: usage-insights
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Using Usage Insights, Usage Insights, Platform Analytics]
---

# User retention

User retention reports help you understand how often your users visit your application to better understand if it meets your users' needs and expectations.

## Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

## About this task

View data such as how many new users you have, how many never returned, and how many returned the following day. User retention data also shows you the frequency of user sessions and the average time in between sessions given a certain time bucket. User retention analytics can help you, for example:

-   Use cohort analysis to identify a month, week, or day with poor retention.
-   Compare retention analytics across versions and devices.

![](../image/uxa-retention-overview-australia.png)

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics** &gt; **Usage Insights**.

2.  Choose the application that you want to review retention for from the **All Applications** list.

3.  Filter the data.

    The default filters are **Aggregation** \(daily, weekly, or monthly\), **Date Range**, and **Country**. For more information on filters in Usage Insights, see [Filter data in Usage Insights](../task/filter-user-list.md).

    |KPI|Description|
    |---|-----------|
    |New Users|Number of new users within the specified time bucket.|
    |Never returned|Percentage of users who never returned to use the app after their initial session.|
    |Returned after a day/week/month|Number of users who used the app in the specified aggregation period after their initial session.|
    |Time to second session|Average time interval between the first and the second sessions.|
    |Session frequency|Measures the average number of sessions within the selected time bucket \(daily/weekly/monthly\). For example, 25% of users used the app two times per day.|
    |Average time between sessions|Average times between initial and subsequent sessions.|

4.  Display the Retention cohort using different metrics.

    The Retention cohort is a heatmap that shows the number or percentage of users who started to use the app during the specified date range using the specified aggregation. In this example the **Aggregation** is `Weekly`, the **Date Range** is `Last 30 days`, and the measure is `Percentage`.![A user retention cohort showing the number of users, aggregated weekly, with a 30-day range.](../image/uxa-retention-cohort2.png)


## How retention is calculated

Understand how Usage Insights calculates user and action retention.

### User retention

User retention analysis groups new users and not the total number of users. A cohort includes every new user that uses the app within a defined time frame and selected date bucket \(daily/weekly/monthly\). A new user is only counted once per cohort, but can be included in more than one cohort.

For example, if looking at weekly cohorts, the numbers marked &lt;1 week, week 1, week 2, and week 3 along the top of the Retention cohort report indicate weekly buckets. The percentage under each weekly bucket represents the number of users who returned to use the application during that specific bucket.

The beginning and ending of each bucket is different for each new user in the cohort. The bucket marked **&lt;1 week** indicates a time frame before the first full week following the user's initial session. The dates the weeks start are on the left of the visualization. For example, if a user's initial session begins on November 16, and the first full week begins on November 18, then the retention information for the period in between is in the &lt;1 week column.

![UXA retention cohort example including <1 week content](../../../use/par-for-workspace/image/uxa-retention-cohort-ex.png)

### Action retention

Retention cohort analysis groups the number of users who performed the first action defined for the cohort, not the total number of application users. The cohort includes every user that uses the app and performs the first action within the defined time frame and date bucket \(daily/weekly/monthly\).

For example, if looking at weekly cohorts, the numbers marked 1, 2, 3 along the top of the retention report indicate weekly buckets. The percentage under each weekly bucket represents the number of users who returned to use the application and performed the second action during that specific bucket.

The beginning and ending of each bucket is different for each new user in the cohort. The bucket marked '1' indicates a time frame of seven days following the user's initial session. For example, if a user's initial session began at 10:00 on Sunday, bucket 1 for them begins at 10:00 on Sunday of the following week. Bucket 1 for the user extends from 7 through 13 days from their initial session.

A new user is only counted once per cohort, but can be included in more than one cohort. For example, if a weekly cohort is based on a login event, a customer who logs in at least once each week appears in every cohort.

When a user performs the second action, it’s counted for every first action that was performed within the time frame, not only the latest one. Each cohort cell is unique. If a user performs the second action twice within the same bucket, it’s counted once. When creating a cohort in which both steps are similar, every action acts both as a first and second action.

For example, a cohort has defined two similar login actions. If a user logged in three times – on Sunday, Monday, and Tuesday – the action performed on Monday is counted as the second action for the login on Sunday. It also opens a new cohort that the Tuesday action completes.

When filtering by application versions, the analysis shows only the users who performed their first action from the selected version.

