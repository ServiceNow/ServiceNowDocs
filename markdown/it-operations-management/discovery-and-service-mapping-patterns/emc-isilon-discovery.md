---
title: Dell EMC Isilon discovery
description: The ServiceNow Discovery application uses the Dell EMC Isilon pattern to find components of Dell EMC Isilon. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: xanadu
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Dell EMC Isilon discovery

The ServiceNow Discovery application uses the Dell EMC Isilon pattern to find components of Dell EMC Isilon. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

For a complete list of devices and applications that ITOM Visibility can discover, see [Detailed information on products discovered by ITOM Visibility](../reference/r_SupportedApplications.md).

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

-   **Create SNMP Community credentials**

    Create an SNMP Community credential for the Isilon cluster. The discovery process begins with using SNMP-based queries to classify an application as an Isilon cluster. For more information, see SNMP community credentials in [SNMP credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).

-   **Verify Dell EMC Isilon user permissions and roles**

    Once the application is classified as an Isilon cluster, the discovery process uses REST queries to find information about it. Provide the Dell EMC Isilon user with the following REST API endpoints:

    -   "https://" + $host + ":8080/platform/3/cluster/config”
    -   "https://" + $host + ":8080/platform/3/network/interfaces”
    -   "https://" + $host\_ip + ":8080/platform/3/cluster/nodes/”
    -   “https://” + $host + ":8080/platform/3/zones”
    -   "https://" + $host + ":8080/platform/3/network/pools”
    -   "https://" + $host + ":8080/platform/3/storagepool/nodepools”
    -   "https://" + $host + ":8080/platform/3/storagepool/storagepools”
    -   "https://" + $host + ":8080/platform/3/protocols/nfs/exports”
    -   "https://" + $host + ":8080/platform/3/protocols/smb/shares"
    The Dell EMC Isilon user must also have the following roles:

    -   ISI\_PRIV\_LOGIN\_PAPI
    -   ISI\_PRIV\_AUTH
    -   ISI\_PRIV\_DEVICES
    -   ISI\_PRIV\_NETWORK
    -   ISI\_PRIV\_NFS
    -   ISI\_PRIV\_SMARTPOOLS
    -   ISI\_PRIV\_SMB
-   **Create basic authentication credentials**

    In the Credentials module of the ServiceNow platform, create a basic authentication credential for the same Dell EMC Isilon user. For more information, see [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=xanadu&pubname=xanadu-platform-security&ft:locale=en-US).


## Data collected by Discovery for Dell EMC Isilon

Discovery populates the data in the CMDB when running the EMC Isilon pattern.

|Table and Field|Description|
|---------------|-----------|
|Storage Server \[cmdb\_ci\_storage\_server\]|The server hosting the Isilon cluster.|
|short\_description|The description configured during the Isilon server installation.|
|firmware\_version|The version of the firmware installed on the Isilon server|
|ip\_address|The IP address of the Isilon server.|
|manufacturer|The company that produced the device: EMC.|
|model\_id|Preconfigured identification string of the device.|
|host\_name|The host name of the Isilon server.|
|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|The name of the IP address of the cluster that Isilon servers form.|
|name|
|ip\_address|
|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|The name and other attributes of the node that is part of the Isilon storage cluster.|
|name|
|cluster|
|operational\_status|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|The name and other attributes of the physical node that are hosted by the storage cluster.|
|name|
|manufacturer|
|cpu\_type|
|model\_id|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|The attribute showing if the network adapter installed on the cluster node is active.|
|active|
|name|
|ip\_address|
|netmask|
|IP Address \[cmdb\_ci\_ip\_address\]|The attributes of the IP address of the cluster node.|
|name|
|netmask|
|Disk \[cmdb\_ci\_disk\]|The storage disk installed on the Isilon Server.|
|device\_id|
|name|
|model\_id|
|interface|
|disk\_interface|
|Storage File Share \[cmdb\_ci\_storage\_fileshare\]|The fileshare server attributes.|
|path|
|name|
|fileshare\_id|
|correlation\_id|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|The attributes of the storage volume belonging to the storage cluster.|
|media\_type|
|object\_id|
|size\_bytes|
|free\_space\_bytes|
|Storage Pool \[cmdb\_ci\_storage\_pool\]|
|pool\_id|The attributes of the storage pool to which the storage cluster belongs.|
|free\_space\_bytes|
|size\_bytes|
|name|
|object\_id|
|Serial Number \[cmdb\_serial\_number\]|The attributes of the serial number of the storage node.|
|serial\_number|
|serial\_number\_type|
|valid|

The graphic illustrates CIs that are part of Isilon discovery.

**Note:** This Dependency Views map was simplified for clarity. Your Isilon deployments can contain many more CIs.

![Isilon components](../image/Isilon-components.png "Dependency Views showing Isilon components")

## CI Relationships

|CI|Relationship/Reference|CI|
|---|----------------------|---|
|cmdb\_ci\_storage\_server|Runs on::Runs|cmdb\_ci\_storage\_cluster|
|cmdb\_ci\_storage\_server|Allocated to::Allocated from|cmdb\_ci\_storage\_node\_element|
|cmdb\_ci\_storage\_cluster\_node|Cluster of::Cluster|cmdb\_ci\_storage\_cluster \(reference **cluster**\)|
|cmdb\_ci\_storage\_cluster\_node|Hosted on::Hosts|cmdb\_ci\_storage\_node\_element \(reference **server**\)|
|cmdb\_ci\_storage\_node\_element|Managed by::Manages|cmdb\_ci\_storage\_cluster|
|cmdb\_ci\_network\_adapter|Owns::Owned by|cmdb\_ci\_storage\_node\_element \(reference **cmdb\_ci**\)|
|cmdb\_ci\_network\_adapter|Used by::Uses|cmdb\_ci\_storage\_server \(reference **cmdb\_ci**\)|
|cmdb\_ci\_ip\_address|Owns::Owned by|cmdb\_ci\_storage\_node\_element|
|cmdb\_ci\_ip\_address|Used by::Uses|cmdb\_ci\_storage\_server|
|cmdb\_ci\_disk|Contains::Contained by|cmdb\_ci\_storage\_node\_element \(reference **computer**\)|
|cmdb\_ci\_storage\_fileshare|Provided by::Provides|cmdb\_ci\_storage\_server|
|cmdb\_ci\_storage\_fileshare|Allocated from::Allocated to|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_storage\_volume|Uses::Used by|cmdb\_ci\_storage\_server|
|cmdb\_ci\_storage\_volume|Owns::Owned by|cmdb\_ci\_storage\_cluster|
|cmdb\_ci\_storage\_pool|Owns::Owned by|cmdb\_ci\_storage\_cluster \(reference **hosted\_by**\)|

**Parent Topic:**[Available discovery patterns](available-patterns.md)

