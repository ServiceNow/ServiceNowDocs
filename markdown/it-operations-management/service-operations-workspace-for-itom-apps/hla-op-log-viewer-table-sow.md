---
title: Customize the Log viewer table
description: Add or remove columns in the Log viewer table to show only the data you want to view.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Viewing the logs for an alert on the Log viewer, Using Service Operations Workspace for ITOM Log Analytics, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Customize the Log viewer table

Add or remove columns in the **Log viewer** table to show only the data you want to view.

## Before you begin

Role required: evt\_mgmt\_operator, or evt\_mgmt\_admin

## About this task

This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Procedure

1.  Open the **Log viewer** using one of the following methods:

    -   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the Log Viewer icon \(![Log viewer icon.](../image/icon-log-viewer-sow.png)\).
    -   While viewing log entries for an alert on the **Surrounding logs** tab, select **Log viewer**.
2.  Select the filter icon \(![Filter icon.](../image/icon-lv-filters-sow.png)\) to display the **Filters** pane.

    The Selected fields list includes the fields that currently display as columns in the **Log viewer** table. By default, the table includes the following columns: Application service, Component, Host, Level, Message, Raw message, and Time. The Available fields include all remaining fields that the system has extracted from the log.

    In the Service Operations Workspace Log Analytics application, Version 21.2.7 - November 2022 and later, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home), the Log message column is added and the Raw message column no longer displays by default. You can add the Raw message column to the table by selecting it from the **Filters** pane.

3.  Add or remove columns in the **Log viewer** table.

    -   To add a column to the table, select the field of the same name in the Available fields list and then select the add icon \(![Add icon.](../image/icon-add-sow.png)\).

        The added field displays as a column in the table. It is now listed in the Selected fields list.

    -   To remove a column, select the field of the same name in the Selected fields list and then select the remove icon \(![Remove icon.](../image/icon-remove-sow.png)\).

        The corresponding column is removed from the table. The removed field is added to the Available fields list.

        If you have filtered the data for specific values in a field, that data still displays even when the field is no longer selected. For more information about filtering data, see [Filter search results on the Log viewer](hla-op-log-viewer-filter-sow.md).

        **Note:** The Time column can't be removed from the table.

4.  Adjust the maximum number of characters per field in the table.

    1.  Navigate to **Health Log Analytics** &gt; **Health Log Analytics Administration** &gt; **System Properties**.

    2.  Open the **sn\_occ.log\_viewer.max.characters** property record.

    3.  In the **Value** field, edit the default value.

    4.  Select **Update**.


## Result

The **Log viewer** table shows the customized view from the current session onward until you change your preferences.

**Parent Topic:**[Viewing the logs for an alert on the Log viewer](../concept/hla-op-logs-log-viewer-concept-sow.md)

