---
title: Dell EMC XtremIO storage array discovery
description: ServiceNow Discovery uses the Dell EMC XtremIO storage array pattern to find Dell EMC XtremIO storage array components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Available on-premise discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Dell EMC XtremIO storage array discovery

ServiceNow Discovery uses the Dell EMC XtremIO storage array pattern to find Dell EMC XtremIO storage array components. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) to view all the available apps, and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Discovery and Service Mapping Patterns store app**

    Verify the Discovery and Service Mapping Patterns store app, version 1.0.96, is installed.

    Verify the CMDB CI Class Models, version 1.42.0, is installed.

    **Note:** The Dell EMC XtremIO storage array pattern 1.0.96 store version was tested only for XtremIO cluster type X2.

-   **Credentials**

    Grant Basic Auth permissions by configuring Basic Auth credentials for RESTful API. Save the admin credentials as Basic Auth credentials to ensure a proper access.

-   **Run Discovery**

    Run Quick Discovery by Target IP. Provide the IP of the XMS \(that manage the storage\).

-   **Permissions for REST API queries**

    During the discovery, the pattern uses the following API queries. The user that is added to the credentials in the instance must have permissions to run these queries.

    -   Get details of XMS by index\_id https://&lt;IP&gt;/api/json/v2/types/xms/&lt;index\_id&gt;
    -   Get details of Storage Server \(Cluster\) by index\_id https://&lt;IP&gt;/api/json/v2/types/clusters/&lt;index\_id&gt;
    -   Get details of Storage Node Element \(Bricks\) by index\_id https://&lt;IP&gt;/api/json/v2/types/bricks/&lt;index\_id&gt;
    -   Get details of Storage Disks \(SSDs\) by index\_id https://&lt;IP&gt;/api/json/v2/types/ssds/&lt;index\_id&gt;
    -   Get details of Storage Enclosure \(DAEs\) by index\_id https://&lt;IP&gt;/api/json/v2/types/daes/&lt;index\_id&gt;
    -   Get details of Storage Switches \(Infiniband Switches\) by index\_id https://&lt;IP&gt;/api/json/v2/types/infiniband-switches/&lt;index\_id&gt;
    -   Get details of Battery Backup Units \(BBUs\) by index\_id https://&lt;IP&gt;/api/json/v2/types/bbus/&lt;index\_id&gt;
    -   Get details of Storage Controllers by index\_id https://&lt;IP&gt;/api/json/v2/types/storage-controllers/&lt;index\_id&gt;
    -   Get details of Storage Ports \(targets\) by index\_id https://&lt;IP&gt;/api/json/v2/types/targets/&lt;index\_id&gt;
    -   Get details of Disks \(local disks\) by index\_id https://&lt;IP&gt;/api/json/v2/types/local-disks/&lt;index\_id&gt;
    -   Get details of Initiator Groups by index\_id https://&lt;IP&gt;/api/json/v2/types/initiator-groups/&lt;index\_id&gt;
    -   Get details of Fibre Channel Ports \(initiators\) by index\_id https://&lt;IP&gt;/api/json/v2/types/initiators/&lt;index\_id&gt;
    -   Get details of Fibre Channel Disks \(Volumes\) by index\_id https://&lt;IP&gt;/api/json/v2/types/volumes/&lt;index\_id&gt;

-   **The new Configuration Item \(CI\) that is classified:**

    Initiator Group.


## Data collected by Discovery during horizontal discovery

The discovered Dell EMC XtremIO storage array Configuration Management Database \(CMDB\) includes the following tables and fields.

<table id="table_w2j_l53_2nb"><thead><tr><th>

Table and field

</th><th>

Description

</th></tr></thead><tbody><tr><td class="sub-head" colspan="2">

Main CI \[cmdb\_ci\_linux\_server\]​

</td></tr><tr><td>

name

</td><td>

The name of the Linux/XMS server

</td></tr><tr><td>

ip\_address

</td><td>

The IP address of the Linux/XMS server

</td></tr><tr><td>

host\_name

</td><td>

The host name of the Linux/XMS server

</td></tr><tr><td>

object\_id

</td><td>

The identifier attribute of the Linux/XMS server

</td></tr><tr><td>

ram

</td><td>

The total available RAM of the Linux/XMS server

</td></tr><tr><td class="sub-head" colspan="2">

Storage Server \[cmdb\_ci\_storage\_server\]

</td></tr><tr><td>

name

</td><td>

The name of the Storage Server \(Cluster\)

</td></tr><tr><td>

object\_id

</td><td>

The IP address of the Storage Server \(Cluster\)

</td></tr><tr><td>

serial\_number

</td><td>

The serial number of the Storage Server \(Cluster\)

</td></tr><tr><td class="sub-head" colspan="2">

Storage Node Element \[cmdb\_ci\_storage\_node\_element\]

</td></tr><tr><td>

name

</td><td>

The name of the Storage Node Element \(X-Brick\)

</td></tr><tr><td>

object\_id

</td><td>

The identifier attribute of the Storage Node Element \(X-Brick\)

</td></tr><tr><td>

serial\_number

</td><td>

The Storage Node Element \(X-Brick\) serial number

</td></tr><tr><td class="sub-head" colspan="2">

Storage Controller \[cmdb\_ci\_storage\_controller\]

</td></tr><tr><td>

name

</td><td>

The name of the Storage Controller

</td></tr><tr><td>

device\_id

</td><td>

The Storage Controller ID

</td></tr><tr><td>

serial\_number

</td><td>

The serial number of the Storage Controller

</td></tr><tr><td>

model\_number

</td><td>

The model number of the Storage Controller

</td></tr><tr><td>

model\_id

</td><td>

The model ID of the of the Storage Controller

</td></tr><tr><td class="sub-head" colspan="2">

Storage Port \[cmdb\_ci\_storage\_port\]

</td></tr><tr><td>

wwpn

</td><td>

The WWPN

</td></tr><tr><td>

name

</td><td>

The name of the Storage Port \(target\)

</td></tr><tr><td>

correlation\_id

</td><td>

The Storage Port \(target\) correlation ID

</td></tr><tr><td>

speed

</td><td>

The speed of the Storage Port \(target\)

</td></tr><tr><td>

port\_type

</td><td>

The Storage Port \(target\) type

</td></tr><tr><td class="sub-head" colspan="2">

Storage Switch \[cmdb\_ci\_storage\_switch\]

</td></tr><tr><td>

object\_id

</td><td>

The identifier attribute of the Storage Switch \(Infiniband Switch\)

</td></tr><tr><td>

name

</td><td>

The name of the Storage Switch \(Infiniband Switch\)

</td></tr><tr><td>

serial\_number

</td><td>

The serial number of the Storage Switch \(Infiniband Switch\)

</td></tr><tr><td>

model\_id

</td><td>

The model ID of the Storage Switch \(Infiniband Switch\)

</td></tr><tr><td class="sub-head" colspan="2">

Storage Enclosure \[cmdb\_ci\_storage\_enclosure\]

</td></tr><tr><td>

name

</td><td>

The name of the Storage Enclosure \(Disk Array Enclosure\)

</td></tr><tr><td>

object\_id

</td><td>

The identifier attribute of the Storage Enclosure \(Disk Array Enclosure\)

</td></tr><tr><td>

serial\_number

</td><td>

The serial number of the Storage Enclosure \(Disk Array Enclosure\)

</td></tr><tr><td>

model\_number

</td><td>

The model number of the Storage Enclosure \(Disk Array Enclosure\)

</td></tr><tr><td class="sub-head" colspan="2">

UPS \[cmdb\_ci\_ups\]

</td></tr><tr><td>

name

</td><td>

The name of the Battery Backup Unit \(BBU\)

</td></tr><tr><td>

serial\_number

</td><td>

The serial number of the Battery Backup Unit \(BBU\)

</td></tr><tr><td>

model\_number

</td><td>

The model number of the Battery Backup Unit \(BBU\)

</td></tr><tr><td>

model\_id

</td><td>

The model ID of the Battery Backup Unit \(BBU\)

</td></tr><tr><td>

estimated\_charge\_remaining

</td><td>

The estimated charge remained for the Battery Backup Unit \(BBU\)

</td></tr><tr><td>

battery\_voltage

</td><td>

The battery voltage of the Battery Backup Unit \(BBU\)

</td></tr><tr><td class="sub-head" colspan="2">

Initiator Group \[cmdb\_ci\_initiator\_group\]​

</td></tr><tr><td>

object\_id

</td><td>

The identifier attribute of the Initiator Group

</td></tr><tr><td>

name

</td><td>

The name of the Initiator Group

</td></tr><tr><td>

number\_of\_initiators

</td><td>

The number of initiators in a the group

</td></tr><tr><td>

number\_of\_volumes

</td><td>

The number of volumes

</td></tr><tr><td class="sub-head" colspan="2">

Fibre Channel Disk \[cmdb\_ci\_fc\_disk\]​

</td></tr><tr><td>

name

</td><td>

The name of the Fibre Channel Disk \(Volume\)

</td></tr><tr><td>

device\_id

</td><td>

The ID of the Fibre Channel Disk \(Volume\)

</td></tr><tr><td>

size

</td><td>

The available storage size of the Fibre Channel Disk \(Volume\)

</td></tr><tr class="sub-head"><td class="sub-head" colspan="2">

Fibre Channel Port \[cmdb\_ci\_fc\_port\]​

</td></tr><tr><td>

wwpn

</td><td>

The WWPN

</td></tr><tr><td>

wwnn

</td><td>

The WWNN.

</td></tr><tr><td>

name

</td><td>

The name of the Fibre Channel Port \(initiator\)

</td></tr><tr><td>

port\_type

</td><td>

The port type of the Fibre Channel Port \(initiator\)

</td></tr></tbody>
</table>## CI relationships

<table id="table_jtg_dtm_pu832"><thead><tr><th>

CI

</th><th>

Relationship Type

</th><th>

CI

</th></tr></thead><tbody><tr><td>

cmdb\_ci\_linux\_server

</td><td>

Manage::Managed by

</td><td>

cmdb\_ci\_storage\_server

</td></tr><tr><td>

cmdb\_ci\_storage\_switch

</td><td>

Connects to::Connected by

</td><td>

cmdb\_ci\_storage\_server

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Allocated to::Allocated from

</td><td>

cmdb\_ci\_storage\_node\_element

</td></tr><tr><td>

cmdb\_ci\_storage\_enclosure

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_storage\_node\_element

</td></tr><tr><td>

cmdb\_ci\_disk

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_storage\_node\_element

</td></tr><tr><td>

cmdb\_ci\_storage\_controller

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_storage\_node\_element

</td></tr><tr><td>

cmdb\_ci\_storage\_controller

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_storage\_port

</td></tr><tr><td>

cmdb\_ci\_ups

</td><td>

Connects to::Connected by

</td><td>

cmdb\_ci\_storage\_node\_element

</td></tr><tr><td>

cmdb\_ci\_storage\_server

</td><td>

Contains::Contained By

</td><td>

cmdb\_ci\_Initiator \_group

</td></tr><tr><td>

cmdb\_ci\_Initiator \_group

</td><td>

Member::Member of

</td><td>

cmdb\_ci\_fc\_port

</td></tr><tr><td>

cmdb\_ci\_Initiator \_group

</td><td>

Connects to::Connected by

</td><td>

cmdb\_ci\_fc\_disk

</td></tr></tbody>
</table>**Parent Topic:**[Available on-premise discovery patterns](../concept/available-patterns.md)

**Related topics**  


[Detailed information on products discovered by ITOM Visibility](r_SupportedApplications.md)

