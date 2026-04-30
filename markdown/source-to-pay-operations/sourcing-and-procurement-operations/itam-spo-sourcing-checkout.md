---
title: Create sourcing request from the ITAM Workspace
description: As an asset manager, use SPO’s sourcing flow from the ITAM Workspace to complete checkout when the requested item doesn’t have contractual pricing.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Create SR or PR via ITAM Workspace, Sourcing and Procurement Operations integration with IT Asset Management, Integrating Sourcing and Procurement Operations with other applications, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create sourcing request from the ITAM Workspace

As an asset manager, use SPO’s sourcing flow from the ITAM Workspace to complete checkout when the requested item doesn’t have contractual pricing.

## Before you begin

Role required: sn\_spend\_asset.spo\_shopper

## About this task

This task describes the options you need to select and the information you need to provide after you select **Request items and checkout** when the requested item does not have an associated price.

During checkout, asset managers interact with a user interface that is similar to Shopping Hub’s "I need a product" record producer to provide key details about the product to be sourced.

## Procedure

1.  Complete steps 1 through 10 as described in [Create Sourcing Request or Purchase Requisition in SPO via ITAM Workspace](spo-itam-submit-requests.md).

2.  On the Select the preferred supplier for the following items page, select **Request items and checkout**.

    ![Record producer where you enter the details for a product without contractual pricing.](../image/itam-spo-sourcing-flow.png)

3.  On the form, fill in the fields in these sections.

<table id="table_lvw_2pk_rfc"><thead><tr><th>

Section

</th><th>

Option

</th></tr></thead><tbody><tr><td>

Request details

</td><td>

From the What do you need for this request? list, select any of the following options:-   I need a quote
-   I need a proposal
-   I need a proof of concept
-   I need more information about the products or suppliers


</td></tr><tr><td>

Delivery information

</td><td>

-   From the **Select delivery address** list, select a delivery address.

**Note:** For an inventory stock order, the delivery address is predefined and cannot be modified.

-   From the Default delivery date list, select one of the following options:
    -   As soon as possible
    -   A specific date
    -   I am not sure


</td></tr><tr><td>

Products

</td><td>

-   Add the products you would like to request. Select the **Open Preview** option to see a preview of the product and make any changes to the metric group, license metric, quantity, and so on. Select Update to save your changes.

**Note:** You can select **Add** to add additional products; however, the quantity that you specify must not exceed the number specified in the original request. However, for an inventory stock order, the quantity of items is predefined and cannot be modified.

-   In the **Why do you need these products?** field, enter a reason for buying these products.


</td></tr><tr><td>

Additional details

</td><td>

Enter any details or questions you want to mention.

</td></tr><tr><td>

Attachments

</td><td>

Select **+Add file** to add any attachments you would like to upload.

</td></tr></tbody>
</table>    **Note:** You cannot modify quantities through this record producer. To make quantity changes, go to the Supplier selection page.

4.  Select **Checkout**.

    A sourcing request \(SR\) is created.


## What to do next

The Procurement Specialist accesses the SR in the Source-to-Pay Workspace and initiates the sourcing process.

**Parent Topic:**[Create Sourcing Request or Purchase Requisition in SPO via ITAM Workspace](spo-itam-submit-requests.md)

