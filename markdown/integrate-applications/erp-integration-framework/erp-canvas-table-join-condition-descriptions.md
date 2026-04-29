---
title: Zero Copy Connector for ERP table join conditions field descriptions
description: The Table join condition form in Zero Copy Connector for ERP enables you to create and edit join conditions for tables in a ERP \(Enterprise Resource Planning\) model.
locale: en-US
release: australia
product: ERP Integration Framework
classification: erp-integration-framework
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
keywords: [erp, canvas, erp canvas, integration, data hub, zero, copy, connector, sap, table, join, condition]
breadcrumb: [Zero Copy Connector for ERP field descriptions, Reference, Zero Copy Connector for ERP overview, Workflow Data Fabric]
---

# Zero Copy Connector for ERP table join conditions field descriptions

The Table join condition form in Zero Copy Connector for ERP enables you to create and edit join conditions for tables in a ERP \(Enterprise Resource Planning\) model.

Table joins link different tables through shared fields. Joins enable you to access data from multiple tables based on logical relationships between them. The relationship can be conditional, which you specify using join conditions. Use inner joins or outer joins. An inner join returns records that have matching values in both tables. Outer joins combine left and right join results to return all rows with matches or NULLS.

Join fields defines the common attribute or key used to connect records in a child table with their corresponding parent records.

For process details, see [Add joins between ERP tables](../task/erp-canvas-add-join-data-model.md).

<table id="table_alq_dmh_cyb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

ERP model table field

</td><td>

Name of the join field on the ERP system of record, which represents an attribute or column in the table where data is stored.

</td></tr><tr><td>

ERP model

</td><td>

ERP model that the join condition applies to.

</td></tr><tr><td>

Field value

</td><td>

Value for the field in the ERP model table that triggers the join.

</td></tr><tr><td>

Order

</td><td>

Numerical value that indicates which part of the join occurs first.This number determines the order join condition position relative to other items, helping to establish the prioritization.

</td></tr><tr><td>

Operator

</td><td>

Operator that defines the conditions for your query. Operators determine how the values are evaluated and filtered in the query results. The following are supported operators:

-   equals
-   contains
-   greater than
-   greater than or equal
-   less than
-   less than or equal
-   not equals

</td></tr><tr><td>

Statement operator

</td><td>

Operator that defines the condition or comparison in your statement. The options are `AND` and `OR`.

</td></tr></tbody>
</table>**Parent Topic:**[Zero Copy Connector for ERP field descriptions](erp-canvas-field-descriptions.md)

