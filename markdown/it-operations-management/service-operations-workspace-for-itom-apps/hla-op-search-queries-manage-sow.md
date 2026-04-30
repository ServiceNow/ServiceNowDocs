---
title: Define, save, and share a search of log data in Health Log Analytics
description: Define, save, and share searches of log data to help determine the causes of Log Analytics alerts.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Review alert-related logs on the Log Viewer, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Define, save, and share a search of log data in Health Log Analytics

Define, save, and share searches of log data to help determine the causes of Log Analytics alerts.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  Open the **Log Viewer** using one of the following methods:

    -   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the Log Viewer icon \(![Log Viewer icon.](../image/icon-log-viewer-sow.png)\).
    -   While viewing log entries for an alert on the **Surrounding logs** tab, select **Log Viewer**.
2.  Define a search.

    1.  Select the selection icon \(![Selection icon.](../image/icon-selection-sow.png)\) and then select **New search**.

    2.  Set the values of the search parameters in the search fields.

<table id="table_yp2_2cf_ftb"><thead><tr><th>

Search field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Query

</td><td>

Search query.**Tip:** The Log viewer uses the Elasticsearch search engine, so you can use any supported search term structure in the **Query** field.

</td></tr><tr><td>

Component

</td><td>

Logical component of the service instance that generated the event. Multiple CIs can sometimes perform the same function.

</td></tr><tr><td>

Time range

</td><td>

Time range to apply to the X-axis when displaying the returned data. The setting that you specify appears in the **Start time** and **End time** fields. Use one of the following methods:-   Select a time period from the list.
-   Click **Custom range** to use the date and time picker to specify a range.
 **Note:** You can modify the settings in the **Start time** and **End time** fields manually. The selected time range shown in **Select range** then changes to Custom range. This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

**Note:** Saved searches do not include time range settings.

</td></tr></tbody>
</table>    3.  Select **Search**.

        The system returns the full list of log lines that match the search values. The information is displayed in the Results over time chart.

3.  Save the search.

    The saved search includes any selected filters. For information about filters, see [Filter search results on the Log Viewer in Health Log Analytics](hla-op-log-viewer-filter-sow.md).

    **Note:** Saved searches do not include time range settings.

    1.  Select **Save As**.

    2.  In the **Search name** field, specify a unique and descriptive name for the search and then click **Save**.

    **Note:** If you are using Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), you can define an alert rule without saving the search. For more information, see [Add a Log Analytics alert rule in Health Log Analytics](hla-op-alert-rule-add.md).

4.  Share the saved search with an assignment group.

    1.  Select **Share**.

    2.  Select an assignment group from the list.

    3.  Select **Save**.


**Parent Topic:**[Reviewing the logs for an alert on the Log Viewer in Health Log Analytics](../concept/hla-op-logs-log-viewer-concept-sow.md)

**Related topics**  


[Use or modify a saved log data search in Health Log Analytics](hla-op-search-queries-saved-sow.md)

[Add a Log Analytics alert rule in Health Log Analytics](hla-op-alert-rule-add-sow.md)

