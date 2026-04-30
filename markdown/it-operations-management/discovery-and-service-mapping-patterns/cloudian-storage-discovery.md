---
title: Cloudian Storage Discovery
description: ServiceNow Discovery uses the Cloudian Storage discovery pattern to find Cloudian servers and related disks. Discovering these resources requires installing the Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Cloudian Storage Discovery

ServiceNow Discovery uses the Cloudian Storage discovery pattern to find Cloudian servers and related disks. Discovering these resources requires installing the Patterns application from the ServiceNow Store.

Discovery uses Cloudian Storage System patterns to find Cloudian Storage system data. Discovering these resources requires installing the Discovery and Service Mapping Patterns and the CMDB CI Class Models applications from the ServiceNow Store, as each application is dependent on the other. You can use the patterns for discovering the Cloudian Storage components on the ServiceNow AI Platform using the Paris release or later.

Cloudian is a software-defined data storage company. Cloudian provides turnkey distributed software-defined S3-compatible object storage solutions.

**Cloudian Hyperstore Software** : Deploy the CentOS operating system, related packages, and Hyperstore software binary files on the Hyperstore Node.

**Cloudian Hyperstore Node**: This is an independent hardware server in which Cloudian Hyperstore software is deployed on an industry standard server, on a VM, or it is pre-installed on a Cloudian Hyperstore appliance.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

To discover a device as a Cloudian server, the **/bin/systemctl status cloudian-s3** command must return valid responses and contain the **Cloudian HyperStore Storage System**. If this is not the case, then the device is discovered as a Linux server.

-   Make sure the client is using Discovery patterns.
-   Set **SSH** credentials for the Cloudian Storage Server.
-   Make sure the MID server has access to the target device.
-   Ensure that the Discovery user has the correct privileges to run commands.
-   Install the following plugins:
-   -   CMDB CI Class Models plugin \(Version 1.31.0 or later\)
-   Discovery and Service Mapping Patterns plugin \(Version 1.0.84 or later\)
-   Discovery and Service Mapping Patterns: \(sn\_itom\_pattern\) version 1.0.84 and dependent plugin **CMDB CI Class Models** \(sn\_cmdb\_ci\_class\) version 1.31.0 \(October content release\)

## Credentials

Make sure the Cloudian Hyperstore Software is deployed on either CentOS or RHEL Servers. The credentials configurations are the same as for a Linux server.

Configure the **SSH** credentials for the Cloudian Storage Server.

## Running Discovery

To discover the Cloudian Storage System, create a Discovery schedule that targets the IP address of the Cloudian Storage Server. Make sure that the **SSH** credentials that you configured can access the Cloudian Server.

## Data collected by Discovery during horizontal discovery

<table id="table_ths_ldd_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

 

</td></tr><tr><td>

serial\_number

</td><td>

 

</td></tr><tr><td>

ip\_address

</td><td>

 

</td></tr><tr><td>

manufacturer

</td><td>

 

</td></tr><tr><td>

model\_id

</td><td>

 

</td></tr><tr><td>

short\_description

</td><td>

 

</td></tr><tr><td>

os\_version

</td><td>

 

</td></tr><tr><td>

os

</td><td>

 

</td></tr><tr><td>

ram

</td><td>

 

</td></tr><tr><td>

cpu\_manufacturer

</td><td>

 

</td></tr><tr><td>

cpu\_name

</td><td>

 

</td></tr><tr><td>

cpu\_core\_count

</td><td>

 

</td></tr><tr><td>

cpu\_type

</td><td>

 

</td></tr></tbody>
</table><table id="table_svv_nfd_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

 

</td></tr><tr><td>

device\_id

</td><td>

 

</td></tr><tr><td>

storage\_type

</td><td>

 

</td></tr><tr><td>

size\_bytes

</td><td>

 

</td></tr><tr><td>

manufacturer

</td><td>

 

</td></tr><tr><td>

model\_id

</td><td>

 

</td></tr><tr><td>

computer \[Reference cmdb\_ci\_storage\_server\]

</td><td>

 

</td></tr></tbody>
</table>## File System \[cmdb\_ci\_file\_system\]

<table id="table_ohd_tbj_2rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

 

</td></tr><tr><td>

size\_bytes

</td><td>

 

</td></tr><tr><td>

free\_space\_bytes

</td><td>

 

</td></tr><tr><td>

file\_system

</td><td>

 

</td></tr><tr><td>

mount\_point

</td><td>

 

</td></tr><tr><td>

computer \[Reference cmdb\_ci\_storage\_server\]

</td><td>

 

</td></tr><tr><td>

provided\_by \[Reference cmdb\_ci\_disk\]

</td><td>

 

</td></tr></tbody>
</table>## Network Adapter \[cmdb\_ci\_network\_adapter\]

<table id="table_phd_tbj_2rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

name

</td><td>

 

</td></tr><tr><td>

ip\_address

</td><td>

 

</td></tr><tr><td>

netmask

</td><td>

 

</td></tr><tr><td>

mac\_address

</td><td>

 

</td></tr><tr><td>

cmdb\_ci \[Reference cmdb\_ci\_storage\_server\]

</td><td>

 

</td></tr></tbody>
</table>## IP Address \[cmdb\_ci\_ip\_address\]

<table id="table_qhd_tbj_2rb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ip\_address

</td><td>

 

</td></tr><tr><td>

netmask

</td><td>

 

</td></tr><tr><td>

nic \[Reference cmdb\_ci\_network\_adapter\]

</td><td>

 

</td></tr></tbody>
</table>The **Cloudian**probe is created in the **Unix-Classify** Multiprobe. The **Cloudian** probe runs the **/bin/systemctl status cloudian-s3** command and checks that the output contains **Cloudian HyperStore Storage System**.

![Cloudian Probe.](../image/cloudian-probe.png "Cloudian Probe")

In Unix classification, the **Cloudian Server** classifier runs before the **Linux Classifier**. The Cloudian classifier creates records in the \[cmdb\_ci\_storage\_server\] table. This classifier invokes the Cloudian Storage System Pattern.

Classification Criteria

![Classification Criteria.](../image/classification_criteria.png "Classification Criteria")

## CMDB Data Model

![CMDB Data Model.](../image/cmdb-data-model.png "CMDB Data Model")

Storage Server to Network Adapter

![Storage Server to Network Adapter.](../image/storage_server_to_network_adapter.png "Storage Server to Network Adapter")

Storage Server to Disks

![Storage Server to Disks.](../image/storage_server_to_disks.png "Storage Server to Disks")

Storage Server to Disks and File Systems

![Storage Server to Disks and File Systems.](../image/storage_server-to_disks_and_file_systems.png "Storage Server to Disks and File Systems")

## CI Relationships

## Relationships created by the Cloudian Storage pattern

|Parent|Relationship|Child|
|------|------------|-----|
|cmdb\_ci\_storage\_server|Owns::Owned by|cmdb\_ci\_network\_adapter|
|cmdb\_ci\_storage\_server|Owns::Owned by|cmdb\_ci\_ip\_address|
|cmdb\_ci\_storage\_server|Contains::Contained by|cmdb\_ci\_disk|
|cmdb\_ci\_storage\_server|Contains::Contained by|cmdb\_ci\_file\_system|
|cmdb\_ci\_storage\_server|Virtualized by::Virtualizes|cmdb\_ci\_vm\_instance|
|cmdb\_ci\_disk|Provides::Provided by|cmdb\_ci\_file\_system|

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

