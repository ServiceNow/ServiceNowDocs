---
title: Google Cloud Platform Linux Out Of Box permissions
description: Google Cloud Platform Linux Out Of Box catalog items permissions
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Google Cloud Platform Linux Out Of Box Catalog items, Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Google Cloud Platform Linux Out Of Box permissions

Google Cloud Platform Linux Out Of Box catalog items permissions

<table id="table_ug3_wqz_dbc"><thead><tr><th>

Catalog item

</th><th>

Services

</th><th>

Permission

</th></tr></thead><tbody><tr><td rowspan="7">

CSC GCP Linux VM

</td><td>

Provision

</td><td>

-   compute.disks.create
-   compute.disks.get
-   compute.instances.create
-   compute.instances.get
-   compute.instances.setMetadata
-   compute.networks.get
-   compute.subnetworks.get
-   compute.subnetworks.use
-   compute.subnetworks.useExternalIp
-   compute.zones.get

</td></tr><tr><td>

Pointed discovery

</td><td>

-   compute.disks.list
-   compute.images.list
-   compute.instanceTemplates.list
-   compute.instances.list
-   compute.machineTypes.list
-   compute.snapshots.list
-   compute.zones.list
-   compute.regions.list

</td></tr><tr><td>

Day 2 VM: Virtual Server - StopNode

</td><td>

-   compute.instances.stop
-   compute.regions.get
-   compute.machineTypes.get

</td></tr><tr><td>

Virtual Server - StartNode

</td><td>

compute.instances.start

</td></tr><tr><td>

Virtual Server - Resize

</td><td>

-   compute.instances.stop
-   compute.machineTypes.get
-   compute.regions.get
-   compute.instances.setMachineType
-   compute.instances.start

</td></tr><tr><td>

Virtual Server - Deprovison

</td><td>

-   compute.instances.delete
-   compute.regions.get

</td></tr><tr><td>

Stack Deprovision

</td><td>

-   compute.instances.delete
-   compute.disks.delete

 **Note:** Day 2 disk permissions are also required. These are same as Linux mutiple disks.

</td></tr><tr><td rowspan="6">

CSC GCP Linux Multiple Disks

</td><td>

Provision

</td><td>

-   compute.disks.create
-   compute.disks.get
-   compute.disks.use
-   compute.instances.create
-   compute.instances.get
-   compute.instances.setMetadata
-   compute.networks.get
-   compute.subnetworks.get
-   compute.subnetworks.use
-   compute.subnetworks.useExternalIp
-   compute.zones.get
-   compute.zoneOperations.get

</td></tr><tr><td>

Pointed discovery

</td><td>

-   compute.disks.list
-   compute.images.list
-   compute.instanceTemplates.list
-   compute.instances.list
-   compute.machineTypes.list
-   compute.snapshots.list
-   compute.zones.list
-   compute.regions.list

</td></tr><tr><td>

Day 2 Disk storage Storage -Detach

</td><td>

compute.instances.detachDisk

</td></tr><tr><td>

Storage Deprovision

</td><td>

compute.disks.delete

</td></tr><tr><td>

Storage Attach disk

</td><td>

compute.instances.attachDisk

</td></tr><tr><td>

Stack Deprovision

</td><td>

-   compute.instances.delete
-   compute.disks.delete

 **Note:** Day 2 VM permissions are also required. These are same as basic Linux VM.

</td></tr><tr><td rowspan="3">

CSC GCP Linux Secure Deployment

</td><td>

Provision

</td><td>

-   compute.disks.create
-   compute.disks.get
-   compute.instances.create
-   compute.instances.get
-   compute.instances.setMetadata
-   compute.instances.setTags
-   compute.firewalls.create
-   compute.firewalls.get
-   compute.networks.get
-   compute.networks.updatePolicy
-   compute.subnetworks.get
-   compute.subnetworks.use
-   compute.subnetworks.useExternalIp
-   compute.zones.get

</td></tr><tr><td>

Pointed discovery

</td><td>

-   compute.disks.list
-   compute.images.list
-   compute.instanceTemplates.list
-   compute.instances.list
-   compute.machineTypes.list
-   compute.snapshots.list
-   compute.zones.list
-   compute.regions.list
-   compute.networks.list
-   compute.firewalls.list

</td></tr><tr><td>

Stack Deprovision

</td><td>

-   compute.firewalls.delete
-   compute.networks.updatePolicy
-   compute.instances.delete
-   compute.disks.delete

 **Note:** Day 2 VM disk permissions are also required.

</td></tr></tbody>
</table>**Parent Topic:**[Google Cloud Platform Linux Out Of Box Catalog items](google-cloud-platform-linux-out-of-box-catalog-items.md)

