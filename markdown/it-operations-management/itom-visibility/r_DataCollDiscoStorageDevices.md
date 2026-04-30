---
title: Data collected by Discovery on storage devices
description: Discovery identifies and classifies information about storage devices.
locale: en-US
release: xanadu
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2025-08-05"
reading_time_minutes: 2
breadcrumb: [Storage Discovery via SMI-S and CIM, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Data collected by Discovery on storage devices

Discovery identifies and classifies information about storage devices.

|Field|Description|
|-----|-----------|
|Name|Name of the storage disk.|
|Computer|Reference to the host CI.|
|Interface|Interface type with which the storage disk is connected to the host.|
|Size|Size of the storage disk.|
|Free disk space \(GB\)|Free space in GV available on the disk.|
|Manufacturer|Manufacturer of the storage disk.|
|Model ID|Model name of the disk.|

|Field|Description|
|-----|-----------|
|Name|Name of the CI.|
|Path|Path to the file share.|

|Field|Description|
|-----|-----------|
|Name|Name of the storage pool.|
|Size|Size of the storage pool.|
|Free space|Free space available in the pool.|
|Hosted by|Reference to the CMDB CI.|

|Field|Description|
|-----|-----------|
|Name|Name of the storage port.|
|WWPN|Unique Worldwide Port Name \(WWPN\) for the storage port.|
|Speed|Speed of the storage port.|

|Field|Description|
|-----|-----------|
|Name|Name of the Storage Host Bus Adapter \(HBA\).|
|Model ID|Model name of the HBA.|
|Computer|Reference to the computer CI.|

|Field|Description|
|-----|-----------|
|Name|Name of the CI.|
|Manufacturer|Manufacturer of the storage server.|
|Model ID|Model name of the storage server.|
|Operating System|Operating system \(OS\) of the storage server.|
|OS Version|OS version of the storage server.|
|Description|Short description of the storage server.|

|Field|Description|
|-----|-----------|
|Name|Name of the storage volume.|
|Object ID|Unique ID for the storage volume.|
|State|State of the storage volume.|
|Size|Size of the storage volume.|
|Storage Type|Type of storage volume.|

## Storage relationships

Discovery establishes the correct relationships between Network-Attached Storage \(NAS\) storage devices and remotely mounted client servers that consume the storage. Discovery maps NAS file shares. It maps by taking the IP or hostname of a remote mounted disk on the client computer. It then matches it to the IP or hostname of the storage server providing the exported file system.

Discovery creates the following relationships for storage CIs running on Storage Area Networks.

|Parent Component|Relationship|Child Component|
|----------------|------------|---------------|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Exports to::Imports from|Fibre Channel Disk \[cmdb\_ci\_fc\_disk\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Exports to::Imports from|iSCSI \[cmdb\_ci\_iscsi\_disk\]|

Discovery maps NAS file shares. It maps by resolving the hostname of a remote mounted disk on the client computer to an IP address. It then matches it to the IP address of the storage server that provides the exported file system. Discovery extracts the hostname or IP address from the NAS path to determine the identity of the storage server. If the hostname is an actual hostname, the system immediately resolves that value into an IP address. It also stores it in the **nas\_ip\_address** field of the NAS File System \[cmdb\_ci\_nas\_file\_system\] table.

Discovery creates the following relationships for storage CIs running on Network Attached Storage \(NAS\). These relationships are the same between Linux and Windows operating system hosts.

|Parent Component|Relationship|Child Component|
|----------------|------------|---------------|
|NAS File System \[cmdb\_ci\_nas\_file\_system\]|Allocated from::Allocated to|Storage File Share \[cmdb\_ci\_storage\_fileshare\]|

**Parent Topic:**[Storage Discovery via SMI-S and CIM](r_DataCollDiscoStorageviaSMISCIM.md)

