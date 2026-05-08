---
title: Configure additional questions for checkout
description: As an administrator, you can configure additional questions for full checkout to collect more information from a shopper specific to a purchase. This information is first stored in the Requisition Additional Info staging table against the purchase requisition ID that is created on checkout, and then mapped to the Purchase Requisitions table for back-end consumption.
locale: en-US
release: australia
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Complete your checkout, Using Shopping Hub, Use, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Configure additional questions for checkout

As an administrator, you can configure additional questions for full checkout to collect more information from a shopper specific to a purchase. This information is first stored in the Requisition Additional Info staging table against the purchase requisition ID that is created on checkout, and then mapped to the Purchase Requisitions table for back-end consumption.

## Before you begin

Role required: sn\_shop.procurement\_administrator

## About this task

Use a record producer to create a custom set of questions to ask shoppers during full checkout. Build this record producer in Catalog Builder using the **ShoppingHub additional questions for a PR** template.

![ShoppingHub additional questions for a PR template.](../image/add-questions-pr-template.png)

A record producer can contain the following question types:

-   Text - Single-line
-   Text - Multi-line
-   Choice - Record references
-   Option - Check box
-   Choice - Dropdown \(fixed values\)
-   Date

## Procedure

1.  Create and add the necessary columns in the Requisition Additional Info staging table.

2.  Create and add the same columns in the Purchase Requisitions table.

3.  In Catalog Builder, configure a record producer titled Shopping Hub Additional Questions using the **ShoppingHub additional questions for a PR** template.

    This record producer is used to store more information from a shopper specific to a purchase.

    **Note:** For information on how to create a record producer, see Create a catalog item using a template.

4.  Navigate to **ShoppingHub** &gt; **Administration** &gt; **ShoppingHub Configuration**.

5.  Select the **Additional Information for a Purchase Request** configuration name associated with the **Checkout configuration** type.

6.  Select the **Content details** tab.

    ![ShoppingHub Configuration page showing the Content details tab and Record producer field.](../image/sh-catalog-record-producer.png)

7.  On the **Record producer** field, search for and select the **Shopping Hub Additional Questions** record producer.

    You must first create this record producer using the **ShoppingHub additional questions for a PR** template.

8.  Select **Update**.

9.  In Workflow Studio, map the fields from the Requisition Additional Info staging table to the Purchase Requisitions table.

    **Note:** This flow is automatically triggered when a purchase requisition ID is created as a result of a checkout.


**Parent Topic:**[Complete your checkout](complete-your-checkout.md)

