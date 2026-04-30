---
title: Sourcing and Procurement Operations integration with IT Asset Management
description: The Asset Management Integration for Sourcing and Procurement Operations plugin \(sn\_spend\_asset\) provides an integration between IT Asset Management \(ITAM\) and Sourcing and Procurement Operations \(SPO\) applications, enhancing operational efficiency.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 7
breadcrumb: [Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Sourcing and Procurement Operations integration with IT Asset Management

The Asset Management Integration for Sourcing and Procurement Operations plugin \(sn\_spend\_asset\) provides an integration between IT Asset Management \(ITAM\) and Sourcing and Procurement Operations \(SPO\) applications, enhancing operational efficiency.

This integration enables asset managers to access Shopping Hub catalog items, including the catalog items without assigned prices, directly within the ITAM workspace. By enabling procurement actions without switching platforms, it streamlines workflows and improves the user experience for asset managers and end users.

## ITAM-SPO better together workflow

The procurement journey begins through an automated inventory stock order or when an end user submits a request for items from the service catalog. The asset manager then evaluates whether the request can be fulfilled by using available local stock, generating transfer orders, or creating purchase orders. After the asset manager identifies the appropriate purchase action, the better together experience begins.

The following figure illustrates the ITAM-SPO workflow.

**Important:** This is an interactive image. Select each box or step in the image to learn about that process or task.

![ITAM-SPO better together workflow](../image/itam-spo-bt-workflow.png)

## Role required for the SPO-ITAM better together feature

The Asset Manager role \(sn\_spend\_asset.spo\_shopper\) is required to work on assigned requests from the ITAM workspace by creating sourcing requests or purchase requisitions in SPO.

**Note:** Additional roles may be required based on the specific asset management product installed.

## Plugin dependencies for the SPO-ITAM better together feature

The following are the plugin dependencies that are required to use Asset Management Integration for Sourcing and Procurement Operations \(sn\_spend\_asset\):

-   Sourcing and Purchasing Automation \(sn\_pr\)
-   Procurement \(procurement\)
-   Shopping Hub \(uib.sn\_spend\_uib\)

Additional plugins may be required based on the specific asset management product installed:

-   Base Asset \(no additional plugins required\)
-   Enterprise Asset Management \(com.sn\_eam\)
-   Hardware Asset Management \(com.sn\_hamp\)
-   Software Asset Management \(samp\)

## Inventory stock orders

Typically, inventory stock orders are automatically submitted based on the stock rules configuration. Stock rules define the conditions under which a specified quantity of an asset is transferred from another stockroom or ordered from a supplier when the inventory in a particular stockroom falls below a defined threshold. For more information, see [Stock rules](https://www.servicenow.com/docs/access?context=c_StockRules&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

The following are the prerequisites for creating a stock order via stock rules:

-   Application: Hardware Asset Management or Enterprise Asset Management
-   Catalog Item: Hardware Inventory Stock Order
-   Category: Asset Lifecycle

**Note:** For an inventory stock order, the delivery address and quantity of items are predefined and can’t be modified.

## End user requests via Service Catalog for IT assets

An asset manager or end user can manually submit a request. If a user has the Inventory user role, they can purchase more than 10 items. For more information, see [Create an inventory stock order request](https://www.servicenow.com/docs/access?context=create-inventory-stock-order&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US). If the user is purchasing 10 items or fewer, a general service catalog request works.

Requesters can only make requests via service catalog for published and approved models. If an approved model is not available, contact Procurement or IT to request the items, based on your business process. For more information, see [Publish models to the hardware or software catalog](https://www.servicenow.com/docs/access?context=t_PublishingModToHrdwreOrSftCat&version=zurich&pubname=zurich-it-asset-management&ft:locale=en-US).

The following are the prerequisites for creating a request for more than 10 items:

-   Application: Hardware Asset Management or Enterprise Asset Management
-   Catalog Item: Hardware or Enterprise Inventory Stock Order
-   Category: Asset Lifecycle

    **Note:** For requests of more than 10 items, the delivery address and item quantities are predefined and cannot be modified.


The following are the prerequisites for creating a standard end-user request for fewer than 10 items:

-   Application: Software Asset Management, Hardware Asset Management, Enterprise Asset Management, or Base Asset
-   Catalog Item: Standard Hardware, Software, or Enterprise Request
-   Category: Asset Lifecycle

## Supported applications and flows in the ITAM-SPO better together feature

The ITAM-SPO better together feature supports the following applications and flows:

-   **ITAM applications**
    -   Software Asset Management \(SAM\)
    -   Hardware Asset Management \(HAM\)
    -   Enterprise Asset Management \(EAM\)
    -   Base Asset
-   **ITAM flows covered as part of this better together solution include the following:**
    -   Hardware, Software, and Enterprise Asset Standard Flows
    -   Hardware and Enterprise Inventory Stock Orders

-   **[Create Sourcing Request or Purchase Requisition in SPO via ITAM Workspace](../task/spo-itam-submit-requests.md)**  
As an Asset Manager, you can create an SR or PR in SPO from the ITAM Workspace to fulfill IT and asset requests submitted through Employee Center.
-   **[Receiving assets in IT Asset Management](itam-spo-receiving-assets.md)**  
As part of the Better Together integration, all asset receiving is handled within IT Asset Management \(ITAM\). When an item is initially received in ITAM, a receipt is automatically generated in SPO in the Pending Submission state.
-   **[Asset creation process in IT Asset Management](itam-spo-asset-creation.md)**  
In IT Asset Management \(ITAM\), assets are created when you acknowledge the receipt of the requested items.
-   **[Considerations for implementing the ITAM-SPO better together flow](itam-spo-key-consideration.md)**  
This section provides information on considerations for implementing the ITAM-SPO better together solution.

**Parent Topic:**[Integrate Sourcing and Procurement Operations with other applications](integrating-spo.md)

**Related topics**  


[Sourcing and Procurement Operations integration with Employee Center](employee-center-integration-psm.md)

[Sourcing and Procurement Operations integration with third-party sourcing solutions](psm-integration-third-party-sourcing.md)

[Sourcing and Procurement Operations integration with Third-party Risk Management](better-together-with-vrm.md)

[Sourcing and Procurement Operations integration with Project Management](integration-psm-ppm.md)

[Sourcing and Procurement Operations integration with Celonis](integration-psm-celonis.md)

[Sourcing and Procurement Operations integration with Field Service Management](integration-psm-fsm.md)

[Source-to-Pay Operations integration with Contract Management Pro](integration-spo-cmpro.md)

[ERP source validation on Sourcing and Procurement Operations objects](../reference/erp-source-val-spo-objects.md)

[SpendInt APIs](../../../integrate/inbound-rest/concept/spendint-api.md)

[Procurement File Transfer Framework](procurement-file-transfer-framework.md)

