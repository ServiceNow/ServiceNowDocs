---
title: Monitor alerts for an application services
description: To view information for application services only, navigate to the application services list. From this list, you can open service maps to view and manage alerts for the CIs in each service.
locale: en-US
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Monitor service health, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Monitor alerts for an application services

To view information for application services only, navigate to the application services list. From this list, you can open service maps to view and manage alerts for the CIs in each service.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Services** &gt; **Application Services**.

    ![Application service list](../image/application-service-list.png)

2.  In the row of the required application services, click **View Map**.

3.  Do one or more of the following.

<table id="choicetable_manualservices"><thead><tr><th align="left" id="d409225e110">

Option

</th><th align="left" id="d409225e113">

Action

</th></tr></thead><tbody><tr><td id="d409225e119">

**View alert details for a CI**

</td><td>

In the service map:1.  Click a CI tile.
2.  Below the map, click the **Alerts** tab and review the listed alerts.


</td></tr><tr><td id="d409225e140">

**View impact on the CI parent**

</td><td>

In the service map:1.  Click a CI tile.
2.  Below the service map, click the **Impact** tab and review the listed impact rules.
3.  Adjust the impact rules as necessary.


</td></tr><tr><td id="d409225e164">

**Change the map display, map layout, or map indicators**

</td><td>

In the service map header:1.  Click the menu icon.
2.  Configure the appropriate settings.


</td></tr><tr><td id="d409225e182">

**Navigate to another application services**

</td><td>

In the service map header:1.  Click the down arrow next to the service name or the folder icon for all services.
2.  Search for and select another application services \(![Manual application service icon](../image/EventManagementManualBSIcon.png)\).
 The icon color represents the highest impact or severity for active alerts on the application services.

-   **Critical**: Red \(highest severity\).
-   **Major**: Orange.
-   **Minor**: Yellow.
-   **Warning**: Blue \(lowest severity\).


</td></tr><tr><td id="d409225e232">

**View properties for a CI**

</td><td>

In the service map:1.  Click a CI tile.
2.  In the side pane, click the **Properties** tab and review information about the CI.
3.  If you want to view more detailed information, scroll to the end of the pane and click **Detailed Properties**.


</td></tr></tbody>
</table>
**Parent Topic:**[Monitor service health](t_EMViewDashboard.md)

