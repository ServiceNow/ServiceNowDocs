---
title: Stock rules
description: Stock rules are defined criteria stating that when the inventory of a particular asset in a particular stockroom reaches a specified threshold, a certain number should either be transferred from another stockroom or ordered from a vendor.
locale: en-US
release: zurich
product: Asset Management
classification: asset-management
topic_type: concept
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Stockrooms, Use, Asset Management, IT Asset Management]
---

# Stock rules

Stock rules are defined criteria stating that when the inventory of a particular asset in a particular stockroom reaches a specified threshold, a certain number should either be transferred from another stockroom or ordered from a vendor.

For example, a specific model of computer keyboard reaches an inventory of 10 in a particular stockroom and, because a stock rule is in place, a transfer order is automatically created to transfer 50 from a different stockroom. Because there can be multiple assets of a model within a stockroom, stock rules enable you to check all assets fitting the criteria and view a total count.

There are two restocking options:

-   Email notifications can be sent to the stockroom manager \(specified in the **Manager** field on the stockroom record\) through the **Asset Restocking** email action when the inventory of a particular asset in the stockroom reaches a specified threshold. You can customize this email notification by updating the details in the following tabs:

    -   **When to send**: Set the conditions under which the email should be triggered.
    -   **Who will receive**: Specify the recipients of the email.
    -   **What it will contain**: Define the content and information included in the email.
    A task is automatically created for the stockroom manager or, if Procurement is active, a purchase order and a purchase order line item are created.

-   A transfer order can be generated automatically to restock the item from another stockroom.

## Stock Rule Runner job

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
</table>**Parent Topic:**[Stockrooms](c_Stockrooms.md)

**Related topics**  


[Create a stock rule](../task/t_CreateAStockRule.md)

