---
title: Create a stock rule
description: Create a stock rule to control what happens when the inventory of a particular asset in a particular stockroom reaches a specified threshold.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/it-asset-management/hardware-asset-management/t\_CreateAStockRule.html
release: australia
product: Hardware Asset Management
classification: hardware-asset-management
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 5
breadcrumb: [Configure stockrooms, Configure, Hardware Asset Management, IT Asset Management, Asset Management]
---

# Create a stock rule

Create a stock rule to control what happens when the inventory of a particular asset in a particular stockroom reaches a specified threshold.

## Before you begin

The stockroom must have an assigned manager with an email address. The stock rule sends the restocking email to the stockroom manager and creates stock orders for that manager.

To source stock orders from a Vendor stock rule with a purchase order, both of these requirements must be met:

-   The model has an active vendor catalog item, or an active catalog item with a vendor specified.
-   The vendor company record has the Vendor check box selected.

If no active catalog item exists for the stock rule’s model, the system still creates the stock order request, but the **Purchase** option is unavailable when you source the request.

Role required: inventory\_admin

## Procedure

1.  Create a stock rule.

<table id="choicetable_ggf_c2c_tfc"><thead><tr><th align="left" id="d289877e83">

Interface

</th><th align="left" id="d289877e86">

Action

</th></tr></thead><tbody><tr><td id="d289877e92">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Inventory** &gt; **Stock** &gt; **Stock Rules**.
2.  Select **New**.


</td></tr><tr><td id="d289877e128">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Asset operations** &gt; **Inventory** &gt; **Stock rules**.
2.  Select **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_w1t_lkt_lq"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Model

</td><td>

Product model to which the rule applies.

</td></tr><tr><td>

Threshold

</td><td>

Quantity that the stock must fall below to trigger restocking. Enter a value greater than 0. For example, enter 10 for a laptop computer that you want to restock when inventory in the specified stockroom drops below 10.Current stock includes Available and Reserved assets in the stockroom, plus assets on open transfer orders going to the stockroom.

**Note:** If the stock falls below the threshold, the result depends on the restocking option:

-   **Vendor**: The system sends an email to the stockroom manager. If Hardware Asset Management is activated, the system also creates a stock order request automatically.
-   **Stockroom**: The system creates a transfer order. The stock rule doesn't send an email or create a stock order request.


</td></tr><tr><td>

Restocking option

</td><td>

Location where additional supplies should come from. If Procurement isn’t active, then restocking option is **Stockroom** only. Otherwise, select one of the following:

 -   **Stockroom**: Creates a transfer order to obtain the asset from another stockroom.

**Note:** Transfer orders are created only when the parent stockroom meets the following conditions:

    -   It has assets in the Available state. Assets in other states, such as Reserved or Pending Install, do not qualify.
    -   Its number of available assets is equal to or greater than the full restocking quantity, not just the raw shortfall.

The restocking quantity is the shortfall \(threshold minus current stock\), rounded up to the nearest multiple of the order size. For example, if the shortfall is 1 and the order size is 5, the restocking quantity is 5. The parent stockroom must have at least 5 available assets. If it has 1 to 4, the system does not create a transfer order.

-   **Vendor**: Sends an email to the stockroom manager to order from a vendor. The system also creates records based on whether Hardware Asset Management is active:

    -   If Hardware Asset Management is active, the system creates a Hardware Inventory Stock Order request, which you source with a purchase order. For enterprise models, it creates an enterprise stock order request.
    -   If Hardware Asset Management is not active, the system creates a purchase order and a purchase order line item.
**Note:**

    -   To enable **Purchase** when you source the stock order request, the stock rule’s model must have an active vendor catalog item.
    -   After a Vendor rule creates an order, the rule does not create another order while that order is open. It resumes after the order closes or after stock rises above the threshold.
**Important:** After a transfer order, purchase order, or purchase order line item is created, it's important to act on it promptly.

</td></tr><tr><td>

Active

</td><td>

Option for enabling the stock rule for restocking automatically.

</td></tr><tr><td>

Stockroom

</td><td>

Stockroom that the rule applies to. This is the stockroom that is restocked when its stock falls below the threshold.

</td></tr><tr><td>

Parent stockroom

</td><td>

Stockroom from which additional supplies are transferred. Required when the restocking option is Stockroom.

</td></tr><tr><td>

Order size

</td><td>

Minimum order quantity for stockroom transfers or vendor purchases. The system calculates the smallest multiple of the order size that restocks the item above the threshold. Enter a value greater than 0. For example, a stockroom has 3 laptops, the threshold is 10, the restocking option is Stockroom, and the order size is 4. The system creates a transfer order for 8 laptops, which brings stock to 11 \(3 in stock + 8 ordered\).

When the restocking option is Vendor, the system emails the stockroom manager the total quantity to order, in multiples of the order size.

**Note:** The order size applies only to transfers that stock rules create automatically. Manual transfers have no such restriction and can move any available quantity from the parent stockroom.

</td></tr></tbody>
</table>3.  Select **Submit** or **Save**.


## Result

-   The stock rule that you created appears in the **Stock rules** tab.
-   If the restocking option was set to **Vendor**, the following changes happen:
    -   The **Stock orders** tab is displayed. All the stock orders that are created using this stock rule are listed under the Stock orders tab.
    -   If Hardware Asset Management is active and the stock falls below the threshold, the system automatically creates a Request Item of the Hardware Inventory Stock Order item type. For more information, see [Create an inventory stock order request](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/create-inventory-stock-order.md).
-   After the rule creates a transfer order, the **Transfer orders** tab appears and lists the transfer orders that the rule created.

**Parent Topic:**[Configure stockrooms](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/hardware-asset-management/configure-stockrooms-ham.md)

**Related topics**  


[Stock rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/it-asset-management/asset-management/c_StockRules.md)

