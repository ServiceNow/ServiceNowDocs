---
title: Viewing links between alerts in mixed alert groups
description: Link View displays the connections between alerts in mixed alert groups in Express List, including how alert attributes relate to each other within the group.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/service-operations-workspace-for-itom-apps/unified-alert-group-link-view.html
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [Link View, mixed alert group, alert group, alert correlation, tag cluster, CMDB-based alert group, CI topology, service map, Service Operations Workspace]
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Viewing links between alerts in mixed alert groups

Link View displays the connections between alerts in mixed alert groups in Express List, including how alert attributes relate to each other within the group.

Link View for mixed alert groups shows the connections between alerts in groups that combine different alert group strategies to form a single cohesive group.

To view how different alert groups are visualized in Link View, see the description of Link view for the relevant alert group types. Currently, mixed groups are composed of Tag cluster alert groups, CMDB-based alert groups, related log entities and shared impacted services.

For more information about alerts in the mixed alert group, see [Mixed alert grouping](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/event-management/unified-grouping.md).

For more information about Link View for related groups, see [Viewing links between alerts in tag-based alert groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/tag-based-link-view-express-list.md), and [Viewing links between alerts in CMDB-based alert groups](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/el-cmdb-based-link-view.md).

\[Omitted image "link-view-mixed-group.png"\] Alt text: Sample mixed alert group in Link View

The preceding figure shows the Link View of a mixed alert group. The dashed line with the number 1 between the CIs indicates that the CIs aren't connected directly but are separated by a CI in the service map in the CMDB topology. The sample also shows the defining attribute for the correlation, datacenter, linked to the relevant CIs.

\[Omitted image "link-view-mixed-group-enhanced.png"\] Alt text: Mixed alert group with related log entities and shared impacted services in Link View

The Link View for a mixed alert group that includes related log entities and shared impacted services displays connected nodes representing each correlation source and attribute, including log analytics data, CMDB information, and impacted services. This information gives operators a picture of the scope and nature of the grouping at a glance.

The Link View **Display** legend lists the meaning of the symbols used to represent the tags and their number of unique nodes. In the legend, defining tags are marked as **Correlation**. You can toggle between hiding and showing tag types to reduce noise. For a description of each tag, see [Attributes in Express List Link View](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/link-view-tags-icons-descriptions.md).

**Related topics**  


[Viewing links between alerts in alert groups in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/el-link-view.md)

[View links between alerts in a group in Express List](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/service-operations-workspace-for-itom-apps/view-relationships-between-alerts-in-groups.md)

