---
title: Viewing links between alerts in alert groups in Express List
description: Gain a better understanding of the relationships between alerts in alert groups in the Express List by using Link View. Link View offers a visual representation of the relationships between the alerts in a group.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Viewing links between alerts in alert groups in Express List

Gain a better understanding of the relationships between alerts in alert groups in the Express List by using Link View. Link View offers a visual representation of the relationships between the alerts in a group.

When Event Management generates an alert group, Link View shows how the attributes of the alerts in the group are linked. The colored tags represent Configuration Items \(CIs\) and other environment items in relation to the alerts. The information shown in Link View is available without the need for a populated Configuration Management Database \(CMDB\). However, when the CMDB is populated, Link View offers additional value by providing the probable cause of the alerts and the service that the alert group impacts.

![Sample alert group in Link View.](../image/el-link-view-rules-sample.png "Sample alert group in Link View")

You can focus on your areas of interest by dragging the nodes in Link View to different positions. When you refresh an alert group, rearranged nodes appear in their original position again. Therefore, Link View is not refreshed automatically, but waits for you to do so manually. If an alert on a CI impacts a service in the Configuration Management Database \(CMDB\), Link View shows the impacted service, enabling you to view it at a glance for quick triage.

A stacked node indicates that multiple nodes were mapped for the same tag. When the same key-value pair appears in more than one alert, the corresponding node is shown with a badge. For example, when the same key-value pair appears in two alerts, the badge on the node shows the number 2, as seen on the Payment tracker node in the sample alert group figure. When a node has no badge, the key-value pair appeared in only one alert. An active change request, a probable cause of the alert, is marked by a Change badge.

![Node with change badge.](../image/link-view-stacked-node.png "Node with a change badge")

The Link View legend lists the meaning of the symbols and colors used and allows you to toggle between hiding and showing types of tags to reduce noise. In addition, the legend describes the meaning of the various lines linking the alert attributes. Attributes linked by a solid line share one or more alerts, whereas attributes linked by a dotted line are correlated by grouping criteria. For a description of each tag, see [Tags in Express List Link View](../reference/link-view-tags-icons-descriptions.md). Hovering over a node displays a tooltip that includes the name of the tag, its class, its severity, the number of alerts in which it appeared, and whether the alert is primary or secondary or the probable cause of the alert, if applicable.

![Node tooltip with probable cause.](../image/link-view-tooltip.png "Node tooltip")

Currently, Link View is supported for tag-based, rule-based, and CMDB-based alert groups. For more information, see:

-   [Viewing links between alerts in tag-based alert groups](tag-based-link-view-express-list.md)
-   [Viewing links between alerts in rules-based alert groups](el-rule-based-link-view.md)
-   [Viewing links between alerts in CMDB-based alert groups](el-cmdb-based-link-view.md)

**Related topics**  


[View links between alerts in a group in Express List](../task/view-relationships-between-alerts-in-groups.md)

