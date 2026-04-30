---
title: Control cascading quantity values in child product offerings
description: Control how the quantities for child line items in a product offering for a quote or order are calculated by using the sn\_prd\_pm.enable\_cascade\_quantity system property.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-11-04"
reading_time_minutes: 1
breadcrumb: [Configuring product offerings and catalogs, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Control cascading quantity values in child product offerings

Control how the quantities for child line items in a product offering for a quote or order are calculated by using the **sn\_prd\_pm.enable\_cascade\_quantity** system property.

## Before you begin

Role required: admin

## About this task

The **sn\_prd\_pm.enable\_cascade\_quantity** system property, if enabled, automatically cascades the quantity value for a top-level offer to child lines, when the quantity for the top-level offer is greater than 1. For example, when an agent creates a quote or an order for a configurable offer and updates the quantity so that it’s greater than 1, the quantity on the child line items is multiplied by the quantity for the top-level offer. Pricing for the child lines is based on the cascaded quantity. If you use the quantity on the child offers as the total quantity ordered, using cascading quantities considers the quantity on the parent offer as well.

However, if you consider the quantity on the child offer as the quantity of the child offer per one quantity of the parent offer, you might not want cascading quantity values.

**Note:** If you're upgrading from a release before the November 2024 release, this property is enabled by default. If you don't want the quantity values to be cascaded to child lines, suppress this feature by setting the property to false.

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Open the **sn\_prd\_pm.enable\_cascade\_quantity** system property.

3.  Set the property value for the cascading quantity feature in the **Value** field.

    -   Enter `true` to activate this property.
    -   Enter `false` to suppress this property if it's currently enabled.
4.  Select **Update**.

    If you enabled this property, quantity values are cascaded to the child lines for product offers. If you suppressed this property, quantity values are not cascaded to the child lines for product offers.


