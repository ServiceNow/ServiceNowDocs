---
title: Create an order guide rule to add a catalog item
description: You can add a catalog item to an order guide using specific rules.
locale: en-US
release: australia
product: Service Catalog
classification: service-catalog
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Order guides, Types of catalog items, Explore, Service Catalog, Manage service capabilities, Extend ServiceNow AI Platform capabilities]
---

# Create an order guide rule to add a catalog item

You can add a catalog item to an order guide using specific rules.

## Before you begin

Role required: admin

## About this task

Order guide rules define conditions that must be met for a specific item to be included in an order. For example, a New Employee Hire order guide rule can state that if the new employee job title is CTO or Director, and the department is IT, then add an executive desktop item to the order.

## Procedure

1.  Navigate to **All** &gt; **Service Catalog** &gt; **Catalog Definition** &gt; **Order Guides**.

2.  Open an order guide.

3.  In the **Rule base** related list, click **New**.

4.  On the form, fill in the fields.

<table id="table_kxq_xjn_cr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Guide

</td><td>

The order guide to which the created rules are applied.

</td></tr><tr><td>

At this position

</td><td>

Tab positions are numbered in order from left to right, with the lowest number appearing at the left of the screen.

</td></tr><tr><td>

Application

</td><td>

Name of the application that is being used.

</td></tr><tr><td>

If this condition is true

</td><td>

Conditions that must be true for this rule to apply. Create conditions using the condition builder . Conditions can be evaluated against Keywords, Requested By, Requested For, or any variables defined for that order guide.

</td></tr><tr><td>

Include this item

</td><td>

Item to include in the order if all conditions defined in If this condition is true are matched.**Note:** You can also include record producers in the order guide.

</td></tr><tr><td>

Ignore Mandatory Evaluation

</td><td>

Option to allow customers to proceed without completing mandatory fields for the Describe Needs and Choose Options screens. The mandatory status of a field is determined by the variable defining that field.If mandatory fields are not enforced, then relevant information is not passed on to the ordered items. For example, in a New Employee Hire order guide, if the address is not provided then this information is not included in business cards ordered.

</td></tr><tr><td>

Use cart layout

</td><td>

Option to use the cart layout that has been configured.

</td></tr><tr><td>

Show quantity

</td><td>

Option to display the ordered quantity of a catalog item in the Choose Options section when a customer requests for an order guide through the Service Portal or Now Mobile app. **Note:** If the **Hide Quantity** portal setting is selected while creating or editing a catalog item, the ordered quantity is displayed in the Summary section but not in the Choose Options section.

</td></tr><tr><td>

Quantity

</td><td>

Option to select the default quantity of a catalog item for the order guide. When quantity is shown, this value can be modified during checkout.

</td></tr></tbody>
</table>5.  Click **Submit**.


**Parent Topic:**[Order guides](../concept/c_ServiceCatalogOrderGuides.md)

