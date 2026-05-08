---
title: Resuming sold products
description: Resume sold products to create a resume order on the CSM Configurable Workspace.Create an order to resume a sold product and its hierarchy on the CSM Configurable Workspace. By resuming a sold product, you can restart a product or service.Create an order to resume multiple sold products and their hierarchy on the CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-05-07"
reading_time_minutes: 2
breadcrumb: [Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Resuming sold products

Resume sold products to create a resume order on the CSM Configurable Workspace.

Resume single or multiple root sold products and create combined orders for suspension and resumption of products and servies at the same time, to improve agent efficiency.

|Task|Description|
|----|-----------|
|Resume a single sold product|[Resume a single sold product](resuming_sold_products.md#)|
|Resume multiple sold products|[Resume multiple sold products](resuming_sold_products.md#)|

## Resume a single sold product

Create an order to resume a sold product and its hierarchy on the CSM Configurable Workspace. By resuming a sold product, you can restart a product or service.

### About this task

After an order is created and marked **Complete**, the order to sold product flow is triggered after fulfillment. This flow enables you to resume a sold product.

### Before you begin

Role required: sn\_ind\_tmt\_orm.order\_admin or sn\_ind\_tmt\_orm.order\_agent

### Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the sold product belongs to.

4.  In the Sold Products related list, select the sold product that you want to resume.

    **Note:** You can do a **Resume** action on the root sold product only if it is in the **Active** state. The sold product must not have a specification that is associated with it. The **Resume** option isn't visible if you select a child sold product.

5.  Select **Resume**.

    The **Resume** action is enabled on sold products that are in **Inactive** or **Suspended** states only.

6.  In the Resume sold product window, in the **Start date and time** field, enter when you want to resume the sold product.

7.  Select **Resume**.


### Result

An order for resuming the sold product is created.

## Resume multiple sold products

Create an order to resume multiple sold products and their hierarchy on the CSM Configurable Workspace.

### About this task

After an order is created and marked **Complete**, the order to sold product flow is triggered after fulfillment. This flow creates sold products on the sold product table \(sn\_install\_base\_sold\_product\).

Role required: sn\_ind\_tmt\_orm.order\_admin or sn\_ind\_tmt\_orm.order\_agent

### Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the sold product belongs to.

4.  In the Sold Products related list, select the sold products that you want to resume.

    **Note:** You can do a **Resume** action only on the root sold product with a product offering and if it is in the **Inactive** or **Suspended** state. The **Resume** option is disabled if you select a child-sold product.

5.  Select **Resume**.

6.  In the Resume sold products window, in the **Start date and time** field, enter when you want to resume the sold products.

7.  Add a reason for a resumption in the **Reason for resumption** field.

8.  Select **Resume**.


### Result

An order for resuming the sold products is created, while order line items are created in an asynchronized manner.

