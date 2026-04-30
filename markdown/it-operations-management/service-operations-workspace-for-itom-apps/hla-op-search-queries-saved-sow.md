---
title: Use or modify a saved search
description: Use a saved search of log data to better understand the causes of an alert. As the owner of a saved search, you can modify the search values and save your changes.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Viewing the logs for an alert on the Log viewer, Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Use or modify a saved search

Use a saved search of log data to better understand the causes of an alert. As the owner of a saved search, you can modify the search values and save your changes.

## Before you begin

**Note:** If you are not the owner of the saved search, save the search with a different name. You can then update search values, save your changes, and share the search with others.

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## Procedure

1.  Open the **Log viewer** using one of the following methods:

    -   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the Log Viewer icon \(![Log viewer icon.](../image/icon-log-viewer-sow.png)\).
    -   While viewing log entries for an alert on the **Surrounding logs** tab, select **Log viewer**.
2.  Use a saved search.

    1.  Select the selection icon \(![Selection icon.](../image/icon-selection-sow.png)\) and then select **Load search**.

    2.  In the Load search dialog box, select the name of the search to load.

    The system returns the full list of log lines that match the search values and displays the information in the Results over time chart.

3.  Update the saved search.

    1.  Select the selection icon \(![Selection icon.](../image/icon-selection-sow.png)\) and then choose **Manage my searches** from the drop-down list.

    2.  Modify the settings.

<table id="table_ctn_5gg_ftb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the saved search.

</td></tr><tr><td>

Query

</td><td>

Search query.The Log viewer uses the Elasticsearch search engine, so you can use any supported search term structure in the **Query** field.

</td></tr><tr><td>

Assignment group

</td><td>

Assignment groups that can access the search. The members of the groups can use the search.

</td></tr><tr><td>

Filter

</td><td>

Column filter in standard format \(`field1=value1, field2=value2, field3=value3, ...`\).

</td></tr><tr><td>

Updated

</td><td>

Date and time the search was updated.This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

</td></tr></tbody>
</table>        To revert changes you have made to the search values, select the selection icon \(![Selection icon.](../image/icon-selection-sow.png)\) and then select **Discard Changes**. The changes that you made to the search values are discarded. You can continue to update the search settings.

    3.  Save the updated search.

        1.  Select **Save as**.
        2.  In the **Search name** field, specify a unique and descriptive name for the search and then click **Save**.

**Parent Topic:**[Viewing the logs for an alert on the Log viewer](../concept/hla-op-logs-log-viewer-concept-sow.md)

