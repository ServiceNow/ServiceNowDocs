---
title: Viewing links between alerts in tag-based alert groups
description: View the connections between alerts in a tag-based alert group in Express List by using Link View. Link View shows how the attributes of the alerts in the group are linked with each other.
locale: en-US
release: zurich
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Viewing links between alerts in alert groups in Express List, Express List in SOW for ITOM, Using SOW for ITOM, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Viewing links between alerts in tag-based alert groups

View the connections between alerts in a tag-based alert group in Express List by using Link View. Link View shows how the attributes of the alerts in the group are linked with each other.

When you've set alert tags and Event Management has generated an alert group based on tag-based rules, Link View offers a visual representation of the relationships between the alerts in the group. The colored tags in the view represent Configuration Items \(CIs\) and other environment items in relation to the alerts.

![Sample tag-based alert group in Link View.](../image/el-link-view-tag-based.png "Sample tag-based alert group in Link View")

In this example, the defining tag for the correlation, Application, is linked to the tags of the relevant CIs. However, a correlation can be defined by any tag or combination of two tags, such as Resource and Metric name. When the defining tag is missing from Link View, the correlation was based on information that is not represented in the view, such as the description. Each CI node is further linked to the tags that appeared on the same alert as that CI.

In an alert group that was generated from tag rules, nodes connected by a dashed line signify an approximate, "fuzzy" match. This means that the nodes were correlated when the match on the tag rule was not exact, but close enough to be significant. For example, this could happen when a location, email address, or IP pattern was similar enough to qualify as a match.

The Link View legend lists the meaning of the symbols and colors used to represent the tags and their number of unique nodes. In the legend, defining tags are marked as Correlation. You can toggle between hiding and showing tag types to reduce noise. For a description of each tag, see [Attributes in Express List Link View](../reference/link-view-tags-icons-descriptions.md).

**Parent Topic:**[Service Operations Workspace for ITOM](sow-landing-page-itom.md)

**Related topics**  


[Viewing links between alerts in alert groups in Express List](el-link-view.md)

[View links between alerts in a group in Express List](../task/view-relationships-between-alerts-in-groups.md)

