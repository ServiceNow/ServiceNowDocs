---
title: Tags in Express List Link View
description: The table lists the node tags that are available in Link View with their icon and description.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/xanadu/it-operations-management/service-operations-workspace-for-itom-apps/link-view-tags-icons-descriptions.html
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

\[Omitted image "tag-icon-impacted-service.png"\] Alt text: Impacted service tag icon.

</td><td>

Service in the Configuration Management Database \(CMDB\) impacted by an alert on a CI,

</td></tr><tr><td>

Resource

</td><td>

\[Omitted image "tag-icon-resource.png"\] Alt text: Resource tag icon.

</td><td>

Node resource that is relevant to the event. For example, Disk C, CPU-1, the name of a process, or service. Maximum length: 100 characters.

</td></tr><tr><td>

Source

</td><td>

\[Omitted image "tag-icon-source.png"\] Alt text: Source tag icon.

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td></tr><tr><td>

Region

</td><td>

\[Omitted image "tag-icon-region.png"\] Alt text: Region tag icon.

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

Location

</td><td>

\[Omitted image "tag-icon-location.png"\] Alt text: Location tag icon.

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

Assignment group

</td><td>

\[Omitted image "tag-icon-assignment-group.png"\] Alt text: Assignment group tag icon.

</td><td>

Alert assignment group.

</td></tr><tr><td>

Environment

</td><td>

\[Omitted image "tag-icon-environment.png"\] Alt text: Environment tag icon

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

Metric

</td><td>

\[Omitted image "tag-icon-metric.png"\] Alt text: Metric tag icon.

</td><td>

Unique name that describes which metric data is collected.

</td></tr><tr><td>

IP address

</td><td>

\[Omitted image "tag-icon-ip-address.png"\] Alt text: IP address tag icon.

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

CI

</td><td>

\[Omitted image "tag-icon-ci.png"\] Alt text: CI tag icon.

</td><td>

JSON string that represents a configuration item. For example, `{"name":"SAP ORA01","type":"Oracle"}`. The CI identifier that generated the event appears in the Additional information field. Maximum length: 1000 characters.

</td></tr><tr><td>

Node

</td><td>

\[Omitted image "tag-icon-node.png"\] Alt text: Node tag icon.

</td><td>

Node name, fully qualified domain name \(FQDN\), IP address, or MAC address that is associated with the event, such as IBM-ASSET. Maximum length: 100 characters.

</td></tr><tr><td>

Application

</td><td>

\[Omitted image "tag-icon-application.png"\] Alt text: Application tag icon.

</td><td>

Predefined tag extracted from connector payload.

</td></tr><tr><td>

Other**Note:** This tag is user-defined. All the other tags are predefined in the system.

</td><td>

\[Omitted image "tag-icon-other.png"\] Alt text: Other tag icon.

</td><td>

User-defined tag.**Note:** All the other tags are predefined in the system.

</td></tr></tbody>
</table>|Link|Visual representation|Description|
|----|---------------------|-----------|
|Solid line|\[Omitted image "link-view-solid-line.png"\] Alt text: Solid line linking attributes in Link View.|Solid line linking attributes in Link View, indicating that the attributes share one or more alerts.|
|Dotted line|\[Omitted image "link-view-dotted-line.png"\] Alt text: Dotted line linking attributes in Link View.|Dotted line linking attributes in Link View, indicating that the attributes are correlated by grouping criteria.|

**Parent Topic:**[Service Operations Workspace for ITOM reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/xanadu/markdown/xanadu/it-operations-management/service-operations-workspace-for-itom-apps/sow-reference-itom.md)

