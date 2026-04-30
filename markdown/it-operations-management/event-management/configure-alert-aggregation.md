---
title: Configure pattern based alert aggregation
description: Configure the Alert Aggregation Learner \(Service Analytics Alert Aggregation Learner - Daily\), which is an offline job that runs daily to process past alerts. The Alert Aggregation Learner identifies patterns of related alerts using a combination of pattern-based and probabilistic techniques.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Automated alert grouping, Alert grouping types, Alert grouping, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Configure pattern based alert aggregation

Configure the Alert Aggregation Learner \(**Service Analytics Alert Aggregation Learner - Daily**\), which is an offline job that runs daily to process past alerts. The Alert Aggregation Learner identifies patterns of related alerts using a combination of pattern-based and probabilistic techniques.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

-   The Alert Aggregation Learner tracks manual additions and removals of alerts from automated alert groups.
-   The Alert Aggregation Learner also learns the patterns of alerts in manual alert groups. Later, when new streams of alerts arrive, alert aggregation automatically forms automatic alert groups according on these patterns.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Alert Corrlelation Properties**.

2.  Enable the following properties.

    -   Enable alert aggregation for Automated, CMDB, and Text-based groups \(**sa\_analytics.aggregation\_enabled**\).

        **Note:** When disabled, disables all other groups.

    -   Enable alert aggregation for CI-based Automated groups \(**sa\_analytics.specific\_patterns\_enabled**\).
3.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

4.  On the System Properties page, select the **sa\_analytics.agg.learner\_period\_days** property.

    If the property doesn't exist, you need to define it.

5.  Set the property's **Value** to the number of days by which you want alert aggregation learner job to process.

    Values larger than 30 days increase the job processing time. Use values of 30 days or less for best performance.


