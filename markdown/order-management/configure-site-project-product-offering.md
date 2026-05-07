---
title: Configure project oversight for Product offering
description: Specify the conditions and decision rules that qualify the product offering for site project oversight. You also specify the project template task used by Order Management to create the project for product offerings.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Setting up project oversight conditions and decision rules, Configuring the Strategic Portfolio Management integration, Order Management integration with Strategic Portfolio Management, Integrate, Sales Customer Relationship Management]
---

# Configure project oversight for Product offering

Specify the conditions and decision rules that qualify the product offering for site project oversight. You also specify the project template task used by Order Management to create the project for product offerings.

## Before you begin

Role required: admin

## About this task

Use the Site project management oversight for product offering Decision Builder to add or change the conditions and decision rules that a product offering and location must meet to be tracked as a site project.

For example, if you want site projects to be created for a specific location, you can add Specific Location in the result section.

## Procedure

1.  Navigate to **All** &gt; **Decision Management** &gt; **Decision Builder**.

2.  Select the **Site Project Management Oversight for Product Offerings** decision table.

    The Product Offering item is displayed in the **Inputs** and the **Project Template Task** and Location columns in the **Results**.

3.  Add a condition that a Product Offering must match.

    1.  Select **Add Condition column**.

    2.  On the form, fill in the fields.

<table id="table_uky_vvw_zxb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Condition column label

</td><td>

Label for the column.

</td></tr><tr><td>

Description

</td><td>

Brief overview of the condition.

</td></tr><tr><td>

Input

</td><td>

Input linked to the condition column.To evaluate multiple fields, you can add multiple conditions with the Reference input type.

</td></tr><tr><td>

Table

</td><td>

If the data type is Reference, the name of the reference table is displayed.For Product Offerings, the table is Product Offering \[sn\_prd\_pm\_product\_offering\].

</td></tr><tr><td>

Data to evaluate

</td><td>

For condition columns with the input type of Reference, specifies whether the condition column evaluates the reference record or a field on the reference table.To evaluate a particular field, select **Field** and choose a field from the Product Offering table, such as **Specification** \(Product Offering.specification\) to specify a product.

</td></tr><tr><td>

Condition type

</td><td>

Data type selected for the condition column.

</td></tr><tr><td>

Default operator

</td><td>

How every row in the condition column evaluates a user-specified value. A default operator is required for all input data types except for True or False.

</td></tr></tbody>
</table>    3.  Select **Save**.

    4.  Repeat steps 3a through 3c for each condition to be added.

4.  Enter a decision rule by selecting **Add new decision row**.

    1.  Select the **Add** action and enter the conditions, Site Project template, and location.

        **Note:** The location doesn't has to be the full location. If the full location isn’t found, it looks for the parent location.

    2.  Select **Save**.

    3.  Repeat steps 4a through 4c for each decision rule to be added.


