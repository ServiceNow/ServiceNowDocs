---
title: Share a Core UI report
description: Control which users and groups can see a report in their Reports list.
locale: en-US
release: zurich
product: Reporting
classification: reporting
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
keywords: [Share a Core UI report, Share a report in the classic environment]
breadcrumb: [Distribute reports, Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Share a Core UI report

Control which users and groups can see a report in their Reports list.

## Before you begin

Role required: report\_admin, report\_global, or report\_group.

This topic refers to Reporting in the Core UI. If your instance is a Zurich release or migrated to Platform Analytics experience, see [Share a data visualization in the Visualization Designer](share-dv-ac.md#).

The following roles can share reports:

<table id="table_pfs_kl1_nmb"><thead><tr><th>

Role

</th><th>

Report sharing permissions

</th></tr></thead><tbody><tr><td>

report\_admin

</td><td>

Can share a report that is shared with the user, any group, or everyone. This role can share with:-   any user
-   any group
-   everyone

The report\_admin can also edit reports.

</td></tr><tr><td>

report\_global

</td><td>

-   Can share a report that is shared with everyone. This role can share with everyone.
-   Cannot share a report that is shared with the user or a group

The report\_global user can also edit reports that are shared with everyone.

</td></tr><tr><td>

report\_group

</td><td>

-   Can share a report that is shared with the user, or a report shared with a group the user belongs to. This role can share the report with:
    -   any user
    -   any group
-   Cannot share a report that is shared with everyone, or with a group the user doesn’t belong to.

The report\_group user can edit reports that are shared with the groups they are members of.

</td></tr><tr><td>

report\_publisher

</td><td>

No sharing permissions.

</td></tr><tr><td>

report\_scheduler

</td><td>

No sharing permissions.

</td></tr><tr><td>

report\_user

</td><td>

No sharing permissions.

</td></tr></tbody>
</table>## About this task

You can control who sees reports by making them:

-   Globally visible to all users
-   Visible only to you if you are the report creator.
-   Visible to one or more specific users
-   Visible to one or more specific groups

**Note:** The permissions of a report can constrain the number of users or groups you can share a report with. For more information, see [Restrict report creation with an ACL rule](t_RestrictRepCreationWAnACLRule.md).

It is not possible to grant edit rights on a report when you share it.

## Procedure

1.  Navigate to **All** &gt; **Reports** &gt; **View / Run** and select the report you want to control.

    On instances with Unified Analytics enabled, and on new Zurich instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations** and select **New**. For more information, see [Differences between Core UI and Platform Analytics dashboards](../../dashboards/reference/differences-between-core-ui-ne-dbs.md).

2.  In the upper right side of the report form, click the **Sharing** icon \(![Sharing icon](../../../common/image/Form_ShareIcon.png)\) and select **Share**.

3.  In the Sharing settings dialog box, fill in the fields and click **OK**.

<table id="table_czf_tlh_yq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Visible to

</td><td>

Users to whom the report is available. You can select the following options:-   **Me** Only you can view the report. This option is only available to you on the reports that you create.
-   **Everyone** All users can view the report. However, you can select required roles, and only users with at least one of those roles can view the report.
-   **Groups and Users** Only specific groups and users can see the report.
The **Groups and Users** option is visible to users with the report\_group role.

</td></tr><tr><td>

Requires role

</td><td>

\(Optional\) Roles from the Roles \[sys\_user\_role\] table. If you select any roles, a user must have at least one of them to view the report. If you do not select a role, all users can view the report.You can specify required roles only for reports that are otherwise visible to Everyone. If you modify such a report to be shared with specific Groups and Users, the required roles no longer apply.

</td></tr><tr><td>

Groups

</td><td>

Groups whose members have permission to see the report.This field is available when the **Groups and Users** option is selected.

</td></tr><tr><td>

Users

</td><td>

Users who have permission to see the report.This field is available when the **Groups and Users** option is selected.

</td></tr></tbody>
</table>4.  Click the **Sharing** icon \(![Sharing icon](../../../common/image/Form_ShareIcon.png)\) and select **Add to Dashboard** or **Publish**.

5.  Share the dashboard or share the URL of the published report.

    You can share the URL of the published report with any user, role, or group with whom you have shared the report.

    To publish a report, enable the property **glide.report.published\_reports.enabled**. For more information, see [\(Legacy\) Publish a report](t_PublishAReport.md#).

    The people with whom you share the report must have rights to view the report data.


**Parent Topic:**[Distribute reports](../concept/c_DistributeReports.md)

**Related topics**  


[Share a responsive dashboard](../../dashboards/task/t_ControlAccessToADashboard.md)

[Administering reports](../concept/c_AdminsteringReports.md)

