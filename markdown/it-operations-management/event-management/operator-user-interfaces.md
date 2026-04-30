---
title: Event Management operator environment
description: As an Event Management operator, your primary work environment is the Service Operations Workspace dashboard.
locale: en-US
release: yokohama
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Event Management Operator Tutorial, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Event Management operator environment

As an Event Management operator, your primary work environment is the Service Operations Workspace dashboard.

In this, the third lesson in the Event Management tutorial, you get an overview of your workspaces so you know how to find the information you need.

<table id="table_or3_vg3_3db"><tbody><tr><td>

Lesson 1

</td><td align="justify">

![Overview icon](../image/progress-complete2.png)

</td><td>

[An overview of events and alerts](operator-events-alerts.md)

</td></tr><tr><td>

Lesson 2

</td><td align="justify">

![Overview BS icon](../image/progress-complete2.png)

</td><td>

[An overview of application services](operator-application-services.md)

</td></tr><tr><td>

Lesson 3

</td><td align="justify">

![Operators icon](../image/progress-wip.png)

</td><td>

Event Management operator environment

</td></tr><tr><td>

Lesson 4

</td><td align="justify">

![Operators do icon](../image/progress-not-started.png)

</td><td>

[What operators do](operator-process.md)

</td></tr></tbody>
</table>## The Service Operations Workspace dashboard

Your main area of work is the Service Operations Workspace dashboard, which provides a view that focuses on how alerts relate to application services. From here, you can drill into each application services to see the affected CIs and get an understanding of the overall impact of whatever caused the alert. To open the dashboard, navigate to **Event Management** &gt; **Service Operations Workspace**.

![Service Operations Workspace dashboard overview](../image/operator-workspace-dashboard.png "Service Operations Workspace")

The main sections of the dashboard are:

-   **Banner**

    The banner contains controls that show or hide application services based on the criteria you select:

<table id="table_jfs_jyq_hdb"><tbody><tr><td>

Click a severity level to show or hide application services based on the alerts associated with them.

 ![Severity slider](../image/severity-breakdown.png)

</td></tr><tr><td>

Use the **Group** and **Segment** controls to organize the view.

 **Note:** Your administrator assigns an application the criticality and cost value to your application services.

![Prioritize by](../image/group-and-segment-controls.png "Group and Segment filters")

</td></tr></tbody>
</table>-   **Application services**

    The Service Operations Workspace dashboard displays tiles that represent application services. The color of a tile represents the severity of the alerts that are associated with the application service.

<table id="table_p1c_hrr_hdb"><tbody><tr><td>

Click a tile to show a summary of alerts associated with the application service. Click to view details or the service map.

 ![Alerts for an application service](../image/dashboard-alert-summary-popup.png)

</td></tr></tbody>
</table>-   **Alerts**

    Click the List icon \(![List icon](../../event-management/image/list-icon.png)\). On the Lists tab, click the kind of alert to view.

<table id="table_zkt_jlr_hdb"><tbody><tr><td>

You can filter or sort the list to find an alert. Sort by any alert details, such as the **Priority**, which considers multiple factors for how serious the alert is, or the **Severity**, which is value provided by the event monitoring tool.

 ![Sort icon](../image/sort-by-severity.png)

</td></tr><tr><td>

Open any alert by clicking the number.

 ![Alert number icon](../image/operator-dashboard-click-alert.png)

</td></tr></tbody>
</table>    You will learn about what each of the columns means for an alert later on when you analyze an alert.


## Application service map views on the Service Operations Workspace dashboard

Double-click the name of an application service tile to open one of the application service map views. The view that you see depends on the type of application service.

-   **For a manual or standard application service, this view appears:**

    ![An application service](../image/operator-manual-service-dashboard.png)

    The application service map that you were introduced to in a previous lesson appears in the main panel. This is what you can do from this view:

<table id="table_fs1_3bs_hdb"><tbody><tr><td>

Click any of the CIs to see the alerts only for that CI and to display the details about that CI in the **Properties** pane.

 ![Click CI to see alerts](../image/operator-dashboard-click-ci.png)

</td></tr><tr><td>

Click **Impact Tree** to see the state of all the CIs and how they affect each other when receiving an alert. You will learn more about the impact tree later on in the tutorial.

 ![Impact tree](../image/operator-dashboard-impact.png)

</td></tr><tr><td>

Open any alert from the **Alerts** list at the bottom by clicking the number.

 ![Alert number icon](../image/operator-dashboard-click-alert.png)

</td></tr><tr><td>

 

</td></tr></tbody>
</table>-   **For a technical application service, this view appears:**

    ![Technical service](../image/operator-technical-service-dashboard.png)

    This is what you can do from this view:

<table id="table_y3b_gvr_hdb"><tbody><tr><td>

Click any CI to view details about it.

 ![Click a database](../image/operator-technical-service-dashboard-db.png)

</td></tr><tr><td>

Open any alert from the **Alerts** list at the bottom by clicking the number.

 ![Alert number icon](../image/operator-dashboard-click-alert.png)

</td></tr></tbody>
</table>
## Continue the tutorial

Proceed to the next lesson: [What Event Management operators do](operator-process.md).

**Parent Topic:**[Event Management Operator Tutorial](operator-guide-em.md)

