---
title: Self-health monitors for Event Management
description: Use the Event Management self-health monitors to track Event Management features and resolve issues.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# Self-health monitors for Event Management

Use the Event Management self-health monitors to track Event Management features and resolve issues.

## Monitor Event Management to detect and resolve issues

Enable the self-health feature to help detect and troubleshoot Event Management health issues. Some configuration is required before the self-health feature can display meaningful data. Once configured and the related scheduled jobs are enabled, the Service Operations Workspace displays data that is automatically collected and calculated on a recurring schedule.

**Note:** Event Management Dashboard is not supported for new instances in the Paris release. However, instances upgraded from a release prior to Orlando that use Event Management Dashboard can continue to do so.

The self-health feature creates CIs in the CMDB to represent the components of the self-health service. Use the provided monitors to monitor and track the health of services and Event Management features.

Event Management self-health can:

-   Trigger alerts when there is an issue with Event Management.
-   Display the **ServiceNow Event Management** application services in Service Operations Workspace. Use Service Operations Workspace to view alerts by application service, technical service, and alert groups. You can double-click a tile to view general information about the service.

    ![Service Operations Workspace tile](../image/op-ws-tile.png)

-   Click **Service Details** to view details of the service.
-   Click **Service Map** to view a map representation of the **ServiceNow Event Management** application services to see the relationships between CIs in the **ServiceNow Event Management** application services.

## Self-health monitoring process workflow

After the **Event Management — self-health monitoring** property is enabled:

1.  The **ServiceNow Event Management** application services is automatically created.
2.  Jobs are automatically scheduled to run scripts that configure what must be monitored.
3.  The Monitoring States \[em\_monitor\_state\] table is updated after each event run that the configuration scripts trigger.
4.  The alerts that are generated are monitored.

    The service displays the status of the monitored entity. For example, alerts are displayed in the Event Management dashboard, Service Operations Workspace or All Alerts list.


You can resolve the alerts according to the underlying issue by using **Quick Response** on the standard platform interface. For details, see [Apply a quick response in an alert](../task/apply-quick-response-in-alert.md).

## Jobs scheduled to process scripts

The jobs scheduled to run by default after the **Event Management — self-health monitoring** property is enabled are:

-   The `Event Management - Insert Health Monitor` scheduled job which runs the scripts.
-   The `Event Management - Update Health Monitor` scheduled job which runs the update scripts. This job runs once every minute.

-   **[Start or stop self-health monitoring](../task/start-self-health.md)**  
You can control the starting or stopping of the self-health monitor feature by configuring the self-health monitoring property. The first time that the self-health monitoring property is enabled, it automatically creates the ServiceNow Event Management application services.
-   **[Configure the Event Management - Insert Health Monitor scheduled job](../task/EM-insert-health-job.md)**  
Determine what the Event Management - Insert Health Monitor scheduled job is to monitor. After the job runs, you can view the **ServiceNow Event Management** application services.
-   **[Monitor self-health with domain separation](../task/domain-self-health.md)**  
Use domain separation to enable self-health to display Event Management health issues that are based on data, rules, and settings from the logged in user domain. The selected domain must not contain any child domains.
-   **[Configure a self-health monitor](../task/configure-threshold-monitoring.md)**  
You can configure a self-health monitor to track Event Management components and see that they do not exceed the specified threshold.
-   **[Create a self-health monitor to use custom health monitor script](../task/custom-configure-threshold-monitoring.md)**  
You can create a self-health monitor to use custom health monitor script to monitor specified Event Management components.
-   **[View the Event Management self-health application services map](../task/view-self-health-manual-service.md)**  
You can view Event Management application services maps to have a visualization of the data on configuration items \(CIs\) that comprise this service, and the relations and connections between these CIs.

**Parent Topic:**[Manage and monitor alerts](c_EMAlert.md)

