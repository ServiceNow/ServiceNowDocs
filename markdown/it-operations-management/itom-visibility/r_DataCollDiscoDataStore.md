---
title: Datastore data collected by Discovery
description: Discovery identifies each datastore in the system and creates the relationships with the virtual machines and the ESX servers that use these datastores.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [VMware vCenter, VMware, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Datastore data collected by Discovery

Discovery identifies each datastore in the system and creates the relationships with the virtual machines and the ESX servers that use these datastores.

## Datastores

Discovery uses the VMWare - vCenter Datastores probe to collect this data from datastores.

|Field Label|Table Name|Column Name|Description|
|-----------|----------|-----------|-----------|
|Accessible|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|accessible|Whether the datastore is collected or not.|
|Capacity \(GB\)|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|capacity|Amount of space provided by the datastore.|
|Clustered|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|clustered|If the datastore is clustered \(belongs to a storage pod\).|
|Free space \(GB\)|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|freespace|Amount of space still available on the datastore.|
|Type|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|type|The type of file system volume, such as WFS or NFS.|
|URL|VMware vCenter Datastore \[cmdb\_ci\_vcenter\_datastore\]|url|The unique URL locator for the datastore.|

## HostMounts

Discovery uses both the VMWare - vCenter ESX Hosts and VMWare - vCenter Datastores probes to collect datastore host mount data.

|Field label|Table|Column|
|-----------|-----|------|
|Accessible|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|accessible|
|Access Mode|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|access\_mode|
|VMware vCenter Datastore|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|datastore|
|ESX Server|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|esx\_server|
|vCenter Reference|VMware Datastore HostMount \[vcenter\_datastore\_hostmount\]|vcenter\_ref|

**Parent Topic:**[Discovery for VMware vCenter](../concept/c_DiscoveryForVMwareVCenter.md)

