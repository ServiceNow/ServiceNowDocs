---
title: Amazon Web Services EC2 Linux Out Of Box Catalog items
description: Cloud Services Catalog Linux VM with agent client collector \(ACC\), up to 10 additional disks on EC2 or with security groups.
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Amazon Web Services EC2 Linux Out Of Box Catalog items

Cloud Services Catalog Linux VM with agent client collector \(ACC\), up to 10 additional disks on EC2 or with security groups.

This is a fully functional sample catalog item that can be used to request a Linux instance of any instance type from Amazon EC2.

Order an AWS EC2 Linux VMThe video demonstrates how to order an Amazon Web Services EC2 Linux virtual machine.

Linux VM orders and features:

<table id="simpletable_jff_kzy_nxb"><thead><tr><th>

Order

</th><th>

Features

</th></tr></thead><tbody><tr><td>

Order a Linux virtual machine on EC2, that allows installation of agent client collector. ACC is compulsory for production instances. VM sizes other than t2.nano, t2.micro require approval. Cloud configuration scan is run for compliance checking.

</td><td>

For instance types other than t2.nano and t2.micro, approval is needed from administrator, by policy. The catalog item has built in client rules to drive an ACC \(Agent Client Collector\) installation when the deployment environment is marked for production.

 To select the credential alias key for ACC deployment from mid, the appropriate ACC admin role permissions are required to be bestowed to the user. For prerequisites check “Deploy ACC-\* in post provisioning” below. The work-flow automation runs a CCG scan on the deployed Linux instance and checks the policy rule with the configuration of the VM. If there is any violation, the stack will be set with 'Follow up required' state to notify that the stack deployment is not as per norms.

</td></tr><tr><td>

Order a Linux virtual machine on EC2 and specify up to 10 additional disk. For up to two disks, no approval is necessary. Seek approval for anything beyond that.

</td><td>

This catalog item form allows ordering up to 10 additional disks \(volumes\) attached to the VM of varying sizes and types. If more than two additional disks are added to the request, seek approval from administrator, by policy.

</td></tr><tr><td>

Order a secure Linux virtual machine with enhanced security by assigning a Network Security Group for highest level of security.

</td><td>

This catalog item form allows capability to assign one Network Security Group to the compute instance so that the network access to the VM is restricted. Security groups are listed for the selected VPC and subnets.

</td></tr></tbody>
</table>**Note:**

Tag \(key-value\) is assigned to all deployed resources. Example: VM, network, storage as present in the stack.

The key-value is updated only in the cmdb\_key\_value table, not in public cloud at this time. This will be fixed in future releases to update the tags in cloud.

-   **[Amazon Web Services EC2 Linux Out Of Box permissions](aws-ec2-linux-oob-catalog-items-permissions.md)**  
Amazon Web Services EC2 Linux OOB catalog items permissions

**Parent Topic:**[Out Of Box Catalogs using Cloud Services Catalog](../concept/out-of-the-box-catalog-items.md)

