---
title: NetApp SolidFire storage system discovery
description: ServiceNow Discovery uses the NetApp SolidFire storage system discovery pattern to find clusters and nodes on the SolidFire storage system. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-operations-management/discovery-and-service-mapping-patterns/solidfire-storage-pattern.html
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-05-31"
reading_time_minutes: 4
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# NetApp SolidFire storage system discovery

ServiceNow Discovery uses the NetApp SolidFire storage system discovery pattern to find clusters and nodes on the SolidFire storage system. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Verify that the following apps are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
-   **Create credential alias for basic authentication credential**

    Configure a credential alias for basic authentication credentials for a SolidFire Cluster Admin user. For more information, see [Create a basic authentication credential alias for NetApp SolidFire discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-solidfire.md).

-   **Verify that the MID Server has access**

    Verify the MID Server can access the target device.

-   **Create a serverless discovery schedule**

    Create a serverless discovery schedule to perform targeted discovery of SolidFire clusters and nodes. For more information, see [Create a serverless discovery schedule for NetApp SolidFire discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-solidfire.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the NetApp SolidFire Storage System pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the CI.|
|Serial number \[serial\_number\]|The serial number associated with the CI.|
|Firmware version \[firmware\_version\]|The firmware version of the CI.|
|IP Address \[ip\_address\]|The IP address of the CI.|
|Description \[short\_description\]|A short textual description of the CI.|
|Manufacturer \[manufacturer\]|The device manufacturer.|
|Model ID \[model\_id\]|The device model ID.|
|OS Version \[os\_version\]|The version of the OS running on the CI.|
|Operating System \[os\]|The OS running on the CI.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the CI.|
|IP Address \[ip\_address\]|The IP address of the storage cluster.|
|Description \[short\_description\]|A short textual description of the CI.|
|Manufacturer \[manufacturer\]|The device manufacturer.|
|Cluster Version \[cluster\_version\]|Element OS API version running on the cluster.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the CI.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|
|Cluster \[cluster\]|References the Storage Cluster \[cmdb\_ci\_storage\_cluster\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the CI.|
|Description \[short\_description\]|A short textual description of the CI.|
|Manufacturer \[manufacturer\]|The device manufacturer.|
|Serial number \[serial\_number\]|The serial number associated with the CI.|
|Model ID \[model\_id\]|The device model ID.|
|Chassis type \[chassis\_type\]|The type of chassis that contains the server.|
|RAM \(MB\) \[ram\]|The memory size of the CI.|
|CPU type \[cpu\_type\]|The CPU type.|
|CPU manufacturer \[cpu\_manufacturer\]|The CPU manufacturer.|
|Operational status \[operational\_status\]|Operational status of the resource. Default value is Operational.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the CI.|
|Device ID \[device\_id\]|The ID of the device.|
|Serial number \[serial\_number\]|The serial number associated with the CI.|
|Storage type \[storage\_type\]|The storage type.|
|Size bytes \[size\_bytes\]|The available storage size in bytes.|
|Manufacturer \[manufacturer\]|The device manufacturer.|
|Model ID \[model\_id\]|The device model ID.|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the CI.|
|IP Address \[ip\_address\]|The IP address of the CI.|
|MAC Address \[mac\_address\]|The MAC address of the network adapter.|
|Netmask \[netmask\]|The netmask of the server hosting the network adapter.|
|Configuration Item \[cmdb\_ci\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|IP Address \[ip\_address\]|The IP address of the CI.|
|Netmask \[netmask\]|The netmask of the server hosting the CI.|
|Nic \[nic\]|References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.|

The Dependency Views map shows all discovered SolidFire storage system clusters and nodes in your organization and the relationships between them.

\[Omitted image "storage-system-dependency.jpg"\] Alt text: SolidFire storage system dependency view

## CI relationships

The NetApp SolidFire Storage System pattern creates the following relationships and references to support storage system discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|Cluster of::Cluster|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|
|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|Hosted on::Hosts|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|Managed by::Manages|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Allocated to::Allocated from|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Runs on::Runs|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|Cluster \[cluster\]|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Disk \[cmdb\_ci\_disk\]|Computer \[computer\]|Storage Server \[cmdb\_ci\_storage\_server\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|Configuration Item \[cmdb\_ci\]|Storage Server \[cmdb\_ci\_storage\_server\]|
|IP Address \[cmdb\_ci\_ip\_address\]|Nic \[nic\]|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Serial Number \[cmdb\_serial\_number\]|Configuration Item \[cmdb\_ci\]|Storage Server \[cmdb\_ci\_storage\_server\]|
|Serial Number \[cmdb\_serial\_number\]|Configuration Item \[cmdb\_ci\]|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|

-   **[Create a basic authentication credential alias for NetApp SolidFire discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-solidfire.md)**  
Create an alias and add it to a basic authentication credential to discover NetApp SolidFire clusters.
-   **[Create a serverless discovery schedule for NetApp SolidFire discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-solidfire.md)**  
Set up a dedicated serverless discovery schedule for NetApp SolidFire cluster and node discovery.

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

