---
title: Control data source availability by role
description: Limit by role the data sources for which users can create data visualizations.
locale: en-US
release: zurich
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Control data source availability by role

Limit by role the data sources for which users can create data visualizations.

## Before you begin

Role required: admin

## About this task

By default, all roles can create data visualizations for all data sources. You can instead limit the available data sources by an allow list. When you create a Visualization Data Sources Visibility \[sys\_viz\_data\_source\_role\] record for a data source, only users with at least one of the roles that you specify can create a data visualization for that data source. Any visualizations that they created before you created the allow list still exist. However, the user who created the visualization will no longer be able to edit that visualization unless they have one of the roles from the allow list.

**Important:** Create only one Visualization Data Sources Visibility record for a data source.

## Procedure

1.  Create a new record on the Visualization Data Sources Visibility \[sys\_viz\_data\_source\_role\] table.

    For example, you can navigate to the list view of the table and select **New**.

2.  In the **Viz data source** field, select the data source whose use you want to limit.

    Your choices include any custom data sources that you have created in the Viz Framework Data Sources \[sys\_viz\_data\_source\] table.

3.  Select the **Edit user roles** icon \(![pencil icon](../../dashboards/image/icon-pencil-ac.png)\) next to Roles.

4.  In the **Available** field, highlight those roles that should be able to create data visualizations for this data source.

    Only users with the roles you add will have access to the data source. You can reopen this record and add or delete roles later. Users with deleted roles will see a message that they don't have access to the data source when they try to edit a visualization based on it.

5.  Select the right arrow &gt; button to add the highlighted roles to the record.

6.  Select **Done**.

7.  Select **Submit**.


## Impact of limiting data source by role

Abel Tuter is a top business analyst. Abel has the pa\_power\_user role and can create indicators. Alissa Mountjoy is a technical expert who schedules [data collection jobs](../../performance-analytics/concept/performance-analytics-glossary.md#) for indicators, but is not a business analyst and does not create indicators. Alissa has the pa\_data\_collector role. By default, both Abel and Alissa can create data visualizations based on an indicator.

Abel creates a time series data visualization on the Number of Open Incidents indicator. Abel shares this visualization with Alissa, also granting editing rights.

![Share Visualization dialog with Alissa Mountjoy being given editing permission.](../image/dv-acl-add-alissa-editor.png)

Alissa can open this visualization in edit mode, accessing the configuration panel. She can edit the data source. She can also create a visualization herself using an incident data source.

![The Number of open incidents data visualization in edit mode, with Alissa Mountjoy the logged-in user and able to edit the data source.](../image/dv-alissa-editing.png)

As a system administrator, you decide that only business experts with the pa\_power\_user role should be able to create data visualizations based on indicators.

![Visual Data Sources Visibility record limiting indicator data sources to pa_power_user role.](../image/dv-data-source-role-record.png)

Alissa still has editing rights to the data visualization, but can no longer edit the data source. Neither can Alissa create a data visualization with an incident data source.

![The Number of open incidents data visualization in edit mode, with Alissa Mountjoy the logged-in user and unable to edit the data source.](../image/dv-alissa-cant-edit.png)

**Parent Topic:**[Configure data visualizations](../../performance-analytics/concept/configure-data-visualizations.md)

**Related topics**  


[Data sources for data visualizations](../reference/data-sources-visualizations.md)

