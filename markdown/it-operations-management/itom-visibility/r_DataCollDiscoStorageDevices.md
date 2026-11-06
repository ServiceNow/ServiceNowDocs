---
title: Data collected by Discovery on storage devices
description: Discovery identifies and classifies information about storage devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/itom-visibility/r\_DataCollDiscoStorageDevices.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-10-09"
reading_time_minutes: 7
breadcrumb: [Storage discovery via SMI-S and CIM, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Data collected by Discovery on storage devices

Discovery identifies and classifies information about storage devices.

**Note:** For information about the probes used to discover these devices, see [Storage discovery via SMI-S and CIM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/r_DataCollDiscoStorageviaSMISCIM.md).

|Field|Description|
|-----|-----------|
|Name|Name of the storage disk.|
|Computer|Reference to the host CI.|
|Interface|Interface type with which the storage disk is connected to the host.|
|Size|Size of the storage disk.|
|Free disk space \(GB\)|Free space in GB available on the disk.|
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

|Field|Description|
|-----|-----------|
|Name|Name of the disk.|
|Computer|Reference to host CI.|
|Interface|Interface type with which the storage device is connected to the host.|
|Size|Size of the disk.|
|Free disk space \(GB\)|Free space in GB available on the disk.|
|Manufacturer|Manufacturer of the disk.|
|Model ID|Model of the disk.|

|Field|Description|
|-----|-----------|
|Export ID|Unique identifier used to group and manage results of exports.|
|LUN|Logical Unit Number \(LUN\) or unique identifier that is specifically designated to be exported via Fibre Channel \(FC\) protocol.|
|Storage|Reference to CMDB CI.|
|Exported by|Reference to CMDB CI.|
|Hosted by|Reference to CMDB CI.|
|Initiator WWPN|Unique Worldwide Port Name \(WWPN\) for a Fibre Channel \(FC\) export from where it is installed.|

|Field|Description|
|-----|-----------|
|WWNN|Unique Worldwide Node Name \(WWNN\) identifier for a Fibre Channel \(FC\) port.|
|WWPN|Unique Worldwide Port Name \(WWPN\) identifier for a Fibre Channel \(FC\) port.|
|Speed|Speed of the FC port.|
|Controller|Reference to CMDB CI.|
|Computer|Reference to storage server CI.|

|Field|Description|
|-----|-----------|
|Export ID|The target IQN that allows iSCSI initiators \(clients\) to connect.|
|IQN|iSCSI Qualified Name \(IQN\) or unique identifier for the iSCSI target.|
|LUN|Logical Unit Number \(LUN\) or unique identifier that is specifically designated to be exported via iSCSI.|
|Storage|Reference to CMDB CI.|
|Exported by|Reference to CMDB CI.|
|Hosted by|Reference to CMDB CI.|
|Initiator IQN|IQN of the initiator \(iSCSI client\).|

|Field|Description|
|-----|-----------|
|Name|Name of the storage controller.|
|Device ID|Universally Unique Identifier \(UUID\) of the storage controller.|

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|Storage|Reference to CMDB CI.|
|Exported by|The device or service that exports storage.|
|Hosted by|The CI that hosts the pool, computer, cluster, etc.|

|Field|Description|
|-----|-----------|
|Name|Name of the storage switch.|
|WWNN|Worldwide node name \(WWNN\) of the storage switch.|
|Manufacturer|Manufacturer of the storage switch.|
|Model ID|Model ID of the storage switch.|
|Serial number|Serial number of the storage switch.|
|SAN|Reference to cmdb\_ci\_san CI.|

## Data collected on SAN components

Discovery collects the following data for storage area network \(SAN\) components.

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|Storage|Reference to CMDB CI.|
|Exported by|The device or service that exports storage.|
|Hosted by|The CI that hosts the pool, computer, cluster, etc.|

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|SAN ID|Unique ID of the SAN.|

|Field|Description|
|-----|-----------|
|Endpoint \#1|The endpoint with the lexicographically smaller WWN.|
|Endpoint \#2|The endpoint with the lexicographically larger WWN.|
|SAN|Reference to cmdb\_ci\_san CI.|

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|Endpoint ID|Unique ID of the SAN endpoint.|
|SAN|Reference to cmdb\_ci\_san CI.|

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|Fabric ID|Unique ID of the SAN fabric.|
|SAN|Reference to cmdb\_ci\_san CI.|

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|Zone ID|Unique ID of the SAN zone.|
|Zone set|Reference to cmdb\_ci\_san\_zone\_set CI.|

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|Zone|Reference to cmdb\_ci\_san\_zone CI.|

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|SAN Zone member|Reference to cmdb\_ci\_san\_zone\_member CI.|
|SAN Zone alias|Reference to cmdb\_ci\_san\_zone\_alias CI.|

|Field|Description|
|-----|-----------|
|Endpoint|The protocol endpoint \(reference to cmdb\_ci\_san\_endpoint CI\).|
|Zone|The SAN zone that this member belongs to \(reference to cmdb\_ci\_san\_zone CI\).|

|Field|Description|
|-----|-----------|
|Name|Unique name, often DNS hostname or computer name.|
|Zone set ID|Name of the zone set as reported by the SMI-S provider. Unique within its fabric.|
|Fabric|The SAN fabric \(reference to cmdb\_ci\_san\_fabric CI\).|

## Storage relationships

Discovery creates relationships for storage CIs running on Storage Area Networks \(SAN\) and Network Attached Storage \(NAS\).

## SAN relationships

Discovery creates the following relationships for storage CIs running on Storage Area Networks.

|Parent Component|Relationship|Child Component|
|----------------|------------|---------------|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Exports to::Imports from|Fibre Channel Disk \[cmdb\_ci\_fc\_disk\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Exports to::Imports from|iSCSI \[cmdb\_ci\_iscsi\_disk\]|

## NAS relationships

Discovery maps NAS file shares by resolving the hostname of a remotely mounted disk on the client computer to an IP address. It then matches the IP address to the storage server that provides the exported file system.

Discovery extracts the hostname or IP address from the NAS path to identify the storage server. If the NAS path contains a hostname, Discovery resolves it to an IP address and stores the value in the **nas\_ip\_address** field of the NAS File System \[cmdb\_ci\_nas\_file\_system\] table.

Discovery creates the following relationships for storage CIs running on Network Attached Storage \(NAS\). These relationships are the same for Linux and Windows hosts.

|Parent Component|Relationship|Child Component|
|----------------|------------|---------------|
|NAS File System \[cmdb\_ci\_nas\_file\_system\]|Allocated from::Allocated to|Storage File Share \[cmdb\_ci\_storage\_fileshare\]|

**Parent Topic:**[Storage discovery via SMI-S and CIM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/r_DataCollDiscoStorageviaSMISCIM.md)

