---
title: Regulatory Change Management overview page
description: The Regulatory Change Management overview page provides a high-level view of the regulatory activities in your organization. If you have the sn\_grc\_reg\_change.manager role, you can view this page in the Compliance Workspace.
locale: en-US
release: australia
product: Regulatory Change Management Service Portal
classification: regulatory-change-management-service-portal
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Regulatory Change Management, Governance, Risk, and Compliance]
---

# Regulatory Change Management overview page

The Regulatory Change Management overview page provides a high-level view of the regulatory activities in your organization. If you have the sn\_grc\_reg\_change.manager role, you can view this page in the Compliance Workspace.

**Note:** The Overview Dashboard in the Classic UI is no longer available from the Yokohama release.

The prerequisites for displaying the Regulatory Change Management overview page in the Compliance Workspace are:

-   Download the GRC: Regulatory Change Management application from the ServiceNow Store in your instance.
-   Log in as a user with the sn\_grc\_reg\_change.manager role into the Regulatory Change Management application.

Use the ![](../image/reg-change-icon.png) to access the landing page.

The Regulatory Change Management application managers with the sn\_grc\_reg\_change.manager user role assign the regulatory alerts and monitor the associated regulatory change tasks, import document tasks, and action tasks.

The Regulatory Change Management application in the Compliance Workspace is designed for the users with the following roles:

-   Regulatory Change Management application managers with the sn\_grc\_reg\_change.manager role: Only the users with the sn\_grc\_reg\_change.manager role can view the Home page of the Regulatory Change Management application in the Compliance Workspace.
-   Regulatory Change Management application users with the sn\_grc\_reg\_change.user role: Users with the sn\_grc\_reg\_change.user role can view the tasks assigned to them in the Regulatory Change Management application, but they cannot view the Regulatory Change Management application landing page in the Compliance Workspace.

## Overview page view

The overview page consists of the data visualization widgets that display the regulatory activity across your organization. The data visualization widgets are selectable widgets that use color coding to distinguish the states of the alerts and the tasks. You can click each widget to view all the associated regulatory alerts or tasks. The color scheme for each donut chart or bar graph is displayed in each subsection.

The GRC: Regulatory Change Management landing page displays the following sections:

-   Activity overview
-   Trends
-   Tracking

![RCM dashboard view from the Compliance Workspace with activity, tracking, and trend reports.](../image/rcm-homepage-ws.png "The GRC: Regulatory Change Management application landing page view")

-   Activity overview: This section contains an overview of the regulatory alerts and the tasks associated with the regulatory alerts across your organization.

    |Section|Description|
    |-------|-----------|
    |Alerts|Active regulatory alerts that are new, in progress, and deferred in numbers and percentage displayed in a donut chart. Also displays impact assessment tasks associated with the alerts.|
    |Change tasks|Active change tasks that are in new, implementation, respond, and awaiting approval state displayed in a donut chart. The tasks are displayed in numbers and the percentage.|
    |Import document tasks|Active import document tasks that are in ready to import, in progress, and awaiting approval state displayed in a donut chart. The tasks are displayed in numbers and the percentage.|
    |Alerts by overall impact|Displays the overall impact of the regulatory alerts such as no impact, low, medium, and high impact alerts displayed in a bar graph.|
    |Impacted entities/Business lines impacted|Grouping of the impact assessment reports based on the impacted entities in a bar graph. The bar graph displays a maximum of five entities for a better display.|
    |Taxonomy alerts|Taxonomy alerts as per the taxonomy elements such as content type, jurisdiction, regulatory body, sector, and theme.|

-   Tracking: This section displays the tracking status of the regulatory alerts and the associated regulatory tasks.

    |Section|Description|
    |-------|-----------|
    |Alerts|Tracking status of the regulatory alerts such as open and unassigned alerts.|
    |Impact assessments|Status of the impact assessments such as open and unassigned impact assessments.|
    |Issues|Status of the issues such as open and overdue issues.|
    |Action tasks|Active action tasks that are open including the action tasks that are in new, in progress, and overdue states.|

-   Trends: This section displays the trends for the open alerts or trends by the taxonomy elements.

    |Section|Description|
    |-------|-----------|
    |Open alerts for last 12 months|Timeline of the incoming regulatory alerts that are active and are not closed over a period of 12 months. For example, if 10 records are received every month, they are grouped by a quarter and a total of 30 records for each quarter are displayed in the line graph. Four plots are displayed on the X-axis and 30 records are displayed in each plot.|
    |Trends by taxonomy|Trends noted by the taxonomy elements such as content type, jurisdiction, regulatory body, sector, and theme.|

-   Tasks: This section contains an overview of the user's tasks and user group's tasks.

    |Section|Description|
    |-------|-----------|
    |My tasks|Tasks assigned to the user such as open and overdue tasks.|
    |My group's work|Tasks assigned to the user group such as open and overdue tasks.|
    |View all tasks|Link to the Tasks view in the Home page.|


