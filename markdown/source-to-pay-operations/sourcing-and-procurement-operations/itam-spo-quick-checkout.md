---
title: Create purchase requisition from the ITAM Workspace
description: As an asset manager, use SPO’s purchasing flow from the ITAM Workspace to complete checkout when the requested item has contractual pricing.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Create SR or PR via ITAM Workspace, Sourcing Procurement Operations integration Asset, Integrate, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create purchase requisition from the ITAM Workspace

As an asset manager, use SPO’s purchasing flow from the ITAM Workspace to complete checkout when the requested item has contractual pricing.

## Before you begin

Role required: sn\_spend\_asset.spo\_shopper

## About this task

This task describes the options you need to select and the information you need to provide after you select **Request items and checkout** when the requested item has an associated price.

## Procedure

1.  Complete steps 1 through 10 as described in [Create Sourcing Request or Purchase Requisition in SPO via ITAM Workspace](spo-itam-submit-requests.md).

2.  Submit sourcing request for items without price.

3.  On the Delivery location page, select a delivery location from the **Delivery location** list.

    ![Delivery location page.](../image/itam-spo-qco-delivery-loc.png)

4.  Select **Deliver to additional locations** to add additional delivery locations and specify the purchase quantity.

5.  Select **Continue to delivery date**.

6.  On the Delivery date page, select any of the following options:

    -   **Get as soon as** \(an estimated date auto-populates based on the current date\)
    -   **On a specific date**
    ![Delivery date page.](../image/itam-spo-qco-delivery-date.png)

7.  Select **Add another delivery date** to add another delivery date.

8.  Select **Continue to Payment method**.

9.  On the Payment method page, you can retain the selected cost center or select any of the following options:

    -   **Use another cost center**
    -   **Pay with multiple cost centers**
    ![Payment method page.](../image/itam-spo-qco-payment.png)

10. Select **Continue to purchase reason**.

11. On the Reason for purchase page, do the following:

    -   In the **Reason for purchase** field, enter a reason for making this purchase.
    -   Select **+Add file** to add any attachments to this purchase.
    -   In the **Watchlist** field, ad individuals who you want notified if any updates are made to this purchase.
    ![Reason for purchase page.](../image/itam-spo-qco-purchase-reason.png)

12. Select **Complete checkout**.

    A purchase requisition is created for the requested items in SPO.


## What to do next

The Procurement Specialist reviews the requisition in the Source-to-Pay Workspace and converts it into a purchase order.

**Note:** The PO created in SPO \(sn\_shop\_purchase\_order table\) references the corresponding PO generated in ITAM \(procure\_po table\). The Asset Manager can monitor the progress of the SR, PR, and PO by closely tracking the PO within ITAM.

If the asset manager has the Shopping Hub shopper role \(sn\_shop.shopper\), they can also view the status of their request directly in Shopping Hub.

The end user who submitted the original RITM continues to track and monitor the request status on the RITM record. Statuses between SPO and ITAM objects are synchronized so that updates appear in real time.

**Parent Topic:**[Create Sourcing Request or Purchase Requisition in SPO via ITAM Workspace](spo-itam-submit-requests.md)

