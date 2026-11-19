---
title: Configure scan filters
description: Create scan filters to exclude applications, tables, or individual records from scans.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/impact/configure-scan-engine-filters.html
release: australia
topic_type: task
last_updated: "2026-11-06"
reading_time_minutes: 1
keywords: [scan filters, scan exclusions, exclude application, exclude table, exclude record, scan scope]
breadcrumb: [Configure Scan Engine properties, Activate Scan Engine and review settings, Run Impact Guided Setup, Configuring Impact, Impact]
---

# Configure scan filters

Create scan filters to exclude applications, tables, or individual records from scans.

## About this task

Use scan filters to define your own exclusions. When a filter is active, the excluded configuration is not scanned, therefore, findings don't appear on the dashboard.

Filters apply to your own scope only. The Impact and Scan Engine applications are excluded from scans, and this can't change with a filter.

## Procedure

1.  Navigate to **ALL** &gt; **Impact** &gt; **Configuration** &gt; **Scan Engine Properties**.

2.  Select the **Scan Filters** tab, and then select **New**.

    The tab lists existing filters with their name, type, application, source table, conditions, and source record.

3.  In the **Name** field, enter a name for the filter.

4.  In the **Type** field, select the level at which to exclude scope, and then complete the fields that appear for that type.

<table id="table_scan_filter_types"><thead><tr><th>

Type

</th><th>

Excludes

</th><th>

Fields to complete

</th></tr></thead><tbody><tr><td>

Application

</td><td>

All records in the selected application.

</td><td>

-   Type: **Application**: Required.
-   Choose an application using the search icon.


</td></tr><tr><td>

Table

</td><td>

Records in the selected table.

</td><td>

-   Type: **Table**
-   **Source Table**: Required. Select the table to exclude.
-   **Conditions**: Limit the exclusion to records that match the conditions using the **Add Filter Condition** and **Add OR Clause** functions.


</td></tr><tr><td>

Record

</td><td>

One specific record.

</td><td>

-   Type: **Record**
-   **Source Table**: Required. Select the table that contains the record.
-   **Source Record**: Required. Select the document to exclude from the specified table.


</td></tr></tbody>
</table>5.  Select the **Active** check box to apply the filter to scans.

6.  Select **Submit**.


## Result

When you run a new scan, the excluded scope is not scanned. Findings for that scope don't appear on the dashboard.

**Parent Topic:**[Configure Scan Engine properties](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/impact/configure-scan-engine-properties.md)

