---
title: Configuring order priority and routing
description: As a provider, you can configure various parameters to prioritize and route orders to ensure that they are fulfilled on time.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure, Sales Customer Relationship Management for Telecommunications, Telecommunications, Media, and Technology \(TMT\)]
---

# Configuring order priority and routing

As a provider, you can configure various parameters to prioritize and route orders to ensure that they are fulfilled on time.

Use order prioritization to:

-   Define prioritization rules using various customer, products, service, and order attributes.
-   Assign order priority while creating orders based on the pre-defined rules.
-   Identify urgent orders that need to be fulfilled immediately.
-   Automatically route high priority orders to a specific fulfiller group.
-   Ensure that orders are fulfilled in a committed date.
-   Recalculate order priority when any changes occur.

In Order Management, the order priority is calculated using pre-defined rules based on the following categories of data.

<table id="table_z35_fpn_xvb"><thead><tr><th>

Category

</th><th>

Input

</th></tr></thead><tbody><tr><td>

Customer

</td><td>

Customer account

</td></tr><tr><td>

Specification

</td><td>

-   Product specification
-   Service specification
-   Product offering

</td></tr><tr><td>

Order type

</td><td>

Order line item

</td></tr><tr><td>

Urgency

</td><td>

Order line item

</td></tr></tbody>
</table>**Note:** The inputs used in these decision tables and the rank can be modified according to your business requirements.

These rules are defined in the following decision tables:

-   Order Priority Policy by Customer Attributes
-   Order Priority Policy by Order Type
-   Order Priority Policy by Specification Attributes
-   Order Priority Policy by Urgency

Each parameter defined in the decision table has a rank value assigned to it. When an order is created, the decision tables are evaluated and a weightage is assigned to each table to calculate the order priority. See [Calculating the order priority](order-mgmt-priority-calculate.md) on how the priority is calculated.

**Note:** You can add new inputs, conditions, or modify the existing conditions in the decision tables. For more details on updating decision tables, see [Using decision tables](https://raw.githubusercontent.com/ServiceNow/ServiceNowDocs/australia/markdown/build-workflows/workflow-studio/using-decision-builder.md).

