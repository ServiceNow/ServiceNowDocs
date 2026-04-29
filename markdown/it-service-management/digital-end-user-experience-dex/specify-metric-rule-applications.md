---
title: Specify the configuration item for metric rules
description: Choose an application or device and define filter conditions for the metric rule.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create metric rules, Metrics collection and metric rules, Configure, Digital End-User Experience, IT Service Management]
---

# Specify the configuration item for metric rules

Choose an application or device and define filter conditions for the metric rule.

## Before you begin

Confirm that the DEX plugin \(sn\_dex\) is installed.

Role required: sn\_dex.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select the DEX Administration icon \(![](../image/icon-administration.png)\).

3.  Select **Configure** on the Metric rules card.

    The list of metric rules appears.

4.  Select **Create new rule**.

    A new tab opens for the Create metric rule window, with the **Select the CI** option pre-selected in the navigation pane.

5.  Select one of the following types of configuration items that you want to monitor.

    -   Device
    -   Saas/web application
    -   Installed application \(.exe, .app, etc.\)
6.  For **Saas/web application** or **Installed application**, select the application to monitor.

    **Note:** If you select **Device**, the option to choose an application wouldn’t be available.

7.  Select the **Applicable for Non-persistent VDIs** toggle switch to apply this metric rule to all the non-persistent Virtual Desktop Infrastructures \(VDIs\).

    **Note:** When this toggle switch is on, only the **Location** option is available in the **Apply filtering for devices** field.

8.  Apply conditional filtering on the configuration items.

    The predetermined filtering choices include Device, Department, Location, OS, User, and Version, with the Version option designed for installed applications.

    To add additional filters, select **+ New condition set**.

    **Note:**

    -   DEX Admins can filter by selecting any available column from the Device \(`cmdb_ci_computer`\) or User \(`sys_user`\) tables. Once a column is used as a filtering condition in any MR, it automatically becomes an enriched field.
    -   Enriched fields are already synced to end-user devices. However, if you select a non-enriched field as a filter condition, the data may take up to 24 hours to sync across all devices.
    -   You can select up to 15 non-enriched fields in addition to the default enriched values.
9.  Select **Next**.

    The **Add criteria** option is selected in the navigation pane.

    -   Static metric rule: This metric rule processes real time data. Lists all metric rules that are stored on the server.
    -   Zscore \(Running average\): Zscore is a measurement that indicates how many deviations a data point is away from the mean value of its dataset. It’s a dynamic value specific for each device or user. Data is evaluated from the end-user computer. Data from the last 7 days is collected. The default values are 5 to -5.

        **Note:** When you select Zscore, the alert is triggered only for the sampled value. Alerts for the average of sample are not available.


## What to do next

[Define alert metric criteria](define-alert-metric-criteria.md).

