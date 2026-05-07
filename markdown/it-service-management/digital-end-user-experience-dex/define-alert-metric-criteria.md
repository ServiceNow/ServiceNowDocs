---
title: Define alert criteria
description: Specify alert metric criteria by choosing alert severity, defining thresholds, and specifying conditions for when the alert must be triggered.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Creating a metric rule, Alert rules, Configure, Digital End-User Experience, IT Service Management]
---

# Define alert criteria

Specify alert metric criteria by choosing alert severity, defining thresholds, and specifying conditions for when the alert must be triggered.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  In the **Alert severity** field, select a severity for the alert.

2.  Define the thresholds for the alert.

    The predetermined metrics types are based on the configuration item \(CI\).

3.  Add another alert severity level by selecting **Add another alert severity**.

4.  Select the **Set the threshold for users \(optional\)** check box and define the criteria based on the number of impacted users to trigger the alert.

5.  In the Alert when section, perform one of the following steps.

    -   Select a time period for the **All sampled values must breach the criteria in the following time period** option.
    -   Select a time period for the **Average of sampled values in the following time period must breach the criteria** option.
6.  Define the conditions for when to clear the alert, under **Clear the alert when**.

    The condition fields are enabled when you create at least one condition.

7.  Select **Next**.


## What to do next

[Add an alert action](add-alert-action.md) \(Optional\).

