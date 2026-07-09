---
title: Create a certification filter
description: A filter is a subset of configuration items from any ServiceNow table that is created with a standard condition builder.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/yokohama/servicenow-platform/configuration-management-database-cmdb/t\_CreatingCertificationFilters.html
release: yokohama
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Data Certification planning, Data Certification on Core UI, Data Certification, CMDB data management, CMDB schema model, Exploring CMDB, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a certification filter

A filter is a subset of configuration items from any ServiceNow table that is created with a standard condition builder.

## Before you begin

Role required: admin

## About this task

An example is a filter that selects all UNIX servers in the Australian data center.

With filters, you can:

-   Create multiple versions of a filter and then select the version you want to use.
-   Use one filter on multiple certification schedules.
-   View the number of records that match your filter as you create the conditions.

**Note:** Be sure to create certification filters before creating certification schedules.

## Procedure

1.  Navigate to **All** &gt; **Data Certification** &gt; **Certification Filters**.

2.  Click **New**.

3.  Fill in the form \(see table\).

4.  Click **Submit**.

    This action saves the filter as version 1.

    \[Omitted image "CertificationFilterV1.png"\] Alt text: Creating a certification filter.

5.  To create another filter version, modify the filter conditions and click **Update**.

    The system saves the new filter and increments the version number.

    \[Omitted image "CertificationFilterV2.png"\] Alt text: Updating a certification filter.

    By default, the Certification Filters list shows only the current version of each filter. To see all filter versions, click **All** in the breadcrumbs.

    \[Omitted image "CertificationFilterList.png"\] Alt text: Viewing the list of certification filters.

6.  To make an inactive filter the current version, open the inactive filter and click **Revert**.

    \[Omitted image "CertificationFilterRevert.png"\] Alt text: Reverting a certification filter.

    This action creates a new, active version of the filter and makes all previous versions inactive.

7.  To delete a single filter version, open that version record and click **Delete**.

8.  To delete inactive versions of a filter, click **Delete inactive versions** under **Related Links** in that filter record.

    You cannot delete a filter that is used in a schedule definition. The system displays a warning and the filter is not deleted.

<table id="table_xc1_gt3_3p"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

\[Required\] Filter name.

</td></tr><tr><td>

Description

</td><td>

\[Optional\] Brief description of the filter.

</td></tr><tr><td>

Number

</td><td>

\[Read-only\] Automatically assigned filter identification number.

</td></tr><tr><td>

Table

</td><td>

Table containing the records to be filtered. Use of the Database View `[sys_db_view]` table is limited by version.

</td></tr><tr><td>

Active

</td><td>

Control to make the filter available for use from the **Filter** field on the Certification Schedule form.

</td></tr><tr><td>

Version

</td><td>

Current version of this filter. Any significant changes to the filter make the current version inactive. The system copies the updated filter, marks it as active, and increments the version number. The system saves all versions of the filter and makes them available to users. More than one version of a filter can be marked active.

</td></tr><tr><td>

Filter condition

</td><td>

Field, operator, and value to create the condition. The available options depend on the table selected. You can view the number of records that match the filter by clicking the refresh icon.

 \[Omitted image "RefreshConditions.png"\] Alt text: refresh icon

 If the filter does not match any records, the system marks the certification instance as **Closed Complete**, with the **Percent complete** value set to **100%**.

</td></tr></tbody>
</table>
**Related topics**  


[Data Certification planning](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/yokohama/markdown/yokohama/servicenow-platform/configuration-management-database-cmdb/c_PlanningDataCertification.md)

