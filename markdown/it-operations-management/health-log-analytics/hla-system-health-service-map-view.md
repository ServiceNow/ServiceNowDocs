---
title: Identify Health Log Analytics system health issues on the service map
description: View Health Log Analytics \(HLA\) system health issues on the ServiceNow Event Management service instance map.
locale: en-US
release: yokohama
product: Health Log Analytics
classification: health-log-analytics
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Viewing Health Log Analytics system health alerts on the service map, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Identify Health Log Analytics system health issues on the service map

View Health Log Analytics \(HLA\) system health issues on the ServiceNow Event Management service instance map.

## Before you begin

Role required: evt\_mgmt\_operator or evt\_mgmt\_admin

## About this task

Viewing the configuration items \(CIs\) that comprise Health Log Analytics and their relationships helps you visualize the impact of HLA system health issues on the service. For more information, see [Viewing Health Log Analytics system health alerts on the service map](../concept/hla-system-health-service-map.md).

## Procedure

1.  Navigate to **All** &gt; **Event Management** &gt; **Services** &gt; **Service Instances**.

2.  On the **Service Instances** page, locate ServiceNow Event Management and select **View Service**.

    ![Event Management health - service instance.](../../event-management/image/application-service.png)

    The Event Management service instance map shows the Health Log Analytics core components and the system health alerts that affect them.

3.  On the service map, identify Health Log Analytics system health issues.

4.  Drill down into an alert to view details about the issue.


## What to do next

Address the alert by performing the action proposed in the notification. For more information, see [Health Log Analytics self-health checks, notifications, and proposed actions](../reference/hla-self-health-notifications.md).

**Related topics**  


[Health Log Analytics system health notifications](../reference/hla-sys-health-notifications-ref.md)

