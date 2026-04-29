---
title: Disconnecting sold products
description: Disconnect sold products to create a disconnect order on the CSM Configurable Workspace.Disconnect a sold product in the CSM Configurable Workspace so that you can permanently disconnect a product and its services.Create an order to disconnect multiple sold products and their hierarchy on the CSM Configurable Workspace.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-04-29"
reading_time_minutes: 2
breadcrumb: [Customer Life Cycle Management Workflows, Product data, Set up your environment, Configure, Customer Service Management]
---

# Disconnecting sold products

Disconnect sold products to create a disconnect order on the CSM Configurable Workspace.

Disconnect single or multiple root sold products at the same time, to improve agent efficiency.

|Task|Description|
|----|-----------|
|Disconnect a single sold product|[Disconnect a single sold product](disconnecting_sold_products.md#)|
|Disconnect multiple sold products|[Disconnect multiple sold products](disconnecting_sold_products.md#)|

## Disconnect a single sold product

Disconnect a sold product in the CSM Configurable Workspace so that you can permanently disconnect a product and its services.

### About this task

After an order is created on the order form and is marked **Complete**, a flow is triggered. This flow enables you to disconnect a sold product and its services after fulfillment.

### Before you begin

Role required: sn\_ind\_tmt\_orm.order\_admin or sn\_ind\_tmt\_orm.order\_agent

### Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the sold product belongs to.

4.  From the Sold Products related list, select the sold product that you want to disconnect.

    **Note:** You can do the **Disconnect** action only on one root sold product whose state is **Active** and has a product offering without a specification that is associated with it. The option isn't visible if you select a child sold product.

5.  Select **Disconnect**.

6.  In the Disconnect sold product pop-up window, enter when you want the disconnection to start in the **Start date and time** field and the reason why you want to disconnect the product in the **Reason for disconnection** field.

7.  Select **Submit**.


### Result

An order for a disconnection is created. After the order is fulfilled, the sold product is moved to the **Inactive** state.

## Disconnect multiple sold products

Create an order to disconnect multiple sold products and their hierarchy on the CSM Configurable Workspace.

### About this task

After an order is created and marked **Complete**, the order to sold product flow is triggered after fulfillment. This flow creates sold products on the sold product table \(sn\_install\_base\_sold\_product\).

Role required: sn\_ind\_tmt\_orm.order\_admin or sn\_ind\_tmt\_orm.order\_agent

### Procedure

1.  Navigate to **All** &gt; **CSM/FSM Configurable Workspace.**.

2.  In the list view, select **Customer** &gt; **Accounts**.

3.  Open the account that the sold products belong to.

4.  In the Sold Products related list, select the sold products that you want to disconnect.

    **Note:** You can do a **Disconnect** action only on the root sold product with a product offering only if it is in the **Active** state. The **Disconnect** option is disabled if you select a child-sold product.

5.  Select **Disconnect**.

6.  In the disconnect sold products window, in the **Start date and time** field, enter when you want to disconnect the sold products.

7.  Add a reason for a suspension in the **Reason for disconnection** field.

8.  Select **Disconnect**.


### Result

An order for disconnecting the sold products is created, while order line items are created in an aysnchronized manner.

