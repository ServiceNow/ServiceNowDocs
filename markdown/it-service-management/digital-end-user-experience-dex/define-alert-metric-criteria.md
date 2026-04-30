---
title: Define alert metric criteria
description: Specify alert metric criteria by choosing alert severity, defining thresholds, and specifying conditions for when the alert must be triggered.
locale: en-US
release: zurich
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Create metric rules, Metrics collection and metric rules, Configure, Digital End-User Experience, IT Service Management]
---

# Define alert metric criteria

Specify alert metric criteria by choosing alert severity, defining thresholds, and specifying conditions for when the alert must be triggered.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  In the **Alert severity** field, select a severity for the alert.

2.  Define the thresholds for the alert.

    The predetermined metrics are based on the configuration item \(CI\) type, such as Device, SaaS/web application, or Installed application.

    **Note:** You can select the following network stability metrics on Windows devices:

    -   Application Crashes
    -   Application Domain Jitter
    -   Application Domain Network Latency
    -   Application Domain Packet Loss
3.  Add another alert severity level by selecting **Add another alert severity**.

4.  Select the **Set the threshold for users \(optional\)** check box and define the criteria based on the number of impacted users to trigger the alert.

5.  In the Alert when section, perform one of the following steps.

    -   Select a time period for the **All sampled values must breach the criteria in the following time period** option.
    -   Select a time period for the **Average of sampled values in the following time period must breach the criteria** option.
6.  If you want to define the conditions for when to clear the alert, under **Clear the alert when**, define the conditions.

    The condition fields are enabled when you create at least one condition.

7.  Select **Next**.

    The **Set alert action \(optional\)** option is selected in the navigation pane.


## What to do next

[Define metric rule name and status](define-alert-name-state.md).

