---
title: Software Asset Management publisher pack for VMware
description: Use the Software Asset Management publisher pack for VMware to track and optimize licensing for your VMware software products.
locale: en-US
release: australia
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Supported software publisher licenses, Software Asset Management, IT Asset Management]
---

# Software Asset Management publisher pack for VMware

Use the Software Asset Management publisher pack for VMware to track and optimize licensing for your VMware software products.

To use the VMware publisher pack, activate the Software Asset Management Professional for VMware \(com.sn\_samp\_vmware\) [plugin](../task/t_RequSoftwareAssetMgmt.md).

VMware offers virtualization and cloud computing technologies that enable you to run software products and applications on virtual machines \(VMs\). The main component of VMware virtualization is the VMware hypervisor, which is a virtual machine monitor \(VMM\) that allows you to create and run VMs on your physical hosts. You can use either a Type 1 \(bare metal\) or Type 2 \(hosted\) hypervisor. A Type 1 hypervisor runs directly on the hardware of the underlying physical host, while a Type 2 hypervisor runs as a software layer on the operating system \(OS\) of the underlying physical host.

You can collect and identify data for your VMware software installations by using a discovery tool, such as the ServiceNow® Discovery application. For more information on the discovery process, see [Data collected by ITOM Visibility](https://www.servicenow.com/docs/access?context=data-collected-by-itom-visibility&version=australia&pubname=australia-it-operations-management&ft:locale=en-US).

View your VMware license compliance position in the License usage view of the Software Asset Workspace. If any of your VMware software products are out of compliance, the License usage view provides corresponding remediation suggestions. For more information, see [License usage view](sam-workspace-workbench.md).

View compliance analysis results for VMware in either the Software Publisher Analytics dashboard for VMware \(Software Asset Management classic application\) or the publisher overview for VMware, Inc. \(Software Asset Workspace\). For more information on the Software Publisher Analytics dashboard for VMware, see [Software Publisher Analytics dashboard for VMware in Software Asset Management classic](../reference/dashboard-vmware.md). For more information on the publisher overview for VMware, Inc., see [Publisher overview for VMware, Inc. in the Software Asset Workspace](../reference/publisher-overview-vmware.md).

## VMware licensing

The VMware publisher pack supports licensing for both subscription-based VMware vSphere software suites and individual perpetual-based VMware software products.

-   **Licensing for VMware vSphere software suites**

    The VMware publisher pack supports licensing for both VMware vSphere Standard \(VVS\) and VMware vSphere Essentials Plus \(VVEP\), which are suite-based product offerings for VMware vSphere. VVS includes VMware vSphere Standard and VMware vCenter Standard. VVEP includes VMware vSphere Essentials Plus and VMware vCenter Essentials. Both software suites are available through the subscription licensing model.

    You can calculate licensing requirements for VVS and VVEP by using the Per Core license metric. With this license metric, you must license the processor cores on the underlying physical hosts of the VMs that are running VMware vSphere Standard or VMware vSphere Essentials Plus. Each core requires one right, and you must license a minimum of 16 cores per processor. If you're using VVEP, each license can be used on a maximum of three physical hosts with up to two processors each, and each processor can have a maximum of 32 cores. Any additional cores remain unlicensed.

    **Note:** vCenters are inferred as suite components of VVS and VVEP. They therefore don't require or consume any rights.

    For example, you have purchased a subscription to VVS. You have deployed VMware vSphere Standard on ESXHost1, which has two processors with 20 cores each, and on ESXHost2, which has two processors with eight cores each. You can determine your licensing requirements based on the following calculations:

    |Host|Product|Number of processors|Number of cores per processor|Number of required rights|
    |----|-------|--------------------|-----------------------------|-------------------------|
    |ESXHost1|VMware vSphere Standard|2|20|2 processors x 20 cores = 40 rights|
    |ESXHost2|VMware vSphere Standard|2|8|2 processors x 16 cores \(minimum\) = 32 rights|

    In this example, you must have a total of 72 rights \(40 rights for ESXHost1 + 32 rights for ESXHost2\).

-   **Licensing for individual VMware software products**

    The VMware publisher pack supports licensing for individual VMware software products. These products are available through the perpetual licensing model using license keys, which are the unique serial numbers that unlock and activate the features and capabilities of each product.

    **Important:** As of December 11, 2023, VMware no longer offers new perpetual licenses for individual VMware software products. All VMware software products are now available through subscription-based software suites. If you still have any existing perpetual licenses, you can continue to manage them through the VMware publisher pack.


You can calculate licensing requirements for these software products by using the following license metrics:

-   Per Application Instance: You must license the instances of an application. Each instance requires one right.
-   Per Device: You must license the underlying physical hosts on which you access the software product. Each host requires one right.
-   Per Named User: You must license the named users that access the software product. Each named user requires one right.
-   Per OSI: You must license the underlying physical and virtual servers on which you access the software product. Each server requires one right.
-   Per Processor: You must license the processors on the underlying physical hosts. Each processor requires one right for every 32 cores.

-   **[Software Publisher Analytics dashboard for VMware in Software Asset Management classic](../reference/dashboard-vmware.md)**  
View compliance analysis results related to VMware on the Software Publisher Analytics dashboard in the Software Asset Management classic application.
-   **[Publisher overview for VMware, Inc. in the Software Asset Workspace](../reference/publisher-overview-vmware.md)**  
View license usage information related to VMware in the publisher overview for VMware, Inc. in the Software Asset Workspace.

**Parent Topic:**[Supported software publisher licenses](sam-publisher-packs.md)

