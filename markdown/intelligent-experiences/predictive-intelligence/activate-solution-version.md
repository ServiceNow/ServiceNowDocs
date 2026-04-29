---
title: Activate a solution version
description: Predictive Intelligence activates the most recent version of the solution when it completes training a solution. However, you can activate any previously trained solution version. Only one solution version can be active at a time, and only the active version is used when making predictions.
locale: en-US
release: australia
product: Predictive Intelligence
classification: predictive-intelligence
topic_type: task
last_updated: "2026-03-24"
reading_time_minutes: 1
breadcrumb: [Configure Predictive Intelligence, Predictive Intelligence, Enable AI experiences]
---

# Activate a solution version

Predictive Intelligence activates the most recent version of the solution when it completes training a solution. However, you can activate any previously trained solution version. Only one solution version can be active at a time, and only the active version is used when making predictions.

## Before you begin

-   Manually train a solution multiple times or set a training schedule.
-   Role required: admin or ml\_admin

## About this task

The system creates a solution version each time you train a solution definition. Typically, you manually create a solution version only when you change the solution definition filter and want to test it. Otherwise, most solution versions are created during scheduled solution training.

## Procedure

1.  Navigate to **All** &gt; **Predictive Intelligence** &gt; **Classification** &gt; **Solutions** or **Predictive Intelligence** &gt; **Similarity** &gt; **Solutions** or **Predictive Intelligence** &gt; **Clustering** &gt; **Solutions** or **Predictive Intelligence** &gt; **Regression** &gt; **Solutions** .

2.  In the list view of the ML Solutions table, find the row that you want to activate, then select the value in the first column to open the individual record.

    You can also open the individual record by selecting the row's reference lookup icon ![Lookup icon](../../../common/image/Form_ReferenceLookupIcon.png), then selecting **Open Record**.

3.  In the solution record, select **Activate**.

    The system activates this solution version and deactivates any other solution version.


## What to do next

For classification solutions, [review the trained solution precision and coverage statistics](review-solution-statistics.md). For similarity solutions, [review the similarity examples](review-similarity-examples.md).

**Parent Topic:**[Configure Predictive Intelligence](configure-predictive-intelligence.md)

