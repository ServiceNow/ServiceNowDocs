---
title: Specify the configuration item for metric rules
description: Choose application or device and define filter conditions for the metric rule.
locale: en-US
release: xanadu
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Create metric rules, Metric rules for Digital End-User Experience, Configuring Digital End-User Experience, Digital End-User Experience, IT Service Management]
---

# Specify the configuration item for metric rules

Choose application or device and define filter conditions for the metric rule.

## Before you begin

Ensure that the DEX plugin \[sn\_dex\] is installed and you are on the Metric rules page.

Role required: sn\_dex.admin

## Procedure

1.  Select **Create new rule**.

    A new tab opens for the Create metric rule window, with the the **Select the CI** option pre-selected in the left pane.

2.  Select any one of the following types of configuration items you want to monitor.

    -   Saas/web application
    -   Installed application \(.exe, .app, etc.\)
    -   Device
3.  For **Saas/web application** or **Installed application**, select the application to monitor.

    **Note:** If you select **Device**, the option to choose an application would not be available.

4.  Apply conditional filtering on the configuration items.

    The predetermined filtering choices include Department, Location, OS, User, and Version, with the Version option specifically designed for installed applications.

    To add additional filters, select **+ New condition set**.

5.  Select **Next**.

    The **Add criteria** option is selected in the left pane.


## What to do next

[Define alert metric criteria](define-alert-metric-criteria.md).

