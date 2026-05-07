---
title: Select event rule filters
description: Configure filtering criteria for event rules to target specific devices and users. Use filters to control which events trigger alerts based on operating system, location, department, or custom conditions.
locale: en-US
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-04-22"
reading_time_minutes: 1
breadcrumb: [Creating an event rule, Alert rules, Configure, Digital End-User Experience, IT Service Management]
---

# Select event rule filters

Configure filtering criteria for event rules to target specific devices and users. Use filters to control which events trigger alerts based on operating system, location, department, or custom conditions.

## Before you begin

Confirm that the DEX plugin \(sn\_dex\) is installed.

Role required: sn\_dex.admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  In the primary navigation pane, select the DEX Administration icon \(![](../image/icon-administration.png)\).

3.  Select **Configure** on the Alert rules card.

    The list of alert rules appears.

4.  Select **Create new rule** &gt; **Event rule**.

    A new tab opens for the Create metric rule window, with the **Select filters** option pre-selected in the navigation pane.

5.  Select an operating system under **Select OS type**.

6.  Select the **Applicable for Non-persistent VDIs** toggle switch to apply this metric rule to all the non-persistent Virtual Desktop Infrastructures \(VDIs\).

    **Note:** When this toggle switch is on, only the **Location** option is available in the **Apply filtering for devices** field.

7.  Apply conditional filtering for a device or a user.

    The predetermined filtering choices include Device or User.

    To add additional filters, select **+ New condition set**.

    **Note:**

    -   DEX Admins can filter by selecting any available column from the Device \(`cmdb_ci_computer`\) or User \(`sys_user`\) tables. Once a column is used as a filtering condition in any MR, it automatically becomes an enriched field.
    -   Enriched fields are already synced to end-user devices. However, if you select a non-enriched field as a filter condition, the data may take up to 24 hours to sync across all devices.
    -   You can select up to 15 non-enriched fields in addition to the default enriched values.
8.  Select **Next**.


## What to do next

[Define alert criteria](define-alert-criteria-event.md).

