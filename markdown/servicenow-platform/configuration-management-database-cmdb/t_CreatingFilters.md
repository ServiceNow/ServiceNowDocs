---
title: Create a filter
description: You can create as many versions of a filter as necessary. You can then designate which versions are active and available for selection in Compliance template records, Governance Risk and Compliance control test definitions, or Data Certification schedule definitions.
locale: en-US
release: australia
product: Configuration Management Database \(CMDB\)
classification: configuration-management-database-cmdb
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Certification filters, CMDB Compliance, Configuration Management Database \(CMDB\), Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Create a filter

You can create as many versions of a filter as necessary. You can then designate which versions are active and available for selection in Compliance template records, Governance Risk and Compliance control test definitions, or Data Certification schedule definitions.

## Before you begin

Role required: none

## Procedure

1.  Navigate to **All** &gt; **Configuration** &gt; **CI Class Manager**, and:

    1.  Click **Hierarchy** to display the CI Classes list.

        Select the class to create a filter for.

    2.  In the class navigation bar, expand **Health**, select **Compliance**, and then click **Certification Filter**.

2.  Or, navigate to one of these modules:

    -   **Compliance** &gt; **Filters**
    -   **Data Certification** &gt; **Schedules** &gt; **Certification Filters**
3.  Select an existing filter to edit, or click **New**.

4.  Fill in the fields \(see table below\).

5.  Click **Submit**.

    This action saves the filter as version 1.

6.  To create another version of this filter, open the record and modify the name, table, or conditions.

    **Note:** You can change a filter Description without incrementing a version.

7.  Click **Update**.

    The system saves a new version of the current filter and makes it the Active version. The previous version is marked inactive. The system displays only active filter versions for selection when you create templates or schedules.

<table id="table_fy2_yhy_z4"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

\[Read-only\] Displays the automatically assigned filter identification number. All versions of a filter have the same number.

</td></tr><tr><td>

Name

</td><td>

\[Required\] Filter name.

</td></tr><tr><td>

Description

</td><td>

\[Optional\] Describes this filter. You can change the description of a filter without incrementing a version.

</td></tr><tr><td>

Table

</td><td>

Specifies the table containing the records to select. The template or schedule that uses this filter works on this table. For example, select the ESXi Server`[cmdb_ci_esx_server]` table to select VMware ESX servers.

</td></tr><tr><td>

Active

</td><td>

Makes this filter available for use from the **Filter** field on the Certification Template or Schedule Definition form. Multiple versions of a filter can be active. You can activate or deactivate a filter without incrementing the version.

</td></tr><tr><td>

Version

</td><td>

\[Read-only\] Indicates the version of this filter. Any changes to this filter, except to the description or the **Active** check box, makes it inactive. The system increments the version of the updated filter and marks it as active. The system saves all versions of the filter and makes them available for reactivation.

</td></tr><tr><td>

Filter condition

</td><td>

Specifies the fields, operators, and values that create the filter. The available fields are based on the selected table. The condition builder shows the number of records that match the conditions. Click the refresh icon ![Refresh conditions icon.](../image/RefreshConditions.png "Refresh Conditions")

 to recalculate the number of matching records when you edit the conditions.

</td></tr></tbody>
</table>
