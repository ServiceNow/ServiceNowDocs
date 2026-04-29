---
title: Create a funnel visualization
description: A funnel visualization shows how data progresses through sequential stages, helping you identify drop-offs or bottlenecks at each step. Use it to track conversions, workflows, or process completion rates. You can add a funnel visualization to an existing dashboard or to a new dashboard.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Data visualization in ITOM, AIOps Dashboards in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create a funnel visualization

A funnel visualization shows how data progresses through sequential stages, helping you identify drop-offs or bottlenecks at each step. Use it to track conversions, workflows, or process completion rates. You can add a funnel visualization to an existing dashboard or to a new dashboard.

## Before you begin

Role required: report\_user, admin, or viz\_creator

Ensure you have an admin role or permission from the dashboard owner to edit the dashboard.

## About this task

If you have the appropriate role, you can add and edit funnel reports on a dashboard. The **Edit** button is not available on the ITOM dashboards unless the user has rights to edit it. For more details on creating dashboards, see [Common dashboard tasks in the in-line editor](https://www.servicenow.com/docs/access?context=common-dashboard-tasks&version=australia&pubname=australia-now-intelligence&ft:locale=en-US).

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the AIOps Dashboards icon \(![AIOps Dashboards icon.](../../health-log-analytics-admin/image/aiops-operational-icon.png)\).

2.  From the Dashboard picker, select **AIOps 360 overview**.

    ![AIOps 360 overview dashboard](../image/sow-aiops-dasboard.png)

3.  Select **Edit** to put dashboard in the edit mode.

    ![Option to add or edit funnel](../image/sow-aiops-dasboard-create-new.png)

4.  From the **Add new element** drop-down menu, select **Data visualization**.

    ![Data visualization option](../image/sow-aiops-data-visualization.png)

5.  In the Add Visualization window, select **New visualization**.

    ![New visualization creation option](../image/sow-aiops-new-visualization.png)

6.  From the **Visualization type** field, select **Funnel**.

    ![Funnel data visualization option](../image/sow-aiops-data-vis-funnel.png)

    **Note:** The **Funnel** visualization type is currently available only to customers who have the ITOM plugin installed.

7.  Under **Data sources**, select **+ Add data source**.

    There are two kinds of data sources avail for the **Funnel** visualization type: Table and Indicator. Visualizations based on table data show a snapshot of the state of that data. Indicator visualizations reflect data over time based on data collection jobs. You can configure funnel stages using indicators in one of the following ways:

    You can configure funnel stages using indicators in one of the following ways:

    -   Option 1: Use a single indicator or table with a breakdown

        Select a single indicator or table, and then define the breakdown using the Group by field. The breakdown values are used as the funnel stages.

        **Note:** If you select only one indicator without a breakdown, the visualization displays an error: `Invalid configuration. A 'Group By' must be selected for the visualization to render.`

    -   Option 2: Use multiple indicators without a breakdown

        Select multiple indicators without setting a breakdown. In this case, each indicator's value represents a stage in the funnel.

        ![Data sources for funnel data visualization](../image/sow-aiops-data-vis-funnel-data-source.png)

8.  Select the required data source and select **Add this source**.

    When you select a table or indicator data source for a funnel visualization, refer to the following topics for the available data configuration options:

    -   [Table data options for funnel visualizations](../reference/funnel-table-data.md)
    -   [Indicator data options for funnel visualizations](../reference/funnel-indicator-data.md)
9.  Select **Save**.


-   **[Table data options for funnel visualizations](../reference/funnel-table-data.md)**  
When you select a table data source for the funnel visualization, the following data configuration options are available.
-   **[Indicator data options for funnel visualizations](../reference/funnel-indicator-data.md)**  
When you select an indicator data source for the funnel visualization, the following data configuration options are available.

**Parent Topic:**[Data visualization in ITOM](../concept/itom-data-visualization.md)

