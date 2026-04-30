---
title: Capacity Function form
description: The Capacity Function form enables you to describe the details for a capacity function record.
locale: en-US
release: zurich
product: Telecommunications Network Inventory
classification: telecommunications-network-inventory
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Reference, Telecommunications Network Inventory]
---

# Capacity Function form

The Capacity Function form enables you to describe the details for a capacity function record.

<table id="table_vhh_t25_mzb"><thead><tr><th>

Field

</th><th>

Value

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the capacity function record.

</td></tr><tr><td>

Application

</td><td>

Application name for which the capacity functions are created.

</td></tr><tr><td>

Description

</td><td>

A brief description about the capacity function.

</td></tr><tr><td>

Function

</td><td>

Type of capacity calculation. Select one from the following.-   **Max**

Maximum number of network assets.

-   **Occupied**

Total number of network assets that are occupied.

-   **Available**

Total number of network assets that are available. It’s the difference between maximum and occupied assets.

-   **Max Contiguous**

Maximum contiguous network assets that are available.


</td></tr><tr><td>

Strategy

</td><td>

Methods for capacity calculation. Select one from the following.-   **Static Value**

A fixed or constant value is used to calculate the capacity. The static value approach uses a predetermined metric to calculate the capacity without considering a field in the record that you query.

-   **Aggregate query count**

A database query that uses an aggregate function to calculate the capacity. In this strategy, you query a related field in a record that is present in the entity table. This type of query is useful for getting summary information about the field in a table, such as the total number of records that meet specific conditions.

-   **Value field**

Use this strategy to check a particular value in a query table, which is present in the database.

-   **Script**

An advanced strategy approach, where a script is used for querying.


Depending on the strategy that you’re selected, additional fields appear in the form. To learn more about the additional fields, see [Capacity function additional fields](capacity-function-additional-fields.md).

</td></tr><tr><td>

Measurement type

</td><td>

Unit of measurement depends on the type of capacity being calculated. Select one from the following.-   Unit
-   Power
-   Weight
-   Slot Unit
-   Port Unit

</td></tr><tr><td>

Order

</td><td>

Order field value.

</td></tr></tbody>
</table>**Parent Topic:**[Telecommunications Network Inventory reference](../concept/telecommunications-network-inventory-reference.md)

**Related topics**  


[Create capacity function](../task/create-capacity-function.md)

[Capacity management](../concept/capacity-management-reporting.md)

