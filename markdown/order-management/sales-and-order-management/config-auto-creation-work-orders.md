---
title: Configuring automatic creation of work orders
description: You can enable automatic creation of work orders from Order Management for Telecommunications, Media, and Technology to Field Service Management. Work orders are created for domain orders and order tasks. To configure the automatic creation of work orders, configure the decision tables in the decision builder.Add a condition in the decision tree for automatic creation of work orders for domain order. The conditions are specified in the Work Order Policy for Domain Order decision table.Add a condition in the decision tree for automatic creation of work orders for order tasks. The conditions are specified in the Work Order Policy for Order Task decision table.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: concept
last_updated: "2024-08-01"
reading_time_minutes: 3
breadcrumb: [Order Management integration with Field Service Management, Extending Order Management with ServiceNow applications and integrations, Sales Customer Relationship Management]
---

# Configuring automatic creation of work orders

You can enable automatic creation of work orders from Order Management for Telecommunications, Media, and Technology to Field Service Management. Work orders are created for domain orders and order tasks. To configure the automatic creation of work orders, configure the decision tables in the decision builder.

Customer orders have multiple order line items that have multiple domain orders, such as product orders, service orders, resource orders, and order tasks. For automatic creation of work orders for a domain order, the conditions are specified in the Work Order Policy for Domain Order decision table. For the automatic creation of work orders for order tasks, the conditions are defined in the Work Order Policy for Order Task decision table.

After an order is approved by the manager, a work order is automatically created if the conditions that are defined in the decision builder are met. If required, the manager can also select **Create Work Order** to create a work order manually. The work order template in the decision table pre-populates the fields of the automatically created work order.

## Configure work order creation for a domain order

Add a condition in the decision tree for automatic creation of work orders for domain order. The conditions are specified in the Work Order Policy for Domain Order decision table.

### Before you begin

Role required: admin

### About this task

Customer Orders have multiple order line items that have multiple domain orders, such as product orders, service orders, resource orders, and order tasks. For automatic creation of work orders for a domain order, the conditions are specified in the Work Order Policy for Domain Order decision table. For conditions not defined in the decision table, the manager can select **Create Work Order** to create a work order manually. The work order template in the decision table pre-populates the fields of the automatically created work order.

### Procedure

1.  Navigate to **All** &gt; **Decision Builder**.

    You can view all the decision tables.

2.  Select the **Work Order Policy for Domain Order** decision table.

3.  In the **Specification** column of the conditions section, select the service package to set a condition.

4.  Select an action from the Domain Order Action list.

5.  Select a template for the condition in the **WO Template** column.

6.  Select **Save**.


### Result

A condition is added in the decision table. If this condition in the decision table is met, a work order is automatically created for a domain order. For more information on decision tables, see [Use decision tables](https://www.servicenow.com/docs/access?context=use-decision-tables&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

## Configure work order creation for order task

Add a condition in the decision tree for automatic creation of work orders for order tasks. The conditions are specified in the Work Order Policy for Order Task decision table.

### Before you begin

Role required: Administrator

### About this task

For the automatic creation of work orders for order tasks, the conditions are defined in the Work Order Policy for Order Task decision table. After an order is approved by the manager, a work order is automatically created if the conditions are met that are defined in the decision builder.

### Procedure

1.  Navigate to **All** &gt; **Decision Builder**.

    You can view all the decision tables.

2.  Select the **Work Order Policy for Order Task** decision table.

3.  In the **Specification** column of the conditions section, select the service package to set a condition.

4.  Select **Add** for Domain Order Action.

5.  Select a Request type for the order task in the **Request Type** column.

6.  Select a template for the service package in the **WO Template** column.

7.  Select **Save**.


### Result

A condition is added in the decision table. If this condition in the decision tree is met, a work order is automatically created for an order task. For information, see [Decision Builder user interface](https://www.servicenow.com/docs/access?context=decision-builder-user-interface&version=xanadu&pubname=xanadu-build-workflows&ft:locale=en-US).

