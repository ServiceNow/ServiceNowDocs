---
title: Microsoft Server licensing on Microsoft Hyper-V virtualization technology
description: The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft Server products, such as Microsoft Windows Server, that are deployed on Microsoft Hyper-V virtualization technology.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Software Asset Management publisher pack for Microsoft, Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Microsoft Server licensing on Microsoft Hyper-V virtualization technology

The Software Asset Management publisher pack for Microsoft supports licensing rules for Microsoft Server products, such as Microsoft Windows Server, that are deployed on Microsoft Hyper-V virtualization technology.

Hyper-V is a Microsoft hypervisor that enables you to create, manage, and run virtual machines \(VMs\) on a physical host, such as a server or computer. With this hardware virtualization capability, you can run multiple VMs on a single physical host while allowing them to share the underlying hardware resources of that host, such as the CPU, memory, storage, and networking. For more information on Hyper-V, see [Hyper-V technology overview](https://learn.microsoft.com/en-us/windows-server/virtualization/hyper-v/hyper-v-overview?pivots=windows-server).

You can use a discovery tool, such as the ServiceNow® Discovery application, to automatically locate and identify the Hyper-V hypervisors and VMs in your environment, as well as the Microsoft Server products that are running on those VMs. For more information on this discovery process and the associated data models, see Hyper-V discovery.

You can license the Microsoft Server products, such as Microsoft SQL Server and Microsoft Windows Server, that are running in your Hyper-V virtualized environments by using licensing rules from Microsoft. If you are licensing Microsoft Windows Server at the physical layer, the **Licenses required** field in the License Metrics Results of the Microsoft publisher overview populates only for your parent Microsoft server, which represents your physical host. This licensing calculation is more intuitive and aligned with your discovered data. For more information on Microsoft server licensing, see [Microsoft Per Core licensing rules](microsoft-sw-license-metrics.md) and [Microsoft Per Core \(with CAL\) licensing rules](microsoft-percore-withcal.md). For more information on the Microsoft publisher overview, see [Publisher overview for Microsoft in the Software Asset Workspace](../reference/publisher-overview-microsoft.md).

The Microsoft publisher pack also supports cost-based licensing optimizations that are specific to Microsoft Server products deployed on Hyper-V. For more information on these licensing optimizations, see [Cost-based licensing optimization for Microsoft](cost-based-microsoft-cluster-licensing.md).

**Parent Topic:**[Software Asset Management publisher pack for Microsoft](microsoft-publisher-pack.md)

