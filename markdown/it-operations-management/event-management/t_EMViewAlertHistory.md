---
title: View discovered service history
description: The discovered service history shows the frequency of discovered services for a particular time period.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/t\_EMViewAlertHistory.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
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

    The history timeline appears, with changes to the service indicated by a clock icon \(\[Omitted image "clock-icon.png"\] Alt text: Clock icon\).

    \[Omitted image "history-map-timeline.png"\] Alt text: History map timeline

4.  To view a map showing changes in the service's severity, click the More icon \(\[Omitted image "more-actions-icon-horizontal.png"\] Alt text: More actions icon\) and select **Advanced map**.

    \[Omitted image "EMTimeline.png"\] Alt text: Discovered services history

    The displayed color corresponds to the discovered services severity, and the length of the bar in each color corresponds to how long the discovered services stayed at that severity.

    The following table explains the severity colors:

    |Severity|Icon color|
    |--------|----------|
    |Critical|Red \[Omitted image "red-critical-icon.png"\] Alt text: Red icon - Critical severity|
    |Major|Orange \[Omitted image "orange-major-icon.png"\] Alt text: Orange icon - Major severity|
    |Minor|Yellow \[Omitted image "yellow-minor-icon.png"\] Alt text: Yellow icon - Minor severity|
    |Warning|Blue \[Omitted image "blue-warning-icon.png"\] Alt text: Blue icon - Warning severity|

5.  To change the information that appears on the discovered services history Advanced map, click a history icon.

    \[Omitted image "disc-services-history-timeline-icon.png"\] Alt text: Discovered services history icons

    -   **Calendar icon**: Show information for currently active discovered services.
    -   **Hours**: Show information for discovered services that occurred in the past hour.
    -   **Days**: Show information for discovered services that occurred in the past 24 hours.
    -   **Weeks**: Show information for discovered services that occurred in the past week.
    -   **Months**: Show information for discovered services that occurred in the past month.

**Parent Topic:**[Monitor service health](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/t_EMViewDashboard.md)

