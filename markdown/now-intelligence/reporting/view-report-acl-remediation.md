---
title: Manage Report ACL assessments
description: When you run the Report ACL \(access control list\) assessment scan, the result is a list of affected reports. The assessment details the users who have seen a report including the report creator. The assessment also includes the roles that the report is limited to and the groups that contain those roles.Add a system property to identify reports affected by report\_view ACLs on dot-walked fields.After you perform the report assessment, you can address affected users. You can change access control list \(ACL\) roles, change sharing options on reports, or add report users to a group to grant them blocking roles.
locale: en-US
release: xanadu
product: Reporting
classification: reporting
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 5
breadcrumb: [ACL Assessment for Reports, Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Manage Report ACL assessments

When you run the Report ACL \(access control list\) assessment scan, the result is a list of affected reports. The assessment details the users who have seen a report including the report creator. The assessment also includes the roles that the report is limited to and the groups that contain those roles.

## Before you begin

Roles required: admin and security\_admin.

## About this task

For reports that are blocked by a table-level read ACL, the assessment displays the table that contains the blocking ACL and which users are blocked. The assessment application does not provide further management tools. For reports that are blocked because they don't have either a report\_view ACL or a read ACL, the report is marked as affected, but doesn’t display the affected users.

**Important:** The roles associated with blocking table access control lists \(ACLs\) and blocking column ACLs come from the sys\_security\_acl\_role table. ACLs that don’t have a role record in this table don’t appear in the Report View ACL List or on lists of affected table, column, and read ACLs.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **ACL Assessment for Reports** &gt; **Affected Reports List**.

2.  Select the info button \(![info button](../../performance-analytics/image/InfoIcon.png)\) next to the report that you want to address and select **Open record** to see the options associated with the report.

    This result shows the following information.

    1.  The users, roles, and groups that the report owner belongs to and has shared the report with. If the field **Is global** is checked, the report is shared with all users. Otherwise, **Shared to users**, **Shared to roles**, and/or **Shared to groups** are selected.
    2.  The number of times users have viewed the report.

        This field is empty if the property **run\_scan\_based\_on\_report\_execution\_only** is false.

    3.  The field **Is blocked by read ACL** is selected when there are no report\_view ACLs on the table the report is based on, but Read ACLs do block access.
    4.  The table with Read ACLs that apply to the report.
    5.  The field **Is blocked without RVA or Read ACL** is selected when the report is blocked for a non-ACL reason.
    6.  Table ACLs \(and column ACLs that apply to all columns on the table\) that apply to the report
    7.  Roles associated with blocking table ACLs
    8.  Links to associated blocking table ACLs
    9.  Column ACLs that apply to the report
    10. Roles associated with blocking column ACLs
    11. Links to the associated blocking column ACLs
    12. A real-time rendition of the report
    ![Report view ACL report options](../image/rep-acl-report-options-2.png)

3.  Select **Ignore Report** to remove this report from future assessments.

    To review these reports later, see [Reassess ignored reports](recover-ignored-reports.md).

4.  Select **Show Affected Users** and then **View Result**.

    The first several affected users appear in a related list below the report assessment. Affected users are users that the report owner has shared the report with but who can’t see the report based on report\_view ACLs.

    The default number of affected users shown is five. To show more, configure the property **sn\_report\_acl.com.par\_report\_acl\_assessment.max\_affected\_users**. For more information, see [Filter report assessment scans](filter-report-assessment-scans.md#).

    ![Report view ACL affected users](../image/rep-acl-report-options-2-pol.png)

5.  Select one or more of the affected users and choose **Action on selected rows** &gt; **Ignore** to leave users' access to the report unchanged.

    Selected users are still unable to view the report but their names don’t show up next time that you run the assessment scan.

6.  Add users to a group.

    1.  Choose one or more affected users.

    2.  Select `Assign to group` from the list **Actions on selected rows**.

        ![Report view ACL affected users](../image/rep-acl-report-options-3-pol.png)

    3.  Choose a group and a role \(if available\) to add the selected users to and select **Submit**.

        Move any users that you don't want to add to the same group into the **Available** column.

        ![Report view ACL affected users](../image/rep-acl-add-users-to-group.png)

    4.  If no groups have at least one blocking role, select an appropriate group and add one of the blocking roles.

        If no groups are appropriate for the users, create a group and assign one of the required roles to it outside of the application. Then within the application, grant access to the selected blocked users. For more information on creating groups, see [Create a user group](https://www.servicenow.com/docs/access?context=t_CreateAGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US).

    5.  Select **Submit**.


## Result

In the Affected Users list, the status of the assigned users changes to Processed. The next time you view this list, these assigned users no longer appear on it.

**Parent Topic:**[ACL Assessment for Reports](../concept/report-view-acl-dashboard.md)

**Related topics**  


[Assign a role to a group](https://www.servicenow.com/docs/access?context=t_AssignRoleToGroup&version=xanadu&pubname=xanadu-platform-administration&ft:locale=en-US)

## Manage reports with ACLs on extended fields

Add a system property to identify reports affected by report\_view ACLs on dot-walked fields.

### Before you begin

Role required: admin and security\_admin.

### Procedure

1.  Create the system property **sn\_report\_acl.com.par\_report\_acl\_assessment.collect\_dotwalk** and set it to `true`.

    For more information on creating system properties, see [Add a system property](https://www.servicenow.com/docs/access?context=r_AvailableSystemProperties&version=xanadu&pubname=xanadu-platform-administration&section=t_AddAPropertyUsingSysPropsList&ft:locale=en-US).

2.  [Perform the Report View assessment scan](perform-report-view-acl-assessment-scan.md).


### Result

The Impacted Reports list has a new column, **Dot walk fields**. This column is visible only when an affected report is identified based on an ACL on a field on an extended table.

**Related topics**  


[Report on extended tables](t_AccessFieldExtendedTable.md#)

## Other report remediation tasks

After you perform the report assessment, you can address affected users. You can change access control list \(ACL\) roles, change sharing options on reports, or add report users to a group to grant them blocking roles.

### Edit ACL roles

Elevate your role to security\_admin and add one or more roles to a blocking ACL. Select the **Table ACLs link**, **Column ACLs link**, or **Read ACLs link** in the Affected Reports form to open the related ACL role list.

![Affected reports list with one blocking ACL link highlighted](../image/affected-reports-blocking-acl.png)

### Edit the report sharing options

-   For reports created in the Classic environment, open the report in the Report Designer and change who the report is shared with. For more information, see [Share a report](t_ShareASetting.md).
-   For reports created in a configurable workspace open the report in the Visualization Designer and change who the report is shared with. For more information, see [Share a data visualization in the Visualization Designer](share-dv-ac.md#).

