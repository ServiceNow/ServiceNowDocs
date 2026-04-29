---
title: NetApp Server and Cluster discovery
description: Discovery and Service Mapping find NetApp servers and clusters using patterns. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.
locale: en-US
release: australia
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2026-03-24"
reading_time_minutes: 13
keywords: [NetApp, Server, Cluster, Patterns]
breadcrumb: [Storage discovery, Data collected by ITOM Visibility, ITOM Visibility reference, ITOM Visibility, IT Operations Management]
---

# NetApp Server and Cluster discovery

Discovery and Service Mapping find NetApp servers and clusters using patterns. Discovering some of these resources may require updating to the latest version of the Discovery and Service Mapping Patterns application from the ServiceNow Store.

## Request new or enhanced Patterns on the ServiceNow® Store

Visit the [ServiceNow Store](https://store.servicenow.com/sn_appstore_store.do#!/store/application/06a71b1367e4130051c9027e2685ef1e/1.6.0?referer=%2Fstore%2Fsearch%3Flistingtype%3Dallintegrations%25253Bancillary_app%25253Bcertified_apps%25253Bcontent%25253Bindustry_solution%25253Boem%25253Butility%25253Btemplate%26q%3DPatterns&sl=sh) to view all the available updates and for information about submitting requests to the store. For cumulative release notes information for all released apps, see the [ServiceNow Store version history release notes](https://docs.servicenow.com/bundle/store-release-notes/page/release-notes/store/sn-store-release-notes.html).

NetApp discovery isn’t supported for NetApp servers in the AWS cloud. To learn about the components and versions of NetApp servers and clusters that you can discover, refer to [Detailed information on products discovered by ITOM Visibility](../../service-mapping/reference/r_SupportedApplications.md).

## NetApp Server and Cluster discovery methods

<table id="table_adb_p4l_nbb"><thead><tr><th>

Method

</th><th>

Supported modes

</th><th>

Upgrades

</th></tr></thead><tbody><tr><td>

Discovery with patterns using ONTAP API.These patterns support native discovery of NetApp servers without requiring the discovery of the SMI-S server.

</td><td>

-   NetApp 7-Mode
-   NetApp Cluster-Mode

</td><td>

Active by default.

</td></tr><tr><td>

Discovery with patterns using HTTP REST API.

</td><td>

NetApp Cluster-Mode

</td><td>

Available on Discovery and Service Mapping Patterns store application starting August 2023.

</td></tr><tr><td>

Discovery with probes and sensors using SMI-S.

</td><td>

-   NetApp 7-Mode
-   NetApp Cluster-Mode

</td><td>

Legacy

</td></tr></tbody>
</table>## NetApp discovery properties

To use discovery with patterns, navigate to **Discovery Definition** &gt; **Properties** and enable these properties:

|Property label|Name|
|--------------|----|
|For 7-Mode NetApp storage servers, use native discovery instead of SMI-S.|glide.discovery.sensors.netapp\_native\_7mode|
|For Cluster-Mode NetApp storage servers, use native discovery instead of SMI-S.|glide.discovery.sensors.netapp\_native\_cluster\_mode|

The following patterns support the NetApp storage discovery:

-   NetApp Storage 7-Mode
-   NetApp Storage Cluster-Mode
-   NetApp Storage Cluster-Mode - HTTP

The Cluster-Mode patterns support chassis and disk shelf chassis discovery through an extension section.

**Note:** If you have already performed NetApp discovery with Probes and then enable these properties, a migration script runs the next time you perform NetApp discovery. This script could delete configuration items \(CIs\) for items like storage pools, which probes discover but the patterns don’t. It also creates relationships.

## SNMP-based discovery prerequisites

-   **Configure SNMP community credentials**

    Configure SNMP community credentials to classify the NetApp server. For more information, see [SNMP community credentials](https://www.servicenow.com/docs/access?context=c_SNMPCredentials&version=australia&pubname=australia-platform-security&ft:locale=en-US).

-   **Enable __read-only__ access to the ONTAP API**

    Enable **read-only** access to the ONTAP API on the NetApp server.

    -   NetApp Storage 7-Mode: The user must have a custom role with the following capabilities:
        -   `login-snmp, login-ndmp, login-sp, and login-http-admin`
        -   `Api-*`
    -   NetApp Storage Cluster-Mode: The user can have a read-only role with default access.
-   **Verify read-only permission for ONTAP SDK APIs**

    Verify that the user has **read-only** permissions for the following ONTAP SDK APIs:

    -   NetApp Storage 7-Mode:
        -   `aggr-list-info`
        -   `cifs-share-list-iter-start`
        -   `disk-list-info`
        -   `fcp-adapter-initiators-list-info`
        -   `fcp-adapter-list-info`
        -   `igroup-list-info`
        -   `iscsi-node-get-name`
        -   `lun-list-info`
        -   `lun-map-list-info`
        -   `net-config-get-active`
        -   `nfs-exportfs-list-rules`
        -   `system-get-info`
        -   `system-get-version`
        -   `volume-list-info`
    -   NetApp Storage Cluster-Mode:
        -   `aggr-get-iter`
        -   `cifs-share-get-iter`
        -   `cluster-identity-get`
        -   `fcp-interface-get-iter`
        -   `fcp-initiator-get-iter`
        -   `igroup-get-iter`
        -   `iscsi-initiator-get-iter`
        -   `lun-get-iter`
        -   `lun-map-get-iter`
        -   `net-interface-get-iter`
        -   `net-port-get-iter`
        -   `storage-disk-get-iter`
        -   `storage-pool-get-iter`
        -   `storage-shelf-info-get-iter`
        -   `system-get-node-info-iter`
        -   `system-get-version`
        -   `system-node-get-iter`
        -   `volume-get-iter`
        -   `vserver-get-iter`
-   **Configure basic authentication credentials**

    Configure basic authentication credentials for the read-only user. For more information, see [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).


## REST-based discovery prerequisites

-   **Disable SNMP-based discovery**

    For more information, see [Disable SNMP-based NetApp storage cluster discovery](../../service-mapping/task/disable-snmp-netapp-discovery.md).

-   **Verify __read-only__ role and permissions**

    Verify that the user has **read-only** role and permissions for the following ONTAP REST APIs:

    -   `/api/cluster`
    -   `/api/cluster/chassis?fields=nodes.name,nodes.uuid,id`
    -   `/api/cluster/nodes?fields=name,serial_number,model,system_id,controller,version`
    -   `/api/cluster/nodes?fields=name,state`
    -   `/api/cluster/nodes?fields=name,uuid,model`
    -   `/api/network/ethernet/ports?fields=mac_address,name,node.name`
    -   `/api/network/fc/interfaces?fields=svm.name,wwnn,wwpn,port_address,name,location.node.name`
    -   `/api/network/fc/logins?fields=initiator,interface.name`
    -   `/api/network/ip/interfaces?fields=ip.netmask,svm.name,ip.address,location.home_node.name,location.home_port.name,service_policy.name`
    -   `/api/network/ip/interfaces?fields=location,svm,state`
    -   `/api/network/ip/interfaces?fields=name,ip,state,enabled,svm,location`
    -   `/api/protocols/cifs/shares?fields=path,name,svm.name`
    -   `/api/protocols/san/igroups?fields=initiators.name,name,os_type,svm.name`
    -   `/api/protocols/san/iscsi/sessions?fields=svm.name,initiator.alias`
    -   `/api/protocols/san/lun-maps?fields=svm.name,lun.uuid,lun.name,lun.node.name,logical_unit_number,igroup.name,igroup.uuid`
    -   `/api/storage/aggregates?fields=space.block_storage.size,space.block_storage.available,node.name`
    -   `/api/storage/disks?fields=sector_count,bytes_per_sector,node.name,serial_number,model,type,vendor,name`
    -   `/api/storage/luns?fields=space.used,space.size,svm.name,location.volume.name,location.volume.uuid,name,location.node.name`
    -   `/api/storage/pools?fields=name,capacity.total,capacity.remaining,nodes.name`
    -   `/api/storage/shelves?fields=name,model,serial_number,paths.node.name,id`
    -   `/api/storage/volumes?fields=aggregates.name,space.size,space.available,svm.name&return_timeout=120`
    -   `/api/svm/svms?fields=name,subtype`
    -   `/api/svm/svms?fields=subtype,name`
-   **Configure basic authentication credentials**

    Configure basic authentication credentials for the read-only user. For more information, see [Basic authentication credentials](https://www.servicenow.com/docs/access?context=r_BasicAuthCredentialsForm&version=australia&pubname=australia-platform-security&ft:locale=en-US).


## General prerequisites

-   **Verify that the following applications are up to date**
    -   Discovery and Service Mapping Patterns
    -   Visibility Content
-   **Disable SSLv3 and enable TLS for the target NetApp server**

    Disable SSLv3 and enable TLS for the target NetApp server, as the Java Runtime used by the MID Server doesn't enable SSLv3 by default. The key to encrypt the certificate must be at least 1024 bits.

-   **Schedule a horizontal discovery**

    To run discovery using Patterns, create a Discovery schedule that targets the management IP address of the NetApp server. For more information, see [create a discovery schedule](running-discoveries.md).

    **Note:** NetApp creates different storage volume identifiers when running with different protocols. When running discovery with HTTP after running discovery with SNMP, duplicate CIs are created for the same storage volume. One CI is created for the unique identifier \(UUID\) NetApp ONTAP API provides, and one CI is created for the unique identifier \(UUID\) NetApp HTTP REST API provides.


## Data collected by Discovery during horizontal discovery

Discovery populates the data in the CMDB when running the NetApp patterns.

<table id="table_dpq_sn1_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the NetApp storage server or Storage Virtual Machine \(SVM\)

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

Manufacturer of the storage server. The value is set to NetApp.

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

Model identifier of the storage server. For SVMs in Cluster-Mode, the value is set to SVM.

</td></tr><tr><td>

Firmware version \[firmware\_version\]

</td><td>

ONTAP firmware version running on the storage server.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Unique serial number of the storage server.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Full version information of the ONTAP software.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

Management IP address of the storage server.

</td></tr><tr><td>

Physical Capacity \(GB\) \[physical\_capacity\]

</td><td>

Total amount of physical storage space available within the NetApp system, measured in gigabytes \(GB\). This capacity includes both allocated and unallocated storage resources.

</td></tr><tr><td>

Free Physical Capacity \(GB\) \[free\_physical\_capacity\]

</td><td>

Available physical storage space within the NetApp system, measured in GB.

</td></tr><tr><td>

Used Physical Capacity \(GB\) \[used\_physical\_capacity\]

</td><td>

Used physical storage space within the NetApp system, measured in GB.

</td></tr></tbody>
</table><table id="table_yj5_p41_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Description \[short\_description\]

</td><td>

Full version information of the ONTAP software running on the cluster.

</td></tr><tr><td>

Name \[name\]

</td><td>

Name of the NetApp storage cluster.

</td></tr><tr><td>

Correlation ID \[correlation\_id\]

</td><td>

Unique identifier \(UUID\) of the cluster.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

Cluster management IP address.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

Manufacturer of the storage server. The value is set to NetApp.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Unique serial number of the cluster, constructed from cluster UUID and name.This field is applicable to HTTP pattern only.

</td></tr><tr><td>

Cluster Version \[cluster\_version\]

</td><td>

ONTAP version running on the cluster, for example: 9.14.1P4.This field is applicable to HTTP pattern only.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the cluster node.|
|Operational status \[operational\_status\]|Operational status of the cluster node. Default status is Operational.|
|Cluster \[cluster\]|References the Storage Cluster \[cmdb\_ci\_storage\_cluster\] table.|
|Server \[server\]|References the Storage Node Element \[cmdb\_ci\_storage\_node\_element\] table.|

<table id="table_uy4_gp1_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the storage node element.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

The hardware manufacturer of the node element, which is: NetApp.This field is applicable to HTTP pattern only.

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

Model identifier of the node hardware.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Serial number of the physical node.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

Full version information of the ONTAP software running on the node.

</td></tr><tr><td>

RAM \(MB\) \[ram\]

</td><td>

Memory size of the node in megabytes \(MB\).

</td></tr><tr><td>

CPU core count \[cpu\_core\_count\]

</td><td>

The total number of CPU cores in the node element.

</td></tr><tr><td>

CPU type \[cpu\_type\]

</td><td>

The processor type used in the node element.

</td></tr><tr><td>

CPU manufacturer \[cpu\_manufacturer\]

</td><td>

References the Company \[core\_company\] table.

</td></tr><tr><td>

Chassis \[chassis\]

</td><td>

References the Chassis \[cmdb\_ci\_chassis\] table.This field is applicable to Cluster-Mode patterns only.

</td></tr></tbody>
</table><table id="table_ohv_gp1_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the network adapter port.

</td></tr><tr><td>

MAC Address \[mac\_address\]

</td><td>

MAC address of the network adapter.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address.

</td></tr><tr><td>

Netmask \[netmask\]

</td><td>

Network subnet mask for the IP address.

</td></tr><tr><td>

Configuration Item \[cmdb\_ci\]

</td><td>

References the Storage Server \[cmdb\_ci\_storage\_server\] or Storage Node Element \[cmdb\_ci\_storage\_node\_element\] table.Physical resources are owned by Storage Node Elements, while logical resources are owned by Storage Servers.

</td></tr></tbody>
</table><table id="table_qpf_hp1_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

IP address.

</td></tr><tr><td>

IP Address \[ip\_address\]

</td><td>

IP address.

</td></tr><tr><td>

Netmask \[netmask\]

</td><td>

Network subnet mask for the IP address.

</td></tr><tr><td>

MAC Address \[mac\_address\]

</td><td>

MAC address of the network adapter.

</td></tr><tr><td>

Nic \[nic\]

</td><td>

References the Network Adapter \[cmdb\_ci\_network\_adapter\] table.

</td></tr><tr><td>

IP version \[ip\_version\]

</td><td>

Indicates whether the IP address is IPv4 or IPv6. This field is applicable for storage 7-Mode pattern only.

</td></tr></tbody>
</table><table id="table_dlk_hp1_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the disk in ONTAP format.

</td></tr><tr><td>

Device ID \[device\_id\]

</td><td>

Device identifier of the disk.

</td></tr><tr><td>

Manufacturer \[manufacturer\]

</td><td>

Manufacturer name of the disk.

</td></tr><tr><td>

Model ID \[model\_id\]

</td><td>

The model identifier for the disk.

</td></tr><tr><td>

Serial number \[serial\_number\]

</td><td>

Serial number of the disk.

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

The total capacity of the disk in bytes.

</td></tr><tr><td>

Device interface \[device\_interface\]

</td><td>

The interface type used to connect the disk.

</td></tr><tr><td>

Interface \[interface\]

</td><td>

Interface type of the disk.

</td></tr><tr><td>

Drive type \[drive\_type\]

</td><td>

Drive type. The value is set to disk.

</td></tr><tr><td>

Storage type \[storage\_type\]

</td><td>

The type of storage used by the disk. The value is set to disk.

</td></tr><tr><td>

Disk space \(GB\) \[disk\_space\]

</td><td>

The total capacity of the disk in GB.

</td></tr><tr><td>

Size \[size\]

</td><td>

Display value of the total disk capacity in GB or terabytes \(TB\).

</td></tr><tr><td>

Computer \[computer\]

</td><td>

-   Storage 7-Mode pattern: References the Storage Server \[cmdb\_ci\_storage\_server\] table
-   Cluster-Mode patterns: References the Storage Node Element \[cmdb\_ci\_storage\_node\_element\] table.

</td></tr><tr><td>

Diskshelf chassis \[diskshelf\_chassis\]

</td><td>

References the Disk Shelf Chassis \[cmdb\_ci\_diskshelf\_chassis\] table.This field is applicable to Cluster-Mode patterns only.

</td></tr></tbody>
</table><table id="table_c1t_hp1_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

The unique name of the storage pool.

</td></tr><tr><td>

Description \[short\_description\]

</td><td>

A brief summary describing the storage pool.

</td></tr><tr><td>

Pool ID \[pool\_id\]

</td><td>

The unique identifier assigned to the storage pool.

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

The total capacity of the storage pool, in bytes.

</td></tr><tr><td>

Free space bytes \[free\_space\_bytes\]

</td><td>

The amount of available space in the pool, in bytes.

</td></tr><tr><td>

Size \[size\]

</td><td>

Display value of the total storage pool capacity in GB or TB.

</td></tr><tr><td>

Free space \[free\_space\]

</td><td>

Display value of the available storage pool capacity in GB or TB.

</td></tr><tr><td>

Hosted by \[hosted\_by\]

</td><td>

References the Storage Server \[cmdb\_ci\_storage\_server\] or Storage Node Element \[cmdb\_ci\_storage\_node\_element\] table.Physical resources are owned by Storage Node Elements, while logical resources are owned by Storage Servers.

</td></tr></tbody>
</table><table id="table_nqx_hp1_4hc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name \[name\]

</td><td>

Name of the storage volume.

</td></tr><tr><td>

Object ID \[object\_id\]

</td><td>

Unique object identifier \(UUID\) for the storage volume.This field is applicable to Cluster-Mode patterns only.

</td></tr><tr><td>

Volume ID \[volume\_id\]

</td><td>

The UUID of the storage volume.

</td></tr><tr><td>

LUN \[lun\]

</td><td>

The logical unit number \(LUN\) associated with the volume.

</td></tr><tr><td>

Size bytes \[size\_bytes\]

</td><td>

Total capacity of the volume in bytes.

</td></tr><tr><td>

Free space bytes \[free\_space\_bytes\]

</td><td>

Available free space in the volume in bytes.

</td></tr><tr><td>

Size \[size\]

</td><td>

Display value of the total storage volume capacity in GB or TB.

</td></tr><tr><td>

Consumable Size \[free\_space\]

</td><td>

Display value of the available storage volume capacity in GB or TB.

</td></tr><tr><td>

Provided by \[provided\_by\]

</td><td>

References the Storage Pool \[cmdb\_ci\_storage\_pool\] table.

</td></tr><tr><td>

Computer \[computer\]

</td><td>

References the Storage Server \[cmdb\_ci\_storage\_server\] table.

</td></tr></tbody>
</table>|Field|Description|
|-----|-----------|
|Path \[path\]|The file system path or mount location of the shared storage.|
|Name \[name\]|The unique name identifying the file share.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the initiator group \(igroup\) that acts as the storage controller.|
|Device ID \[device\_id\]|UUID of the LUN associated with this storage controller.|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name identifying the Fibre Channel \(FC\) port.|
|WWNN \[wwnn\]|The World Wide Node Name \(WWNN\) of the FC port.|
|WWPN \[wwpn\]|The World Wide Port Name \(WWPN\) of the FC port.|
|Speed \[speed\]|Speed of the FC port in Gigabit Fibre Channel \(GFC\).|
|Computer \[computer\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|The name of the iSCSI export target.|
|LUN \[lun\]|The LUN mapped to the iSCSI export.|
|Export ID \[export\_id\]|Unique identifier combining LUN path and controller name.|
|Initiator IQN \[initiator\_iqn\]|The iSCSI Qualified Name of the connecting initiator.|
|IQN \[iqn\]|The iSCSI Qualified Name of the target being exported.|
|Exported by \[exported\_by\]|References the Storage Controller \[cmdb\_ci\_storage\_controller\] table.|
|Hosted by \[hosted\_by\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|
|Storage \[storage\]|References the Storage Volume \[cmdb\_ci\_storage\_volume\] table.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the FC export combining LUN path and initiator WWPN.|
|LUN \[lun\]|LUN ID number for the FC export.|
|Export ID \[export\_id\]|Unique identifier combining LUN path and controller name.|
|Initiator WWPN \[initiator\_wwpn\]|The WWPN of the Fibre Channel initiator.|
|Exported by \[exported\_by\]|References the Storage Controller \[cmdb\_ci\_storage\_controller\] table.|
|Hosted by \[hosted\_by\]|References the Storage Server \[cmdb\_ci\_storage\_server\] table.|
|Storage \[storage\]|References the Storage Volume \[cmdb\_ci\_storage\_volume\] table.|

Discovery populates the data in the CMDB when running the NetApp Cluster-Mode Patterns Only.

|Field|Description|
|-----|-----------|
|Name \[name\]|Name of the cluster that the chassis belongs to.|
|Manufacturer \[manufacturer\]|The value is set to NetApp.|
|Model ID \[model\_id\]|Model identifier of the chassis hardware.|
|Serial number \[serial\_number\]|Serial number of the chassis.|
|Description \[short\_description\]|The value is set to NetApp Storage Chassis.|

|Field|Description|
|-----|-----------|
|Name \[name\]|Identifier of the disk shelf.|
|Manufacturer \[manufacturer\]|The value is set to NetApp.|
|Model ID \[model\_id\]|Model identifier of the disk shelf.|
|Serial number \[serial\_number\]|Serial number of the disk shelf.|
|Description \[short\_description\]|The value is set to NetApp Storage Disk Shelf Chassis.|
|Chassis \[chassis\]|References the Chassis \[cmdb\_ci\_chassis\] table.|

**Note:** For more information on NetApp discovery with CIM, see [Storage Discovery via SMI-S and CIM](../reference/r_DataCollDiscoStorageviaSMISCIM.md).

## CI relationships

Discovery creates these relationships to support the NetApp discovery.

|CI|Relationship|CI|
|---|------------|---|
|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|Hosted on::Hosts|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|
|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|References|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|
|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|Cluster of::Clusters|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Cluster Node \[cmdb\_ci\_storage\_cluster\_node\]|References|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|Managed by::Manages|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|References|Company \[core\_company\]|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\] or Storage Server \[cmdb\_ci\_storage\_server\]\*|Owns::Owned by|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Network Adapter \[cmdb\_ci\_network\_adapter\]|References|Storage Server \[cmdb\_ci\_storage\_server\] or Storage Node Element \[cmdb\_ci\_storage\_node\_element\]\*|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\] or Storage Server \[cmdb\_ci\_storage\_server\]\*|Owns::Owned by|IP Address \[cmdb\_ci\_ip\_address\]|
|IP Address \[cmdb\_ci\_ip\_address\]|References|Network Adapter \[cmdb\_ci\_network\_adapter\]|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\] or Storage Server \[cmdb\_ci\_storage\_server\]\*\*|Contains::Contained by|Disk \[cmdb\_ci\_disk\]|
|Disk \[cmdb\_ci\_disk\]|References|Storage Server \[cmdb\_ci\_storage\_server\] or Storage Node Element \[cmdb\_ci\_storage\_node\_element\]\*\*|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\] or Storage Server \[cmdb\_ci\_storage\_server\]\*|Contains::Contained by|Storage Pool \[cmdb\_ci\_storage\_pool\]|
|Storage Pool \[cmdb\_ci\_storage\_pool\]|References|Storage Server \[cmdb\_ci\_storage\_server\] or Storage Node Element \[cmdb\_ci\_storage\_node\_element\]\*|
|Storage Server \[cmdb\_ci\_storage\_server\]|Allocated to::Allocated from|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Runs on::Runs|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|References|Storage Cluster \[cmdb\_ci\_storage\_cluster\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Owns::Owned by|Fibre Channel Port \[cmdb\_ci\_fc\_port\]|
|Fibre Channel Port \[cmdb\_ci\_fc\_port\]|References|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage File Share \[cmdb\_ci\_storage\_fileshare\]|Provided By::Provides|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Server \[cmdb\_ci\_storage\_server\]|Contains::Contained by|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|References|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Volume \[cmdb\_ci\_storage\_volume\]|References|Storage Pool \[cmdb\_ci\_storage\_pool\]|
|Storage Controller \[cmdb\_ci\_storage\_controller\]|Controller for::Controlled by|Fibre Channel Port \[cmdb\_ci\_fc\_port\]|
|Storage Controller \[cmdb\_ci\_storage\_controller\]|Controller for::Controlled by|Storage Server \[cmdb\_ci\_storage\_server\]|
|Storage Controller \[cmdb\_ci\_storage\_controller\]|References|Storage Server \[cmdb\_ci\_storage\_server\]|
|iSCSI Export \[cmdb\_ci\_iscsi\_export\]|Hosted on::Hosts|Storage Server \[cmdb\_ci\_storage\_server\]|
|iSCSI Export \[cmdb\_ci\_iscsi\_export\]|References|Storage Server \[cmdb\_ci\_storage\_server\]|
|iSCSI Export \[cmdb\_ci\_iscsi\_export\]|References|Storage Controller \[cmdb\_ci\_storage\_controller\]|
|iSCSI Export \[cmdb\_ci\_iscsi\_export\]|References|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|Hosted on::Hosts|Storage Server \[cmdb\_ci\_storage\_server\]|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|References|Storage Server \[cmdb\_ci\_storage\_server\]|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|References|Storage Controller \[cmdb\_ci\_storage\_controller\]|
|Fibre Channel Export \[cmdb\_ci\_fc\_export\]|References|Storage Volume \[cmdb\_ci\_storage\_volume\]|
|Serial Number \[cmdb\_serial\_number\]|References|Storage Server \[cmdb\_ci\_storage\_server\] or Storage Node Element \[cmdb\_ci\_storage\_node\_element\]\*|

\* The CI table \(Storage Server or Storage Node Element\) is determined by the resource type and owner information returned by the NetApp ONTAP API. Physical resources are owned by Storage Node Elements, while logical resources are owned by Storage Servers.

\*\* The CI table \(Storage Server or Storage Node Element\) is determined by the pattern type. The Storage 7-Mode pattern uses the Storage Server table, while the Cluster-Mode patterns use the Storage Node Element table.

Discovery creates these relationships when running the NetApp Cluster-Mode patterns only.

|CI|Relationship|CI|
|---|------------|---|
|Serial Number \[cmdb\_serial\_number\]|References|Chassis \[cmdb\_ci\_chassis\] or Disk Shelf Chassis \[cmdb\_ci\_diskshelf\_chassis\]\*|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|Hosted on::Hosts|Chassis \[cmdb\_ci\_chassis\]|
|Storage Node Element \[cmdb\_ci\_storage\_node\_element\]|References|Chassis \[cmdb\_ci\_chassis\]|
|Disk Shelf Chassis \[cmdb\_ci\_diskshelf\_chassis\]|Hosted on::Hosts|Chassis \[cmdb\_ci\_chassis\]|
|Disk Shelf Chassis \[cmdb\_ci\_diskshelf\_chassis\]|References|Chassis \[cmdb\_ci\_chassis\]|
|Disk \[cmdb\_ci\_disk\]|Hosted on::Hosts|Disk Shelf Chassis \[cmdb\_ci\_diskshelf\_chassis\]|
|Disk \[cmdb\_ci\_disk\]|References|Disk Shelf Chassis \[cmdb\_ci\_diskshelf\_chassis\]|

\* The CI table \(Chassis or Disk Shelf Chassis\) is determined by the serial number type field.

**Parent Topic:**[Storage discovery](c_Storage.md)

