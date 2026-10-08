---
title: Distribute reports
description: Distribute reports to provide business information to other users.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/now-intelligence/reporting/c\_DistributeReports.html
release: brazil
product: Reporting
classification: reporting
topic_type: concept
last_updated: "2026-09-24"
reading_time_minutes: 2
breadcrumb: [Core UI Reporting, Reporting, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Distribute reports

Distribute reports to provide business information to other users.

On instances with Unified Analytics enabled, and on new Brazil instances, both Core UI reports and Platform Analytics experience data visualizations are found in the Platform Analytics library. Navigate to **All** &gt; **Platform Analytics** &gt; **Library** &gt; **Data Visualizations**. For more information, see [Exploring the Data Visualizations library](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/explore-data-vis-library.md).

## Report access control

You can control who sees reports by applying a security state. You can make reports that are:

-   Globally visible to all users
-   Visible only to you if you're the report creator.
-   Visible to one or more specific roles
-   Visible to one or more specific users or groups

Sharing by user, group, or role, is the primary method of sharing reports. You can use access control lists \(ACLs\) to control access to the underlying table or [database view](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/performance-analytics/performance-analytics-glossary.md) data. Users can view reports when the user does not have access rights to a data record in a data source or source table of a report. However, they aren't able to see that record in a list view or in a drill-down view. Database-view-list reports require the reporting user to satisfy ACLs on the target data to view records in the list. Users without sufficient permissions see filtered list reports.

**Note:** ACLs for a table do not propagate to database views based on that table. Database views require separate ACLs.

Reports that present aggregate data, such as pie or bar reports, don't require the user to satisfy target table ACLs to view the report. ACLs are required to view the list of records when you select a portion of a report visualization. If you have access to a report but not to some of its records, those records don't appear in drill-down lists or list views. However, they are included in visualizations of data.

If a user saves a global report as a group or personal report, the platform copies the report rather than changing its security state. Copying the report enables users who cannot create their own global reports to modify a global report, and then save a personal version of the report.

If a user opens a personal report and tries to save it as a group or global report, the security state is changed rather than copying the report.

-   **[Share a Core UI report](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/t_ShareASetting.md)**  
Control which users and groups can see a Core UI report.
-   **[Schedule emails of Core UI reports](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/t_ScheduleAReport.md)**  
Generate and distribute scheduled reports via email.
-   **[Add a report to a responsive dashboard](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/add-report-to-dashboard.md)**  
Make actionable decisions faster by combining relevant reports and widgets onto a dashboard. Navigating to single reports and widgets is time-consuming and less efficient.
-   **[Export a report to PDF](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/export-report-pdf.md)**  
Export a report to PDF to use it outside of your ServiceNow instance.

**Parent Topic:**[Using reporting](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/now-intelligence/reporting/c_GenerateReports.md)

**Related topics**  


[ACL troubleshooting reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-security/r_ACLTroubleshoot.md)

[Managing roles](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ua-creating-roles.md)

[Creating groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/brazil/markdown/platform-administration/ua-creating-groups.md)

