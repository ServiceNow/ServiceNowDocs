---
title: Configure install base
description: Track which products and services have been purchased by a customer, how they've been installed or provisioned, along with the detailed configuration for each installed item.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Configure product data, Product data, Set up your environment, Configuring Customer Service Management, Customer Service Management]
---

# Configure install base

Track which products and services have been purchased by a customer, how they've been installed or provisioned, along with the detailed configuration for each installed item.

## Before you begin

Role required: admin

## About this task

Install the Customer Service Install Base Management plugin \(com.snc.install\_base\) from the ServiceNow Store.

Capture the install base for a customer by creating sold products, install base items, and installed products. This would enable the customer service agents to trace issues back to the relevant product, instances of that product, and other entities impacting their functioning.

Before setting up your install base, create your product data by creating or importing product models. For more information, see [Configure product data](configure-csm-products.md).

This example shows the summary of the customer's purchase on the Solana microwave.

![Solana corporation sells 800 series microwave in different colors and two capacity choices. Boxeo installed one model in their break room in the office as installed base and manages it.](../image/install-base-example.png "Using install base management")

There are three parts to setting up your install base.

<table id="table_ekf_rwq_rgb"><tbody><tr><td>

Sold Products

</td><td>

Create a sold product to provide customers, consumers, and customer service agents visibility into the products and services sold to an account or a consumer.

</td></tr><tr><td>

Install Base Items

</td><td>

Create an install base item to track instances that have been provisioned for an account or consumer. An install base item can be any configuration item that has been made accessible to customers. For Software as a Service \(SaaS\) products, an install base item refers to an application service configuration item.

</td></tr><tr><td>

Installed Products

</td><td>

Create an installed product to track information on the instances that a sold product is deployed on at an account or consumer. A sold product can have multiple installed product records depending on the number of instances of the product in use.

</td></tr></tbody>
</table>You can create sold products, install base items, and installed products as individual records, import them in bulk, or create them from an Account or Consumer record.

Customer service agents can view install base information in Agent Workspace. Customers can view install base information on the Customer Service Portal.

## Procedure

1.  Navigate to **All** &gt; **Customer Service** &gt; **Administration** &gt; **Guided Setup**.

2.  On the Getting Started page of the guided setup, click **Get Started**

3.  In the Foundation Data category, view the list of tasks to configure the feature.

    |Task|Description|
    |----|-----------|
    |Import Sold Products|Import sold products to track the products or services sold to an account or consumer.|
    |Import Install Base Items|Import install base items that represent the items installed or provisioned for a customer.|
    |Import Installed Products|Import installed products to create an association between sold products and install base items.|

4.  To perform a task, click **Configure**.

    This button opens the page in your instance where the configuration is completed.


