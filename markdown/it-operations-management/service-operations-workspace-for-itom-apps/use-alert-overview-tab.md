---
title: View alert details in Express List
description: View information about different aspects of an alert in the Express List.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-operations-workspace-for-itom-apps/use-alert-overview-tab.html
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View alert details in Express List

View information about different aspects of an alert in the Express List.

## Before you begin

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon \[Omitted image "express-list1.png"\].

3.  Select the alert number to open it.

    The alert opens in a separate tab, displaying the **Overview** tab.

4.  View different aspects of the alert under each tab.

<table id="table_vs2_prb_5tb"><thead><tr><th>

Tab

</th><th>

Description

</th></tr></thead><tbody><tr><td colspan="2">

Overview tab

</td></tr><tr><td>

Summary

</td><td>

Contains a description of the selected alert, describing why it is considered an issue.

</td></tr><tr><td>

Identified issue

</td><td>

Contains a description of the identified issue, including the affected connector and the underlying error that caused it.

</td></tr><tr><td>

Impact

</td><td>

Lists the Configuration item and any services impacted by the alert.The **Impacted Services** tile includes the following subtabs:

-   **Application services:** The application services affected by the alert. For details on application services, see [Application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/application-services.md).
-   **Related service offerings:** The service offerings connected to the application services affected by the alert.
Application services and their related service offerings display on a many-to-many basis. That is, several service offerings can relate to one or more application services, and several application services can relate to one or more service offerings.

</td></tr><tr><td>

Cause

</td><td>

Lists the log properties with information contributing the alert issue, as well as probable root causes for the alert.

</td></tr><tr><td colspan="2">

 

</td></tr><tr><td>

Details tab

</td><td>

Shows the alert's core attributes, including its number, configuration item, class, resource, type, severity, state, and full description of the identified issue. Alongside are assignment fields \(assigned to, assignment group, task, parent\) plus the work notes and a chronological Activity log tracking state changes and system events.

</td></tr><tr><td colspan="2">

 

</td></tr><tr><td>

Related Records tab

</td><td>

Displays lists of records associated with the alert, organized into categories such as events, impacted services, service offerings, related changes, configuration items, remediation tasks, incidents on CI, repeated alerts, and similar alerts.

</td></tr></tbody>
</table>
