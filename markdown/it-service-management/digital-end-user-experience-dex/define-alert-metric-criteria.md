---
title: Define alert metric criteria
description: Specify alert metric criteria by choosing alert severity, defining thresholds, and specifying conditions for when the alert must be triggered.
locale: en-US
release: yokohama
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create metric rules, DEX administration, Configure, Digital End-User Experience, IT Service Management]
---

# Define alert metric criteria

Specify alert metric criteria by choosing alert severity, defining thresholds, and specifying conditions for when the alert must be triggered.

## Before you begin

Role required: sn\_dex.admin

## Procedure

1.  In the **Alert severity** field, select a severity for the alert.

2.  Define the thresholds for the alert.

    The predetermined metrics are based on the configuration item \(CI\) type, such as SaaS/web, Installed, or Device.

    **Note:** You can select the following network stability metrics on Windows devices:

    -   Application Crashes
    -   Application Domain Jitter
    -   Application Domain Network Latency
    -   Application Domain Packet Loss
3.  Add another alert severity level by selecting **Add another alert severity**.

4.  Select the **Set the threshold for users** check box and define the criteria based on the number of impacted users to trigger the alert.

5.  In the Alert when section, perform one of the following steps.

    -   Select **All sampled values must breach the criteria in the following time period** and define the time period.
    -   Select **Average of sampled values in the following time period must breach the criteria** and define the time period.
6.  If you want to define the conditions when to clear the alert, under **Clear the alert when**, define the conditions.

    The condition fields are enabled when you create at least one condition.

7.  Select **Next**.

    The **Set alert action \(optional\)** option is selected in the left pane.


## What to do next

[Define metric rule name and status](define-alert-name-state.md).

