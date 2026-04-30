---
title: Tags in Express List Link View
description: The table lists the node tags that are available in Link View with their icon and description.
locale: en-US
release: xanadu
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Service Operations Workspace for ITOM reference, Service Operations Workspace for ITOM, ITOM Health, IT Operations Management]
---

# Tags in Express List Link View

The table lists the node tags that are available in Link View with their icon and description.

<table id="table_icp_2f3_d1c"><thead><tr><th>

Tag name

</th><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Impacted service

</td><td>

![Impacted service tag icon.](../image/tag-icon-impacted-service.png)

</td><td>

Service in the Configuration Management Database \(CMDB\) impacted by an alert on a CI,

</td></tr><tr><td>

Resource

</td><td>

![Resource tag icon.](../image/tag-icon-resource.png)

</td><td>

Node resource that is relevant to the event. For example, Disk C, CPU-1, the name of a process, or service. Maximum length: 100 characters.

</td></tr><tr><td>

Source

</td><td>

![Source tag icon.](../image/tag-icon-source.png)

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td></tr><tr><td>

Region

</td><td>

![Region tag icon.](../image/tag-icon-region.png)

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

Location

</td><td>

![Location tag icon.](../image/tag-icon-location.png)

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

Assignment group

</td><td>

![Assignment group tag icon.](../image/tag-icon-assignment-group.png)

</td><td>

Alert assignment group.

</td></tr><tr><td>

Environment

</td><td>

![Environment tag icon](../image/tag-icon-environment.png)

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

Metric

</td><td>

![Metric tag icon.](../image/tag-icon-metric.png)

</td><td>

Unique name that describes which metric data is collected.

</td></tr><tr><td>

IP address

</td><td>

![IP address tag icon.](../image/tag-icon-ip-address.png)

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

CI

</td><td>

![CI tag icon.](../image/tag-icon-ci.png)

</td><td>

JSON string that represents a configuration item. For example, `{"name":"SAP ORA01","type":"Oracle"}`. The CI identifier that generated the event appears in the Additional information field. Maximum length: 1000 characters.

</td></tr><tr><td>

Node

</td><td>

![Node tag icon.](../image/tag-icon-node.png)

</td><td>

Node name, fully qualified domain name \(FQDN\), IP address, or MAC address that is associated with the event, such as IBM-ASSET. Maximum length: 100 characters.

</td></tr><tr><td>

Application

</td><td>

![Application tag icon.](../image/tag-icon-application.png)

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

Other**Note:** This tag is user-defined. All the other tags are predefined in the system.

</td><td>

![Other tag icon.](../image/tag-icon-other.png)

</td><td>

User-defined tag.**Note:** All the other tags are predefined in the system.

</td></tr></tbody>
</table>|Link|Visual representation|Description|
|----|---------------------|-----------|
|Solid line|![Solid line linking attributes in Link View.](../image/link-view-solid-line.png)|Solid line linking attributes in Link View, indicating that the attributes share one or more alerts.|
|Dotted line|![Dotted line linking attributes in Link View.](../image/link-view-dotted-line.png)|Dotted line linking attributes in Link View, indicating that the attributes are correlated by grouping criteria.|

**Parent Topic:**[Service Operations Workspace for ITOM reference](../concept/sow-reference-itom.md)

