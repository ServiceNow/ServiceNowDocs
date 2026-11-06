---
title: Manage report view ACL assessments
description: When you run the Report ACL assessment scan, the result is a list of affected visualizations. The assessment details the users who have seen a report including the report creator. The assessment also includes the roles that the report is limited to and the groups that contain those roles.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/view-report-acl-remediation.html
release: australia
topic_type: task
last_updated: "2026-10-20"
reading_time_minutes: 4
breadcrumb: [ACL Assessment for Data Visualizations, Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# Manage report view ACL assessments

When you run the Report ACL assessment scan, the result is a list of affected visualizations. The assessment details the users who have seen a report including the report creator. The assessment also includes the roles that the report is limited to and the groups that contain those roles.

## Before you begin

Roles required: admin and security\_admin.

## About this task

**Important:**

-   For data visualizations that are blocked by a table-level read ACL, the assessment displays the table that contains the blocking ACL and which users are blocked. The assessment application does not provide further management tools.

-   For reports that are blocked because they have neither a report\_view ACL nor a read ACL, the report is marked as affected, but doesn’t display the affected users.
-   The roles associated with blocking table access control lists \(ACLs\) and blocking column ACLs come from the sys\_security\_acl\_role table. ACLs that don’t have a role record in this table don’t appear in the Report View ACL List or on lists of affected table, column, and read ACLs.

## Procedure

1.  Navigate to **All** &gt; **Platform Analytics Administration** &gt; **ACL Assessment for Data Visualizations** &gt; **Affected Data Visualizations** or report\_view\_acl\_assessment\_list.do.

2.  Locate the assessment that you want to address.

3.  Hover over the beginning of the row and select the info button \(\[Omitted image "InfoIcon.png"\] Alt text: info button\) to open a preview of the assessment record.

    \[Omitted image "preview-record-info-button.png"\] Alt text: Info button for previewing the record for a report view ACL assessment.

4.  Select **Open record**.

    For a guide to the fields in the record, open [Guide to report view ACL assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-impacted-reports.md) in another tab.

5.  If you don't want to address this visualization, select **Ignore Report** to remove it from future assessments.

    To review these reports later, see [Reassess ignored visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/recover-ignored-reports.md).

6.  Perform remediation.

    -   If you think more roles should be granted access, select the **Table ACLs link**, **Column ACLs link**, or **Read ACLs link**. These links open the relevant Access Control \[sys\_security\_acl\] record where you can add more roles.
    -   Under **Shared with groups**, if you see a group that should be able to view the visualization, modify the group record to include a supported role.
    -   Under **Shared with roles**, if you see a role that should be able to view the visualization, modify the report\_view ACL rules for the table or field and add the role. For more information, see [Configure an ACL](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-security/t_CreateAnACLRule.md).
7.  To address the access rights of individual users, select **Show Affected Users** and then **View Result**.

    The first several affected users appear in a related list after the report assessment. Affected users are users that the visualization owner has shared the visualization with but who can’t see its contents based on report\_view or read ACLs.

    The default number of affected users shown is five. To show more, configure the property **sn\_report\_acl.com.par\_report\_acl\_assessment.max\_affected\_users**. For more information, see [Filter report assessment scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/filter-report-assessment-scans.md).

    \[Omitted image "rep-acl-report-options-2-pol.png"\] Alt text: Report view ACL affected users

8.  If you don't want to address the access of a specific user, tick the box at the beginning of their row and select **Action on selected rows** &gt; **Ignore**.

    Selected users are still unable to view the contents of the visualization, but their names don’t show up next time that you run the assessment scan. You can reassess the ignored user later. For more information, see [Reassess ignored users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/recover-ignored-users.md).

9.  If you think a blocked user should be blocked, consider opening the shared visualization and removing the user from the Shared list.

    For more information, see [Manage data visualization access](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/share-dv-ac.md).

10. To enable a user to meet ACL requirements, do one of the following:

    -   Open the user record and give them a role from the blocking ACL rule or security attribute.
    -   Add the user to a group that has the required role. You can do this directly in the Report view ACL assessment users list. For details, see [Add report\_view ACL blocked user to authorized group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/add-report-view-blocked-user-group.md).

## Result

In the Affected Users list, the status of the assigned users changes to Processed. The next time you view this list, these assigned users no longer appear on it.

-   **[Add report\_view ACL blocked user to authorized group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/add-report-view-blocked-user-group.md)**  
From a report view ACL assessment, you can add an affected user to a group that has a required role. The user can then view the data visualization or Core UI report.
-   **[Manage visualizations with ACLs on extended fields](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/manage-reports-extended-fields.md)**  
Add a system property to identify data visualizations and Core UI reports affected by report\_view ACLs on dot-walked fields.
-   **[Guide to report view ACL assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-impacted-reports.md)**  
The Report view ACL assessments table shows the impacted data visualizations and Core UI reports identified by the ACL Assessment for Data Visualizations. Use this list to remediate affected visualizations and users.

**Parent Topic:**[ACL Assessment for Data Visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/report-view-acl-dashboard.md)

**Related topics**  


[Assign a role to a group](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/platform-administration/t_AssignRoleToGroup.md)

