---
title: Viewing links between alerts in network traffic-based alert groups
description: View the connections between alerts in network traffic-based alert groups in Express List by using Link View. Network traffic-based alert groups are created by analyzing network traffic connections between processes across hosts.
locale: en-US
release: yokohama
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in the Service Operations Workspace for ITOM, Using Service Operations Workspace for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Viewing links between alerts in network traffic-based alert groups

View the connections between alerts in network traffic-based alert groups in Express List by using Link View. Network traffic-based alert groups are created by analyzing network traffic connections between processes across hosts.

Service candidates identified by ML Service Mapping group alerts based on network traffic connections between processes. Link View shows a contextual view of network incidents based on these groups of directly connected processes. Service candidates are potential collections of processes within your IT environment that are identified based on their network connections and interactions.

![A map with seven nodes with links between the network traffic-based alerts.](../image/el-link-view-network-traffic.png "Sample network traffic-based alert group in Link View")

In this sample Link View of a network traffic-based alert group, the dashed lines indicate that there are connected processes running on the CIs. Attributes linked by a solid line share one or more alerts.

**Related topics**  


[Viewing links between alerts in alert groups in Express List](el-link-view.md)

[View links between alerts in a group in Express List](../task/view-relationships-between-alerts-in-groups.md)

