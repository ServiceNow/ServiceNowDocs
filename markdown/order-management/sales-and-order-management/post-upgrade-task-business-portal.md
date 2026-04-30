---
title: Post-upgrade order migration for the Business Portal
description: Migrate draft proxy order carts to the new sales cart to avoid having your customers lose products they added to their carts on the Business Portal
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Business Portal, Configure, Sales Customer Relationship Management]
---

# Post-upgrade order migration for the Business Portal

Migrate draft proxy order carts to the new sales cart to avoid having your customers lose products they added to their carts on the Business Portal

## Before you begin

Ensure that the Sales Cart application has been installed. For more information, see [Install Sales Cart](install-sales-cart-plugin.md).

Role required: admin

## About this task

**Note:** If you have used the Business Portal and are upgrading to the Zurich release, you must run the **Migrate proxy orders to sales cart** scheduled job after installing the Sales Cart application. This job migrates the draft proxy order carts to the new sales cart and prevents your customers from losing products added to their carts on the Business Portal.

The **Migrate proxy orders to sales cart** scheduled job performs the following actions:

-   Migrates items from customers' existing cart to the new sales cart
-   Creates cart-related records in the Sales Cart tables
-   Updates the value of the **sn\_sales\_cart.show\_cart\_migration\_msg** property to false

Until you run the this job, the following message is displayed to your customers on the Business Portal:

```
A system update cleared your cart. Please contact your administrator for help.
```

## Procedure

1.  Select **All** &gt; **System Definition** &gt; **Scheduled Jobs**.

2.  On the Scheduled Jobs page, enter `Migrate proxy orders to sales cart` in the search field.

3.  Select the job.

4.  On the Scheduled Script Execution page, select **Execute Now**.


