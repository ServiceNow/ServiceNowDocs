---
title: ACL Assessment for Data Visualizations
description: Use the ServiceNow ACL Assessment for Data Visualizations to identify data visualizations and reports whose contents are blocked by report\_view or read ACLs \(access control lists\).
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/now-intelligence/report-view-acl-dashboard.html
release: australia
topic_type: concept
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Configure, Data visualizations, Platform Analytics experience, Platform Analytics]
---

# ACL Assessment for Data Visualizations

Use the ServiceNow® ACL Assessment for Data Visualizations to identify data visualizations and reports whose contents are blocked by report\_view or read ACLs \(access control lists\).

## Application components

Use the Report ACL dashboard to identify data visualizations and Core UI reports that users aren't able to see. If the owner doesn't meet ACL constraints, ACLs can even block report creators from their own data visualizations and reports. Consider a report shared with all ITIL users. A table or table column the report is based on limits access to those users with an admin role. In this case, most users with the itil role aren’t able to view the report. The application identifies both the users and the data visualizations and reports. Using the information from the assessment, you can ignore users and visualizations and address them later.

The scan evaluates all data visualizations and reports against the report\_view ACLs on the instance. It also identifies tables without report\_view ACLs and evaluates which users won’t pass the READ ACLs on a table. The ACL assessment then allows you to address users in both categories: those who don't pass report\_view ACLs, and those who don't pass read ACLs on data visualizations and reports that have no report\_view ACLs.

Outside of the application, you can change sharing in the report or visualization designer, or change the access of users, groups, and roles.

The application has three components:

-   **ACL Dashboard**

    Run the scan from within the dashboard.

-   **Affected Data Visualizations List**

    View all affected data visualizations and reports in a platform list. You can remediate data visualizations and reports here using platform filtering capabilities.

-   **Ignored Data Visualizations and Users List**

    Remove users and data visualizations and reports from this list so that they appear the next time you scan your data visualizations and reports.


**Note:** Some tables in the ServiceNow platform have access control lists created on them by default.

-   **[Install the ACL Assessment for Data Visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/install-report-acl-app.md)**  
The ACL Assessment for Data Visualizations enables you to identify users that don't have access to reports and to enable access where appropriate.
-   **[Perform the Report View Assessment scan](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/perform-report-view-acl-assessment-scan.md)**  
Scan your instance for data visualizations and Core UI reports that users were stopped from viewing based on existing access control lists \(ACLs\).
-   **[Manage report view ACL assessments](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-report-acl-remediation.md)**  
When you run the Report ACL assessment scan, the result is a list of affected visualizations. The assessment details the users who have seen a report including the report creator. The assessment also includes the roles that the report is limited to and the groups that contain those roles.
-   **[Filter report assessment scans](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/filter-report-assessment-scans.md)**  
Especially on large instances, the ACL Assessment for Data Visualizations can take a long time. To reduce the assessment time, you can use system properties to filter the reports that the assessment applies to.
-   **[The report\_view ACLs list](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/view-report-acls-list.md)**  
View the entire list of report\_view ACLs and their associated roles to have a higher-level view of the access control on your instance.
-   **[Reassess ignored visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/recover-ignored-reports.md)**  
When you address the ACL Assessment for Data Visualizations, you can ignore any data visualization or Core UI report. View these visualizations to consider their statuses again.
-   **[Reassess ignored users](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/recover-ignored-users.md)**  
When you address the ACL Assessment for Data Visualizations, you can ignore any individual user. View these users to consider their statuses again.
-   **[Report assessment and domain separation](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/report-acl-dashboard-domain-sep.md)**  
In domain separated instances, the ACL Assessment for Data Visualizations has certain limitations.

**Parent Topic:**[Configure data visualizations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/now-intelligence/configure-data-visualizations.md)

