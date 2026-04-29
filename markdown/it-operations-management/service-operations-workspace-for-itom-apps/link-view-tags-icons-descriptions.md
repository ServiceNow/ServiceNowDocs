---
title: Attributes in Express List Link View
description: The table lists the node attributes available in Link View with their icon and description.
locale: en-US
release: australia
product: Service Operations Workspace for ITOM Apps
classification: service-operations-workspace-for-itom-apps
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Service Operations Workspace for ITOM reference, Service Operations Workspace for ITOM, ITOM AIOps, IT Operations Management]
---

# Attributes in Express List Link View

The table lists the node attributes available in Link View with their icon and description.

**Note:** "Attribute" is a generic term that represents fields and tags found on the alerts or configuration items \(CI\).

<table id="table_icp_2f3_d1c"><thead><tr><th>

Attribute name

</th><th>

Icon

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Impacted service

</td><td>

![](../image/tag-icon-impacted-service.png)

</td><td>

Service in the Configuration Management Database \(CMDB\) impacted by an alert on a CI.

</td></tr><tr><td>

Resource

</td><td>

![](../image/tag-icon-resource.png)

</td><td>

Node resource that is relevant to the event. For example, Disk C, CPU-1, the name of a process, or service. Maximum length: 100 characters.

</td></tr><tr><td>

Source

</td><td>

![](../image/tag-icon-source.png)

</td><td>

Event monitoring software that generated the event, such as SolarWinds or SCOM. Maximum length: 100 characters.

</td></tr><tr><td>

Region

</td><td>

![](../image/tag-icon-region.png)

</td><td>

Predefined attribute extracted from connector payload.

</td></tr><tr><td>

Location

</td><td>

![](../image/tag-icon-location.png)

</td><td>

Predefined attribute extracted from connector payload.

</td></tr><tr><td>

Assignment group

</td><td>

![](../image/tag-icon-assignment-group.png)

</td><td>

Alert assignment group.

</td></tr><tr><td>

Environment

</td><td>

![](../image/tag-icon-environment.png)

</td><td>

Predefined attribute extracted from connector payload.

</td></tr><tr><td>

Metric

</td><td>

![](../image/tag-icon-metric.png)

</td><td>

Unique name that describes which metric data is collected.

</td></tr><tr><td>

IP address

</td><td>

![](../image/tag-icon-ip-address.png)

</td><td>

Predefined attribute extracted from connector payload.

</td></tr><tr><td>

CI

</td><td>

![](../image/tag-icon-ci.png)

</td><td>

JSON string that represents a configuration item. For example, `{"name":"SAP ORA01","type":"Oracle"}`. The CI identifier that generated the event appears in the Additional information field. Maximum length: 1000 characters.

</td></tr><tr><td>

Node

</td><td>

![](../image/tag-icon-node.png)

</td><td>

Node name, fully qualified domain name \(FQDN\), IP address, or MAC address that is associated with the event, such as IBM-ASSET. Maximum length: 100 characters.

</td></tr><tr><td>

Application

</td><td>

![](../image/tag-icon-application.png)

</td><td>

Predefined attribute extracted from connector payload.

</td></tr><tr><td>

Process

</td><td>

![](../image/attribute-icon-process.jpg)

</td><td>

A process or a cluster of processes running on the host that are identified by the horizontal discovery.

</td></tr><tr><td>

Component

</td><td>

![](../image/attribute-icon-component.png)

</td><td>

A logical part of a service instance where the alert was detected, with one component shown for each child alert.

</td></tr><tr><td>

Service

</td><td>

![](../image/attribute-icon-service.png)

</td><td>

Attribute extracted from the log file. The impact of this alert on the service might not be clear or defined.

</td></tr><tr><td>

Host

</td><td>

![](../image/attribute-icon-host.png)

</td><td>

Attribute extracted from the log file. It might not be identified in the CMBD.

</td></tr><tr><td>

User

</td><td>

![](../image/attribute-icon-user.png)

</td><td>

Attribute extracted from the log file.

</td></tr><tr><td>

Account

</td><td>

![](../image/attribute-icon-account.png)

</td><td>

Attribute extracted from the log file.

</td></tr><tr><td>

Path

</td><td>

![](../image/attribute-icon-path.png)

</td><td>

Path or route extracted from the log file.

</td></tr><tr><td>

Request id

</td><td>

![](../image/attribute-icon-request-id.png)

</td><td>

The request ID extracted from the log file.

</td></tr><tr><td>

URL

</td><td>

![](../image/attribute-icon-url.png)

</td><td>

Web address or URL extracted from the log file.

</td></tr><tr><td>

Detection

</td><td>

![](../image/attribute-icon-detection.png)

</td><td>

An identified anomaly on a metric measured by Health Log Analytics.

</td></tr><tr><td>

Other**Note:** This attribute is user-defined. All the other attributes are predefined in the system.

</td><td>

![](../image/tag-icon-other.png)

</td><td>

User-defined attribute.**Note:** All the other attributes are predefined in the system.

</td></tr></tbody>
</table>|Link|Visual representation|Description|
|----|---------------------|-----------|
|Solid line|![Solid line linking attributes in Link View.](../image/link-view-solid-line.png)|Solid line linking attributes in Link View, indicating that the attributes share one or more alerts.|
|Dotted line|![Dotted line linking attributes in Link View.](../image/link-view-dotted-line.png)|Dotted line linking attributes in Link View, indicating that the attributes are correlated by grouping criteria.|

**Parent Topic:**[Service Operations Workspace for ITOM reference](../concept/sow-reference-itom.md)

