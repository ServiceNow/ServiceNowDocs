---
title: ACL Assessment for Reports
description: Use the ServiceNow ACL Assessment for Reports to identify reports that are blocked by report\_view ACLs \(access control lists\).
locale: en-US
release: yokohama
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Administering reports, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# ACL Assessment for Reports

Use the ServiceNow® ACL Assessment for Reports to identify reports that are blocked by report\_view ACLs \(access control lists\).

## Application components

Use the Report ACL dashboard to identify reports that users aren't able to see. If the owner doesn't meet ACL constraints, ACLs can even block report creators from their own reports. Consider a report shared with all ITIL users. A table or table column the report is based on limits access to those users with an admin role. In this case, most users with the itil role aren’t able to view the report. The application identifies both the users and the reports. Using the information from the assessment, you can ignore users and reports and address them later.

The scan evaluates all reports against the report\_view ACLs on the instance. It also identifies tables without report\_view ACLs and evaluates which users won’t pass the READ ACLs on a table. The ACL assessment then allows you to address users in both categories - those who don't pass report\_view ACLs and those who don't pass READ ACLs on reports without report\_view ACLs.

Outside of the application, you can change sharing in the report or visualization designer, or change the access of users, groups, and roles.

The application has three components:

-   **Report ACL Dashboard**

    Run the scan from within the dashboard.

-   **Affected Reports List**

    View all affected reports in a platform list. You can remediate reports here using platform filtering capabilities.

-   **Ignored Reports and Users List**

    Remove users and reports from this list so that they appear the next time you scan your reports.


**Note:** Some tables in the ServiceNow platform have access control lists created on them by default.

-   **[Install the ACL Assessment for Reports](../task/install-report-acl-app.md)**  
The ACL Assessment for Reports enables you to identify users that don't have access to reports and to enable access where appropriate.
-   **[Perform the Report View assessment scan](../task/perform-report-view-acl-assessment-scan.md)**  
Scan your instance for reports that users would be unable to view based on existing access control lists \(ACLs\).
-   **[View the list of affected reports](../task/view-impacted-reports.md)**  
You can view a list of all impacted reports identified by the ACL assessment for reports. Use this list to remediate affected reports and users.
-   **[Manage Report ACL assessments](../task/view-report-acl-remediation.md#)**  
When you run the Report ACL \(access control list\) assessment scan, the result is a list of affected reports. The assessment details the users who have seen a report including the report creator. The assessment also includes the roles that the report is limited to and the groups that contain those roles.
-   **[Filter report assessment scans](../task/filter-report-assessment-scans.md#)**  
Especially on large instances, the ACL Assessment for Reports can take a long time. To reduce the assessment time, you can use system properties to filter the reports that the assessment applies to.
-   **[The report\_view ACLs list](../task/view-report-acls-list.md)**  
View the entire list of report\_view ACLs and their associated roles to have a higher-level view of the access control on your instance.
-   **[Reassess ignored reports](../task/recover-ignored-reports.md)**  
When you address the ACL Assessment for Reports, you can ignore any report. View these reports to consider their statuses again.
-   **[Reassess ignored users](../task/recover-ignored-users.md)**  
When you address the ACL Assessment for Reports, you can ignore any individual user. View these users to consider their statuses again.
-   **[Report assessment and domain separation](../reference/report-acl-dashboard-domain-sep.md)**  
In domain separated instances, the ACL Assessment for Reports has certain limitations.

**Parent Topic:**[Administering reports](c_AdminsteringReports.md)

