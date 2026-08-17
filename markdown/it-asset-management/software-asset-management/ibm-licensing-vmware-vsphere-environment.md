---
title: IBM licensing in VMware vSphere and Nutanix environments
description: When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, the Software Asset Management application supports IBM licensing rules for VMware vSphere and Nutanix.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/it-asset-management/software-asset-management/ibm-licensing-vmware-vsphere-environment.html
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Virtualization technologies and cloud platforms supported by ASP integrations, CVA integrations, Software Asset Management publisher pack for IBM, Supported software publisher licenses, Software Asset Management, IT Asset Management, Asset Management]
---

# IBM licensing in VMware vSphere and Nutanix environments

When you integrate the Software Asset Management publisher pack for IBM with Software Asset Management providers that are authorized to participate in the IBM Client Value Acceleration \(CVA\) Program, the Software Asset Management application supports IBM licensing rules for VMware vSphereand Nutanix.

VMware vSphere and Nutanix are virtualization platforms through which you can install and run IBM software products on virtual machines \(VMs\). The Software Asset Management application supports both full capacity and sub-capacity processor value unit \(PVU\), resource value unit \(RVU\), and virtual processor core \(VPC\) licensing for IBM software products in VMware vSphere and Nutanix environments.

When you run a discovery on a VMware vSphere or Nutanix AHV environment, the discovered data is populated and stored in Configuration Management Database \(CMDB\) tables on your ServiceNow instance.

For a Nutanix AHV environment, data is stored in the following tables. For more information on the Nutanix discovery pattern, see [Nutanix Acropolis discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/nutanix-pattern.md).

-   cmdb\_ci\_nutanix\_vm\_instance
-   cmdb\_ci\_nutanix\_cluster
-   cmdb\_ci\_nutanix\_host

To populate and store the Nutanix AHV data, request and install the CMDB CI Class Models application from the ServiceNow Store. This application adds or updates the CMDB classes required for the Nutanix AHV platform. For more information, see [Nutanix extension classes](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/servicenow-platform/cmdb-ci-class-models-nutanix.md).

For a VMware vSphere environment, data is stored in the following tables. For more information on the VMware vSphere discovery, see [Data collected for VMware Cloud Discovery](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-operations-management/data-collected-vmware-cloud-disco.md).

-   cmdb\_ci\_vcenter\_datacenter
-   cmdb\_ci\_vcenter\_cluster
-   cmdb\_ci\_esx\_server
-   cmdb\_ci\_vmware\_instance

<table id="table_ufn_22l_wwb"><thead><tr><th>

Licensing capacity

</th><th>

Licensing model

</th></tr></thead><tbody><tr><td>

Full capacity

</td><td>

When you install and run an IBM software product on a VM, you must license each processor core on the underlying physical ESXi host that is running the VM. If the physical ESXi host is running multiple VMs simultaneously, you must still license each processor core on the host regardless of how many VMs you install and run the IBM software product on.

 Use the total number of processor cores on the underlying physical ESXi host to determine the number of rights that are required for your license, based on the license type. To determine the number of rights that are required for a PVU or RVU license, see [IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/ibm-pvu-rvu-licensing.md). To determine the number of rights that are required for a VPC license, see [IBM virtual processor core \(VPC\) licenses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/ibm-virtual-processor-core-licensing.md).

</td></tr><tr><td>

Sub-capacity**Note:** You can use sub-capacity licensing only if you configure and specify a VM manager for your VMs. For more information on VM managers, see [Specify VMMs for IBM licenses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/specify-vm-managers-anglepoint-integration.md).

</td><td>

You must license only the virtual cores that are assigned to the VMs on which you install and run an IBM software product.

 Use the sum of virtual cores that must be licensed across your VMs to determine the number of rights that are required for your license, based on the license type. To determine the number of rights that are required for a PVU or RVU license, see [IBM processor value unit \(PVU\) and resource value unit \(RVU\) licenses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/ibm-pvu-rvu-licensing.md). To determine the number of rights that are required for a VPC license, see [IBM virtual processor core \(VPC\) licenses](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/ibm-virtual-processor-core-licensing.md).

 **Note:** By default, the number of required rights is calculated using the sum of virtual cores. If the sum of virtual cores exceeds the total number of processor cores on the underlying physical ESXi hosts that are running the VMs, the number of required rights is calculated using the total number of processor cores on the hosts instead.

 **Note:** If you install and run an IBM software product on both a VM and the underlying physical ESXi host that is running the VM, you must also license the installation on the host.

</td></tr></tbody>
</table>**Parent Topic:**[Virtualization technologies and public cloud platforms supported by IBM Authorized SAM Provider \(ASP\) integrations](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/it-asset-management/software-asset-management/supported-virtualization-technologies-iasp-integrations.md)

