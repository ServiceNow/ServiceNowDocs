---
title: Filter report assessment scans
description: Especially on large instances, the ACL Assessment for Reports can take a long time. To reduce the assessment time, you can use system properties to filter the reports that the assessment applies to.Use these properties to configure the ACL Assessment for Reports scan.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [ACL Assessment for Reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Filter report assessment scans

Especially on large instances, the ACL Assessment for Reports can take a long time. To reduce the assessment time, you can use system properties to filter the reports that the assessment applies to.

## Before you begin

Roles required: admin and security\_admin.

You can work with all the properties in the ACL Assessment for Reports except two:

-   **sn\_report\_acl.com.par\_report\_acl\_assessment.report\_view.sys\_ids**
-   **sn\_report\_acl.glide.script.block.client.globals**

## Procedure

1.  Navigate to **All** &gt; **System Properties** &gt; **All Properties**.

2.  Filter the list to show only the properties that contain report\_acl in the name.

    ![System properties list header with Name filter option *report_acl entered](../image/rep-acl-sys-props.png)

3.  Filter out the properties **sn\_report\_acl.com.par\_report\_acl\_assessment.report\_view.sys\_ids** and **sn\_report\_acl.glide.script.block.client.globals**.

    ![Filtered list of report ACL system properties](../image/rep-acl-sys-props-filtered.png)

4.  Use the remaining properties to configure the assessment scan.


**Parent Topic:**[ACL Assessment for Reports](../concept/report-view-acl-dashboard.md)

## Report assessment system properties

Use these properties to configure the ACL Assessment for Reports scan.

To configure system properties, navigate to `sys_properties.list` and filter on the property name.

<table id="table_a5d_h2k_zw"><thead><tr><th>

Property

</th><th>

Description

</th></tr></thead><tbody><tr><td>

sn\_report\_acl.run\_scan\_with\_queryNoDomain

</td><td>

Only valid on domain-separated instances. Defines whether the app considers the user domain when you run the query. If false, the security\_admin gets results only for the domains they have visibility to. A global security\_admin can set the property to true and retrieve the results for all the domains on the instance. The individual security\_admins can then view the collected results for their own domains. For more information, see [Report assessment and domain separation](../reference/report-acl-dashboard-domain-sep.md).If you set this property to true on an instance that is not domain separated, then the assessment runs as a normal query.

 If you delete this property, the default value in the code is false.

 Type: true/false

 Default: false

</td></tr><tr><td>

sn\_report\_acl.add\_encoded\_query\_for\_sys\_report\_table

</td><td>

Allows security admin users to add an encoded AND query condition to the query that the assessment scan is executing on the sys\_report table. For example, you can add an encoded query that evaluates reports only on specified tables.The validity of the encoded query is the user's responsibility. For performance reasons, the app does not validate additional queries in code before execution.

 If you delete this property or it has an empty value, then the assessment scan runs with the original conditions only.

 Type: string

</td></tr><tr><td>

sn\_report\_acl.com.par\_report\_acl\_assessment.collect\_dotwalk

</td><td>

Determines whether the app checks dot-walked fields for affected reports.When false, the performance of the app improves, but the app gives only a subset of the total results.

 Type: true/false

 Default: false

</td></tr><tr><td>

sn\_report\_acl.add\_encoded\_query\_for\_sys\_user\_table

</td><td>

Allows security admin users to add an encoded AND query condition to the query that the assessment scan executes on the sys\_user table. For example, you can add an encoded query that evaluates only specified roles.The validity of the encoded query is the user's responsibility. For performance reasons, the app doesn’t validate additional queries in the code before execution.

 If you delete this property, or it has an empty value, then the assessment scan runs with the original conditions only.

 Type: string

</td></tr><tr><td>

sn\_report\_acl.process\_reports\_executed\_within\_X\_days\_ago

</td><td>

Defines the maximum number of days since the last time that a report was viewed by any user that the app considers when running the assessment scan.Type: Integer

 Default: 365

</td></tr><tr><td>

sn\_report\_acl.run\_scan\_based\_on\_report\_execution\_only

</td><td>

The scan calculates the number of executions of each affected report. If this property is false, the **Total Executions** column in the Impacted Reports list is always empty, and **process\_reports\_executed\_within\_X\_days\_ago** is ignored.Type: true/false

 Default: true

</td></tr><tr><td>

sn\_report\_acl.com.par\_report\_acl\_assessment.max\_affected\_users

</td><td>

The maximum number of affected users retrieved when you click **Show Affected Users**. Applies to reports viewable by users with specified roles or reports viewable by everyone.

 For reports viewable by groups, this value is the maximum number of affected users retrieved per group.

 Type: Integer

 Default: 5

</td></tr><tr><td>

sn\_report\_acl.com.par\_report\_acl\_assessment.collect\_dotwalk

</td><td>

Captures report fields on extended tables that cause a report to be blocked. This property adds the column **Dot Walk Fields** to the Impacted Reports table if those fields exist.Type: true/false

 Default: true

</td></tr></tbody>
</table>