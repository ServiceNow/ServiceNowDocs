---
title: Pure Storage FlashArray discovery
description: The Discovery and Service Mapping Patterns application uses the Pure Storage Flash Array pattern to find Pure Storage FlashArray on your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2026-03-25"
reading_time_minutes: 6
keywords: [Patterns]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Pure Storage FlashArray discovery

The Discovery and Service Mapping Patterns application uses the Pure Storage Flash Array pattern to find Pure Storage FlashArray on your infrastructure. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

**Note:** Starting March 2024, the pattern execution is disabled by default. To create a CI for Pure Storage FlashArray, synchronize the pattern to the MID Server.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Verify the configuration of the credentials**

    Configure basic authentication credentials to classify FlashArray. For more information, see [basic authentication](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Verify the permissions to run REST API calls**

    The Pure Storage Flash Array pattern supports the API 2.17 version.

    -   `/api/1.17/auth/apitoken`
    -   `/api/2.17/auth/session`
    -   `/api/2.17/arrays`
    -   `/api/2.17/volumes`
    -   `/api/2.17/volume-groups`
    -   `/api/2.17/host-groups`
    -   `/api/2.17/hardware`
    -   `/api/2.17/dns`
    -   `/api/2.17/ports`

**Note:** The February 2024 Pure Storage pattern version supports only iSCSI protocol discovery.

## Running Discovery

To run discovery using Patterns, create a discovery schedule that targets the management IP address of the FlashArray storage. For more information, see [Running discoveries in your network](running-discoveries.md).

## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the Pure Storage pattern.

<table id="table_urh_ypg_tbc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The user-assigned identifier or label for the FlashArray storage.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Serial number that uniquely identifies each individual FlashArray storage.

</td></tr><tr><td>

Operating System \[os\]

</td><td>

Operating system running on the FlashArray storage.

</td></tr><tr><td>

OS Version \[os\_version\]

</td><td>

Software version that is installed on the FlashArray storage.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP Address of the FlashArray storage.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

Manufacturer name: Pure Storage.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Credential affinity assigned during discovery to the FlashArray storage. For more information about credential affinity, see [Credential affinity for Discovery and Orchestration](https://www.servicenow.com/docs/access?context=c_CredentialAffinity&version=australia&pubname=australia-platform-security&ft:locale=en-US).

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

Model ID of the FlashArray storage.

</td></tr><tr><td>

Encryption at rest \[encryption\_at\_rest\]

</td><td>

Encrypted data stored on a physical device or in a database. Possible values are: -   active
-   disable

</td></tr><tr><td>

Encryption algorithm \[encryption\_algorithm\]

</td><td>

Type of algorithm the storage server employs. Possible values are:-   AES-256: Advanced Encryption Standard \(AES\) 256 Encryption
-   multiple methods: Pure Storage doesn't currently support multiple methods
-   Unknown: If during a previous discovery an algorithm type was discovered but during the next discovery it isn't discovered, the value is unknown

</td></tr><tr><td>

Total Free Capacity \(GB\) \[total\_free\_capacity\]

</td><td>

Total amount of storage space that is currently available for use on the FlashArray storage system, which is measured in gigabytes \(GB\).

</td></tr><tr><td>

Physical Capacity \(GB\) \[physical\_capacity\]

</td><td>

Total amount of physical storage space available within the FlashArray system, measured in GB. This capacity includes both allocated and unallocated storage resources.

</td></tr><tr><td>

Free Physical Capacity \(GB\) \[free\_physical\_capacity\]

</td><td>

Available physical storage space within the FlashArray system, measured in GB.

</td></tr><tr><td>

Used Physical Capacity \(GB\) \[used\_physical\_capacity\]

</td><td>

Used physical storage space within the FlashArray system, measured in GB.

</td></tr><tr><td>

Virtual Capacity \(GB\) \[virtual\_capacity\]

</td><td>

Total virtual storage capacity provisioned within the FlashArray system, measured in GB.

</td></tr><tr><td>

Free Virtual Capacity \(GB\) \[free\_virtual\_capacity\]

</td><td>

Available virtual storage capacity within the FlashArray system, measured in GB.

</td></tr><tr><td>

Used Virtual Capacity \(GB\) \[used\_virtual\_capcity\]

</td><td>

Used virtual storage capacity within the FlashArray system, measured in GB.

</td></tr><tr><td>

Install Status \[install\_status\]

</td><td>

Install status of the resource. Default value is Installed.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the resource. Default value is Operational.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|Cluster node name.|
|Cluster \[cluster\]|Host group associated with this cluster node in the FlashArray environment.|
|Manufacturer \[manufacturer\]|Manufacturer name: Pure Storage.|
|Comments \[comments\]|All the logical unit numbers \(LUN\) connected to the cluster node.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Storage cluster name.|
|Correlation ID \[correlation\_id\]|Combines the cluster name and the storage's serial number to create a unique identifier \(UID\).|
|Manufacturer \[manufacturer\]|Manufacturer name: Pure Storage.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Volume name.|
|Serial number \[serial\_number\]|Serial number of the volume.|
|Volume ID \[volume\_id\]|Volume ID.|
|Installed \[install\_date\]|Date the volume was installed.|
|Size bytes \[size\_bytes\]|Volume size in bytes.|
|Pool ID \[pool\_id\]|ID of the pool containing the volumes.|
|Attributes \[attributes\]|Names of the hosts connected to the volumes.|
|Manufacturer \[manufacturer\]|Manufacturer name: Pure Storage.|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|
|Provided by \[provided\_by\]|References the Storage Pool \[cmdb\_ci\_storage\_pool\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the storage pool.|
|Object ID \[object\_id\]|ID of the storage pool.|
|Manufacturer \[manufacturer\]|Manufacturer name: Pure Storage.|
|Hosted by \[hosted\_by\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Combination of asset and asset tag.|
|Model ID \[model\_id\]|Model ID of the controller.|
|Assigned \[assigned\]|Availability status.|
|Device ID \[device\_id\]|A unique label for the controller.|
|Manufacturer \[manufacturer\]|Manufacturer name: Pure Storage.|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Spindle ID.|
|Size bytes \[size\_bytes\]|Disk size in bytes.|
|Drive type \[drive\_type\]|Type of drive installed on the disk.|
|Device ID \[device\_id\]|Combination of the storage system serial number with the disk name that uniquely identifies each disk within the FlashArray environment.|
|Manufacturer \[manufacturer\]|Disk manufacturer.|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the network adapter.|
|IP Address \[ip\_address\]|IP address of the network adapter.|
|MAC Address \[mac\_address\]|MAC address of the network adapter.|
|IP default gateway \[ip\_default\_gateway\]|IP address of the default gateway.|
|Alias \[alias\]|The user-assigned name for the network adapter.|
|Netmask \[netmask\]|Netmask of the network adapter.|
|Configuration Item \[cmdb\_ci\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Initiator ID in FlashArray systems, which serves as a UID for the initiator in the context of Fibre Channel exports.|
|Export ID \[export\_id\]|UID for a Fibre Channel export within FlashArray systems, facilitating the management and tracking of Fibre Channel connections.|
|Initiator WWPN \[initiator\_wwpn\]|UID combining the Director ID, port number, and Initiator ID.|
|Hosted by \[hosted\_by\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|
|Storage \[storage\]|References the Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Initiator ID in FlashArray systems, which serves as a UID for the initiator in the context of iSCSI exports.|
|Export ID \[export\_id\]|UID for an iSCSI export within FlashArray systems, facilitating the management and tracking of iSCSI connections.|
|Initiator IQN \[initiator\_iqn\]|iSCSI Qualified Name \(IQN\) assigned to an initiator in the iSCSI network.|
|Hosted by \[hosted\_by\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|
|Storage \[storage\]|References the Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\] table.|

## CI relationships

|CI|Relationship type|CI|
|---|-----------------|---|
|Disk \[cmdb\_ci\_disk\]|Contains::Contained by|Storage Server \[cmdb\_ci\_storage\_server\]|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|Hosted on::Hosts|Storage Server \[cmdb\_ci\_storage\_server\]|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|References|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|
|iSCSI Export \[cmdb\_ci\_iscsi\_export\]|Hosted on::Hosts|Storage Server \[cmdb\_ci\_storage\_server\]|
|iSCSI Export \[cmdb\_ci\_iscsi\_export\]|References|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Owns::Owned by|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|Cluster of::Cluster|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Controller \[cmdb\_ci\_storage\_controller\]|Controller for::Controlled by|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Allocated to::Allocated from|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Contains::Contained by|Storage Pool \[cmdb\_ci\_storage\_pool\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Runs on::Runs|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Contains::Contained by|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Contains::Contained by|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|References|Storage Pool \[cmdb\_ci\_storage\_pool\]|

**Parent Topic:**[Available on-premise discovery patterns](../../service-mapping/concept/available-patterns.md)

