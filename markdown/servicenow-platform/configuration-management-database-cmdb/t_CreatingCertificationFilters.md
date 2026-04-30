---
title: Create a certification filter
description: A filter is a subset of configuration items from any ServiceNow table that is created with a standard condition builder.
locale: en-US
release: zurich
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Data Certification planning, Data Certification on Core UI, Data Certification, CMDB data management, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
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

    ![Creating a certification filter.](../image/CertificationFilterV1.png "Certification filter V1")

5.  To create another filter version, modify the filter conditions and click **Update**.

    The system saves the new filter and increments the version number.

    ![Updating a certification filter.](../image/CertificationFilterV2.png "Certification filter V2")

    By default, the Certification Filters list shows only the current version of each filter. To see all filter versions, click **All** in the breadcrumbs.

    ![Viewing the list of certification filters.](../image/CertificationFilterList.png "Certification Filter List")

6.  To make an inactive filter the current version, open the inactive filter and click **Revert**.

    ![Reverting a certification filter.](../image/CertificationFilterRevert.png "Certification filter revert")

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

 ![refresh icon](../../compliance/image/RefreshConditions.png "Refresh Conditions")

 If the filter does not match any records, the system marks the certification instance as **Closed Complete**, with the **Percent complete** value set to **100%**.

</td></tr></tbody>
</table>
**Related topics**  


[Data Certification planning](../concept/c_PlanningDataCertification.md)

