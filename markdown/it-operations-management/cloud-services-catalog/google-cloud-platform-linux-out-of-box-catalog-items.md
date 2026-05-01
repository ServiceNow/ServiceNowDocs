---
title: Google Cloud Platform Linux Out Of Box Catalog items
description: Cloud Services Catalog Linux VM with Agent Client Collector \(ACC\), up to 10 additional disks or secure Linux deployment.
locale: en-US
release: zurich
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2026-05-01"
reading_time_minutes: 2
breadcrumb: [Out of Box, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Google Cloud Platform Linux Out Of Box Catalog items

Cloud Services Catalog Linux VM with Agent Client Collector \(ACC\), up to 10 additional disks or secure Linux deployment.

This is a fully functional sample catalog item that can be used to request a Linux instance of any instance type from Google Cloud Platform.

Linux VM orders and features:

<table id="simpletable_jff_kzy_nxb"><thead><tr><th>

Order

</th><th>

Features

</th></tr></thead><tbody><tr><td>

CSC GCP Linux VM: Order a Linux Virtual machine that allows installation of Agent Client Collector. ACC is compulsory for production instances. VM sizes other than e2-micro and e2-small require approval.

</td><td>

This is a fully functional sample catalog item that can be used to request a Linux instance of any instance type from Google Cloud Provider. For instance types other than e2-micro and e2-small, approval is needed from administrator, by policy.

 The catalog item has built-in client rules to drive an ACC \(Agent Client Collector\) installation, when the deployment environment is marked for production. To select the credential alias key for ACC deployment from mid, the appropriate ACC admin role permissions must be provided to the user.

</td></tr><tr><td>

CSC GCP Linux multiple disks: Order a Linux virtual machine and specify up to 10 additional disk. No approval is necessary for up to two disks, but for anything beyond that, approval will be required.

</td><td>

This catalog item form allows ordering up to 10 additional disks \(volumes\) attached to the VM of varying sizes and types. If more than two additional disks are added to the request, seek approval from administrator, by policy.

</td></tr><tr><td>

CSC GCP Linux Cloud Firewall: Order a secure Linux virtual machine with enhanced security to allow or deny traffic to and from your VM instances based on your specified configuration for highest level of security.

</td><td>

This is a fully functional sample catalog item that can be used to request a Linux instance of any instance type from Google Cloud Provider. This catalog item form allows capability to assign one or more security groups \(firewall-port rules\) to the compute instance so that the network access to the VM is restricted. Security groups are listed for the selected VPC and subnets.

</td></tr></tbody>
</table>**Note:**

Tag \(key-value\) is assigned to all deployed resources. Example: VM, network, storage as present in the stack.

The key-value is updated only in the cmdb\_key\_value table, not in public cloud at this time. This will be fixed in future releases to update the tags in cloud.

-   **[Google Cloud Platform Linux Out Of Box permissions](gcp-linux-oob-permissions.md)**  
Google Cloud Platform Linux Out Of Box catalog items permissions

**Parent Topic:**[Out Of Box Catalogs using Cloud Services Catalog](../concept/out-of-the-box-catalog-items.md)

