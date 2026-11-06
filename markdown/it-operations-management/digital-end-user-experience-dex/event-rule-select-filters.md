---
title: Select event rule filters
description: Configure event rule filters to target specific devices and users by operating system, location, department, or custom conditions.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/digital-end-user-experience-dex/event-rule-select-filters.html
release: australia
product: Digital End-User Experience \(DEX\)
classification: digital-end-user-experience-dex
topic_type: task
last_updated: "2026-10-23"
reading_time_minutes: 1
keywords: [event rule filters, select filters, event filtering, conditional filtering]
breadcrumb: [Creating an event rule, Managing alert rules, Configure, Digital End-User Experience, IT Operations Management]
---

# Select event rule filters

Configure event rule filters to target specific devices and users by operating system, location, department, or custom conditions.

## Before you begin

Confirm that the DEX plugin \(sn\_dex\) is installed.

Role required: sn\_dex.admin

## Procedure

1.  In the primary navigation pane, select the DEX Administration icon \(\[Omitted image "icon-administration.png"\] Alt text:\).

2.  Select **Configure** on the Alert rules card.

    The list of alert rules appears.

3.  Select **Create new rule** &gt; **Event rule**.

    A new tab opens for the Create metric rule window, with the **Select filters** option preselected in the navigation pane.

4.  Select an operating system under **Select OS type**.

5.  Select the **Applicable for Non-persistent VDIs** toggle switch to apply this event rule to all the non-persistent virtual desktop infrastructures \(VDIs\).

    **Note:** When this toggle switch is on, only the **Location** option is available in the **Apply filtering for devices** field.

6.  Apply conditional filtering for a device or a user.

    The predefined filtering choices are Device and User.

    To add more filters, select **+ New condition set**.

    **Note:**

    -   Administrators can filter by selecting any available column from the Device \(`cmdb_ci_computer`\) or User \(`sys_user`\) tables. After a column is used as a filtering condition in any rule, it automatically becomes an enriched field.
    -   Enriched fields are already synced to end-user devices. However, if you select a non-enriched field as a filter condition, the data might take up to 24 hours to sync across all devices.
    -   Besides the default enriched values, you can select up to 15 non-enriched fields.
7.  Select **Next**.


## What to do next

For the next step, see [Define alert criteria](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/digital-end-user-experience-dex/define-alert-criteria-event.md).

