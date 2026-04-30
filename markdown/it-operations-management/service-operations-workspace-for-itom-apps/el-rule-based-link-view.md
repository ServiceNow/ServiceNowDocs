---
title: Viewing links between alerts in rules-based alert groups
description: View the connections between alerts in a rules-based alert group in Express List by using Link View. Link View shows how the attributes of the alerts in the group are linked with each other.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Viewing links between alerts in rules-based alert groups

View the connections between alerts in a rules-based alert group in Express List by using Link View. Link View shows how the attributes of the alerts in the group are linked with each other.

When you've set alert rules and Event Management has generated an alert group based on these rules, Link View offers a visual representation of the relationships between the alerts in the group. The colored tags in the view represent Configuration Items \(CIs\) and other environment items in relation to the alerts.

![Sample rules-based alert group in Link View.](../image/el-link-view-rules-based.png "Sample rules-based alert group in Link View")

Rules-based alert groups are comprised of a primary alert and one or more secondary alerts. The primary alert is generated directly and is represented in Link View as the Home node. Secondary alert nodes are connected to the Home node by a dashed line, indicating that they don't share the same alert, but are correlated using rule criteria. A solid line between nodes indicates that the connected nodes share the same alert or multiple alerts.

If an alert on a CI impacts a service in the Configuration Management Database \(CMDB\), Link View shows the impacted service, enabling you to view it at a glance for quick triage. Hovering over a node displays a tooltip that includes the name of the tag, its type, the number of alerts in which it appeared, and whether it is a primary or secondary alert.

**Related topics**  


[Viewing links between alerts in alert groups in Express List](el-link-view.md)

[View links between alerts in a group in Express List](../task/view-relationships-between-alerts-in-groups.md)

