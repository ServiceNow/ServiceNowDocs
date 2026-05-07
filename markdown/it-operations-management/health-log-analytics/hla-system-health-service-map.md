---
title: Viewing Health Log Analytics system health alerts on the service map
description: The ServiceNow Event Management service map includes a model of the Health Log Analytics core components and the system health alerts that affect them.
locale: en-US
release: australia
product: Health Log Analytics
classification: health-log-analytics
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
keywords: [service map, system health alerts, configuration items, core components, self-health checks, alert criticality, colored bars, critical alerts, major alerts, minor alerts, component monitoring, log ingestion process, data inputs, log sources, HLA AI Engine, Metric Base, impact visualization]
breadcrumb: [Viewing system features and health alerts, Health Log Analytics, ITOM AIOps, IT Operations Management]
---

# Viewing Health Log Analytics system health alerts on the service map

The ServiceNow Event Management service map includes a model of the Health Log Analytics core components and the system health alerts that affect them.

Health Log Analytics and the Event Management application form a single service. Viewing the configuration items \(CIs\) that comprise Health Log Analytics and their relationships helps you visualize the impact of HLA system health issues on the service.

![HLA core components on the Event Management service map.](../image/hla-system-health-service-map.png "HLA components on the Event Management service instance map")

Health Log Analytics uses self-health checks to monitor the health of its components. When it discovers a system health issue, a notification triggers an alert. System health alerts display on the affected CIs on the service map. A colored bar on an affected CI indicates the criticality level of the alert: A red bar signifies a critical alert, an orange bar a major alert, and a yellow bar a minor alert.

For example, the red bar indicates a critical alert on this CI:

![Red critical alert.](../image/hla-service-map-alert-red.png)

If the alert impacts the parent object, the parent object has a bar of the same color. For more information, see [View an alert impact on CIs in a service map](../../event-management/task/t_EMViewTopology.md).

You can drill down into an alert to view details about the issue and then address it by performing the action proposed in the notification. For more information, see [Health Log Analytics self-health checks, notifications, and proposed actions](../reference/hla-self-health-notifications.md).

<table id="table_ryf_rjj_zsb"><thead><tr><th>

Component

</th><th>

What is monitored

</th></tr></thead><tbody><tr><td>

Health Log Analytics core

</td><td>

-   Elasticsearch
-   Metric Base
-   HLA AI Engine

</td></tr><tr><td>

Health Log Analytics

</td><td>

-   Data inputs
-   Log sources

 **Note:** New data inputs and log sources are automatically added to the service map.

</td></tr><tr><td>

Log ingestion process

</td><td>

All elements that affect the log ingestion process.

</td></tr></tbody>
</table>**Related topics**  


[Identify Health Log Analytics system health issues on the service map](../task/hla-system-health-service-map-view.md)

