---
title: Create a rule entity filter
description: Create a rule filter for the product entity to be used in a product eligibility matrix. The rule filter defines how the rule is applied, for example to a product catalog, category, or offering.
locale: en-US
release: zurich
product: Sales and Order Management
classification: sales-and-order-management
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Product offer eligibility, Product offerings and catalogs, Lead-to-cash foundation apps, Configure, Sales Customer Relationship Management]
---

# Create a rule entity filter

Create a rule filter for the product entity to be used in a product eligibility matrix. The rule filter defines how the rule is applied, for example to a product catalog, category, or offering.

## Before you begin

Determine the entity to which the filter applies, for example a particular product catalog, category, or a product offering.

Role required: sn\_prd\_pm\_product\_catalog\_admin and sn\_prd\_pm\_product\_catalog\_manager

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![image.Lists] view.

2.  Navigate to **Context Rule Management** &gt; **Rule Entity Filter**.

3.  Select **New**.

    On the form, fill in the fields.

<table id="table_ztv_ndr_dcc"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Filter Name

</td><td>

Name of the filter, for example `Ineligible offers for CA`.

</td></tr><tr><td>

Entity

</td><td>

Product entity for the rule:-   Product catalog
-   Product offering category
-   Product offering


</td></tr><tr><td>

Filter type

</td><td>

Type of filter to be applied:-   Static: Use a particular list to filter the product entity.
-   Dynamic: Set the conditions to filter the entity.


</td></tr><tr><td>

Code

</td><td>

System-generated alphanumeric number based on the filter name.

</td></tr><tr><td>

Product &lt;catalogs, categories, or offerings&gt;

</td><td>

The product catalog, category, or offering to be filtered, based on the **Entity** selected. This field appears only when Static is selected as the **Filter type**.

</td></tr><tr><td>

Condition

</td><td>

Condition to be used to filter the entity. Use the **Set conditions** builder to specify the conditions. This field appears only when Dynamic is selected as the **Filter type**.

</td></tr></tbody>
</table>4.  Select **Save**.

    The rule filter can now be used in a product eligibility matrix.


