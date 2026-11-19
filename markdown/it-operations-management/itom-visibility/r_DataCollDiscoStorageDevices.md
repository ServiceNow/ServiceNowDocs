---
title: Data collected by Discovery on storage devices
description: Discovery identifies and classifies information about storage devices.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-operations-management/itom-visibility/r\_DataCollDiscoStorageDevices.html
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: reference
last_updated: "2026-11-12"
reading_time_minutes: 7
breadcrumb: [Storage discovery via SMI-S and CIM, Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# Data collected by Discovery on storage devices

Discovery identifies and classifies information about storage devices.

**Note:** For information about the probes used to discover these devices, see [Storage discovery via SMI-S and CIM](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-operations-management/itom-visibility/r_DataCollDiscoStorageviaSMISCIM.md).

|Field|Description|
|-----|-----------|
|Name|Name of the CI.|
|Path|Path to the file share.|

|Field|Description|
|-----|-----------|
|Name|Name of the storage pool.|
|Size|Size of the storage pool.|
|Free space|Free space available in the pool.|
|Hosted by|Reference to the storage server CI that hosts the pool.|

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
|Computer|Reference to the storage server CI that contains the disk.|
|Interface|Interface type of the disk, such as SAS, SCSI, or SATA. Populated only when the SMI-S provider reports it.|
|Size|Size of the disk.|
|Free disk space \(GB\)|Free space in GB available on the disk.|
|Manufacturer|Manufacturer of the disk. Populated only when the SMI-S provider reports it.|
|Model ID|Model of the disk. Populated only when the SMI-S provider reports it.|

|Field|Description|
|-----|-----------|
|Export ID|Identifier made up of the exported volume name and the device ID of the exporting storage controller.|
|LUN|Logical Unit Number \(LUN\) or unique identifier that is specifically designated to be exported via Fibre Channel \(FC\) protocol.|
|Storage|Reference to the exported storage volume \[cmdb\_ci\_storage\_volume\] CI.|
|Exported by|Reference to the storage controller \[cmdb\_ci\_storage\_controller\] CI that exports the volume.|
|Hosted by|Reference to the storage server CI.|
|Initiator WWPN|WWPN of the host initiator port that the LUN is exported to.|

|Field|Description|
|-----|-----------|
|Name|Name of the FC port, as reported by the SMI-S provider. For storage switch ports without a reported name, Discovery uses Port \# followed by the port number.|
|WWNN|WWNN of the node that the FC port belongs to, as reported by the SMI-S provider. Not populated for every port.|
|WWPN|Unique Worldwide Port Name \(WWPN\) identifier for a Fibre Channel \(FC\) port.|
|Speed|Speed of the FC port.|
|Controller|Reference to the storage controller \[cmdb\_ci\_storage\_controller\] CI.|
|Computer|Reference to the storage server or storage switch CI.|

|Field|Description|
|-----|-----------|
|Export ID|Identifier made up of the exported volume name and the device ID of the exporting storage controller.|
|IQN|iSCSI Qualified Name \(IQN\) or unique identifier for the iSCSI target.|
|LUN|Logical Unit Number \(LUN\) or unique identifier that is specifically designated to be exported via iSCSI.|
|Storage|Reference to the exported storage volume \[cmdb\_ci\_storage\_volume\] CI.|
|Exported by|Reference to the storage controller \[cmdb\_ci\_storage\_controller\] CI that exports the volume.|
|Hosted by|Reference to the storage server CI.|
|Initiator IQN|IQN of the initiator \(iSCSI client\).|

|Field|Description|
|-----|-----------|
|Name|Name of the storage controller.|
|Device ID|Device ID that the SMI-S provider reports for the storage controller.|
|Computer|Reference to the storage server CI.|

|Field|Description|
|-----|-----------|
|Name|Name of the export, made up of the exported volume name and either the target IQN \(iSCSI exports\) or the LUN \(Fibre Channel exports\).|
|Storage|Reference to the exported storage volume \[cmdb\_ci\_storage\_volume\] CI.|
|Exported by|Reference to the storage controller \[cmdb\_ci\_storage\_controller\] CI that exports the volume.|
|Hosted by|Reference to the storage server CI.|

|Field|Description|
|-----|-----------|
|Name|Name of the storage switch.|
|WWNN|Worldwide node name \(WWNN\) of the storage switch. Populated by the SMI - Fibre Channel Switch probe.|
|Manufacturer|Manufacturer of the storage switch.|
|Model ID|Model ID of the storage switch.|
|Serial number|Serial number of the storage switch.|
|SAN|Reference to cmdb\_ci\_san CI.|

## Data collected on SAN components

Discovery collects the following data for storage area network \(SAN\) components.

|Field|Description|
|-----|-----------|
|Name|Name of the export, made up of the exported volume name and either the target IQN \(iSCSI exports\) or the LUN \(Fibre Channel exports\).|
|Storage|Reference to the exported storage volume \[cmdb\_ci\_storage\_volume\] CI.|
|Exported by|Reference to the storage controller \[cmdb\_ci\_storage\_controller\] CI that exports the volume.|
|Hosted by|Reference to the storage server CI.|

|Field|Description|
|-----|-----------|
|Name|Name of the SAN, as reported by the SMI-S provider.|
|SAN ID|WWN of the SAN, as reported by the SMI-S provider.|

|Field|Description|
|-----|-----------|
|Endpoint \#1|The endpoint with the lexicographically smaller WWN.|
|Endpoint \#2|The endpoint with the lexicographically larger WWN.|
|SAN|Reference to cmdb\_ci\_san CI.|

|Field|Description|
|-----|-----------|
|Name|WWN of the SAN endpoint.|
|Endpoint ID|WWN of the SAN endpoint. Same value as Name.|
|SAN|Reference to cmdb\_ci\_san CI.|
|FC port|Reference to the Fibre Channel port \[cmdb\_ci\_fc\_port\] CI that has the same WWPN as the endpoint.|

|Field|Description|
|-----|-----------|
|Name|Name of the SAN fabric.|
|Fabric ID|WWN of the SAN fabric.|
|SAN|Reference to cmdb\_ci\_san CI.|

|Field|Description|
|-----|-----------|
|Name|Name of the SAN zone.|
|Zone ID|Identifier of the SAN zone. Same value as Name.|
|Zone set|Reference to cmdb\_ci\_san\_zone\_set CI.|

|Field|Description|
|-----|-----------|
|Name|Name of the zone alias.|
|Zone|Reference to cmdb\_ci\_san\_zone CI.|

|Field|Description|
|-----|-----------|
|Name|WWN of the zone alias member.|
|SAN Zone member|Reference to cmdb\_ci\_san\_zone\_member CI.|
|SAN Zone alias|Reference to cmdb\_ci\_san\_zone\_alias CI.|

|Field|Description|
|-----|-----------|
|Endpoint|The protocol endpoint \(reference to cmdb\_ci\_san\_endpoint CI\).|
|Zone|The SAN zone that this member belongs to \(reference to cmdb\_ci\_san\_zone CI\).|

Discovery collects only active zone sets.

|Field|Description|
|-----|-----------|
|Name|Name of the zone set.|
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

