---
title: Create log data dashboards and visualizations in Health Log Analytics
description: Build Health Log Analytics log data dashboards and visualizations in real time for easier identification and understanding of issues.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Dashboards for real-time visualization of log data, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Create log data dashboards and visualizations in Health Log Analytics

Build Health Log Analytics log data dashboards and visualizations in real time for easier identification and understanding of issues.

## Before you begin

This functionality is supported in the Service Operations Workspace Log Analytics application, Version 21.2.7 - November 2022 and later, and has a dependency on the Platform Analytics Workspace, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

For detailed information about creating and working with dashboards, see [Dashboards in the Analytics Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center-dashboards.md).

**Note:** As an alternative to defining your own dashboard, you can use the AIOps dashboards, which offer comprehensive visualizations of critical operational data. For more information, see [AIOps Dashboards in Service Operations Workspace for ITOM](../../service-operations-workspace-itom/concept/aiops-dashboards-sow-itom.md).

Role required: evt\_mgmt\_operator or viz\_admin

## Procedure

1.  Navigate to **Workspaces** &gt; **Platform Analytics Workspace**.

2.  On the Analytics Overview page, select the **Dashboards** tab.

    This tab enables you to view all the dashboards you have rights to access on your instance. You can filter the dashboard tiles to limit the number that are visible.

    **Note:** If you want to use an existing dashboard, select the dashboard here to open it. Otherwise, create a dashboard as explained in the remainder of this procedure.

3.  Create a dashboard.

    1.  Select **Create new dashboard**.
    2.  In the New dashboard dialog, choose **In-line editor** and specify a name and optional description for the dashboard.

        **Note:** The in-line editor does not automatically save your work. Ensure that you save regularly.

        ![New dashboard dialog.](../image/hla-log-dashboard-inline.png)

    3.  Select **Create new dashboard**.
4.  Add an element to the dashboard.

    Various elements are available to help you organize and populate the information on the dashboard. For more information, see [Analytics Center dashboard elements](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/ac-elements.md).

    1.  Select **Add new element**.

    2.  Select **Data visualization** from the available elements.

        The **Data visualization** element appears on the dashboard, where you can edit it.

        **Note:** You can click and drag the corners of the element to resize it.

5.  Edit the element.

    1.  On the element, select the Settings icon:

        ![Data visualization settings.](../image/hla-data-viz-settings.png)

        The Configuration panel opens.

    2.  From the **Visualization type** list, choose the type of visual representation you want for the log data.

        You can choose from various types of graphs and charts.

        For detailed information, see [Data visualizations in the Analytics Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center-data-visualizations.md).

    3.  In the Data section, select **+ Add data source**.

        The Health Log Analytics data source that you select is used to ingest the log data that is provided to the visualization.

        ![Add data source button.](../image/hla-log-dashboard-data-source.png)

    4.  Select the Health Log Analytics Log components data source.

    5.  Choose the required data source from these options:

        -   Saved searches – a list of all the searches you saved in the Log viewer.
        -   Select component – a list of all the components that stream data to Health Log Analytics.
    6.  Use Conditions, a Lucene query, or both to specify the data segment you're interested in and then select **Run**.

        ![Add a data source.](../image/hla-log-dashboard-hla-component3.png)

    7.  Select **Add this source** to add the selected Health Log Analytics data source.

        The specified visualization displays in the **Data visualization** element.

    8.  Set fixed start and end dates to customize the time range of the presented data.

        ![Data range.](../image/hla-log-dashboard-date-range.png)

        1.  In the Date range section, select **Set absolute period**.
        2.  Specify the start and end date for the absolute period in the appropriate calendars.
    9.  Adjust the other settings of the visualization as needed.

        For detailed information on settings for all the visualization types, select the link for the relevant type in [Data visualizations in the Analytics Center](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/analytics-center-data-visualizations.md).

    10. Add more elements as needed.

    11. Select **Save** to save your changes and continue editing.

    12. Select **Exit editing mode** to stop editing and display the dashboard.


**Parent Topic:**[Dashboards for real-time visualization of log data in Health Log Analytics](../concept/hla-dashboard-visualizations.md)

**Related topics**  


[Share a Platform Analytics dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/now-intelligence/share-db-in-ac.md)

