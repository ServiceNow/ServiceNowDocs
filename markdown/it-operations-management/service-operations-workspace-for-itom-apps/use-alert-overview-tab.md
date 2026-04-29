---
title: View details about the impact and cause of an alert in Express List
description: View information about an alert on the alert's Overview tab in the Express List.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# View details about the impact and cause of an alert in Express List

View information about an alert on the alert's Overview tab in the Express List.

## Before you begin

Role required: evt\_mgmt\_operator

## Procedure

1.  Navigate to **Workspaces** &gt; **Service Operations Workspace**.

2.  From the navigation bar, select the Express list icon ![](../../event-management/image/express-list1.png).

3.  Select the alert number to open it.

    The alert opens in a separate tab, displaying the **Overview** tab.

4.  View alert information on the **Overview** tab.

<table id="table_vs2_prb_5tb"><thead><tr><th>

Section

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Summary

</td><td>

Contains a description of the selected alert, describing why it is considered an issue.

</td></tr><tr><td>

Impact

</td><td>

Lists the Configuration item and any services impacted by the alert.The **Impacted Services** tile includes the following subtabs:

-   **Application services:** The application services affected by the alert. For details on application services, see [Application services](https://www.servicenow.com/docs/access?context=application-services&version=australia&pubname=australia-servicenow-platform&ft:locale=en-US).
-   **Related service offerings:** The service offerings connected to the application services affected by the alert.
Application services and their related service offerings display on a many-to-many basis. That is, several service offerings can relate to one or more application services, and several application services can relate to one or more service offerings.

</td></tr><tr><td>

Cause

</td><td>

Lists the log properties with information contributing the alert issue, as well as probable root causes for the alert.

</td></tr></tbody>
</table>
