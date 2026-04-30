---
title: Microsoft Azure Windows Out Of Box Catalog items
description: Cloud Services Catalog Windows VM, up to 10 additional disks on Microsoft Azure or with security groups.
locale: en-US
release: yokohama
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Microsoft Azure Windows Out Of Box Catalog items

Cloud Services Catalog Windows VM, up to 10 additional disks on Microsoft Azure or with security groups.

This is a fully functional sample catalog item that can be used to request a Windows instance of any instance type from Microsoft Azure.

<table id="simpletable_jff_kzy_nxb"><thead><tr><th>

Order

</th><th>

Features

</th></tr></thead><tbody><tr><td>

Order a Microsoft Windows VM that allows installation of agent client collector. VM sizes other than Standard\_A1\_v2 and Standard\_A2\_v2 require approval. Cloud configuration scan is run for compliance checking.

</td><td>

For instance types other than Standard\_A1\_v2 and Standard\_A2\_v2, approval is needed from administrator, by policy. The work-flow automation runs a CCG scan on the deployed Linux instance, and checks the policy rule with the configuration of the VM.

</td></tr><tr><td>

Order a Windows virtual machine on Microsoft Azure and specify up to 10 additional disks. For up to two disks, no approval is necessary, but for anything beyond that, approval will be required.

</td><td>

This catalog item form allows ordering up to 10 additional disks \(volumes\) attached to the VM of varying sizes and types. If more than two additional disks are added to the request, seek approval from administrator, by policy.

 The Windows admin password is obtained from Microsoft Azure at the time of creation.

</td></tr><tr><td>

Order a secure Windows virtual machine on Microsoft Azure, assign security groups. Select as many required for the highest level of security.

</td><td>

This catalog item form allows capability to assign one or more security groups \(firewall-port rules\) to the compute instance so that the network access to the VM is restricted. Security groups are listed for the selected VPC and subnets.

</td></tr></tbody>
</table>**Note:**

Tag \(key-value\) is assigned to all deployed resources. Example: VM, network, storage as present in the stack. The key-value is updated only in the cmdb\_key\_value table, not in public cloud, at this time. This will be fixed in future releases to update the tags in cloud.

**Parent Topic:**[Out Of Box Catalogs using Cloud Services Catalog](../concept/out-of-the-box-catalog-items.md)

