---
title: Create a custom validation definition
description: Provide a script that validates a context rule input or output in the decision table for a pricing or product eligibility matrix.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Configuring matrix validation rules, Configuring product pricing, Configuring Sales Customer Relationship Management applications, Sales Customer Relationship Management]
---

# Create a custom validation definition

Provide a script that validates a context rule input or output in the decision table for a pricing or product eligibility matrix.

## Before you begin

Role required: admin

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../image/Lists.png) view.

2.  Navigate to **Context Rule Management** &gt; **Validation Definitions**.

3.  Select **New**.

4.  In the **Script** field, enter the custom script that defines the error check, warning messages, and error messages for the validation.

5.  If the decision condition won’t be active by default, select **Inactivate decision condition**.

6.  Enter the **Name** of the validation definition.

7.  Select **Save**.

8.  Associate the custom definition to a rule matrix.

    1.  Navigate to **Context Rule Management** &gt; **Matrix Validations**.

    2.  Select **New**.

    3.  In the **Matrix type** field, select the rule matrix to which this custom validation definition applies.

9.  Select **Save**.


