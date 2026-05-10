---
title: Export directly from a URL
description: Dynamically export data from a script or web service by building a URL query.
locale: en-US
release: australia
product: Table Administration and Data Management
classification: table-administration-and-data-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Exporting data, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Export directly from a URL

Dynamically export data from a script or web service by building a URL query.

## Before you begin

Role required: None

**Note:** ServiceNow enforces [basic authentication](http://www.w3.org/Protocols/HTTP/1.0/draft-ietf-http-spec.html#BasicAA) for direct URL access. The data extracted from the URL contains only the fields to which the currently authenticated user has read access.

## About this task

You can use URL queries to generate filtered lists of records programmatically before exporting them. URL queries are useful for scripts that generate a list of records or when no user can manually add the filter from the UI.

You must be familiar with the ServiceNow table and column names to export data directly from the URL. See [Navigate to a record or a module using a URL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/navigate-using-url.md).

You can control whether to export the display value or raw value of fields and the field label or field name for headers using query parameters or system properties.

-   For details on using query parameters, see [Query parameters for display value and header](../concept/query-parameters-display-value.md).
-   For details on using system properties, see [System properties for display value and header](../concept/system-properties-display-value-header.md).

Query parameters, if present, override system properties.

## Procedure

1.  Specify the instance URL.

    For example:

    ```
    https://<instance name>.service-now.com/
    ```

2.  Specify the table form or list to export.

    For example:

    ```
    incident_list.do
    ```

3.  Specify the export format processor to use for the export.

    You can specify CSV, XLS, JSON, XLSX, or XML. For example:

    ```
    ?CSV
    ```

    **Note:** The XML processor in a URL export doesn't export attachments or journal fields. To export attachments and journal fields like the **Work Notes** or **Additional Comments** fields, export the records from a list by using the **Export** &gt; **XML** option in the context menu.

4.  Query for specific records by adding the **sysparm\_query** parameter.

    The required syntax is `sysparm_query=[column name][operator][value]`. For example:

    ```
    https://<instance name>.service-now.com/incident_list.do?XML&sysparm_query=priority=1
    ```

    **Note:** All queries use a column name, an operator, and a value. See [Condition Builder](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/c_ConditionBuilder.md) for a list of available operators.

5.  Sort the records by column name using the **sysparm\_orderby** parameter.

    The required syntax is `sysparm_orderby=[column name]`. For example:

    ```
    https://<instance name>.service-now.com/incident_list.do?XML&sysparm_query=priority=1&sysparm_orderby=assigned_to
    ```

    **Note:** You can sort by only one column using **sysparm\_orderby**. To sort by multiple columns, use multiple orderby entries. For example:

    ```
    sysparm_query=ORDERBYassigned_to^ORDERBYpriority
    ```

6.  Export fields from a specific view using the **sysparm\_view** parameter.

    The required syntax is `sysparm_view=[view name]`. For example:

    ```
    https://<instance name>.service-now.com/incident.do?CSV&sysparm_view=ess
    ```

    This URL exports incident fields visible from the Self Service \(ess\) view.

    -   By default, exporting data from a list exports only the fields that are visible from the current view. If you want to export fields from another list view, you can switch views from the UI. See [View management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-user-interface/view-management-overview.md).
    -   If you're exporting CSV or Excel data and don't specify a view, the export uses the default list view.
    -   If you're exporting XML data, all fields are exported by default unless you specify a particular view.
7.  Export specific fields from the table using the **sysparm\_fields** parameter.

    The required syntax is `sysparm_fields=[field1],[field2]`. For example:

    ```
    https://<instance name>.service-now.com/incident_list.do?CSV&sysparm_fields=sys_id,number
    ```

8.  Export all fields from the table, including the sys\_id, using the **sysparm\_default\_export\_fields** parameter.

    The required syntax is `sysparm_default_export_fields=all`. For example:

    ```
    https://<instance name>.service-now.com/incident_list.do?CSV&sysparm_default_export_fields=all
    ```

    The **sysparm\_default\_export\_fields** parameter has no effect on XML exports unless you include the **sysparm\_view** parameter to specify a non-default view.


## Sample URLs

|URL|Description|
|---|-----------|
|https://&lt;instance name&gt;.service-now.com/incident\_list.do?CSV|Export all incidents to a comma-separated value text file.|
|https://&lt;instance name&gt;.service-now.com/incident\_list.do?CSV&amp;sysparm\_query=sys\_id%3E%3Db4aedb520a0a0b1001af10e278657d27|Export a particular incident to a comma-separated value text file.|
|https://&lt;instance name&gt;.service-now.com/incident\_list.do?CSV&amp;sysparm\_orderby=sys\_id|Export all incidents to a comma-separated value text file and sort the list by sys\_id.|
|https://&lt;instance name&gt;.service-now.com/incident\_list.do?XML&amp;sysparm\_query=priority=1&amp;sysparm\_orderby=assigned\_to|Export a list of all priority 1 incidents to an XML file and sort the list by **Assigned to** field.|

