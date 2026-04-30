---
title: InfiniBox Discovery
description: ServiceNow Discovery uses the InfiniBox pattern to find and map instances. Discovering these resources requires installing the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: yokohama
product: Discovery and Service Mapping Patterns
classification: discovery-and-service-mapping-patterns
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 13
breadcrumb: [Available discovery patterns, Discovery patterns used by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# InfiniBox Discovery

ServiceNow Discovery uses the InfiniBox pattern to find and map instances. Discovering these resources requires installing the Discovery and Service Mapping Patterns application from the ServiceNow Store.

Discovery uses multiple patterns to find InfiniBox storage system data. Discovering these resources requires installing the Discovery and Service Mapping Patterns and the CMDB CI Class Models applications from the ServiceNow Store, as each application is dependent on the other. You can use the patterns for discovering the InfiniBox components on the ServiceNow AI Platform using the Paris release or later.

The InfiniBox enterprise storage array delivers faster-than-all-flash performance, high availability, and multi-petabyte scale for mixed application workloads.​ The InfiniBox hardware redundancy design enables rapid recovery from any component failures.

## Request apps on the Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/home) website to view all the available apps and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

## Prerequisites

**Note:** Discovery of 'Hosts' and 'Clusters' associated to the InfiniBox system are not supported from version 1.0.83 of the Discovery and Service Mapping Patterns \(sn\_itom\_pattern\) plugin.

-   Install the following plugins:
    -   CMDB CI Class Models plugin \(Version 1.28.0 or later\)
    -   Discovery and Service Mapping Patterns plugin \(Version 1.0.81 or later\)
-   Set Basic Auth credentials for the InfiniBox storage system
-   Set a credential alias and associate it with the InfiniBox system credential record.

-   Set discovery schedule type to Serverless.

-   Make sure that the MID server has access to the target device.


-   **Authentication**

    Configure the credentials of the Basic Auth type for authenticating the REST API calls. They are used for discovery of the CI types associated with the InfiniBox Storage system.​

    1.  Navigate to **Connections &amp; Credential Aliases**.
    2.  Create a new **Credential** record.
    3.  Create a new **Basic Auth** credential record from the Credentials related list form. Configure the **Basic Auth** parameters:

        ​​

        ![Connection & Credential Aliases.](../image/connectionandcredentialaliases.png "Connection & Credential Aliases")


![Basic Auth Credentials.]()

Configure the credentials of the **Basic Auth** type and the credential Alias associated with the credential record.

You can make the same configuration from the credential record form where you previously created the Credential alias. Associate the Connections and Credential Alias records respectively.

![Basic Auth Credentials.](../image/basicauthcredentials.png "Basic Auth Credentials")

-   **Discovery schedule**
    1.  ​Create the Discovery schedule with the Serverless Discovery type.

        ![Discovery Schedule.](../image/discoveryschedule.png)

    2.  For the Discovery schedule with the Discover type of Serverless, configure the InfiniBox Storage System LP pattern within the Serverless Execution Patterns tab.
    3.  Set the Run Child Patterns to True.

        This enables the system to trigger all the patterns associated Child Patterns with the InfiniBox Storage System \(LP\). This is necessary due to the Large Payload \(LP\) mechanism. This is used for the discovery of the InfiniBox storage system and all the corresponding CI types.


![serverless execution patterns.](../image/serverlessexecutionpatterns.png)

Apply the values for **ip\_address** and **credential\_alias** from the Serverless Execution Pattern related section. These serve as input parameters for triggering the discovery schedule and the associated InfiniBox discovery pattern.

Apply the IP Address of the InfiniBox system and the ID of the previously created Connections &amp; Credential Aliases record. These are related to the InfiniBox credential **Basic Auth** type record.

![Serverless Execution Pattern.](../image/serverlessexecutionpattern.png "Serverless Execution Pattern")

## Data collected by Discovery during horizontal discovery

|Field|Description|
|-----|-----------|
|ip\_address|The IP address of the InfiniBox system.|
|name|The name of the InfiniBox system.|
|os\_version|The current version of the InfiniBox system.|
|model\_id|The model ID of the InfiniBox system.|
|manufacturer|The product name of the InfiniBox system.|
|serial\_number|The serial number of the InfiniBox system.|
|operational\_status|The operational state of the InfiniBox system.|
|physical\_capacity|The total physical capacity of the InfiniBox system in gigabytes.|
|virtual\_capacity|The total virtual capacity of the InfiniBox system in gigabytes.|

![Storage Server View Map.](../image/storageserverviewmap.png "Storage Server View Map")

|Field|Description|
|-----|-----------|
|device id ​|The ID of the physical disk device, combination of NODE\_ID@DISK\_ID.|
|name|The name of physical disk device, combination of INFINIBOX\_NAME:NODE\_ID@DISK\_ID|
|drive\_type|The drive type of the physical disk device.|
|model\_id|The model ID of the physical disk device.|
|manufacturer|The vendor of the physical disk device.|
|operational\_status|The operational state of the physical disk device.|
|serial\_number|The serial number of the physical disk device.|
|computer|Reference to any of the physical nodes part of the InfiniBox system.|

|Field|Description|
|-----|-----------|
|wwpn|The world wide port name of fibre channel port.|
|name|The name of fibre channel port \(wwpn\).|
|speed|The speed value of the fibre channel port in gigabits per second, if applied.|
|wwnn|The world wide node name of fibre channel port.|
|port\_role|The role of fibre channel port.|
|state|The state of fibre channel port.|
|link\_state|The state of the connectivity of fibre channel port.|
|manufacturer|The vendor of the fibre channel port.|
|model\_id|The model ID of the of fibre channel port.|
|computer|The reference to any of the physical nodes part of the InfiniBox system.|

![Fibre channel view map.](../image/fibrechannelportviewmap.png "Fibre channel view map")

<table id="table_x43_j5j_2qb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

object\_id

</td><td>

The ID of the storage switch.

</td></tr><tr><td>

name

</td><td>

The name of storage switch, combination of id:SWITCH\_ID@SWITCH\_NAME.

</td></tr><tr><td>

wwnn

</td><td>

The world wide node name of the storage switch.

</td></tr><tr><td>

manufacturer

</td><td>

The vendor of the storage switch.

</td></tr></tbody>
</table>![Storage Switch View Map.](../image/storageswitchviewmap.png "Storage Switch View Map")

|Field|Description|
|-----|-----------|
|mac\_address|The ethernet address of the network adapter.|
|name|The ethernet name of the network adapter.|
|operational\_status|The ethernet link state of the network adapter.|
|manufacturer|The ethernet vendor of the network adapter.|
|model\_id|The ethernet model ID of the network adapter.|
|ip\_address|The IPv4 IP address associated with the ethernet network adapter.|

![Network Adapter View Map.](../image/networkadaptorviewmap.png "Network Adapter View Map")

|Field|Description|
|-----|-----------|
|netmask|The netmask associated with the InfiniBox storage system.|
|name|The IPv4 IP address of any of the InfiniBox nodes or the InfiniBox storage system.|
|ip\_address|The IPv4 IP address of any of the InfiniBox nodes.|

|Field|Description|
|-----|-----------|
|object\_id|The name of the InfiniBox Storage Node, combination of id:NODE\_ID@NODE\_NAME.|
|name|The name of the InfiniBox Storage Node, combination of INFINIBOX\_NAME@NODE\_NAME.|
|node\_state|The operational state of the InfiniBox Storage Node.|
|manufacturer|The vendor of the InfiniBox Storage Node.|
|model\_id|The model of the InfiniBox Storage Node.|
|ip\_address|The IPv4 IP address assigned to the InfiniBox Storage Node.|

![Storage Node Element View Map.](../image/storagenodeviewmap.png "Storage Node Element View Map")

|Field|Description|
|-----|-----------|
|serial\_number|The serial number associated to the InfiniBox storage system.|
|serial\_number\_type|The serial number type of the InfiniBox storage system.|
|valid|The serial number valid type of the InfiniBox storage system.|

|Field|Description|
|-----|-----------|
|object\_id|The ID of the storage volume, combination of id:VOLUME\_ID@VOLUME\_NAME.|
|volume\_id|The ID of the storage volume, combination of id:VOLUME\_ID@VOLUME\_NAME.|
|name|The name of the storage volume.|
|storage\_type|The role of the storage volume.|
|size\_bytes|The total size of the storage volume in bytes.|
|serial\_number|The serial number of the storage volume.|
|pool\_id|The ID of the pool to which the storage volume is associated.|
|state|The lock state of the storage volume.|
|provisioning\_type|The type of provisioning of the storage volume.|
|size|The total size of the storage volume in gigabytes|
|provided\_by|The reference to the storage pool, to which the storage volume is associated.|

![Storage Volume View Map.](../image/storagevolumeviewmap.png "Storage Volume View Map")

|Field|Description|
|-----|-----------|
|object\_id|The ID of the storage volume snapshot, combination of id:VOLUME\_ID@VOLUME\_NAME.|
|storage\_server|The name of InfiniBox system, to which the volume snapshot is associated.|
|name|The name of the storage volume snapshot.|
|size\_bytes|The total size of the storage volume snapshot in bytes.|
|size|The total size of the storage volume snapshot in gigabytes.|
|serial\_number|The serial number of the storage volume snapshot.|
|pool\_id|The ID of the pool, to which the storage volume snapshot is associated.|
|parent\_id|The ID of the storage volume, parent of the storage volume snapshot.|
|state|The lock state of the storage volume snapshot.|
|provisioning\_type|The type of provisioning of the storage volume snapshot.|
|provided\_by|The reference to the storage pool, to which the storage volume is associated.|

![Storage Volume Snapshot.](../image/snapshotstoragevolumeviewmap.png "Storage Volume Snapshot")

|Field|Description|
|-----|-----------|
|object\_id|The ID of the storage volume, combination of id:POOL\_ID@POOL\_NAME.|
|name|The name of the storage pool.|
|physical\_capacity|The total physical capacity of the storage pool in gigabytes.|
|virtual\_capacity|The total virtual capacity of the storage pool in gigabytes.|
|free\_phys\_capacity|The available physical capacity of the storage pool in gigabytes.|
|free\_virt\_capacity|The available virtual capacity of the storage pool in gigabytes.|
|num\_vols|The number of the volumes participating into the storage pool.|
|num\_file\_sys|The number of the file systems participating into the storage pool.|
|num\_file\_sys\_snap|The number of the file system snapshots participating into the storage pool.|
|num\_vol\_snap|The number of the volume snapshots participating into the storage pool.|
|pool\_id|The ID of the storage pool.|
|pool\_state|The state of the storage pool.|

![Storage Pool View Map.](../image/storagepoolviewmap.png "Storage Pool View Map")

|Field|Description|
|-----|-----------|
|object\_id|The ID of the primary file system, combination of id:FILE\_SYSTEM\_ID.|
|server\_name|The name of InfiniBox system, to which the primary file system is associated.|
|name|The name of the primary file system, combination of id:FILE\_SYSTEM\_ID@FILE\_SYSTEM\_NAME.|
|size\_bytes|The total size of the primary file system in bytes.|
|size|The total size of the primary file system in gigabytes.|
|free\_space\_bytes|The free space of the primary file system in bytes.|
|serial\_number|The serial number of the primary file system.|
|storage\_type|The type of the primary file system.|
|pool\_id|The ID of the pool, to which the primary file system is associated.|
|provisioning\_type|The type of provisioning of the primary file system.|
|provided\_by|The reference to the storage pool, to which the primary file system is associated.|

![File System View Map.](../image/InfiniboxFileSystemviewmap.png "File System View Map")

|Field|Description|
|-----|-----------|
|object\_id|The ID of the snapshot file system, combination of id:FILE\_SYSTEM\_ID@FILE\_SYSTEM\_NAME.|
|volume\_id|The ID of the snapshot file system, combination of id:FILE\_SYSTEM\_ID@FILE\_SYSTEM\_NAME.|
|server\_name|The name of InfiniBox system, to which the snapshot file system is associated.|
|name|The name of the snapshot file system.|
|size\_bytes|The total size of the snapshot file system in bytes.|
|free\_space\_bytes|The free space of the snapshot file system in bytes.|
|serial\_number|The serial number of the snapshot file system.|
|storage\_type|The type of the snapshot file system.|
|pool\_id|The ID of the pool, to which the snapshot file system is associated.|
|parent\_id|The ID of the primary file system, to which the snapshot file system is associated.|
|provisioning\_type|The type of provisioning of the snapshot file system.|

![File System Snapshot View Map.](../image/snapshotfilesystemviewmap.png "File System Snapshot View Map")

|Field|Description|
|-----|-----------|
|path|The export path of the InfiniBox export entity.|
|name|The name of the InfiniBox export entity, combination of id:EXPORT\_ID@EXPORT\_PATH.|
|fileshare\_id|The ID of the export entity in the context of the InfiniBox system.|

![Export View Map.](../image/exportviewmap.png "Export View Map")

|Field|Description|
|-----|-----------|
|object\_id|TheID of the primary InfiniBox consistency group, combination of id:CONSISTENCY\_GROUP\_ID@ CONSISTENCY\_GROUP\_NAME.|
|created\_time|The creation time of the primary InfiniBox consistency group in format YY-MM-DD HH:mm::SS.|
|updated\_time|The updated time of the primary InfiniBox consistency group in the format YY-MM-DD HH:mm::SS.|
|name|The name of the primary InfiniBox consistency group.|
|type|The type of the primary InfiniBox consistency group.|
|members\_count|The count of the entities participating in the primary InfiniBox consistency group.|
|pool\_id|The ID of the pool, to which the primary InfiniBox consistency group is associated.|
|lock\_state|The lock state of the primary InfiniBox consistency group.|

![Primary Consistency Group View Map.](../image/primaryconsistencygroupmap.png "Primary Consistency Group View Map")

|Field|Description|
|-----|-----------|
|object\_id|The ID of the snapshot InfiniBox consistency group, combination of id:CONSISTENCY\_GROUP\_ID@ CONSISTENCY\_GROUP\_NAME.|
|created\_time|The creation time of the snapshot InfiniBox consistency group in format YY-MM-DD HH:mm::SS.|
|updated\_time|The updated time of the snapshot InfiniBox consistency group in format YY-MM-DD HH:mm::SS.|
|name|The name of the snapshot InfiniBox consistency group.|
|type|The type of the snapshot InfiniBox consistency group.|
|members\_count|The number of entities participating in the snapshot InfiniBox consistency group.|
|pool\_id|The ID of the pool, to which the snapshot InfiniBox consistency group is associated.|
|lock\_state|The lock state of the snapshot InfiniBox consistency group.|

![Snapshot Consistency Group View Map.](../image/snapshotconsistancygroupviewmap.png "Snapshot Consistency Group View Map")

|Field|Description|
|-----|-----------|
|object\_id|The ID of the InfiniBox link.|
|name|The name of the InfiniBox link.|
|remote\_version|The version of the remote InfiniBox storage system.|
|remote\_host|The host name or IP address of the remote InfiniBox storage system.|
|remote\_ip|The IP address of the remote InfiniBox storage system.|
|remote\_link\_id|The link ID of the remote InfiniBox storage system.|
|remote\_serial\_number|The serial number of the remote InfiniBox storage system.|
|remote\_sys\_name|The system name of the remote InfiniBox storage system.|
|link\_state|The state of the link between the InfiniBox storage systems.|
|link\_config\_id|The link configuration ID of the remote InfiniBox storage system in GUID format.|
|link\_mode|The mode of the link between the InfiniBox storage systems.​|
|resiliency\_mode|The resiliency mode between the InfiniBox storage systems.​|
|local\_witness\_state|The local witness state of the InfiniBox storage system.​|
|witness\_address|The local witness address of the InfiniBox storage system, if assigned.​|
|last\_connection\_time|The time stamp of the established connection between the Infinibox storage systems in format YY-MM-DD HH:MM::SS.​|
|local\_replica\_net\_space\_id|The local replica network space ID of the Infinibox storage system.​|
|link\_replication\_type|The replication type of the link between the Infinibox storage systems.​|

![Link View Map.](../image/linkviewmap.png "Link View Map")

|Field|Description|
|-----|-----------|
|object\_id|The ID of the InfiniBox replica, combination of LOCAL\_ENTITY\_NAME@REMOTE\_ENTITY\_NAME@replica:REPLICA\_ID.|
|name|The ID of the InfiniBox replica, combination of LOCAL\_ENTITY\_NAME@REMOTE\_ENTITY\_NAME@replica:REPLICA\_ID.|
|replica\_role|The role of the InfiniBox storage system replica.|
|entity\_type|The type of the entity replicated in the context of the InfiniBox storage system.|
|replica\_state|The state of the replica in the context of the InfiniBox storage system|
|replication\_type|The type of the replication of the context of the InfiniBox storage system, if applied.|
|sync\_state|The synchronization state of the InfiniBox storage system replica.|
|link\_id|The ID of the link associated to the replica in the context of the InfiniBox storage system.|
|entity\_id|The ID of the replicated entity in the context of the InfiniBox storage system.​|
|remote\_entity\_id|The ID of the remote replicated entity of the InfiniBox storage system.​|
|entity\_name|The name of the local replicated entity in the context of the InfiniBox storage system.​|
|remote\_entity\_name ​|The name of the remote replicated entity in the context of the InfiniBox storage system.|
|dataset\_type|The local dataset type in the context of the InfiniBox storage system.​|

![Replica View Map.](../image/replicaviewmap.png "Replica View Map")

## CI Relationships

## Relationships created by the InfiniBox Storage System \(LP\) pattern

|CI|Relationship|CI|
|---|------------|---|
|cmdb\_ci\_storage\_server|"Contains :: Contained by"|cmdb\_ci\_storage\_switch|
|cmdb\_ci\_fc\_port|“Connects to :: Connected by”|cmdb\_ci\_storage\_switch​|
|cmdb\_ci\_storage\_server|“Uses :: Used by”|cmdb\_ci\_network\_adapter​|
|cmdb\_ci\_storage\_node\_element|“Owns :: Owned by”|cmdb\_ci\_network\_adapter​|
|cmdb\_ci\_ip\_address|“reference by column name nic”|​cmdb\_ci\_network\_adapter​|
|cmdb\_ci\_storage\_node\_element ​|“Owns :: Owned by”|cmdb\_ci\_fc\_port​|
|​cmdb\_ci\_storage\_server|“Owns :: Owned by”|cmdb\_ci\_ip\_address​|
|cmdb\_ci\_storage\_node\_element ​|“Owns :: Owned by”|cmdb\_ci\_ip\_address|
|cmdb\_ci\_storage\_node\_element|“Contains :: Contained by”|cmdb\_ci\_disk​|
|cmdb\_serial\_number|“reference”|cmdb\_ci\_storage\_server​|
|cmdb\_ci\_storage\_server|“Allocated to :: Allocated from”|cmdb\_ci\_storage\_node\_element​|

|CI|Relations|CI|
|---|---------|---|
|cmdb\_ci\_storage\_volume|“Provisioned From :: Provisioned”|cmdb\_ci\_storage\_vol\_snapshot|
|cmdb\_ci\_storage\_pool|“reference by column name provided by”|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_storage\_server|"Contains :: Contained by and reference by column name computer”|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_storage\_server|“Contains :: Contained by”|cmdb\_ci\_storage\_vol\_snapshot|
|cmdb\_ci\_infinibox\_cg|“Contains :: Contained by”|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_infinibox\_snapshot\_cg|“Contains :: Contained by”|cmdb\_ci\_storage\_vol\_snapshot|

|CI|Relations|CI|
|---|---------|---|
|cmdb\_ci\_storage\_server|“Contains :: Contained by”|cmdb\_ci\_storage\_pool|

|CI|Relations|CI|
|---|---------|---|
|cmdb\_ci\_storage\_fileshare|“Provided By :: Provides”|cmdb\_ci\_storage\_server|

|CI|Relations|CI|
|---|---------|---|
|cmdb\_ci\_storage\_server|“Contains :: Contained by”|cmdb\_ci\_file\_system|
|cmdb\_ci\_storage\_server|“Contains :: Contained by”|cmdb\_ci\_file\_system\_snapshot|
|cmdb\_ci\_file\_system|“Provided By :: Provides”|cmdb\_ci\_storage\_pool|
|cmdb\_ci\_file\_system\_snapshot|“Provided By :: Provides”|cmdb\_ci\_storage\_pool|
|cmdb\_ci\_file\_system|“Provisioned From :: Provisioned”|cmdb\_ci\_file\_system\_snapshot|
|cmdb\_ci\_file\_system|“Provided By :: Provides”|cmdb\_ci\_storage\_fileshare|
|cmdb\_ci\_file\_system\_snapshot|“Provided By :: Provides”|cmdb\_ci\_storage\_fileshare|

|CI|Relations|CI|
|---|---------|---|
|cmdb\_ci\_storage\_server|“Contains :: Contained by”|cmdb\_ci\_infinibox\_cg|
|cmdb\_ci\_infinibox\_cg|“Provisioned From :: Provisioned”|cmdb\_ci\_infinibox\_snapshot\_cg|
|cmdb\_ci\_storage\_server|“Contains :: Contained by”|cmdb\_ci\_infinibox\_snapshot\_cg|
|cmdb\_ci\_infinibox\_cg|“Contains :: Contained by”|cmdb\_ci\_storage\_pool|
|cmdb\_ci\_infinibox\_snapshot\_cg|“Contains :: Contained by”|cmdb\_ci\_storage\_pool|

|CI|Relations|CI|
|---|---------|---|
|cmdb\_ci\_storage\_server|“Contains :: Contained by”|cmdb\_ci\_infinibox\_replica|
|cmdb\_ci\_infinibox\_replica|“Replicates to :: Replicated by”|cmdb\_ci\_infinibox\_cg|
|cmdb\_ci\_infinibox\_replica|“Uses :: Used by”|cmdb\_ci\_infinibox\_link|
|cmdb\_ci\_infinibox\_replica|“Replicates to :: Replicated by”|cmdb\_ci\_storage\_volume|
|cmdb\_ci\_infinibox\_replica|“Replicates to :: Replicated by”|cmdb\_ci\_file\_system|

|CI|Relations|CI|
|---|---------|---|
|cmdb\_ci\_storage\_server|“Contains :: Contained by”|cmdb\_ci\_infinibox\_link|

![infinibox class model.](../image/infinibox-class-model.png "Infinibox Class Model")

**Parent Topic:**[Available discovery patterns](../concept/available-patterns.md)

