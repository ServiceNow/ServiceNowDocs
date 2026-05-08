---
title: Google Cloud Platform Windows Out Of Box Catalog items
description: Cloud Services Catalog Windows VM, up to 10 additional disks on Google Cloud Platform or with cloud firewall.
locale: en-US
release: australia
product: Cloud Services Catalog
classification: cloud-services-catalog
topic_type: reference
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Out Of Box Catalogs using Cloud Services Catalog, Cloud Services Catalog, ITOM Cloud Accelerate, IT Operations Management]
---

# Google Cloud Platform Windows Out Of Box Catalog items

Cloud Services Catalog Windows VM, up to 10 additional disks on Google Cloud Platform or with cloud firewall.

This is a fully functional sample catalog item that can be used to request a Windows instance of any type from Google Cloud Platform.

Linux VM orders and features:

<table id="simpletable_jff_kzy_nxb"><thead><tr><th>

Order

</th><th>

Features

</th></tr></thead><tbody><tr><td>

CSC GCP Windows VM: Order a Windows Virtual machine that allows installation of Agent Client Collector. VM sizes other than e2-micro and e2-small require approval.

</td><td>

This is a fully functional sample catalog item that can be used to request a Windows instance of any instance type from Google Cloud Provider. For instance types other than e2-micro and e2-small, approval is needed from administrator, by policy.

 The Windows credentials are provided by the user in catalog order form. The credentials to meet complexity requirement based on windows version.

 The workflow automation runs a CCG scan on the deployed Windows instance, and checks the policy rule with the configuration of the VM. If there is any violation, the stack will be set with 'Follow up needed' state to notify that the stack deployment is not as per norms.

</td></tr><tr><td>

CSC GCP Windows multiple disks: Order a Windows virtual machine and specify up to 10 additional disk. No approval is necessary for up to two disks, but for anything beyond that, approval will be required.

</td><td>

This is a fully functional sample catalog item that can be used to request a Windows instance of any instance type from Google Cloud Provider. This catalog item form allows ordering up to 10 additional disks \(volumes\) attached to the VM of varying sizes and types. If more than two additional disks are added to the request, approval is needed from administrator, by policy.

 The Windows credentials are provided by the user in catalog order form. The credentials to meet complexity requirement based on windows version.

</td></tr><tr><td>

CSC GCP Windows Cloud Firewall: Order a secure Windows virtual machine with enhanced security to allow or deny traffic to and from your VM instances based on your specified configuration for highest level of security.

</td><td>

This is a fully functional sample catalog item that can be used to request a Windows instance of any instance type from Google Cloud Provider. This catalog item form allows capability to assign one or more security groups \(firewall-port rules\) to the compute instance so that the network access to the VM is restricted. Security groups are listed for the selected VPC and subnets.

 The Windows credentials are provided by the user in catalog order form. The credentials to meet complexity requirement based on windows version.

</td></tr></tbody>
</table>**Note:**

Tag \(key-value\) is assigned to all deployed resources. Example: VM, network, storage as present in the stack.

The key-value is updated only in the cmdb\_key\_value table, not in public cloud at this time. This will be fixed in future releases to update the tags in cloud.

-   **[CSC GCP Windows OOB permissions](gcp-windows-oob-permissions.md)**  
Google Cloud Platform Windows Out Of Box permissions

**Parent Topic:**[Out Of Box Catalogs using Cloud Services Catalog](../concept/out-of-the-box-catalog-items.md)

