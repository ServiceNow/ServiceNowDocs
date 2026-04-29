---
title: IBM licensing in VMware vSphere environments
description: When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, the Software Asset Management application supports IBM licensing rules for VMware vSphere.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Virtualization technologies and cloud platforms supported by ASP integrations, Authorized SAM Provider \(ASP\) integrations for IBM, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# IBM licensing in VMware vSphere environments

When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, the Software Asset Management application supports IBM licensing rules for VMware vSphere.

VMware vSphere is a virtualization platform through which you can install and run IBM software products on virtual machines \(VMs\). The Software Asset Management application supports both full capacity and sub-capacity processor value unit \(PVU\), resource value unit \(RVU\), and virtual processor core \(VPC\) licensing for IBM software products in VMware vSphere environments.

<table id="table_ufn_22l_wwb"><thead><tr><th>

Licensing capacity

</th><th>

Licensing model

</th></tr></thead><tbody><tr><td>

Full capacity

</td><td>

When you install and run an IBM software product on a VM, you must license each processor core on the underlying physical ESXi host that is running the VM. If the physical ESXi host is running multiple VMs simultaneously, you must still license each processor core on the host regardless of how many VMs you install and run the IBM software product on.

 Use the total number of processor cores on the underlying physical ESXi host to determine the number of rights that are required for your license, based on the license type. To determine the number of rights that are required for a PVU or RVU license, see [IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses](ibm-pvu-rvu-licensing.md). To determine the number of rights that are required for a VPC license, see [IBM virtual processor core \(VPC\) licenses](ibm-virtual-processor-core-licensing.md).

</td></tr><tr><td>

Sub-capacity**Note:** You can use sub-capacity licensing only if you configure and specify a VM manager for your VMs. For more information on VM managers, see [Specify the virtual machine managers \(VMMs\) for which you are tracking IBM licenses](../task/specify-vm-managers-anglepoint-integration.md).

</td><td>

You must license only the virtual cores that are assigned to the VMs on which you install and run an IBM software product.

 Use the sum of virtual cores that must be licensed across your VMs to determine the number of rights that are required for your license, based on the license type. To determine the number of rights that are required for a PVU or RVU license, see [IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses](ibm-pvu-rvu-licensing.md). To determine the number of rights that are required for a VPC license, see [IBM virtual processor core \(VPC\) licenses](ibm-virtual-processor-core-licensing.md).

 **Note:** By default, the number of required rights is calculated using the sum of virtual cores. If the sum of virtual cores exceeds the total number of processor cores on the underlying physical ESXi hosts that are running the VMs, the number of required rights is calculated using the total number of processor cores on the hosts instead.

 **Note:** If you install and run an IBM software product on both a VM and the underlying physical ESXi host that is running the VM, you must also license the installation on the host.

</td></tr></tbody>
</table>**Parent Topic:**[Virtualization technologies and public cloud platforms supported by IBM Authorized SAM Provider \(ASP\) integrations](supported-virtualization-technologies-iasp-integrations.md)

