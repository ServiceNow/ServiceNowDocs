---
title: Supending sold products
description: Suspend sold products to create a suspend order or quote on the CSM Configurable Workspace.Create an order to suspend a sold product and its hierarchy on the CSM Configurable Workspace. By suspending a sold product, you can reduce the number of canceled products or services and take the time to fix that product or service.Create an order to suspend multiple sold product and their hierarchy on the CSM Configurable Workspace. By suspending a sold product, you can reduce the number of canceled products or services and take the time to fix that product or service.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 4
breadcrumb: [Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Supending sold products

Suspend sold products to create a suspend order or quote on the CSM Configurable Workspace.

Supend single or multiple root sold products and create combined orders for suspension and resumption of products and servies at the same time, to improve agent efficiency.

|Task|Description|
|----|-----------|
|Suspend a single sold product|[Suspend a single sold product](supending_sold_products.md#)|
|Suspend multiple sold products|[Suspend multiple sold products](supending_sold_products.md#)|

## Suspend a single sold product

Create an order to suspend a sold product and its hierarchy on the CSM Configurable Workspace. By suspending a sold product, you can reduce the number of canceled products or services and take the time to fix that product or service.

### About this task

After an order is created and marked **Complete**, the order to sold product flow is triggered after fulfillment. This flow enables you to suspend a sold product.

**Note:** You can also indefinitely suspend a sold product without creating a resume order.

### Before you begin

Role required: sn\_ind\_tmt\_orm.order\_admin or sn\_ind\_tmt\_orm.order\_agent

### Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the sold product belongs to.

4.  In the Sold Products related list, select the sold product that you want to suspend.

    **Note:** You can do a **Suspend** action on the root sold product only if it is in the **Active** state. The sold product must not have a specification that is associated with it. The **Suspend** option isn't visible if you select a child sold product.

5.  Select **Suspend**.

6.  In the Suspend sold product window, in the **Start date and time** field, enter the start date and time that you want to start the suspension.

    **Note:** If you fill in only the **Start date and time** field, a suspend order line item is created. A resume order line item is created within the same order header if the **End date and time** field is also filled in.

7.  Add a reason for a suspension in the **Reason for suspension** field.

    For example, a disturbance due to a renovation can be a reason for suspension.

8.  Select **Suspend**.


### Result

An order with the suspend action is created for the suspend order line items. If you specify an end date and time, a resume order line item is created as a part of the same order. When you update the suspend action line item to **Complete**, the sold product state automatically updates to **Suspended**. When you move the state of the resume action line item to **Completed**, the sold product state updates to the **Active** state. The **Resume** action is enabled only if you set the state of the sold product as **Inactive**.

## Suspend multiple sold products

Create an order to suspend multiple sold product and their hierarchy on the CSM Configurable Workspace. By suspending a sold product, you can reduce the number of canceled products or services and take the time to fix that product or service.

### Before you begin

Role required: sn\_ind\_tmt\_orm.order\_admin or sn\_ind\_tmt\_orm.order\_agent

### About this task

After an order is created and marked **Complete**, the order to sold product flow is triggered after fulfillment. This flow creates sold products on the sold product table \(sn\_install\_base\_sold\_product\).

### Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the sold product belongs to.

4.  In the Sold Products related list, select the sold products that you want to suspend.

    **Note:** You can do a **Suspend** action only on root sold products with a product offering and if it is in the **Active** state. The **Suspend** option is disabled if you select a child sold product.

5.  Select **Suspend**.

6.  In the Suspend sold products window, in the **Start date and time** field, enter the start date and time that you want to start the suspension.

    You can see the selected sold products in the accordian.

    **Note:** If you fill in only the **Start date and time** field, a suspend order line item is created. If you fill in the **End date and time** field, a resume order line item is also created within the same order header.

7.  Add a reason for a suspension in the **Reason for suspension** field.

    For example, a disturbance due to a renovation can be a reason for suspension.

8.  Select **Suspend**.


### Result

An order with the suspend action is created. Suspend order line items are created in an asynchronized process. If you specify an end date and time, a resume order line item is also created as a part of the same order.

When you update the suspend order line item to **Complete**, the sold product state automatically updates to **Suspended**.

When you update the state of the resume order line item to **Completed**, the sold product state updates to the **Active** state.

