---
title: Stockrooms
description: Stockrooms are places to which assets are assigned.You can create a stockroom.You can delete a stockroom. If the stock room has assets, you must remove the assets from the stockroom first.You can delete a stockroom that has no assets.Stockroom types are categories of stockrooms.If you need stockroom types that are not included in the base system, you can create a custom stockroom type.Stock rules are defined criteria stating that when the inventory of a particular asset in a particular stockroom reaches a specified threshold, a certain number should either be transferred from another stockroom or ordered from a vendor.Create a stock rule to control what happens when the inventory of a particular asset in a particular stockroom reaches a specified threshold.
locale: en-US
release: xanadu
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 10
breadcrumb: [Asset Management, IT Service Management]
---

# Stockrooms

Stockrooms are places to which assets are assigned.

When stock is low on a particular asset, stock rules can either notify an asset manager or automatically transfer inventory from one stockroom to another.

Stockrooms are separate, standalone entities in the Asset Management application.

**Parent Topic:**[Asset Management](c_AssetManagement.md)

## Create a stockroom

You can create a stockroom.

### Before you begin

Role required: inventory\_admin

### Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Stock** &gt; **Stockrooms** and create a new record \(see table for field descriptions\).

    |Fields|Description|
    |------|-----------|
    |Name|Display name and identifier of the stockroom.|
    |Assignment group|Group that primarily uses the stockroom.|
    |External|Whether this stockroom is managed internally \(check box is cleared\) or is managed externally by a third party \(check box is selected\).|
    |Location|Physical location of the stockroom.|
    |Type|Type of stockroom, such as Field Agent or On site.|
    |Manager|Person in charge of the stockroom. Receives restocking notifications and requests for the stockroom's stock rules.|

2.  Click **Submit**.


## Delete a stockroom with assets

You can delete a stockroom. If the stock room has assets, you must remove the assets from the stockroom first.

### Before you begin

Role required: inventory\_admin

### Procedure

1.  Navigate to **All** &gt; **Asset** &gt; **All Assets**.

2.  Personalize the list to add the **Stockroom** column.

3.  Filter the list to show only the assets in the stockroom that you want to delete.

4.  Change or remove the stockroom for all of the asset records.

5.  After removing assets from the stockroom you want to delete, continue with the instructions for [deleting a stockroom with no assets](c_Stockrooms.md#).


## Delete a stockroom with no assets

You can delete a stockroom that has no assets.

### Before you begin

Incomplete transfer orders must be deleted before you delete the stockroom.

Role required: inventory\_admin

### Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Stock** &gt; **Stockrooms**.

2.  Select the check box beside the stockroom name.

3.  In the **Actions** list, select **Delete**.

    **Note:** Transfer order history is deleted when you delete the stockroom.


## Stockroom types

Stockroom types are categories of stockrooms.

The stockroom type has two significant characteristics.

-   **Priority**: Order of stockrooms the parts should be sourced from. For example, if a personal stockroom \(priority 2\) contains the required part, the personal stockroom receives priority over the Central Stockroom \(priority 7\) because the part in the personal stockroom doesn’t require delivery.
-   **Shipment Required**: Informs the system if a transfer order must be created when the part is sourced from a stockroom of the given type. For example, a part in a personal stockroom doesn’t require shipment, so no transfer order is needed.

|Value|Name|Priority|Shipment Required|Description|Comment|
|-----|----|--------|-----------------|-----------|-------|
|on\_site|On Site|1|False|Stockroom at the customer site.|Close to the users and doesn’t require shipping.|
|field\_agent|Field Agent|2|False|Virtual, personal stockroom linked with a field service agent \(FSA\) directly, used for delivery.|Used to indicate to the system that the part has been delivered and is with the FSA.|
|fsl|FSL|4|True|Forward Shipping Location.|Small stockrooms where the parts can typically be shipped via overnight delivery.|
|pudo|PUDO|5|True|Pick Up/Drop out location.|This type is sometimes called a by-box. Can be a postal box that can receive new and returned parts that are often near major customer sites.|
|stockroom|Warehouse|6|True| |A regional stockroom.|
|central\_stockroom|Central Warehouse|7|True| |A central stockroom, usually a large facility from which most parts are shipped.|

## Create a new stockroom type

If you need stockroom types that are not included in the base system, you can create a custom stockroom type.

### Before you begin

Role required: inventory\_admin

### About this task

Check the [priority level](c_Stockrooms.md#) of the stockroom types provided in the base instance to ensure that you assign the correct priority level to any new stockroom types you create. You can also modify the stockroom types included in the base system.

### Procedure

1.  Navigate to **All** &gt; **Inventory** &gt; **Stock** &gt; **Stockroom Types** and create a new record \(see table for field descriptions\).

    |Field|Description|
    |-----|-----------|
    |Name|Display name of the stockroom type.|
    |Description|General information about the stockroom type.|
    |External stockroom|Whether stockrooms of this type are managed internally \(check box cleared\) or managed externally by a third party \(check box selected\).|
    |Priority|Level of precedence for this type of stockroom.|
    |Shipment required|Option that determines if stockrooms of this type require shipment by default.|
    |Value|Internal identifier of the stockroom type.|

2.  Click **Submit**.


## Stock rules

Stock rules are defined criteria stating that when the inventory of a particular asset in a particular stockroom reaches a specified threshold, a certain number should either be transferred from another stockroom or ordered from a vendor.

For example, a specific model of computer keyboard reaches an inventory of 10 in a particular stockroom and, because a stock rule is in place, a transfer order is automatically created to transfer 50 from a different stockroom. Because there can be multiple assets of a model within a stockroom, stock rules enable you to check all assets fitting the criteria and view a total count.

There are two restocking options:

-   Email notifications can be sent to the stockroom manager \(specified in the **Manager** field on the stockroom record\) through the **Asset Restocking** email action when the inventory of a particular asset in the stockroom reaches a specified threshold. You can customize this email notification by updating the details in the following tabs:

    -   **When to send**: Set the conditions under which the email should be triggered.
    -   **Who will receive**: Specify the recipients of the email.
    -   **What it will contain**: Define the content and information included in the email.
    A task is automatically created for the stockroom manager or, if Procurement is active, a purchase order and a purchase order line item are created.

-   A transfer order can be generated automatically to restock the item from another stockroom.

### Stock Rule Runner job

The Stock Rule Runner job runs everyday to check if the inventory in the stockroom has reached the threshold set by the stock rule. The job then triggers tasks or workflows to restock the inventory. This job creates tasks for stockroom managers and also sends email notifications to them.

**Important:** If restocking is in progress, the system doesn’t create duplicate email messages or duplicate transfer orders. It's important to act on it promptly.

By default, the **glide.sc.checkout.twostep** system property that's set to **false**, results in the automatic submission of requests when items are added to the Service Catalog cart. Also, with this setting of the system property, the Stock Rule Runner job triggers the creation of tasks, purchase orders, transfer orders, and Service Catalog requests.

If the value of the **glide.sc.checkout.twostep** system property is set to **true**, then the **CartJS** API adds items to the cart but the requests aren't submitted automatically. Instead, the request submission requires additional actions to be performed, affecting the automatic flow of the Stock Rule Runner job.

The **pending\_delivery** is used to indicate whether a stock rule is awaiting fulfillment or delivery. The pending\_delivery can be set to any of the following values:

-   When this flag is set to **true**, the stock rule is in progress, and the system doesn't generate duplicate tasks or orders for the same item.
-   When this flag is set to **false**, the system reprocesses the stock rule and triggers the creation of tasks and orders again.

**Note:** Make sure that the pending\_delivery flag is updated to false when a stock rule has been processed, enabling the Stock Rule Runner job to run without redundancy.

Based on the Stock rule type and the plugin activated on your ServiceNow instance, the Stock Rule Runner job creates purchase orders, transfer orders, Service Catalog requests, or tasks.

**Important:**

If the Procurement plugin and the Hardware Asset Management application aren't activated, the Stock Rule Runner job creates a task instead of a purchase order or a Service Catalog request. This task prompts the stockroom manager to take the necessary actions to replenish the inventory.

<table id="table_xsx_532_d2c"><thead><tr><th>

Stock rule type

</th><th>

Orders/Requests created

</th></tr></thead><tbody><tr><td>

Stockroom

</td><td>

A transfer order is created automatically when the inventory in a stockroom reaches the threshold set by the stock rule. The transfer order is created to transfer stock from another stockroom to replenish the inventory.

**Note:** If a transfer order is already in progress, then additional transfer orders aren't created.

</td></tr><tr><td>

Vendor

</td><td>

When the Procurement plugin \(com.snc.procurement\) is activated, a purchase order and corresponding purchase order line items are created.Purchase orders and purchase order line items are created when the inventory in a stockroom reaches the defined threshold and needs replenishment directly from the vendor.

**Note:** You must have a procurement\_user role to access the purchase order and purchase order line item.

</td></tr><tr><td>

Vendor or Service Catalog

</td><td>

When the Hardware Asset Management application is installed and the stock rule is set to Vendor or Service Catalog, then note the following points:-   The Stock Rule Runner job submits a Service Catalog request instead of creating a purchase order.
-   The Service Catalog request is automatically submitted for stock replenishment through the Service Catalog. The items are added to the Service Catalog cart for the Stockroom manager to review and approve.
-   The pending\_delivery flag is used to track the status of the Service Catalog requests. This flag guarantees that the Service Catalog requests are processed correctly, avoiding duplicate actions.

</td></tr></tbody>
</table>**Related topics**  


[Create a stock rule](c_Stockrooms.md#)

### Create a stock rule

Create a stock rule to control what happens when the inventory of a particular asset in a particular stockroom reaches a specified threshold.

#### Before you begin

Role required: inventory\_admin

#### Procedure

1.  Create a stock rule.

<table id="choicetable_ggf_c2c_tfc"><thead><tr><th align="left" id="d447429e1171">

Interface

</th><th align="left" id="d447429e1174">

Action

</th></tr></thead><tbody><tr><td id="d447429e1180">

**Core UI**

</td><td>

1.  Navigate to **All** &gt; **Inventory** &gt; **Stock** &gt; **Stock Rules**.
2.  Select **New**.


</td></tr><tr><td id="d447429e1216">

**Hardware Asset Workspace**

</td><td>

1.  Navigate to **Asset operations** &gt; **** &gt; **Inventory**.
2.  From the Inventory list, select **Stock rules**.
3.  Select **New**.


</td></tr></tbody>
</table>2.  On the form, fill in the fields.

<table id="table_ns3_kxf_zfc"><thead><tr><th>

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

Quantity that the stock must reach to trigger restocking. For example, enter a threshold of 10 for a laptop computer that should be restocked when inventory drops below 10 in the specified stockroom.**Note:** If a stock rule is created for a hardware or software model reaches the threshold limit, a notification is sent to the stockroom manager and a stock order request is automatically created.

</td></tr><tr><td>

Restocking option

</td><td>

Location where additional supplies should come from. If Procurement isn’t active, then restocking option is **Stockroom** only. Otherwise, select one of the following:

 -   **Stockroom**: Creates a transfer order to obtain the asset from another stockroom.
-   **Vendor**: Sends an email to the stockroom manager to order from a vendor. In addition to the email notification, a purchase order and purchase order line item are created.
**Important:** Once a transfer order, purchase order, or purchase order line item is created, it's important to act on it promptly. Any email notifications or reminders won't be sent for these actions.

</td></tr><tr><td>

Active

</td><td>

Option for enabling the stock rule for restocking automatically.

</td></tr><tr><td>

Stockroom

</td><td>

Current physical location of the asset.

</td></tr><tr><td>

Order size

</td><td>

Minimum order quantity for stockroom transfers or vendor purchases. ServiceNow calculates the smallest multiple of the order size needed to restock the item above the threshold. For example, there are 3 laptops in stock with a threshold of 10 and the **Stockroom** option selected. If the order size is set to 4, the system creates a transfer order for 8 laptops to exceed the threshold and satisfy the rule \(3 in stock + 8 ordered = 11\). When restocking from a vendor, ServiceNow sends an email to the stockroom manager showing the total number of items to order, as multiples of the order size.

</td></tr></tbody>
</table>3.  Select **Submit** or **Save**.


#### Result

-   The stock rule that you created appears in the **Stock rules** tab.
-   If the restocking option was set to **Vendor**, the **Stock orders** tab will be displayed. All the stock orders that are created using this stock rule are listed under the Stock orders tab.

    **Important:** The Stock orders tab is available with Hardware Asset Management version 13.0.0 and later.

-   If the restocking option was set to **Stockroom**, the **Transfer orders** tab will be displayed. All the transfers orders created using this stock rule are listed under the **Transfer orders** tab.

    **Important:** The Transfer orders tab is available with Hardware Asset Management version 13.0.0 and later.

    For stock orders created through the restocking by a vendor, the stock order tab shows all stock orders generated by that stock rule. But for transfer orders, the tab only displays transfer orders after the upgrade.


**Related topics**  


[Stock rules](c_Stockrooms.md#)

