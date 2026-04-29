---
title: Set up a configurable product in a Salesforce-integrated environment
description: A configurable product links a blueprint to the configuration experience for the product. Learn how to set up a configurable product in an environment that is integrated with Salesforce. This procedure is valid for users whose Salesforce Managed Package was installed in June 2022 or later.
locale: en-US
release: australia
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up configurable products, CPQ app, Configure, price, quote apps, Configure, Sales and Order Management]
---

# Set up a configurable product in a Salesforce-integrated environment

A configurable product links a blueprint to the configuration experience for the product. Learn how to set up a configurable product in an environment that is integrated with Salesforce. This procedure is valid for users whose Salesforce Managed Package was installed in June 2022 or later.

## Before you begin

Role required: Admin

## About this task

If your CPQ SF Managed Package was installed in June 2022 or later, follow these steps to associate a configurable product with a blueprint.

**Note:** If your CPQ SF Managed Package was installed before June 2022, see [Set up a configurable product in a Salesforce-integrated environment \(older managed package\)](cpq-set-up-a-configurable-product-in-a-salesforce-integrated-environment-older-managed-package.md).

## Procedure

1.  On the Salesforce Products tab, find the Product2 record to connect to a CPQ configuration experience \(blueprint\).

2.  Associate the Product with a Price Book entry.

    The amount can be $0.00, but a value must be entered.

3.  Set the product to **Active** and **Enabled**, and then click **Save**.

4.  On the SFDC Products tab, select the list view to CPQ View.

5.  Find the Product Name of the Product2 record created in step 3, and click the **Click Here** link under View CPQ Setup column.

6.  Click **Associate Blueprint**.

7.  Select the desired blueprint, and then click **Save**.


**Related topics**  


[Set up a configurable product in a headless environment](cpq-set-up-a-configurable-product-in-a-headless-environment.md)

[Set up blueprints](../concept/blueprints_101.md)

