---
title: Create a purchasing assignment rule
description: Automatically assign a sourcing request, negotiation, or purchase requisition to a procurement specialist user or a task fulfiller’s group based on pre-defined conditions by using a purchasing assignment rule.
locale: en-US
release: yokohama
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-01-30"
reading_time_minutes: 2
breadcrumb: [Sourcing and Purchasing Automation, Exploring Sourcing and Procurement Operations, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create a purchasing assignment rule

Automatically assign a sourcing request, negotiation, or purchase requisition to a procurement specialist user or a task fulfiller’s group based on pre-defined conditions by using a purchasing assignment rule.

## Before you begin

To create a purchasing assignment rule, you must have set up your product catalog \(with the necessary product categories, product models, and supplier products\) and should be able to raise a purchase request. For more information on how to set up your product catalog, see [Create a product category](create-product-model-categories.md), [Create a product model](create-product-models.md), and [Add a supplier product](add-supplier-product.md). You should have also set up user attributes on the sys\_user record appropriately.

Role required: sn\_shop.procurement\_administrator

## About this task

You can create a purchasing assignment rule to route sourcing requests, negotiations, or purchase requisitions to an individual or group, from the Sourcing and Purchasing Automation module.

## Procedure

1.  Navigate to **All** &gt; **Sourcing and Purchasing Automation** &gt; **Administration ** &gt; **Purchasing Assignment Rules **.

2.  Select **New**.

3.  On the form, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Name|The name you assign to the assignment rule.|
    |Application|The application containing this record. In this case, it displays the default application, which is Sourcing and Procurement Operations.|
    |Active|Option to decide if this rule is in use.|

4.  Select the **Applies To** tab and fill in the fields.

<table id="table_ysk_5rb_glb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Name of the table for which conditions must be set.

</td></tr><tr><td>

Conditions

</td><td>

Combination of conditions that must be met before the task is assigned to a user or group. You must add at least one filter condition, select a field type, and specify a value, for the condition to be set.

 **Note:** The rule is applied only if the task is not already assigned to another user or group.

</td></tr></tbody>
</table>5.  Select the **Assign To** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |User|The user to whom the task is assigned.|
    |Group|The group to which the task is assigned.|

6.  Select the **Script** tab and fill in the fields.

    |Field|Description|
    |-----|-----------|
    |Script|A script to further customize the assignment rule. Scripts provide access to the current pool of variables.|

7.  Select **Submit**.


**Parent Topic:**[Sourcing and Purchasing Automation](../reference/purchase-experience-workflow.md)

