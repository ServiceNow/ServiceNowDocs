---
title: Allow changes to published pricing and product eligiblity matrices
description: Use the allow\_edit\_on\_published\_matrices system property to allow changes to published pricing and product eligibility matrices.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-11-30"
reading_time_minutes: 1
breadcrumb: [Pricing Management, Configure, price, quote apps, Configure, Sales Customer Relationship Management]
---

# Allow changes to published pricing and product eligiblity matrices

Use the **allow\_edit\_on\_published\_matrices** system property to allow changes to published pricing and product eligibility matrices.

## Before you begin

Role required: admin

## About this task

If your pricing admin or product catalog admins want to change a published pricing or product eligibility matrix, they must create a new version of the matrix. However, as an admin, you can allow changes to published matrices by using the allow\_edit\_on\_published\_matrices system property.

## Procedure

1.  Navigate to **All** and in the filter enter `sys_properties.list`.

2.  Open the **allow\_edit\_on\_published\_matrices** system property.

3.  Set the property value in the **Value** field.

    -   Enter `true` to allow edits to published matrices.
    -   Enter `false` so that published matrices can't be edited. You must generate a new version of the matrix to make changes.
4.  Select **Update**.

    If you enable this property, published matrixes can be updated by pricing and product catalog admins.


