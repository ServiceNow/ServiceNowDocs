---
title: Enable relationship aggregation
description: The Process Last Month CI Costs scheduled job processes costs of configuration items. To start aggregating expenses to parents, identify the relationships to use for aggregation. Because there are many options for CMDB relationships, using all available paths for aggregation is generally not efficient.
locale: en-US
release: xanadu
product: Cost Management
classification: cost-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [CI rate cards, Cost Management, Strategic Portfolio Management]
---

# Enable relationship aggregation

The Process Last Month CI Costs scheduled job processes costs of configuration items. To start aggregating expenses to parents, identify the relationships to use for aggregation. Because there are many options for CMDB relationships, using all available paths for aggregation is generally not efficient.

## Before you begin

Role required: financial\_mgmt\_admin

## About this task

You can have multiple relationships for each child class. For example, to enable only certain relationships or parent classes, create a new record for each type and class combination paired with the child class.

When an expense line is generated from a configuration item cost, the parents of the configuration item are evaluated. The parent class and relationship type are compared to the list of relationship path records to see if there is a match to use for aggregation. If there is a match, an expense line is generated for the parent configuration item. The process repeats for all parents until there are either no parent relationships or the relationships in place do not meet the criteria defined in the relationship path records.

## Procedure

1.  Navigate to **All** &gt; **Cost** &gt; **Administration** &gt; **Relationship Paths**.

2.  Click **New**.

3.  Fill in the fields, as appropriate.

<table id="simpletable_bqs_2lq_3r"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Active

</td><td>

Check box that indicates whether the relationship path is enabled.

</td></tr><tr><td>

Child class

</td><td>

The child configuration item class. This class is the source of the expense generated during configuration item cost processing.

</td></tr><tr><td>

All parent classes

</td><td>

Check box that indicates whether [CI relationships in the CMDB](https://www.servicenow.com/docs/access?context=c_CIRelationships&version=xanadu&pubname=xanadu-servicenow-platform&ft:locale=en-US) to all parent classes are processed.

</td></tr><tr><td>

Parent class

</td><td>

A valid parent CI class for the selected child class. Available only if **All parent classes** is not selected.

</td></tr><tr><td>

All relationships

</td><td>

Check box that indicates whether all relationship types between the child and parent classes are processed.

</td></tr><tr><td>

Relationship type

</td><td>

The type of relationship to process between the child and parent classes. Available only if **All relationships** is selected.

</td></tr></tbody>
</table>
## What to do next

When a configuration item has multiple parents that have valid relationship paths, the amount aggregated to each parent is split to prevent over-aggregation of a item cost. When evaluating parent relationships to active relationship paths, the aggregation counts the total number of valid relationships. The expense line amount from the child configuration item is evenly divided among the number valid paths and that amount is used when creating the inherited expense line for the parent.

**Parent Topic:**[CI rate cards](../concept/c_CIRateCards.md)

