---
title: Add or modify another user's personal target or threshold
description: If you can create global targets or thresholds, you can modify or add personal targets and thresholds for any user.
locale: en-US
release: yokohama
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Targets and thresholds, Configuring fundamentals, Performance Analytics \(Indicator data sources\), Platform Analytics]
---

# Add or modify another user's personal target or threshold

If you can create global targets or thresholds, you can modify or add personal targets and thresholds for any user.

## Before you begin

Role required: pa\_target\_admin, pa\_threshold\_admin, pa\_power\_user

## About this task

You can either look up the personal targets or thresholds of a user or create a new target or threshold and assign it to a user.

## Procedure

1.  Navigate to **Performance Analytics** &gt; **Targets** or **Performance Analytics** &gt; **Thresholds**.

2.  To open an existing personal threshold or target to modify, follow these steps:

    1.  Search the records by the Owner.

    2.  When you find the target or threshold that you want to modify, select the info icon ![](../../dashboards/image/IconInformation.png) on the row for that target or threshold record.

        ![Opening the preview of a target record.](../image/target-record-open-preview.png)

        The preview for that target or threshold record appears.

    3.  In the preview, select **Open Record**.

        The previewed record opens.

3.  To create a new personal threshold or target, follow these steps:

    1.  In the Targets or Thresholds list, select **New**.

    2.  In the target or threshold form that opens, specify the **Owner**.

        The owner is the only person who will see this target or threshold in the indicator's KPI Details or Analytics Hub.

        For a threshold, instead of selecting a single owner, you can specify several users in a related list. All of these users will see this threshold in the KPI Details and Analytics Hub of the indicator.

4.  Specify or change the **Indicator** and any breakdowns, breakdown elements, or time series aggregation for the target or threshold.

5.  Complete any other relevant fields.

6.  If you are creating a new target, save it.

    The Target values related list appears.

7.  For a target, alter the start date, review date, or value of any existing target value, or select **New** to create a new target value.

    You can have more than one target value, but the date ranges between start and review cannot overlap.


**Parent Topic:**[Performance Analytics targets and thresholds](../concept/pa-targets-thresholds.md)

