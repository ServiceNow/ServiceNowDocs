---
title: Viewing links between alerts in mixed alert groups
description: View the connections between alerts in mixed alert groups in Express List by using Link View. Link View shows how the attributes of the alerts in the group are linked with each other.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Viewing links between alerts in mixed alert groups

View the connections between alerts in mixed alert groups in Express List by using Link View. Link View shows how the attributes of the alerts in the group are linked with each other.

Link View for mixed alert groups shows the connections between alerts in groups that combine different alert group strategies to form a single cohesive group. For more information, see [Mixed alert grouping](../../event-management/concept/unified-grouping.md).

To view how different alert groups are visualized in Link View, see the description of Link view for the relevant alert group types. Currently, mixed groups are composed of Tag cluster alert groups and CMBD-based alert groups. For more information about Link View for these groups, see [Viewing links between alerts in tag-based alert groups](tag-based-link-view-express-list.md), and [Viewing links between alerts in CMDB-based alert groups](el-cmdb-based-link-view.md).

![Sample mixed alert group in Link View](../image/link-view-mixed-group.png "Sample mixed alert group in Link View")

In this sample Link View of a mixed alert group, the dashed line with the number 1 between the CIs indicates that the CIs are not connected directly but are separated by a CI in the service map in the CMDB topology. The sample also shows the defining attribute for the correlation, datacenter, linked to the relevant CIs.

The Link View **Display** legend lists the meaning of the symbols used to represent the tags and their number of unique nodes. In the legend, defining tags are marked as Correlation. You can toggle between hiding and showing tag types to reduce noise. For a description of each tag, see [Attributes in Express List Link View](../reference/link-view-tags-icons-descriptions.md).

