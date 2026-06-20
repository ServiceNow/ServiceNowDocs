---
title: Filter search results on the Log Viewer in Health Log Analytics
description: Apply filters on the Log Viewer to show only your desired data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-log-viewer-filter-sow.html
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Review alert-related logs on the Log Viewer, Log Analytics in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Filter search results on the Log Viewer in Health Log Analytics

Apply filters on the **Log Viewer** to show only your desired data.

## Before you begin

Role required: evt\_mgmt\_operator, or evt\_mgmt\_user, or evt\_mgmt\_admin

## About this task

This feature is supported in the Health Log Analytics application, Version 20.0.11 - July 2021, and the Health Log Analytics Viewer application, Version 20.0.4 - July 2021, available from the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home).

## Procedure

1.  Open the **Log Viewer** using one of the following methods:

    -   Navigate to **Workspaces** &gt; **Service Operations Workspace** and select the Log Viewer icon \(\[Omitted image "icon-log-viewer-sow.png"\] Alt text: Log Viewer icon.\).
    -   While viewing log entries for an alert on the **Surrounding logs** tab, select **Log Viewer**.
2.  Define and run a search.

    For more information, see [Define, save, and share a search of log data in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-search-queries-manage-sow.md).

3.  Filter the search results in one of the following ways.

<table id="choicetable_ymv_1jg_ftb"><tbody><tr><td id="d133053e141">

**Add filters using the fields list**

</td><td>

1.  Select the filter icon \(\[Omitted image "icon-lv-filters-sow.png"\] Alt text: Filter icon.\).

The Selected fields list includes the fields that currently display as columns in the **Log Viewer** table. By default, the table includes the following columns: Application service, Component, Host, Level, Message, Raw message, and Time. The Available fields list includes all remaining fields that the system has extracted from the log.

2.  Select a field in the list.

**Note:** You can search for a specific field using the search option.

The top five values the system has found in the records for this field are displayed, along with the percentage of their occurrence.

\[Omitted image "log-viewer-filters-sow.png"\] Alt text: Log Viewer filters.

3.  Define a filter for a value in the field.
    -   To display only data that contains a value, select **Add** for it.

For example, to set the filter **\[Level\]\[is\]\[critical\]**, select **Add** for the value "critical" in the Level field.

    -   To create negative filters that exclude data that contains a value, select **Exclude** for it.

For example, to set the filter **\[Level\]\[is not\]\[critical\]**, select **Exclude** for the value "critical" in the Level field.

</td></tr><tr><td id="d133053e215">

**Add filters from the __Log Viewer__ table**

</td><td>

1.  In a column header, select the more actions icon \(\[Omitted image "icon-menu-sow.png"\] Alt text: More actions icon.\).
2.  In the dialog box, select the operator and specify the filter terms for the field.

\[Omitted image "log-viewer-filters-terms-sow.png"\] Alt text: Search filter terms.

3.  Select **Apply**.

A filter icon in the column header indicates that a filter applies for this field.

</td></tr></tbody>
</table>    The applied filter appears at the top of the **Filters** pane. The total number of applied field value filters in the **Filter** icon adjusts.

    \[Omitted image "log-viewer-filters-values-sow.png"\] Alt text: Field value filters.

4.  Remove a filter in one of the following ways.

    -   In the **Filters** pane:
        1.  Locate the filter you want to remove.
        2.  Select **Remove**.
    -   In a column header:
        1.  Select the more actions icon \(\[Omitted image "icon-menu-sow.png"\] Alt text: More actions icon.\).
        2.  Select the filter you want to remove.
        3.  Select **Remove filter**.

**Parent Topic:**[Reviewing the logs for an alert on the Log Viewer in Health Log Analytics](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/service-operations-workspace-for-itom-apps/hla-op-logs-log-viewer-concept-sow.md)

