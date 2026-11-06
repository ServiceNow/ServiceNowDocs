---
title: Create compatible records in compatibility rules
description: Create a compatible record in a compatibility rule so that you can define a target specification to establish the horizontal relationship with.
locale: en-US
canonical_url: https://www.servicenow.com/docs/r/australia/order-management/order-mgt-create-compatibles.html
release: australia
topic_type: task
last_updated: "2026-09-10"
reading_time_minutes: 1
breadcrumb: [Configuring compatibility rules, Order management, Configure, Sales Customer Relationship Management]
---

# Create compatible records in compatibility rules

Create a compatible record in a compatibility rule so that you can define a target specification to establish the horizontal relationship with.

## Before you begin

Create a compatibility rule. To learn more, see [Create a compatibility rule](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/create-compatibility-rules.md).

Role required: sn\_prd\_pm.product\_catalog\_manager, sn\_prd\_pm\_adv.catalog\_creator

## About this task

A compatibility record enables you to define the target specification for creating a horizontal relationship with the source specification.

## Procedure

1.  In the CRM Workspace, select the **List** \[Omitted image "list-outline-24.svg"\] Alt text: view.

2.  Navigate to **Rules** &gt; **Compatibility Rule**.

3.  In the Compatibility Rules list, select the compatibility rule that you want to create a compatible record for.

4.  Select **New**, and then fill in the fields.

<table id="table_db1_lb1_stb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Rule

</td><td>

Compatibility rule.

</td></tr><tr><td>

Number

</td><td>

System-assigned number for the compatibility rule.

</td></tr><tr><td>

Name

</td><td>

Name of the compatible.

</td></tr><tr><td>

Description

</td><td>

Description of the compatibility rule.

</td></tr><tr><td>

Relationship type

</td><td>

Relationship type of the compatibility rule: -   **Requires**

The source specification requires the defined target specification in the compatible record.

-   **Excludes**

The source specification doesn't require the defined target specification in the compatible record.

</td></tr><tr><td>

Min Quantity

</td><td>

Minimum number of the target specifications that you want to define in the compatible record.

</td></tr><tr><td>

Max Quantity

</td><td>

Maximum number of the target specifications that you want to define in the compatible record.

</td></tr><tr><td>

Rule

</td><td>

Name of the compatibility rule based on the source configuration. Displays when the rule is saved.

</td></tr></tbody>
</table>5.  Define the target specification in a compatible record to establish the horizontal relationship, which includes the details of a product inventory item in the compatibility rule.

    1.  In the **Specification** field, select the product specification.

    2.  In the Available columns section, select the characteristics to be used in the compatibility rule.

6.  In the Conditions section, use the condition builder to select the characteristic options used in the compatibility rules.

7.  Select **Save**.


**Parent Topic:**[Configuring compatibility rules for horizontal relationships](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/australia/order-management/order-mgt-compatibility-management.md)

