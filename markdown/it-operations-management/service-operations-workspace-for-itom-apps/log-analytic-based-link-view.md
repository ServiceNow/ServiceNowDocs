---
title: Viewing links between alerts in log analytics-based alert groups
description: Use Link View in Express List to see why alerts in a log analytics-based alert group are correlated together through the visualization of shared attributes.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Viewing links between alerts in log analytics-based alert groups

Use Link View in Express List to see why alerts in a log analytics-based alert group are correlated together through the visualization of shared attributes.

Link View for log analytics-based alert groups shows the connections between component-based alerts. Each component-based alert may involve multiple host configuration items \(CIs\). A component represents a logical part of a service instance where the alert was detected. Components can consist of multiple CIs that perform the same function, such as multiple redundant hosts. For more information, see [Types of Health Log Analytics alerts](../../health-log-analytics-operator/reference/hla-op-log-analytics-alert-types.md).

The colored tags in the link view represent attributes of the alerts such as hosts, users, or correlation indicators extracted from the logs. The lines connect attributes that share the same alert. This visualization helps you understand the relationships between different alerts in the group using their shared attributes.

Log analytics-based groups often contain multiple correlation attributes within a single group. Link View enables you to explore why anomalies detected on different components were correlated into one group. By manipulating the attribute display, you can better understand the relationships between alerts that share common attributes.

![Sample log analytics-based alert group in Link View.](../image/el-link-view-log-analytics.png "Sample log analytics-based alert group in Link View")

In this sample Link View, a component attribute is shown for each child alert in the log analytics alert group. Other attributes show connections between the component alerts.

The Link View legend lists the meaning of the symbols used to represent the attributes. You can toggle between hiding and showing attributes types to reduce noise. For a description of each attribute, see [Attributes in Express List Link View](../reference/link-view-tags-icons-descriptions.md).

![Sample log analytics-based Link View legend.](../image/el-link-view-log-analytics-legend.png)

