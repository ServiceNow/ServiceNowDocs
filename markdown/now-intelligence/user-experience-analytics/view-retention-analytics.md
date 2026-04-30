---
title: User retention
description: User retention reports can help you understand if your app meets your users' needs and expectations, and enables you to measure how your app optimization efforts impact user retention.Understand how Analytics calculates user and action retention.
locale: en-US
release: xanadu
product: User Experience Analytics
classification: user-experience-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Using User Experience Analytics, User Experience Analytics, Platform Analytics]
---

# User retention

User retention reports can help you understand if your app meets your users' needs and expectations, and enables you to measure how your app optimization efforts impact user retention.

## Before you begin

Role required: analytics\_admin, mobile\_analytics\_admin, web\_analytics\_admin, or portal\_analytics\_admin

## About this task

View data such as how many new users you have, how many never returned, and how many returned the following day. User retention data also shows you the frequency of user sessions and the average time in between sessions given a certain time bucket. User retention analytics can help you, for example:

-   Use cohort analysis to identify a month, week, or day with poor retention.
-   Compare retention analytics across versions and devices.

![Analytics module - User Retention screen](../image/retention-overview.png)

## Procedure

1.  Navigate to **All** &gt; **Analytics** &gt; **Retention**.

2.  Select whether to view **Daily**, **Weekly**, or **Monthly** insights.

    |KPI|Description|
    |---|-----------|
    |New Users|Number of new users within the specified time bucket.|
    |Never returned|Percentage and number of users who never returned to use the app after their initial session.|
    |Returned after a day/week/month|Percentage and number of users who used the app on the following week after their initial session.|
    |Time to 2nd session|Average time interval between the first and the second session.|
    |Sessions Frequency|Measures the average number of sessions within the selected time bucket \(daily/weekly/monthly\). For example, 25% of users used the app two times per day.|
    |Average Time Between Sessions|Average times between initial and subsequent sessions.|
    |Retention Cohort Analysis|Shows the number of new users who started to use the app during a specified time bucket, and the number who returned to use the app during a later week.|


## How retention is calculated

Understand how Analytics calculates user and action retention.

### User retention

User retention analysis groups new users and not the total number of users. A cohort includes every new user that uses the app within a defined time frame and selected date bucket \(daily/weekly/monthly\). A new user is only counted once per cohort, but can be included in more than one cohort.

For example, if looking at weekly cohorts, the numbers marked 1, 2, 3 along the top of the retention report indicate weekly buckets. The percentage under each weekly bucket represents the number of users who returned to use the application during that specific bucket.

The beginning and ending of each bucket is different for each new user in the cohort. The bucket marked '1' indicates a time frame of seven days following the user's initial session. For example, if a user's initial session began at 10:00 on Sunday, bucket 1 for them begins at 10:00 Sunday of the following week. Bucket 1 for the user extends from 7 through 13 days from their initial session.

### Action retention

Retention cohort analysis groups the number of users who performed the first action defined for the cohort, not the total number of application users. The cohort includes every user that uses the app and performs the first action within the defined time frame and date bucket \(daily/weekly/monthly\).

For example, if looking at weekly cohorts, the numbers marked 1, 2, 3 along the top of the retention report indicate weekly buckets. The percentage under each weekly bucket represents the number of users who returned to use the application and performed the second action during that specific bucket.

The beginning and ending of each bucket is different for each new user in the cohort. The bucket marked '1' indicates a time frame of seven days following the user's initial session. For example, if a user's initial session began at 10:00 on Sunday, bucket 1 for them begins at 10:00 Sunday of the following week. Bucket 1 for the user extends from 7 through 13 days from their initial session.

A new user is only counted once per cohort, but can be included in more than one cohort. For example, if a weekly cohort is based on a login event, a customer who logs in at least once each week appears in every cohort.

When a user performs the second action, it is counted for every first action that was performed within the timeframe, not only the latest one. Each cohort cell is unique. If a user performs the second action twice within the same bucket, it is counted once. When creating a cohort in which both steps are similar, every action acts both as a first and second action.

For example, a cohort has defined two similar login actions. If a user logged in three times – on Sunday, Monday, and Tuesday – the action performed on Monday is counted as the second action for the login on Sunday. It also opens a new cohort that the Tuesday action completes.

When filtering by application versions, the analysis shows only the users who performed their first action from the selected version.

