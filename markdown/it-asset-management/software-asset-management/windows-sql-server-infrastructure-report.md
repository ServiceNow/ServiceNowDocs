---
title: Windows and SQL Server Infrastructure report
description: You can use the Windows and SQL Server Infrastructure report to gain visibility into the infrastructure details for all physical hosts and virtual machines \(VMs\) that are running Microsoft Windows Server or Microsoft SQL Server across your on-premise and public cloud environments, such as AWS and Microsoft Azure.
locale: en-US
release: yokohama
product: Software Asset Management
classification: software-asset-management
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 3
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Windows and SQL Server Infrastructure report

You can use the Windows and SQL Server Infrastructure report to gain visibility into the infrastructure details for all physical hosts and virtual machines \(VMs\) that are running Microsoft Windows Server or Microsoft SQL Server across your on-premise and public cloud environments, such as AWS and Microsoft Azure.

The Windows and SQL Server Infrastructure report is available in both the Software Asset Workspace and the Software Asset Management classic application.

To view this report in the Software Asset Workspace, navigate to **Workspaces** &gt; **Software Asset Workspace**. From the Software Asset Workspace, navigate to **License usage** &gt; **Reports** &gt; **Windows and SQL Server Infrastructure**.

To view this report in the Software Asset Management classic application, navigate to **All** &gt; **Reports** &gt; **View/Run**. From the list of available reports, search for and select **Windows and SQL Server infrastructure details report**. When the corresponding Edit report page opens, select **Run**.

<table id="table_wtb_xwl_gtb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Deployment type

</td><td>

Type of deployment that the physical host or VM is running in. The options are **On premise** and **Cloud**.

</td></tr><tr><td>

Cloud provider

</td><td>

Cloud provider that Microsoft Windows Server or Microsoft SQL Server is deployed on. The options are **AWS** and **Microsoft Azure**.**Note:** This field is applicable for cloud deployments only.

</td></tr><tr><td>

vCenter

</td><td>

VMware vCenter Server that you are using to manage the physical host or VM in a virtual VMware vSphere environment.**Note:** This field is applicable only if you are using VMware virtualization technology.

</td></tr><tr><td>

Cluster

</td><td>

Cluster that the physical host or VM resides in.

</td></tr><tr><td>

Host

</td><td>

For physical hosts, this field identifies the host that Microsoft Windows Server or Microsoft SQL Server is installed on.For VMs, this field identifies the physical host that the VM is running on.

</td></tr><tr><td>

Host processor count

</td><td>

Number of CPUs that are assigned to the physical host.

</td></tr><tr><td>

Host core count

</td><td>

Number of cores within each CPU that is assigned to the physical host.

</td></tr><tr><td>

Virtualization technology

</td><td>

Virtualization technology that you are using to deploy and manage your physical hosts and VMs.

</td></tr><tr><td>

Virtual server

</td><td>

VM on which you are running Microsoft Windows Server or Microsoft SQL Server.**Note:** If a VM resides in an on-premise cluster, it can migrate to any physical host within that cluster. Additionally, if you are using VM-Host affinity rules to specify the physical hosts on which a VM can run, the VM can migrate to any physical host that is specified in those rules. In these scenarios, the same VM can appear on the Windows and SQL Server Infrastructure report multiple times based on the physical hosts to which it can migrate.

 **Note:** This field is applicable for VMs only.

</td></tr><tr><td>

Windows Server installation

</td><td>

Microsoft Windows Server version that is installed on the physical host or VM.If multiple Microsoft Windows Server versions are installed on the same host or VM, this field displays all installed versions using a comma-separated list.

</td></tr><tr><td>

SQL Server installation

</td><td>

Microsoft SQL Server version that is installed on the physical host or VM.If multiple Microsoft SQL Server versions are installed on the same host or VM, this field displays all installed versions using a comma-separated list.

</td></tr><tr><td>

VM processor count

</td><td>

Number of virtual CPUs \(vCPUs\) that are assigned to the VM.**Note:** This field is applicable for VMs only.

</td></tr><tr><td>

VM core count

</td><td>

Number of virtual cores within each vCPU that is assigned to the VM.**Note:** This field is applicable for VMs only.

</td></tr><tr><td>

VM CPU thread count

</td><td>

Number of threads that divide each virtual core within the vCPUs that are assigned to the VM.**Note:** This field is applicable for VMs only.

</td></tr><tr><td>

Cloud host type

</td><td>

Type of cloud host that the VM is running on. The options are **Shared** and **Dedicated**.**Note:** This field is applicable for cloud deployments only.

</td></tr><tr><td>

Cloud license type - Windows Server

</td><td>

Cloud license type of the Microsoft Windows Server installation. The options are **BYOL** and **License Included**.**Note:** This field is applicable for cloud deployments only.

</td></tr><tr><td>

Cloud license type - SQL Server

</td><td>

Cloud license type of the Microsoft SQL Server installation. The options are **BYOL** and **License Included**.**Note:** This field is applicable for cloud deployments only.

</td></tr></tbody>
</table>**Parent Topic:**[Software Asset Management publisher pack for Microsoft](../concept/microsoft-publisher-pack.md)

