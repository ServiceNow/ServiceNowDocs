---
title: Microsoft Azure Linux Out Of Box Catalog items
description: Cloud Services Catalog Linux VM with agent client collector \(ACC\), up to 10 additional disks, security groups or with scalable web servers or with security groups.
locale: en-US
release: xanadu
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Microsoft Azure Linux Out Of Box Catalog items

Cloud Services Catalog Linux VM with agent client collector \(ACC\), up to 10 additional disks, security groups or with scalable web servers or with security groups.

This is a fully functional sample catalog item that can be used to request a Linux instance of any instance type from Microsoft Azure.

<table id="simpletable_jff_kzy_nxb"><thead><tr><th>

Order

</th><th>

Features

</th></tr></thead><tbody><tr><td>

Order a Linux virtual machine on Microsoft Azure, that allows installation of agent client collector. ACC is compulsory for production instances. VM sizes other than Standard\_A1\_v2 and Standard\_A2\_v2 require approval. Cloud configuration scan is run for compliance checking.

</td><td>

For instance types other than Standard\_A1\_v2 and Standard\_A2\_v2, approval is needed from administrator by policy. The catalog item has built in client rules to drive a ACC \(Agent Client Collector\) installation, when the deployment environment is marked for production.

 To select the credential alias key for ACC deployment from mid, the appropriate ACC admin role permissions are required to be bestowed to the user.

 The work-flow automation runs a CCG scan on the deployed Linux instance, and checks the policy rule with the configuration of the VM. If there is any violation, the stack will be set with 'Follow up required' state to notify that the stack deployment is not as per norms.

</td></tr><tr><td>

Order a Linux virtual machine and specify up to 10 additional disks. For up to two disks, no approval is necessary. Seek approval for anything beyond that.

</td><td>

This catalog item form allows ordering up to 10 additional disks \(volumes\) attached to the VM of varying sizes and types. If more than two additional disks are added to the request, seek approval from administrator, by policy.

</td></tr><tr><td>

Order a secure Linux virtual machine, assign security groups. Select as many you require, for the highest level of security.

</td><td>

This catalog item form allows capability to assign one or more security groups \(firewall-port rules\) to the compute instance so that the network access to the VM is restricted. Security groups are listed for the selected VPC and subnets.

</td></tr><tr><td>

Order a Linux virtual machine scale set to deploy identical virtual machines, enabling automated scaling and ensuring high availability.

</td><td>

This catalog item provides the capability to deploy identical virtual machines using a Linux virtual machine scale set, which supports automated scaling for enhanced availability. Email URL is added as a post provision operation which emails the deployed application's end point URL to the requester.

</td></tr></tbody>
</table>**Note:**

Tag \(key-value\) is assigned to all deployed resources. Example: VM, network, storage as present in the stack.

The key-value is updated only in the cmdb\_key\_value table, not in public cloud at this time. This will be fixed in future releases to update the tags in cloud.

**Parent Topic:**[Out Of Box Catalogs using Cloud Services Catalog](../concept/out-of-the-box-catalog-items.md)

