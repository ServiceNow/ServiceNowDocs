---
title: Create an inventory stock order request
description: Create an inventory stock order request so that you can order new hardware in bulk for your stockrooms. The Hardware Stock Order flow tracks your order through approval, sourcing, and receiving.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/hardware-asset-management/create-inventory-stock-order.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 3
breadcrumb: [Procurement and fulfillment, Use, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Create an inventory stock order request

Create an inventory stock order request so that you can order new hardware in bulk for your stockrooms. The Hardware Stock Order flow tracks your order through approval, sourcing, and receiving.

## Before you begin

To source a request with a purchase order, confirm that both conditions are true:

-   The requested model has an active vendor catalog item, or an active catalog item that specifies a vendor for the model.
-   The vendor company record has the **Vendor** option selected. Without it, you can still submit the request, but the **Purchase** option is unavailable on the sourcing page.

Role required: inventory\_admin

## About this task

A stock order is a catalog request to replenish the stock in a stockroom.

You can manually create a hardware inventory stock order request. If Hardware Asset Management is activated, a stock rule with the **Vendor** restocking option also automatically creates a hardware inventory stock order request when stock falls below the threshold. A stock rule with the **Stockroom** restocking option creates a transfer order from the parent stockroom instead.

When you submit the stock order request, the Hardware Stock Order flow starts. The Workflow Studio application is used to create the Hardware Stock Order flow to take you through the entire process of requesting, sourcing, and receiving your order.

\[Omitted image "hardware-stock-order-flow.png"\] Alt text: Hardware stock order flow

## Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Submit Stock Order**.

2.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Model|New hardware that you want to order. The list shows only hardware and consumable models with the Operational status and the In Use substatus.|
    |Quantity|Amount of the new hardware that you want to order.|
    |Stockroom|Stockroom where you want to stock the new hardware.|
    |Comments|Details that are specific to your order request.|

3.  Select **Order Now**.

    The Order Status form displays all the order details.

    An existing Service Catalog request workflow handles the approvals for the request:

    -   If the total price is $1,000 or less, the request is approved automatically.
    -   If the total price is more than $1,000, the request goes to an approver group for approval.
    After the request is approved, you can source it.

4.  Select the request number to open the request.

    The price of the request item is set from the cost of the model. The price of the request is the quantity multiplied by the price of the request item.

    After the request is approved, the Source Request flow creates a catalog task for the request when both of these conditions are true:

    -   The Source Request flow is active.
    -   The **Model** field on the request is filled in, which makes the request sourceable.
    **Note:**

    If the catalog task isn't created after the request is approved, verify that the **com.sn\_itam.enable\_flow\_designer.source\_request** is set to **true**.

5.  Select **Catalog Tasks** and open the catalog task.

6.  Select **Source Request**.

    The Source Request form layout lists the model name, the quantity of items to be sourced, and the transferable stock.

7.  Select **Transfer** or **Purchase** to source the request via a transfer order or a purchase order.

    The quantity mentioned in **Total in Stock** does not include the stock that's available in the destination stockroom.

    If the requested item is not available in any stockroom, then **Transfer** is unavailable. If there are no available vendors for the requested item, then **Purchase** is unavailable.

    To enable **Purchase**, create an active vendor catalog item for the requested model, or an active catalog item for the model with a vendor specified. The vendor company record must also have **Vendor** selected.


**Parent Topic:**[Procurement and fulfillment](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/procurement-fulfillment-ham.md)

**Related topics**  


[Fulfilling hardware asset requests]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Manage loaner assets]()

[Track shipments using the integration framework]()

