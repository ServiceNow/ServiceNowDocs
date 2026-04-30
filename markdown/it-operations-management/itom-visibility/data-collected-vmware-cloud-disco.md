---
title: Data collected for VMware Cloud Discovery
description: Discovery collects information about VMware resources in your cloud service accounts.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Cloud resource discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Data collected for VMware Cloud Discovery

Discovery collects information about VMware resources in your cloud service accounts.

## Distributed Resource Scheduler \(DRS\) discovery

VMware Discovery collects these DRS settings and saves them to the DRS VM Config \[cmdb\_ci\_drs\_vm\_config\] table:

-   DRS settings of vCenter clusters.
-   DRS settings of VMs configured to override cluster behavior.

|Field label|Column name|
|-----------|-----------|
|Cluster|cluster|
|DRS behavior|drs\_behavior|
|DRS enabled|drs\_enabled|
|Virtual machine|virtual\_machine|

## VMware tags

VMware Cloud Discovery finds VMware tags from vCenter and saves them to the Key Value \[cmdb\_key\_value\] table.

|Field label and name|Description|
|--------------------|-----------|
|Configuration item \[configuration\_item\]|Referenced VM with tag attached in vCenter.|
|Key \[key\]|Category name of the tag applied to the resource in vCenter.|
|Tag \[tag\]|Source in vCenter from which tags are fetched. In this case, the value is always **Tags**.|
|Value \[value\]|Tag name that is applied to the resource in vCenter.|

**Parent Topic:**[Cloud resource discovery](cloud-discovery-collected-data.md)

