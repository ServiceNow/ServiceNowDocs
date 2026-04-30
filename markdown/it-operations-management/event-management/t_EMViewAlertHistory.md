---
title: View discovered service history
description: The discovered service history shows the frequency of discovered services for a particular time period.
locale: en-US
release: zurich
product: Event Management
classification: event-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Monitor service health, Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# View discovered service history

The discovered service history shows the frequency of discovered services for a particular time period.

## Before you begin

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

The discovered services history appears only when there are multiple discovered services that occur over a period. A discovered service is a service that is discovered by Service Mapping. The discovered services history is not available for application services. If no discovered services are generated for a particular service, the discovered services history is hidden.

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Service Operations Workspace**.

2.  Click a service tile and click **Service Map**.

3.  Click the **History map** button.

    The history timeline appears, with changes to the service indicated by a clock icon \(![Clock icon](../image/clock-icon.png)\).

    ![History map timeline](../image/history-map-timeline.png)

4.  To view a map showing changes in the service's severity, click the More icon \(![More actions icon](../image/more-actions-icon-horizontal.png)\) and select **Advanced map**.

    ![Discovered services history](../image/EMTimeline.png)

    The displayed color corresponds to the discovered services severity, and the length of the bar in each color corresponds to how long the discovered services stayed at that severity.

    The following table explains the severity colors:

    |Severity|Icon color|
    |--------|----------|
    |Critical|Red ![Red icon - Critical severity](../image/red-critical-icon.png)|
    |Major|Orange ![Orange icon - Major severity](../image/orange-major-icon.png)|
    |Minor|Yellow ![Yellow icon - Minor severity](../image/yellow-minor-icon.png)|
    |Warning|Blue ![Blue icon - Warning severity](../image/blue-warning-icon.png)|

5.  To change the information that appears on the discovered services history Advanced map, click a history icon.

    ![Discovered services history icons](../image/disc-services-history-timeline-icon.png)

    -   **Calendar icon**: Show information for currently active discovered services.
    -   **Hours**: Show information for discovered services that occurred in the past hour.
    -   **Days**: Show information for discovered services that occurred in the past 24 hours.
    -   **Weeks**: Show information for discovered services that occurred in the past week.
    -   **Months**: Show information for discovered services that occurred in the past month.

**Parent Topic:**[Monitor service health](t_EMViewDashboard.md)

