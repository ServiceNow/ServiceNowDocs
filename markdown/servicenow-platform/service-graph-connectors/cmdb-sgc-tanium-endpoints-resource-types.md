---
title: Supported Tanium resource types
description: Several Tanium resource types are imported as CMDB data.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/servicenow-platform/service-graph-connectors/cmdb-sgc-tanium-endpoints-resource-types.html
release: australia
product: Service Graph Connectors
classification: service-graph-connectors
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Reference, Tanium Endpoints, Service Graph Connectors, Integrating third-party data into CMDB, Configuration Management, Extend ServiceNow AI Platform capabilities]
---

# Supported Tanium resource types

Several Tanium resource types are imported as CMDB data.

Tanium resource types refer to the sensors included in the queries used for filtering data using the Tanium API for a specific data source.

The following table lists the Service Graph Connector for Tanium Endpoints data sources and the Tanium sensors they import. ✓ indicates supported, and ✕ indicates not supported.

<table id="table_o2t_br4_q1c"><thead><tr><th>

Data source

</th><th>

CMDB CI classes

</th><th>

Tanium sensors

</th><th>

Data import

</th></tr></thead><tbody><tr><td rowspan="25">

SG-Tanium-Endpoints Hardware-Software

</td><td rowspan="14">

Computer \[cmdb\_ci\_computer\]

</td><td>

Computer Name

</td><td>

✓

</td></tr><tr><td>

Computer Serial Number

</td><td>

✓

</td></tr><tr><td>

Domain Name

</td><td>

✓

</td></tr><tr><td>

Manufacturer

</td><td>

✓

</td></tr><tr><td>

Model

</td><td>

✓

</td></tr><tr><td>

RAM

</td><td>

✓

</td></tr><tr><td>

CPU Details

</td><td>

✓

</td></tr><tr><td>

CPU Manufacturer

</td><td>

✓

</td></tr><tr><td>

Operating System

</td><td>

✓

</td></tr><tr><td>

Asset OS Version

</td><td>

✓

</td></tr><tr><td>

Service Pack

</td><td>

✓

</td></tr><tr><td>

Total Memory

</td><td>

✓

</td></tr><tr><td>

Is Virtual

</td><td>

✓

</td></tr><tr><td>

eidLastSeen

</td><td>

✓

</td></tr><tr><td>

Disk \[cmdb\_ci\_disk\]

</td><td>

Physical disk

</td><td>

✓

</td></tr><tr><td>

File System \[cmdb\_ci\_file\_system\]

</td><td>

Logical Disk

</td><td>

✓

</td></tr><tr><td rowspan="2">

Handheld Computing Device \[cmdb\_ci\_handheld\_computing\]

</td><td>

Mobile Devices**Note:** Mobile Devices isn't a sensor.

</td><td>

✓

</td></tr><tr><td>

All sensors supported by the Computer \[cmdb\_ci\_computer\] class

</td><td>

✓

</td></tr><tr><td>

IP Address \[cmdb\_ci\_ip\_address\]

</td><td>

Tanium Client IP Address

</td><td>

✓

</td></tr><tr><td>

Key Value \[cmdb\_key\_value\]

</td><td>

Custom Tags

</td><td>

✓

</td></tr><tr><td>

Network Adapter \[cmdb\_ci\_network\_adapter\]

</td><td>

Asset Network Adapter

</td><td>

✓

</td></tr><tr><td rowspan="2">

When the Software Asset Management \(SAM\) application isn't installed:

-   Software \[cmdb\_ci\_spkg\]
-   Software Instance \[cmdb\_software\_instance\]

</td><td>

Asset SIU Installed Products \(for software installed on the Computer class\)

</td><td>

✓

</td></tr><tr><td>

Asset Installed Applications \(for software installed on the Handheld Computing Device class\)

</td><td>

✓

</td></tr><tr><td rowspan="2">

When the SAM application is installed: Software Installation \[cmdb\_sam\_sw\_install\]

</td><td>

Asset SIU Installed Products \(for software installed on the Computer class\)

</td><td>

✓

</td></tr><tr><td>

Asset Installed Applications \(for software installed on the Handheld Computing Device class\)

</td><td>

✓

</td></tr><tr><td>

SG-Tanium-Endpoints Usage

</td><td>

Software Usage \[samp\_sw\_usage\]

</td><td>

Asset SIU Product Usage

</td><td>

✓

</td></tr></tbody>
</table>**Note:** Of the four tags available in Tanium \(Custom, Extended Custom, Enhanced, and Meta\), the Service Graph Connector for Tanium Endpoints 1.0.0 version supports only Custom Tags.

**Parent Topic:**[Service Graph Connector for Tanium Endpoints reference](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/service-graph-connectors/sgc-cmdb-tanium-endpoints-reference.md)

