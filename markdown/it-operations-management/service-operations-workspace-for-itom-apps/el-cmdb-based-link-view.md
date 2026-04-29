---
title: Viewing links between alerts in CMDB-based alert groups
description: View the connections between alerts in alert groups in Express List that were created based on the proximity of Configuration Items \(CIs\) in the Configuration Management Database \(CMDB\). Link View shows how the attributes of the alerts in the group are linked with each other.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Viewing links between alerts in CMDB-based alert groups

View the connections between alerts in alert groups in Express List that were created based on the proximity of Configuration Items \(CIs\) in the Configuration Management Database \(CMDB\). Link View shows how the attributes of the alerts in the group are linked with each other.

When alerts on CIs that are located near each other in the CMDB topology occur within a certain time-frame, Event Management generates a CMDB-based alert group. Event Management correlates CIs in a service map when they are separated by a maximum of three other CIs. The colored tags in Link View offer a visual representation of the CIs and other environment items in relation to the alerts in the group.

![Sample CMDB-based alert group in Link View.](../image/el-link-view-topology.png "Sample CMDB-based alert group in Link View")

In this sample Link View of a CMDB-based alert group, the dashed line with the number 2 between the CIs indicates that the CIs are not connected directly, but are separated by two CIs in the service map in the CMDB topology. The sample CMDB service map also shows correlated CIs separated by two CIs.

![Sample service map with correlated CIs.](../image/el-correlated-cis.png "Sample service map with correlated CIs")

**Related topics**  


[Viewing links between alerts in alert groups in Express List](el-link-view.md)

[View links between alerts in a group in Express List](../task/view-relationships-between-alerts-in-groups.md)

