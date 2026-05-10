---
title: Create a compatibility rule
description: Create a compatibility rule in the product catalog to define the horizontal relationships between your product, service, and resource specifications.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configuring compatibility rules, Configuring product offerings and catalogs, Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Create a compatibility rule

Create a compatibility rule in the product catalog to define the horizontal relationships between your product, service, and resource specifications.

## Before you begin

Role required: sn\_prd\_pm.product\_catalog\_manager, sn\_prd\_pm\_adv.catalog\_creator

## Procedure

1.  In the CSM Configurable Workspace, select the **List** ![](../../../reuse/icons/product-icons/list-outline-24.svg) view.

2.  Navigate to **Rules** &gt; **Compatibility Rule**.

3.  Select **New**, and then fill in the fields.

<table id="table_db1_lb1_stb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

System-assigned number for the compatibility rule.

</td></tr><tr><td>

Name

</td><td>

Name of the compatibility rule.

</td></tr><tr><td>

Description

</td><td>

Description of the compatibility rule.

</td></tr><tr><td>

State

</td><td>

State of the compatibility rule:-   **Draft \(Default\)**

Unpublished draft compatibility rule that is created when you fill in the fields and submit the compatibility rule.

-   **Published**

Published compatibility rule that is created when you formally publish it after defining the source and target specifications for a product, service, or resource.

**Note:** Only published compatibility rules are considered for the order capture and fulfillment process.

-   **Archived**

Compatibility rule that is no longer used in the product catalog.

</td></tr><tr><td>

Rule

</td><td>

Name of the compatibility rule based on the source configuration. Displays when the rule is saved.

</td></tr></tbody>
</table>4.  In the Source Configuration section, select the product specification to be the source of the compatibility rule.

5.  In the Available columns section, select the characteristics.

    The selected characteristics are displayed in the Selected columns section.

6.  Select **Save**.

7.  In the Conditions section, use the condition builder to create one or more conditions to specify the characteristic options used in the compatibility rule.

8.  Select **Save**.


## What to do next

[Create compatible records in compatibility rules](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/order-management/order-mgt-create-compatibles.md).

