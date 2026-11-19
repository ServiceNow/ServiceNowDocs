---
title: Create an inventory stock order request
description: Create an inventory stock order request so that you can order new hardware in bulk for your stockrooms. The Hardware Stock Order flow tracks your order through approval, sourcing, and receiving.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/zurich/it-asset-management/hardware-asset-management/create-inventory-stock-order.html
release: zurich
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 8
breadcrumb: [Use, Hardware Asset Management, IT Asset Management]
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

4.  Click the request number to open the request.

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


**Parent Topic:**[Using Hardware Asset Management](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/zurich/markdown/zurich/it-asset-management/hardware-asset-management/using-ham-classic.md)

**Related topics**  


[Work with hardware normalization]()

[Manage asset bundles from your inventory]()

[Manage your inventory through pallet assets]()

[Manage loaner assets]()

[Donate assets to charity organizations]()

[Use Advanced Shipment Notification]()

[Manage RMA requests]()

[Create a disposal order]()

[Use a hardware asset request flow]()

[Audit hardware asset inventory]()

[Request a Hardware Asset Refresh]()

[Manage your expiring contracts for leased hardware assets]()

[Reclaim hardware assets]()

[View RFID information of assets]()

[Manage the lifecycle of hardware models with calculated lifecycle templates]()

[Create an internal lifecycle in the Hardware Asset Workspace]()

[Calculate the active lifecycle phase for a model]()

[Receive asset warranty details from Lenovo]()

[Manage stockrooms]()

[Track shipments using the integration framework]()

[Track asset location using indoor maps]()

[Assess performance of Hardware Asset Management]()

[Manage refresh of assets using Zero Touch Refresh]()

[Configure the Total Cost of Ownership of assets]()

[Manage Hardware Asset Management subscriptions]()

[Manage repair of defective assets in your stockroom in the Hardware Asset Workspace]()

[Manage picking hardware assets within your stockroom for Hardware Asset Management workflows]()

[Manage hardware asset tasks using the Mobile Agent application]()

[Manage asset put away using the Hardware Asset Workspace]()

[Audit your hardware assets by using Asset Attestation]()

[Acknowledge receipt of assets on the Employee Center portal]()

[Update associated Decision tables for HAM flows]()

