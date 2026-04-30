---
title: Datastore Discovery
description: A datastore is a storage object for virtual machines that are hosted on an ESXi server.
locale: en-US
release: yokohama
product: ITOM Visibility
classification: itom-visibility
topic_type: concept
last_updated: "2025-12-02"
reading_time_minutes: 3
keywords: [datastore discovery, storage object, datastore]
breadcrumb: [Discovery for VMware virtualization, Operating systems discovery, Data collected by ITOM Visibility, ITOM Visibility, IT Operations Management]
---

# Datastore Discovery

A datastore is a storage object for virtual machines that are hosted on an ESXi server.

A datastore is a collection of one or more physical disks, such as an iSCSI disk, and can be used by more than one ESXi host. However, a physical disk can only connect to one datastore. Because ESXi hosts can share datastores, it is easy to move virtual machine between hosts that have a common datastore.

**Note:** From the perspective of a virtual machine attached to a datastore, storage is provided by a single disk.

The advantages to connecting a datastore to multiple disks are:

-   The ability to mirror the disks for failover protection.
-   The ease of adding storage to the datastore.

For information about the tables used by Discovery to store the data for physical disks and their relationship to datastores and ESXi hosts, see [ESXi server discovery](../reference/r_DiscoverESXServers.md).

In this example configuration, two ESXi hosts share a common datastore that uses different types of storage.

![Datastore Discovery](../image/DatastoreDiscoveryDiagram.png "Datastore Discovery with different storage types")

## Relationships

ServiceNow provides tables that contain the relationships between an ESXi host and its datastore and the specific disks to which the datastore is connected.

ServiceNow Discovery establishes the relationships between a datastore, the disks attached to the datastore, and the ESXi server that hosts the virtual machines using that datastore. From the perspective of the ESXi host, iSCSI and fibre channel disks connected to the datastore are treated as physical disks. Discovery does not show the direct relationship of the storage disks to the ESXi host.

**Note:** Storage can be hosted on computers that are not discovered by Discovery. ESXi hosts are discovered through vCenter, and storage is discovered separately through CIM. The system can only establish the relationship between the two when storage is discovered before ESXi.

|Table|Description|
|-----|-----------|
|cmdb\_ci\_vcenter\_datastore\_disk|Stores the relationship of the physical disk to the datastore.|
|vcenter\_datastore\_hostmount|Stores the relationship between the datastore and the ESXi server to which it is connected.|
|cmdb\_ci\_disk|Contains the physical disks connected directly to the datastore. This table also contains a reference to the ESXi host.|
|cmdb\_ci\_fc\_disk|Contains the fibre channel disks in a storage area network \(SAN\) connected to the datastore. This table also contains a reference to the ESXi host.|
|cmdb\_ci\_iscsi\_disk|Contains the iSCSI disks in an IP network connected to the datastore. This table also contains a reference to the ESXi host.|

**Parent Topic:**[Discovery for VMware virtualization](c_DiscoverVMwareInfrastructure.md)

**Related topics**  


[Discovery for VMware vCenter](c_DiscoveryForVMwareVCenter.md)

[ESXi server discovery](../reference/r_DiscoverESXServers.md)

[Standalone ESXi discovery](../reference/StandaloneESXiDiscovery.md)

[Discovery for VMware virtual machines](c_VMwareVirtualMachines.md)

[VM instance state and status fields](../reference/vm-instance-state-and-status-fields.md)

