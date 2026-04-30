---
title: View maps for application services in legacy Agent Workspace
description: Use maps to see the details of application services. Maps show configuration items \(CIs\) making up application services, connections between these CIs and other service-related details.
locale: en-US
release: zurich
product: Service Mapping
classification: service-mapping
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Application service analysis and maintenance using legacy Agent Workspace, Using Service Mapping, Service Mapping, ITOM Visibility, IT Operations Management]
---

# View maps for application services in legacy Agent Workspace

Use maps to see the details of application services. Maps show configuration items \(CIs\) making up application services, connections between these CIs and other service-related details.

## Before you begin

Role required: sm\_app\_owner, service\_mapping\_user, evt\_mgmt\_admin, evt\_mgmt\_operator, or evt\_mgmt\_user

## About this task

The service instance map in the Event Management view reflects the severity status of CIs belonging to the service instance. For more information about viewing service details on maps, see [Application service maps in legacy Agent Workspace](../reference/workspace-application-service-map.md).

## Procedure

1.  In Agent Workspace, click the **Lists** icon on the left pane.

2.  Navigate to **All** &gt; **Services** &gt; **All Services**.

    The list of services displays services in Operational status.

3.  Click the name of the relevant service instance.

    The service tab opens showing service details on the Details tab.

4.  Click **Service Map**.

    The Service Map tab opens displaying the map of this application service.

    ![View application service map](../image/ws-service-map-tab.png)

5.  Click on CIs or their connections to display their details in the Service properties pane on the right.

6.  Display additional information for a CI or application service itself by displaying related records such as alerts, outages, incidents, and problems.

    For more information, see [Modify view for an application service map in legacy Agent Workspace](workspace-modify-map-view.md).

7.  To access the service map in the standard Event Management UI that provides full map-related functionality, click **Full map**.


**Parent Topic:**[Application service analysis and maintenance using legacy Agent Workspace](../concept/service-analysis-maintenance-legacy-workspace.md)

**Related topics**  


[Service Mapping](../reference/c_ServiceMappingOverview.md)

