---
title: Create shopping controls
description: Set conditions to control the visibility of supplier products for an employee or a department who visits the Shopping Hub portal. Shopping Hub administrators can manage access to products based on categories, suppliers, or any attribute related to a supplier product.​
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Setting up primary data for Shopping Hub, Configure, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Create shopping controls

Set conditions to control the visibility of supplier products for an employee or a department who visits the Shopping Hub portal. Shopping Hub administrators can manage access to products based on categories, suppliers, or any attribute related to a supplier product.​

## Before you begin

Role required: sn\_shop.shopping\_hub\_admin

## About this task

Employees who meet these conditions cannot see products from specified suppliers or product categories while browsing or searching on the Shopping Hub portal.

For example, you define a shopping control for an employee, Jane Doe, to exclude visibility for all products of the Apparel and Bags category. So, Jane Doe cannot see any products of this category on the Shopping Hub portal.

Also, these supplier products are not visible on the Shopping Hub portal when another employee shops as a delegate on behalf of Jane Doe.

Shopping controls can be overridden with employee credits. For details, see [Shopping controls overridden by credits](../reference/shopping-controls-overridden.md).

## Procedure

1.  Navigate to **All** &gt; **ShoppingHub** &gt; **Administration** &gt; **Shopping Controls**.

2.  Select **New**.

3.  On the form, fill in the fields.

<table id="table_icw_knt_zkb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Short description

</td><td>

Description of the shopping controlFor example, **Shopping Control for Jane Doe**.

</td></tr><tr><td>

Active

</td><td>

Check box to determine if this shopping control is active.

</td></tr><tr><td class="sub-head" colspan="2">

Employee Exclusion Criteria section

</td></tr><tr><td>

User criteria

</td><td>

Select from existing user criteria to whom the controls must apply.

</td></tr><tr><td>

User conditions

</td><td>

Define conditions to identify the user to whom the shopping controls must apply. For example, **User ID** **is** **jane.doe**.

</td></tr><tr><td class="sub-head" colspan="2">

Supplier Product Criteria section

</td></tr><tr><td>

Exclude supplier products if

</td><td>

Define conditions to identify products that must not be visible to the employees who meet the defined user conditions.For example,

 **Product Category** **is** **Computer Displays** **OR**

 **Max known price** **is** **1000 USD**.

</td></tr></tbody>
</table>    **Note:**

    If the shopping control is set to **Active**, a scheduled job is run once per day to find and update any new users or supplier products with the appropriate controls. This job considers:

    -   Users created after the last scheduled job run time.
    -   Supplier products created after the last scheduled job run time
4.  Select **Submit**.


## What to do next

-   Apply the shopping control to your users and product catalog:
    1.  Open the shopping control record you created.
    2.  Select **Implement control**.
    3.  Reload the form:
        -   The User Control related list is populated with the records of users as defined in Employee Exclusion Criteria.
        -   The Supplier Products related list is populated with the records of supplier products that meet the conditions in Supplier Product Criteria.
-   You can choose to deactivate any active shopping control.

    1.  Deselect the **Active** check box.
    2.  select **Update**
    Any user which references to this shopping control is then updated so that this control is no longer applied to that user. On reloading the form, you can see that the User Control and Supplier Products related lists are empty.


**Parent Topic:**[Setting up primary data for Shopping Hub](../reference/set-up-master-data-shopping-hub.md)

