---
title: Configure pattern based alert grouping
description: Configure the Alert Aggregation Learner \(Service Analytics Alert Aggregation Learner - Daily\), an offline job that runs daily to process past alerts. It identifies patterns of related alerts using a combination of pattern-based and probabilistic techniques, enabling quicker detection and resolution of recurring issues.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Automated alert grouping, Alert grouping types and creation methods, Alert grouping, Configuring Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Configure pattern based alert grouping

Configure the Alert Aggregation Learner \(Service Analytics Alert Aggregation Learner - Daily\), an offline job that runs daily to process past alerts. It identifies patterns of related alerts using a combination of pattern-based and probabilistic techniques, enabling quicker detection and resolution of recurring issues.

## Before you begin

Role required: evt\_mgmt\_admin

## About this task

The Alert Aggregation Learner tracks manual additions and removals of alerts from automated alert groups. If you undo any previous alert additions or removals, the automatic process adjusts accordingly.

You can review user additions and removals from automated alert groups and undo any action to prevent it from being automatically repeated. The Alert Aggregation Learner also identifies patterns in manual alert groups, enabling automatic formation of new alert groups based on these patterns when new streams of alerts arrive.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Administration** &gt; **Alert Corrlelation Properties**.

2.  Enable the following properties.

    -   Enable alert aggregation for Automated, CMDB, and Text-based groups \(**sa\_analytics.aggregation\_enabled**\).

        **Note:** When disabled, disables all other groups.

    -   Enable ML based Automation correlation \(**sa\_analytics.specific\_patterns\_enabled**\).
3.  To configure the time period for the Alert Aggregation Learner to process alerts, perform the following steps:

    1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.
    2.  On the System Properties page, select the **sa\_analytics.agg.learner\_period\_days** property.

        If the property doesn't exist, you need to define it.

    3.  Set the property's **Value** to the number of days by which you want alert aggregation learner job to process.

        **Note:** Values larger than 30 days increase job processing time. For optimal performance, use values of 30 days or less.


