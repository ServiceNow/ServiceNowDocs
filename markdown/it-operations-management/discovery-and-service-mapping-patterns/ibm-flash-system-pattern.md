---
title: IBM Flash System pattern-based discovery
description: Discovery and Service Mapping Patterns finds IBM Flash System storage servers in your environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-operations-management/discovery-and-service-mapping-patterns/ibm-flash-system-pattern.html
release: zurich
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-08-11"
reading_time_minutes: 5
keywords: [IBM Flash System, IBM Flash Storage, storage server discovery, IBM storage patterns]
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# IBM Flash System pattern-based discovery

Discovery and Service Mapping Patterns finds IBM Flash System storage servers in your environment. Discovering some of these resources might require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://www.servicenow.com/docs/r/store-release-notes/sn-store-release-notes.html).

## IBM Flash System data model

The following diagram illustrates the tables and relationships that the Discovery and Service Mapping Patterns application creates when discovering IBM resources.

\[Omitted image "ibm-flash-system-diagram.png"\] Alt text: IBM Flash System data model

## Prerequisites

-   **Verify that the applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
    -   CMDB CI Class Models
-   **Verify REST API access**

    Verify that the MID Server is active and can reach the following REST API endpoints on the IBM Flash System array:

    -   `POST /rest/v1/auth`
    -   `POST /rest/v1/lssystem`
    -   `POST /rest/v1/lsmdiskgrp`
    -   `POST /rest/v1/lsvdisk`
    -   `POST /rest/v1/lsportfc`
    -   `POST /rest/v1/lsenclosurecanister`
    -   `POST /rest/v1/lsdrive`
    -   `POST /rest/v1/lsfabric`
-   **Create an alias for a basic authentication credential**

    For more information, see [Create an alias for a basic authentication credential for IBM Flash System discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-ibm-flash.md).

-   **Schedule a serverless discovery schedule**

    For more information, see [Create a serverless discovery schedule for IBM Flash System discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-ibm-flash.md).


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the IBM Flash System pattern.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the storage server.|
|Model ID \[model\_id\]|Hardware model of the storage server.|
|Manufacturer \[manufacturer\]|Name of the manufacturer. The value is set to **IBM**.|
|IP Address \[ip\_address\]|Console IP address of the storage server.|
|Serial number \[serial\_number\]|Serial number of the storage server.|
|OS Version \[os\_version\]|Software version of the storage server.|
|Firmware version \[firmware\_version\]|Software version of the storage server.|
|Physical Capacity \(GB\) \[physical\_capacity\]|Total physical storage capacity, in gigabytes \(GB\).|
|Used Physical Capacity \(GB\) \[used\_physical\_capacity\]|Amount of physical storage capacity in use, in GB.|
|Free Physical Capacity \(GB\) \[free\_physical\_capacity\]|Amount of physical storage capacity available, in GB.|
|Virtual Capacity \(GB\) \[virtual\_capacity\]|Total virtual storage capacity, in GB.|
|Free Virtual Capacity \(GB\) \[free\_virtual\_capacity\]|Amount of virtual storage capacity available, in GB.|
|Used Virtual Capacity \(GB\) \[used\_virtual\_capacity\]|Amount of virtual storage capacity in use, in GB.|
|Operational status \[operational\_status\]|Operational status of the storage server. Default value is Operational.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the storage pool.|
|Pool ID \[pool\_id\]|Unique identifier of the storage pool.|
|Size \[size\]|Total capacity of the storage pool.|
|Size bytes \[size\_bytes\]|Total capacity of the storage pool, in bytes.|
|Physical Capacity \(GB\) \[physical\_capacity\]|Total physical capacity of the storage pool, in GB.|
|Free space \[free\_space\]|Amount of free space available in the storage pool.|
|Free space bytes \[free\_space\_bytes\]|Amount of free space available in the storage pool, in bytes.|
|Operational status \[operational\_status\]|Operational status of the storage pool.|
|Hosted by \[hosted\_by\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

<table id="table_storage_volume"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the storage volume.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Serial number of the storage volume.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique identifier of the storage volume.

</td></tr><tr><td>

State \[state\]

</td><td>

Current state of the storage volume. For example: Available or Offline.

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

Total capacity of the storage volume, in bytes.

</td></tr><tr><td>

Operational status \[operational\_status\]

</td><td>

Operational status of the storage volume.

</td></tr><tr><td>

Computer \[computer\]

</td><td>

References the Storage Server \[cmdb\_ci\_storage\_server\] table.

</td></tr><tr><td>

Provided by \[provided\_by\]

</td><td>

References the Storage Pool \[cmdb\_ci\_storage\_pool\] table.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Fibre Channel port, derived from the port ID.|
|WWPN \[wwpn\]|World Wide Port Name of the Fibre Channel port.|
|Speed \[speed\]|Port speed of the Fibre Channel port.|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|
|Controller \[controller\]|References the Storage Controller \[cmdb\_ci\_storage\_controller\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the storage controller node.|
|Device ID \[device\_id\]|Canister ID of the storage controller.|
|Correlation ID \[correlation\_id\]|Node ID used to correlate the storage controller with associated Fibre Channel ports.|
|Operational status \[operational\_status\]|Operational status of the storage controller.|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the disk.|
|Device ID \[device\_id\]|Identifier of the disk drive.|
|Size bytes \[size\_bytes\]|Capacity of the disk, in bytes.|
|Correlation ID \[correlation\_id\]|Identifier used to correlate the disk with its managed disk group.|
|Device bus ID \[device\_bus\_id\]|Member ID of the disk within its enclosure.|
|Device interface \[device\_interface\]|Slot ID of the disk within its enclosure.|
|Device target ID \[device\_target\_id\]|Drive class ID of the disk.|
|Operational status \[operational\_status\]|Operational status of the disk.|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the Fibre Channel export.|
|Initiator WWPN \[initiator\_wwpn\]|WWPN of the remote initiator.|
|Export ID \[export\_id\]|Local WWPN that identifies this Fibre Channel export.|
|Operational status \[operational\_status\]|Operational status of the Fibre Channel export.|
|Hosted by \[hosted\_by\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

## CI relationships and references

The IBM Flash System pattern creates the following relationships and references to support IBM Flash System storage server discovery. References link to records in other tables and don't appear in the CI Relationship \[cmdb\_rel\_ci\] table.

|CI|Relationship|CI|
|---|------------|---|
|Storage Server \[cmdb\_ci\_storage\_server\]|Contains::Contained by|Storage Pool \[cmdb\_ci\_storage\_pool\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Owns::Owned by|Fibre Channel Port \[cmdb\_ci\_fc\_port\]|
|Storage Controller \[cmdb\_ci\_storage\_controller\]|Controller for::Controlled by|Storage Server \[cmdb\_ci\_storage\_server\]|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|Hosted on::Hosts|Storage Server \[cmdb\_ci\_storage\_server\]|

|CI|Field|Referenced CI|
|---|-----|-------------|
|Storage Pool \[cmdb\_ci\_storage\_pool\]|Hosted by \[hosted\_by\]|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Computer \[computer\]|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|Provided by \[provided\_by\]|Storage Pool \[cmdb\_ci\_storage\_pool\]|
|Fibre Channel Port \[cmdb\_ci\_fc\_port\]|Computer \[computer\]|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Controller \[cmdb\_ci\_storage\_controller\]|Computer \[computer\]|Storage Server \[cmdb\_ci\_storage\_server\]|
|Fibre Channel Port \[cmdb\_ci\_fc\_port\]|Controller \[controller\]|Storage Controller \[cmdb\_ci\_storage\_controller\]|
|Disk \[cmdb\_ci\_disk\]|Computer \[computer\]|Storage Server \[cmdb\_ci\_storage\_server\]|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|Hosted by \[hosted\_by\]|Storage Server \[cmdb\_ci\_storage\_server\]|

-   **[Create an alias for a basic authentication credential for IBM Flash System discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-alias-basic-auth-cred-ibm-flash.md)**  
Create an alias for a basic authentication credential to run IBM Flash System discovery.
-   **[Create a serverless discovery schedule for IBM Flash System discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/create-serverless-schedule-ibm-flash.md)**  
Create a serverless discovery schedule to run IBM Flash System storage discovery.

**Parent Topic:**[Available on-premise discovery patterns](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-operations-management/discovery-and-service-mapping-patterns/available-patterns.md)

