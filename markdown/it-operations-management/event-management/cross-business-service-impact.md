---
title: View impact of child service on parent service
description: In the map view of an application service, the severity of a child service is propagated to its parent service.
locale: en-US
release: xanadu
product: Event Management
classification: event-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Alert impact calculation, Manage and monitor alerts, Configuring Event Management, Event Management, ITOM Health, IT Operations Management]
---

# View impact of child service on parent service

In the map view of an application service, the severity of a child service is propagated to its parent service.

## Before you begin

Role required:

-   for application services, evt\_mgmt\_admin
-   for discovered services, service\_mapping\_admin

## About this task

In the map view of a discovered application service, you can see that the severity of a child service is propagated to the parent service.

An application service is affected by the severity of alerts that are directly associated with it and alerts on the CIs that are in the service. If the severity of a child service is higher than that of its parent service, on the map view the parent service shows the severity of the child service. In the map view, the **Impact Tree** list shows the CIs. The color of the CIs indicates the alert severity. The child service is also affected by application services that are under it.

![Child service severity is propagated to parent service](../image/service-health-propagated.png "Example where the parent service shows the severity of the child service")

If a loop is created, for example, by connecting a parent service to a sub-service, this relationship can be viewed in the map view. The impact of this loop is not calculated and the Impact Tree does not display this relationship. For example, assume that there are three CIs, A, B, and C, where C is a sub-service to B and B is a sub-service to A. The relationship of the A connected service to C is displayed in the map view. However, this relationship is not shown in the Impact Tree.

**Note:** A message appears in the system error log in the following format, where the sys\_id of the service and the node changes accordingly: `Found loop in ServiceId:[sysId], and node:[sysId]. Removing this relation to avoid impact loops`

For example, `Found loop in ServiceId:409d4fd59f030200fe2ab0aec32e705c, and node:df5cf6159f030200fe2ab0aec32e70a2. Removing this relation to avoid impact loops`

Click a service or CI to see the alerts that are associated with it. For example, if you click the high-level application service, the alerts that are associated with it are displayed in the alert area under the Map View. The alerts listed are those of the selected service. Alerts of child-services are listed when those services are selected.

![Alert list in the Map View](../image/alert-list-map-view.png "Example of alerts listed under the Map View")

## Procedure

1.  Open an application service map:

    1.  Navigate to **Event Management** &gt; **Services** &gt; **Application Services**.
    2.  Select **View Service** next to the service.
    3.  On the right-hand panel, select **Impact tree**.
    4.  On the lower panel, select **Impact**.

## Result

In the service map, you can visually verify that the service health of the sub-service is rolled-up to the parent service. At the bottom of each icon of an impacted CI is a colored bar that represents the severity of the alert. This color bar also displays in the bottom bar of its parent service. For manual cluster configuration, you can modify the Application Impact and Application Cluster Member.

**Related topics**  


[Transfer a map segment into another application service](../../service-mapping/task/add-segment-to-business-service-map.md)

[Configure a manual cluster](configure-manual-cluster.md)

[Adjust alert impact while triaging an alert](../../event-management-operator/task/operator-adjust-impact-rules.md)

[View an alert impact on CIs in a service map](t_EMViewTopology.md)

