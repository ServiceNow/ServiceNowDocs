---
title: View loaded files for a plugin
description: Get a related list view of all the files loaded for a plugin by clicking View all plugin duration.
locale: en-US
release: yokohama
product: Upgrade Management
classification: upgrade-management
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Upgrade Summary Report, Monitor an upgrade to an instance, Upgrade Monitor tool in Upgrade Console, Upgrade Console tools, Using Upgrade Console, Upgrade Console, Upgrade, Administer the ServiceNow AI Platform]
---

# View loaded files for a plugin

Get a related list view of all the files loaded for a plugin by clicking **View all plugin duration**.

## Before you begin

Role required: admin.

## Procedure

1.  Navigate to Upgrade Monitor using one of the following ways.

    |Option|Navigation|
    |------|----------|
    |Using left navigation|Navigate to **All** &gt; **Admin Center** &gt; **Upgrade Management** &gt; **Upgrade Monitor**.|
    |Using Admin tab option|Navigate to **Admin** &gt; **Upgrade Management** &gt; **Upgrade Monitor**.|

    **Note:** When the system finishes the upgrade, it displays the Upgrade Summary Report.

2.  Scroll down to **Top 10 Plugins by Duration**.

3.  Click **View all plugin duration**.

    The **System Upgrade Metrics** list of all the plugins and their durations shows up.

4.  Click one of the plugins from the list to open the **System Upgrade Metrics** form view of that plugin.

    The Plugin Files related list of all the loaded files for that plugin is displayed. ![Image showing the System Upgrade Metric form with the duration message and all loaded files](../../upgrade-center/image/uc-plugin-form-view.png)

    **Note:** The total plugin load duration is not the sum of the load duration of all the loaded files for that plugin.


**Parent Topic:**[Upgrade Summary Report](../reference/um-complete-summary.md)

