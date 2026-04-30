---
title: Create Sourcing Request or Purchase Requisition in SPO via ITAM Workspace
description: As an Asset Manager, you can create an SR or PR in SPO from the ITAM Workspace to fulfill IT and asset requests submitted through Employee Center.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Sourcing and Procurement Operations integration with IT Asset Management, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create Sourcing Request or Purchase Requisition in SPO via ITAM Workspace

As an Asset Manager, you can create an SR or PR in SPO from the ITAM Workspace to fulfill IT and asset requests submitted through Employee Center.

## Before you begin

Role required: sn\_spend\_asset.spo\_shopper

## About this task

After an employee submits a request through the Employee Center or an automated stock rule is triggered, the Asset Manager can view the request in the Service Catalog application and start sourcing and procuring the requested items from the appropriate ITAM Workspace.

The ITAM workspace used depends on the type of items being requested, such as hardware, software, or enterprise assets.

-   Asset Workspace
-   Hardware Asset Workspace
-   Software Asset Workspace
-   Enterprise Asset Workspace

To ensure a seamless integration between ITAM and SPO, the following updates have been implemented:

-   SPO's Purchase Requisition \(PR\), Sourcing Request \(SR\), and Purchase Order \(PO\) tables are mapped to their corresponding tables in ITAM to enable smooth data flow between the two products.
-   When a PR, SR, or PO is created in SPO, the associated data and states are synchronized with the corresponding PO in ITAM.
-   The ITAM Purchase Order \(PO\), generated during the creation of a sourcing request or purchase requisition, provides visibility to both the employee and the asset manager.
-   ITAM Purchase Order Lines \(POLs\) are generated after a supplier has been awarded in the sourcing request flow.
-   The ITAM PO includes references to SPO’s SR, PR, and PO records.
-   The ITAM POL includes references to SPO’s purchase requisition line \(PRL\) or POL records.

## Procedure

1.  Navigate to **All** &gt; **Open Records** &gt; **Requests**.

2.  Open the request.

3.  On the **Catalog tasks** tab, select and open the sourcing task for the request.

    ![Catalog tasks tab showing the sourcing task.](../image/itam-spo-catalog-tasks.png)

4.  Select **Source Request**.

    ![Source Request option on the Catalog tasks page.](../image/itam-spo-source-request.png)

    A confirmation message is displayed informing you that you're being redirected to the appropriate Asset Management workspace.

5.  Select **OK**.

6.  On the Sourcing page, select **Purchase**.

    ![Purchase option on the Sourcing page.](../image/itam-spo-workspace.png)

    You' are guided through stages that enhance the better together experience using SPO’s Shopping Hub workflows, helping you efficiently source the products you need.

7.  On the Select the requested items you want to purchase page, select the items that you requested.

8.  Select **Select Supplier**.

    ![Select Supplier option on the Select the requested items you want to purchase page.](../image/itam-spo-select-items.png)

9.  On the Select suppliers for requested items page, select the suppliers from whom you want to buy the requested items.

    ![Request items and checkout option on the Select Suppliers page.](../image/itam-spo-select-suppliers.png)

    **Note:** The purchase quantity you specify should not exceed the quantity specified on the original request in the Service Catalog application. In the **Purchase quantity** field, if you specify a quantity that exceeds the original quantity, you see a message that informs you that the total quantity selected exceeds the quantity to be sourced.

10. Select **Request items and checkout**.

    One of the following occurs depending on whether the requested items have a price associated with them.

    -   For products that do not have an associated price, the sourcing flow is triggered. For more information, see [Create sourcing request from the ITAM Workspace](itam-spo-sourcing-checkout.md).

    -   For products, that have an associated price, the purchasing flow is triggered. For more information, see [Create purchase requisition from the ITAM Workspace](itam-spo-quick-checkout.md).
11. Select **Checkout**.


-   **[Create sourcing request from the ITAM Workspace](itam-spo-sourcing-checkout.md)**  
As an asset manager, use SPO’s sourcing flow from the ITAM Workspace to complete checkout when the requested item doesn’t have contractual pricing.
-   **[Create purchase requisition from the ITAM Workspace](itam-spo-quick-checkout.md)**  
As an asset manager, use SPO’s purchasing flow from the ITAM Workspace to complete checkout when the requested item has contractual pricing.

**Parent Topic:**[Sourcing and Procurement Operations integration with IT Asset Management](../concept/spo-itam-better-together.md)

