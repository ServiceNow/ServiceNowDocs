---
title: Create a product adoption roadmap template
description: Create a template that defines a pre-configured adoption strategy with products or capabilities organized into lanes, that can be customized as needed.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Customer success, Customer Success Management, Customer Success Management]
---

# Create a product adoption roadmap template

Create a template that defines a pre-configured adoption strategy with products or capabilities organized into lanes, that can be customized as needed.

## Before you begin

Role required: sn\_acct\_lc.customer\_success\_application\_admin

## About this task

Use templates to define recommended adoption strategies for specific product portfolios. Templates organize products or capabilities into lanes based on your chosen phase field, helping users quickly create roadmaps without planning the adoption approach from scratch. When you create a template, you organize items into lanes to establish the recommended adoption approach, providing a reusable starting point for creating roadmaps.

## Procedure

1.  Navigate to **All** &gt; **Templates** &gt; **** &gt; **All Product Adoption Roadmap Templates** and select **New**.

2.  Fill in the fields in the form.

<table id="table_lxh_ghc_33c"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Enter a name for the template.

</td></tr><tr><td>

Type

</td><td>

Select:-   Product: Organizes products you select in the List of products field.
-   Capability: Organizes capabilities within the selected products.


</td></tr><tr><td>

List of products

</td><td>

Select one or more sold products to be included in the template.

</td></tr><tr><td>

Phase table

</td><td>

Automatically set based on your selection in the Type field. Displays the table \(Product Usage or Product Capability Usage\) that contains the phase field options

</td></tr><tr><td>

Phase field

</td><td>

Select a choice field that defines the lanes for the roadmap. For example, selecting Business criticality creates lanes with choices like Critical, High, Low, and so on.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the template's purpose and the adoption approach it represents.

</td></tr></tbody>
</table>3.  Select **Submit**.

    Template items are automatically created based on your Type and List of products selections.

4.  In the PAR Template Items related list, define your adoption strategy by organizing items into priority lanes.

    All items appear in the Unmapped lane.

    ![Product adoption roadmap template](../image/product-adopt-road-temp.jpg)

5.  To organize the items, follow these steps:

    -   Select the **Unmapped** link for an item to open up the record. In the Lane field, select the priority lane that reflects when this item should be adopted.
    -   In the Lane Order field, enter the number to set the item's position within the lane and select **Update**.
6.  Repeat this step to define your adoption strategy by organizing all items into their recommended lanes and setting priorities.

    The Item order maintains the order within the lane. When specifying the Item order, note the following:

    -   The Item order value starts at 0 and increments by 1 for each item.
    -   For capability roadmaps, the Item order is maintained per capability and per lane.
    -   For product roadmaps, the Item order is maintained per lane.
7.  Select **Publish** to save the template and make it available for use.


## Result

The template is created with items organized into lanes. When you create a roadmap from this template, the items are already arranged according to the template's organization, eliminating the need to organize them from scratch. You can customize the roadmap for your specific needs while maintaining the template's structure.

**Parent Topic:**[Customer success](../concept/account-lifecycle-config-cust-success.md)

**Related topics**  


[View a product adoption roadmap](../concept/account-lifecycle-view-par-roadmap.md)

[Product adoption roadmap](../concept/account-lifecycle-par-roadmap.md)

