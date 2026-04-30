---
title: CSC GCP Windows OOB permissions
description: Google Cloud Platform Windows Out Of Box permissions
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Google Cloud Platform Windows Out Of Box Catalog items, Out of Box, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# CSC GCP Windows OOB permissions

Google Cloud Platform Windows Out Of Box permissions

<table id="table_ug3_wqz_dbc"><thead><tr><th>

Catalog item

</th><th>

Services

</th><th>

Permission

</th></tr></thead><tbody><tr><td rowspan="7">

CSC GCP Windows VM

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

 **Note:** Day 2 disk permissions are also required. These are same as Windows mutiple disks.

</td></tr><tr><td rowspan="6">

CSC GCP Windows Multiple Disks

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

 **Note:** Day 2 VM permissions are also required. These are same as basic Windows VM.

</td></tr><tr><td>

CSC GCP Windows Secure Deployment

</td><td>

Stack Deprovision

</td><td>

-   compute.firewalls.delete
-   compute.networks.updatePolicy
-   compute.instances.delete
-   compute.disks.delete

 **Note:** Day 2 VM disk permissions are also required.

</td></tr></tbody>
</table>**Parent Topic:**[Google Cloud Platform Windows Out Of Box Catalog items](google-cloud-platform-windows-out-of-box-catalog-items.md)

