---
title: Software license maintenance
description: Get visibility into your software maintenance entitlements to effectively manage these licenses throughout their life cycle.
locale: en-US
release: zurich
product: Software Asset Management
classification: software-asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 7
breadcrumb: [Explore, Software Asset Management, IT Asset Management]
---

# Software license maintenance

Get visibility into your software maintenance entitlements to effectively manage these licenses throughout their life cycle.

Manage and optimize your software maintenance spend by:

-   Importing, updating, and creating maintenance entitlements that specify a start and end date.
-   Getting accurate true-up costs.
-   Maximizing your resources by getting to know your potential savings.
-   Being aware of expiring, unused, and under-used maintenance entitlements.

## Determining expiring maintenance entitlements

ServiceNow Software Asset Management Professional helps you keep a track of all expiring maintenance entitlements using the Software Asset Workspace. You can track your entitlements by navigating to **All** &gt; **Software Asset** &gt; **Software Asset Workspace** &gt; **Expiring maintenance and subscriptions**. This tracking ability enables SAM managers to get an overall view of all their expiring maintenance entitlements and take required action.

## Maintenance for Microsoft

Microsoft Software Assurance \(SA\) is the maintenance program that Microsoft uses to provide active maintenance to its users.

Microsoft provides several benefits such as access to the latest software version and releases, cloud special rights, license mobility and many more. For more information on these benefits, see Microsoft [documentation](https://www.microsoft.com/en-us/licensing/licensing-programs/software-assurance-by-benefits).

ServiceNow Software Asset Management Professional leverages these benefits while licensing Microsoft products in the following ways:

-   New version rights: With access to the latest version of a Microsoft product, SA users can upgrade their product licenses at zero additional cost. Also, there’s no need for tracking or reassigning covered licenses based only on the software version. Software Asset Management Professional adds version support using the following mechanisms:
    -   Automatic application of new version: If a software entitlement with active SA is associated with a newer version software model, Software Asset Management Professional automatically upgrades the entitlement and associates it with the latest version software model. Also, these changes are saved on the Upgrade History related list. For more information on software models and versions, see [Software model fields](../reference/software-model-fields.md).
    -   Management of software entitlement: Microsoft supplies publisher part number \(PPN\) with SA coverage without any version assigned for the product. Thus, there's a risk of incorrect assignment of SA benefits to all versions of Microsoft products. ServiceNow Software Asset Management Professional determines the latest software version released by Microsoft on or before the expiry date of the SA coverage, selects the software model with the correct version, and associates the entitlement to the same. Also, these changes are saved on the Upgrade History Entitlement section.
-   License mobility benefits: License Mobility provides the flexibility to manage licensing on premise \(in high-density virtualized environments\), or on cloud environments \(AWS or Azure\) using Azure Hybrid Benefits \(AHB\). For more information on license mobility, see Microsoft [documentation](https://download.microsoft.com/download/7/9/b/79bd917e-760b-48b6-a266-796b3e47c47a/License-Mobility-through-Software-Assurance-Customer-Licensing-Guide.pdf).

    Software Asset Management Professional automatically applies the license mobility benefits while licensing deployments of your datacenter products such as Windows Server and SQL Server. The following are some of the benefits that are applied automatically:

    -   Provides options to license by virtual machine \(VM\) layer: With subscription licenses or licenses with SA, SQL Server 2022 can be licensed by the VM and licenses can move with the VM at any time to another server in the same server farm.
    -   Supports unlimited virtualization: Enables you to run any number of instances of SQL Server Enterprise Edition software in an unlimited number of VMs if the hosts are completely licensed. This feature is applicable only for the core licensing model.
    -   Provides AHB and Bring Your Own License \(BYOL\) support: AHB for SQL Server is a benefit for Azure that enables you to use SQL Server licenses with SA or subscription licenses to pay a reduced rate for only cloud-based computing. For more information on BYOL support, see [BYOL support](byol-concepts.md).

If you're covered under Microsoft SA, you can also upgrade, or step-up, a standard version of your software to an enterprise edition. Use the **Upgraded Entitlements** tab of the Software Entitlement form to link related versions of your software under active maintenance and your upgrades.

You can upgrade a Step-up license type entitlement to a Subscription, Perpetual, Perpetual + Software Assurance, or a Step-up license type entitlement. You can upgrade a Subscription Step-up license type entitlement to only an entitlement with a Subscription license type.

**Note:** Step-up at any time if you have the Microsoft Open Value agreement with Software Assurance.

Step-up license types with no upgraded entitlements could result in inaccurate reconciliation results due to double counting of active rights.

If you have the Microsoft SQL Server Enterprise edition with SA for the Per Core license metric, you can run unlimited virtual machines on the host machine. It doesn't matter how many physical core licenses that you have. For example, let's say that you have a license for running only four physical cores on a host machine. You can then run unlimited virtual machines on the host machine.

If you create a software entitlement at the time of receiving a purchase order and SA is activated on that entitlement, the new entitlement is created with one of the following license types:

-   Perpetual + SA: If all previous entitlements have the license type specified as Perpetual + SA.
-   Perpetual: If the previous entitlements have a combination of license types set to Perpetual + SA and Perpetual.

You can't use SA entitlements to license your software. SA entitlements aren’t counted during reconciliation. Only perpetual license entitlements are considered.

SA entitlements need a base entitlement, or a perpetual entitlement, to determine license compliance. Thus, when you import entitlements from a Microsoft License Statement \(MLS\), without a base entitlement, you see an error. For importing entitlements from an MLS, see [Importing entitlements from an MLS](../task/import-mls-entitlements-workspace.md).

**Note:** For creating entitlements for Microsoft SA in the Software Asset Workspace, see [Create Microsoft Software Assurance entitlements in workspace](../task/create-sa-entitlements-workspace.md). For creating entitlements in for Microsoft SA in Software Asset Management classic or for adding SA coverage to an existing entitlement, see [Create entitlements for Microsoft Software Assurance in Software Asset Management classic](../task/create-entitlement-microsoft-sa.md).

## Maintenance for publishers other than Microsoft

For all publishers other than Microsoft, you can create maintenance entitlements to support their software license maintenance needs.

You can associate maintenance entitlements with Perpetual, Perpetual + Maintenance, and Upgrade entitlements. Open the maintenance entitlement form layout, select the **Upgraded Entitlements** tab, and select the perpetual entitlement that you want to associate with.

**Note:** If a maintenance entitlement is associated with a perpetual entitlement, the maintenance entitlement cost is part of the total cost when reconciliation runs.

If you create a software entitlement while you’re receiving a purchase order and maintenance is activated on that entitlement, the new entitlement is created with one of the following license types:

-   Perpetual + Maintenance: If all previous entitlements have the license type specified as Perpetual + Maintenance.
-   Perpetual: If the previous entitlements have a combination of license types that are set to Perpetual + Maintenance and Perpetual.

**Note:** For creating maintenance entitlements in the Software Asset Workspace, see [Create maintenance entitlements in workspace](../task/create-maint-entitlements-workspace.md). For creating maintenance entitlements in Software Asset Management classic, see [Create maintenance entitlements in Software Asset Management classic](../task/Record-software-rights-non-microsoft.md).

-   **[Microsoft Per Core licensing rules](microsoft-sw-license-metrics.md)**  
The Per Core licensing model is used by many Microsoft server products, such as SQL Server and BizTalk Server. It's useful when counting users or devices connecting to the software is difficult, often for internet-facing software.
-   **[Microsoft Per Core \(with CAL\) licensing rules](microsoft-percore-withcal.md)**  
The Per Core \(with CAL\) metric licensing model is followed by various Microsoft Server products such as Windows Server, System Center, and Core Infrastructure Server Suite. The number of licenses depends on the number of installations and operating system environments \(OSE\).

**Parent Topic:**[Exploring Software Asset Management](explore-sam-workspace.md)

**Related topics**  


[Impact of different license types on software reconciliation](../reference/license-types-impact-reconciliation.md)

