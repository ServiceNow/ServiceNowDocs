---
title: OT Asset Workspace
description: The OT Asset Workspace is the intuitive and streamlined user interface of the OT Asset Management application to manage your Operational Technology \(OT\) and Operational Equipment \(OE\) assets.
locale: en-US
release: yokohama
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: concept
last_updated: "2025-01-30"
reading_time_minutes: 12
breadcrumb: [OT Asset Management, Exploring Enterprise Asset Management, Enterprise Asset Management, IT Asset Management]
---

# OT Asset Workspace

The OT Asset Workspace is the intuitive and streamlined user interface of the OT Asset Management application to manage your Operational Technology \(OT\) and Operational Equipment \(OE\) assets.

## OT Asset Workspace overview

The OT Asset Workspace is a unified medium with multiple views that help you manage your OT and OE assets efficiently. The views provide you with visibility into all the important aspects of your assets, such as dashboards on Asset count by model, lifecycle state, model category, and overall performance of assets.

## OT Asset Workspace roles

<table id="table_pyd_1q1_gdc"><thead><tr><th>

Role title

</th><th>

Contains roles

</th><th>

Description

</th></tr></thead><tbody><tr><td>

OT asset manager

 \[sn\_otam.ot\_asset\_manager\]

</td><td>

-   model\_manager
-   model\_admin

</td><td>

This role has full access to the OT Asset Workspace.

**Note:** Given that this role is part of the Enterprise Admin \(sn\_eam.enterprise\_admin\) role, the Enterprise Admin role also has complete access to the OT workspace.

</td></tr><tr><td>

OT technician

 sn\_otam.ot\_asset\_technician

</td><td>

-   sn\_eam.asset\_technician
-   sn\_eam.enterprise\_mobile\_user
-   canvas\_user

</td><td>

This role is for users who perform tasks and update OT hardware asset records as part of the OT hardware asset lifecycle.

</td></tr></tbody>
</table>## OT Asset Workspace views

Efficiently manage your assets by utilizing the different views available in the OT Asset Workspace.

The following table mentions all the views that the OT Asset Workspace consists of, a brief description of each view, and the tabs or lists that are present in each view:

<table id="table_nvv_54v_gdc"><thead><tr><th>

Name of the view

</th><th>

Description of the view

</th><th>

Tabs/lists in the view

</th></tr></thead><tbody><tr><td>

OT asset overview

</td><td>

View important actions and quick links to active tasks.

</td><td>

No tabs in this view.

</td></tr><tr><td>

Asset analytics

</td><td>

Manage resources efficiently by tracking the Total Cost of Ownership \(TCO\) of assets.

</td><td>

**Overview**, **Asset TCO**, **Asset performance**, and **Data visualizations**.

</td></tr><tr><td>

Inventory

</td><td>

View details of the entire asset inventory and stockrooms that enable you to perform inventory tasks.

</td><td>

**Overview**, **All stockrooms**,**Stock rules**, **Transfer orders**, **Asset audits**,**Loaner asset orders**, **RMA orders**, **RMA line orders**, **Repair orders**, **Recall orders**, **Reclamation requests**, **Resale orders**, and **Disposal orders**.

</td></tr><tr><td>

OT asset estate

</td><td>

View the asset functions and maintain accurate hardware and consumable records.

</td><td>

**Overview**, **All assets**, **All enterprise**, **Industrial**, **Hardware**, **Consumables**, and **Pallets**.

</td></tr><tr><td>

OT model management

</td><td>

View details of different types of OT models that are being managed.

</td><td>

**Overview**, **All models**, **All enterprise**, **Industrial**, **Hardware**, **Firmware**,**Firmware discovered**, and **Pallet**.

</td></tr><tr><td>

Procurement

</td><td>

View and manage details of all ongoing procurement activities.

</td><td>

**Overview**, **Requests**, **Request items**, **Purchase orders**, **Receiving slips**, **Advance shipment**, and **Catalog tasks**.

</td></tr><tr><td>

Contract and lease management

</td><td>

View and manage all asset contracts.

</td><td>

**Overview**, **All contracts**, **Lease contracts**, **Leased assets**, **Lease-end assets**, **Renewals**, **Renewal lines**, **My contracts**, **My contract tasks**, **My contract approvals**, and **Terms and conditions**.

</td></tr><tr><td>

Asset operations

</td><td>

View asset operations related to shipment, onboarding, move orders, and calculated model lifecycle.

</td><td>

**Shipment**, **Onboarding**, **Moves**, and **Calculated model lifecycle**.

</td></tr><tr><td>

Work management

</td><td>

Create and manage maintenance plans, work orders, and work order tasks.

</td><td>

**Overview**, **Calibrations**, **My work**, **Maintenance plans**, **Work orders**, **Work order tasks**, **Asset tasks**, **Work order templates**, **Checklist templates**, **My stockroom assets**, and **My asset pickup tasks**.

</td></tr><tr><td>

OT model normalization

</td><td>

View information related to normalization of models.

</td><td>

**Overview**, **Custom OT model types**, **Custom OT product models**, **Custom OT model libraries**, **Custom firmware UNSPSC**, **Custom firmware products**, **Custom firmware versions**, and **Custom firmware CPE**

**Note:** The **Custom firmware UNSPSC**, **Custom firmware products**, **Custom firmware versions**, and **Custom firmware CPE** tabs are available only in the OT Asset Workspace. For more information on these tabs, refer to the following topics:

-   [Create a custom United Nations Standard Products and Services Code \(UNSPSC\) classification for firmware in your operational technology \(OT\) assets](../task/create-custom-unspsc-classification-firmware-ot-assets.md)
-   [Create a custom firmware product for your operational technology \(OT\) assets](../task/create-custom-firmware-product-ot-assets.md)
-   [Create a custom firmware version for your operational technology \(OT\) assets](../task/create-custom-firmware-version-ot-assets.md)
-   [Create a custom Common Platform Enumeration \(CPE\) mapping for firmware in your operational technology \(OT\) assets](../task/create-custom-firmware-cpe-mapping.md)

</td></tr><tr><td>

Admin center

</td><td>

Perform configuration and administrative tasks related to TCO configuration.

</td><td>

**Model and asset tabs**, **Model categories**, **Model classifications**, **Stockroom types**, **Bulk import**, **Roles-to-class access**, **Workflow assignments**, **Calibration configuration**, **TCO configuration**, **Risk configuration**, **Other configuration**, **Shipping**, **Asset knowledge base**, and **Normalization opt-in**.

 As an OT asset manager and OT asset technician, you can only make changes to the Task rate card and Labor rate card options under the **TCO Configuration** list.

</td></tr></tbody>
</table>## Hardware models and OT hardware assets in OT Asset Workspace

OT managers can create hardware models and OT hardware assets in the OT Asset Workspace. The **Hardware** tab in the OT model management and OT asset estate views lists the hardware models and OT hardware assets for all categories.

You can publish hardware models, more than once, to the enterprise catalog using the **Publish** button in the OT model management view. The **Publish** button appears only if there isn't already an active enterprise catalog item for that specific hardware model.

**Note:** Only the OT asset manager \(sn\_otam.ot\_asset\_manager\) and the enterprise admin \(sn\_eam.enterprise\_admin\) can publish hardware models.

Hardware models and OT hardware assets are also integrated into the following Enterprise Asset Management flows:

-   [Asset request](../task/create-eam-assetrequest.md)
-   [Asset refresh](../task/request-eam-assetrefresh.md)
-   Stock order
-   [Single and multi-asset onboarding](onboarding-multi-asset-from-ws.md)
-   [Return Merchandise Authorization \(RMA\)](requesting-return-merchandise-authorization-enterprise-assets.md)
-   [Repair](manage-repair-of-defective-eam-assets.md)
-   [Disposal](../task/create-eamdisposal-order.md)
-   [Bulk import](overview-bulk-import-eam.md)

    **Note:**

    Starting with the Zurich release, the bulk import templates include the **OT entity** and **Parent asset attribute** columns. When the OT Asset Management application is activated, you can bulk import hardware assets and models in both the Enterprise Asset Workspace and the OT Asset Workspace only if the OT entity column is marked as **TRUE**. With the **Parent asset attribute** field, you can choose to identify the parent of a child asset using either the Asset tag, Serial number, or MAC address.

    To view instructions for bulk importing assets, select the **Bulk import instructions** icon \[![Import instructions](../image/bulk-imp-instructions-icon.png)\] on the contextual side bar.

-   [Asset reclamation](enterprise-asset-reclamation.md)

    **Note:** When a reclamation request for an OT hardware asset is created in the OT Asset Workspace, a hardware reclamation request line is generated and displayed in the **Hardware Asset Reclamation Lines** tab.

-   [Advanced shipment notification \(ASN\)](../task/asn-eam.md)

    **Note:** Starting with the Zurich release, the Download template for Advanced Shipment Notification includes the **OT entity** column. When this column is set to **TRUE** for hardware models, it creates OT hardware assets in the OT Asset Workspace.

-   [Asset audits](../task/audit-eam-assetinventory.md)
-   [Asset Total Cost of Ownership \(TCO\)](asset-tco-eam.md)

    **Note:** You can create a TCO report using a hardware model as a benchmark model, by selecting **Hardware** in the Report table field and then selecting the required hardware model in the **Benchmark model** field.

-   [Lease contract](managing-expiring-contracts-leased-assets.md)

    **Note:** The **Begin lease-end process** option is available if the contract includes OT hardware assets.

-   [Risk](risk-scoring-eam.md)

    **Note:** The Enterprise asset risk heat map in the OT asset estate view and the Enterprise model risk heat map in the OT model management view also include hardware models with OT entity flag set to **TRUE**.

-   [Asset resale](../task/enterprise-asset-resale-flow.md)
-   [Loaner](../task/request-eam-assetloaner-request.md)
-   [Move orders](managing-enterprise-asset-move-orders.md)
-   [Recall](managing-recalled-enterprise-assets.md)
-   [Stock rule](../task/create-eamstockrules.md)

    **Note:** The **OT stock rule** check box on the stock rule form indicates whether the stock rule was created in the OT Asset Workspace.

    This check box appears for all models in both the OT Asset Workspace and Enterprise Asset Workspace only when the OT Asset Management application is activated. However, only the OT asset manager can select or deselect this check box in the OT Asset Workspace.

    If you have activated the Hardware Asset Management application, the **com.sn\_otam.enable\_ot\_stock\_rule** asset property enables you to separate OT and non-OT hardware assets in stock rules and stock rule reports. If you set this property to **true** and select the **OT stock rule** check box, only OT hardware assets are included. If the **OT stock rule** check box isn't selected, only non-OT hardware will be included. By default, for existing stock rules, this property is set to **false**, and the OT stock rule is also set to **false**. This means that both OT and non-OT hardware assets are included in the stock rules and reports, regardless of the OT entity flag.


Furthermore, you can generate maintenance plans and work orders for OT hardware assets.

All OT hardware assets are automatically tagged as an OT entity. When an OT hardware asset is sourced from an existing stockroom via a transfer order or from the local stockroom, the asset is automatically tagged as an OT entity. Similarly, during the receiving process of OT hardware assets procured via a purchase order, the asset is automatically tagged as an OT entity. The **OT entity** field appears in the Hardware asset form in OT asset estate view and is selected by default for all OT hardware assets.

You can evaluate how effectively your assets are functioning and being used through the reports based on asset key performance indicators in the **Asset performance** tab of the **Asset analytics** view. The asset performance report is also available on the contextual sidebar of the asset record, displayed by selecting the **Asset availability and related KPIs** icon \[![Asset KPI icon](../image/asset-kpi-icon.png)\].

You can receive assets from any workﬂow directly at the stockroom using the unified receiving functionality in the OT asset Asset Workspace. You can receive assets in any of the following ways:

-   Receive a single asset
-   Receive multiple assets in the shipments
-   Import assets in bulk and receive them

You can also manage supply and demand in your stockrooms effectively with inventory demand reports. To view the reports, follow these steps

1.  Navigate to **Inventory**.
2.  Select the **All stockrooms** tab.
3.  Select a stockroom for which you want to view the inventory reports.
4.  Select the **Inventory insights** tab.

## Consumables in OT Asset Workspace

Consumables can be created in the OT Asset Workspace for hardware models, OT hardware assets, and industrial assets.

-   For hardware models: Create consumables while creating a hardware model by selecting **Create consumable asset** from the **Asset tracking strategy** drop-down. Once selected, all OT hardware assets for the given hardware model will be consumables. After a consumable is created, the following related lists appear in the hardware model form: Compatibles, Substitutes, Consumables, Vendor catalog items, Consumable model lifecycle, Skills, Knowledge, Application.
-   For OT hardware assets: Create consumables from the Consumables tab in the OT asset estate view by selecting **Hardware asset** in the **Type** drop-down.
-   For industrial assets: Create consumables from the Consumables tab in the OT asset estate view by selecting **Industrial asset** in the **Type** drop-down.

Any consumable model that you create in the in the OT Asset Workspace, has the consumable model category.

**Parent Topic:**[OT Asset Management](ot-asset-management.md)

**Related topics**  


[OT Asset Management licensing](licensing-ot-asset-management.md)

[View the license report for the OT Asset Management application](../task/view-license-report-otam.md)

[Asset and Configuration Item \(CI\) synchronization for Operational Technology \(OT\) assets](asset-ci-sync-ot-assets.md)

[OT Asset Workspace roles](../reference/ot-workspace-roles.md)

[Enterprise Asset Workspace](using-eam-workspace.md)

