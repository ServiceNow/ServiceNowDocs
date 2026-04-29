---
title: Create a purchase order from a request
description: You can create a purchase order directly from a request. This approach enables procurement managers to obtain items and fulfill requests from the Service Catalog. You can create multiple purchase orders from a request.
locale: en-US
release: australia
product: Procurement
classification: procurement
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Sourcing items in a service catalog request, Procurement, Asset Management, IT Service Management]
---

# Create a purchase order from a request

You can create a purchase order directly from a request. This approach enables procurement managers to obtain items and fulfill requests from the Service Catalog. You can create multiple purchase orders from a request.

## Before you begin

Role required: procurement\_admin or procurement\_user

## About this task

If you don't have the Sourcing and Procurement Operations \(SOP\) application, you can create a purchase order to obtain items and fulfill requests from the Service Catalog.

If you have the Sourcing and Procurement Operations \(SPO\) application along with required plugins installed, and the necessary role assigned, you can create a purchase order by accessing the Shopping Hub catalog items.

-   Required Plugins:
    -   Asset Management Integration for Sourcing and Procurement Operations \(com.snc.sn\_spend\_asset\)
    -   Sourcing and Purchasing Automation \(com.snc.sn\_pr\)
    -   Shopping Hub \(com.snc.uib.sn\_spend\_uib\)
-   Required Roles: The procurement manager has the asset manager role \(sn\_spend\_asset.spo\_shopper\) and other roles depending on the IT Asset Management applications.

For more information about the Asset Management Integration for Sourcing and Procurement Operations \(com.snc.sn\_spend\_asset\) plugin, see [Sourcing and Procurement Operations integration with IT Asset Management](https://www.servicenow.com/docs/access?context=spo-itam-better-together&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).

## Procedure

1.  Navigate to **All** &gt; **Procurement** &gt; **Requests** &gt; **Requests**.

2.  Select the **Number** of a request that has been approved but not sourced.

    Look in the **Request State** and **Sourced** columns.

3.  In the **Catalog Tasks** related list, select a Source Request Items number.

4.  Select **Source Request**.

    The Source Request screen is displayed with a list of all the requested items.

5.  Select **Purchase** in the requested item section.

    **Important:** If you're using the Sourcing and Procurement Operations \(SPO\) application, when you select **Purchase**, a validation check runs to verify that the following conditions are met:

    -   Required plugins are installed to enable the procurement manager to work on assigned requests by using the SPO's Shopping Hub workflows.
    -   The procurement manager has the correct role.
    After successful validation, you're directed to a new Source Request page. The SPO's Shopping Hub workflow guides you through the steps to complete the checkout of the requested items, and you don't need to follow steps 6 through 11 on this page for purchase order creation. Depending on whether the requested items have contractual pricing or not, a purchasing or sourcing flow is triggered, and you need to provide the details for completing the order. For more information about creating sourcing request or purchase requisition, see [Create Sourcing Request or Purchase Requisition in SPO via ITAM Workspace](https://www.servicenow.com/docs/access?context=spo-itam-submit-requests&version=australia&pubname=australia-source-to-pay-operations&ft:locale=en-US).

6.  In the **Vendor** list, select the vendor from which the requested item or items should be delivered.

7.  Verify if the **Out of Stock** field is set to **false**.

    If the vendor doesn't have stock, the field value is **true**.

8.  In the **Quantity** field, specify the quantity you want to order.

9.  In the **Destination Stockroom** list, select the destination to which the requested item or items should be delivered.

10. Select the **Consolidate PO** check box to combine the listed items with existing purchase orders.

    When you check Consolidate Purchase Orders, all items sourced from the same vendor on the same request are placed on the same purchase order. When you select a vendor, the system automatically searches for purchase orders that have been created for the same request, have the same **Vendor** selected, and have the **Requested** status. If the system finds a match, all items are placed on the same purchase order and can be ordered together. If the system doesn’t find a match, a new purchase order is created.

    For example, if you’re purchasing 25 phones from Apple and an open purchase order exists for Apple, the 25 phones are added to the open purchase order. If there are no open purchase orders for the selected vendors, new purchase orders are created. Items ordered from the same vendor are grouped. Different items are shown on separate lines on the purchase order.

11. Select **Submit**.


## Result

-   A purchase order is created.
-   On the request, the **Sourced** check box is selected

**Parent Topic:**[Sourcing items in a service catalog request](../concept/c_SourcingRequestItems.md)

**Related topics**  


[Create a transfer order from a request](t_CreatingTransferOrderFromReq.md)

[Source requests from local stockrooms](consume-local-asset-stock.md)

[Add an assignment from a request](t_AddingAssignmentsFromReq.md)

