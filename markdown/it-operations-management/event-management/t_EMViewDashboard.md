---
title: Monitor service health
description: On the Operator Workspace, you can view alerts by application services, technical service, and alert group. For services, you can also open a service map to view relationships between CIs in the service.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/event-management/t\_EMViewDashboard.html
release: australia
product: Event Management
classification: event-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Using Event Management, Event Management, ITOM AIOps, IT Operations Management]
---

# Monitor service health

On the Operator Workspace, you can view alerts by application services, technical service, and alert group. For services, you can also open a service map to view relationships between CIs in the service.

## Before you begin

Ask an administrator to create at least one application services, technical service, or alert group if none of these items exist.

Role required: evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

The Operator Workspace tiles represent a service, alert group, or CI. The tile color represents the overall alert severity.

**Note:** Event Management Dashboard is not supported for new instances in the Paris release. However, instances upgraded from a release prior to Orlando that use Event Management Dashboard can continue to do so.

These tile icons are available:

|Icon|Meaning|
|----|-------|
|\[Omitted image "mapped-app-service-icon.png"\] Alt text: Mapped application service icon|Represents the status of a mapped application services.|
|\[Omitted image "alert-group-icon.png"\] Alt text: Alert group icon|Represents the status of an Alert group with a set of corresponding open alerts.|
|\[Omitted image "dynamic-ci-group-icon.png"\] Alt text: Dynamic CI group icon|Represents the status of a dynamic CI group.|

Each tile represents the highest severity of an alert for the service, alert group, or CI. For example, a tile appears in red if an alert is critical. A green tile indicates either information alerts or no currently active alerts. As the alert severities change, the tile colors update accordingly. The following severities are available:

-   **Red**: critical severity \(highest severity\). Immediate action is required. The resource is either not functional or critical problems are imminent.
-   **Orange**: major severity. Major functionality is severely impaired or performance has degraded.
-   **Yellow**: minor severity. Partial, non-critical loss of functionality or performance degradation occurred.
-   **Blue**: warning severity \(lowest severity\). Attention is required, even though the resource is still functional.
-   **Green**: informational. No severity. An alert is created. The resource is still functional.

## Procedure

1.  To integrate with Operational Intelligence, activate the Operational Intelligence \(com.snc.sa.metric\) plugin.

    Follow the steps in the [Get started with Metric Intelligence](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/get-started-metrics.md) topic. Metrics information appears on the **Metrics** tab in the Service Operations Workspace.


-   **[View discovered service history](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/t_EMViewAlertHistory.md)**  
The discovered service history shows the frequency of discovered services for a particular time period.
-   **[Monitor alerts for an application services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/t_EMMonitorManualService.md)**  
To view information for application services only, navigate to the application services list. From this list, you can open service maps to view and manage alerts for the CIs in each service.
-   **[View monitored services](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/monitor-services.md)**  
View all services that Event Management supports, such as, alert groups, discovered services, application services, and technical services. According to the type of service, you can view service definition details or drill down into the service.

**Parent Topic:**[Using Event Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/user-guide.md)

**Related topics**  


[View metric values in the Insights Explorer](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/metric-intelligence/view-metrics-explorer.md)

