---
title: Components installed with Spend and Savings Management
description: Several types of components are installed with activation of the Spend and Savings Management \(sn\_spend\_mgmt\) plugin, including user roles and tables.
locale: en-US
release: zurich
product: Sourcing and Procurement Operations
classification: sourcing-and-procurement-operations
topic_type: reference
last_updated: "2025-11-17"
reading_time_minutes: 1
breadcrumb: [Spend and Savings Management, Explore, Sourcing and Procurement Operations, Finance and Supply Chain]
---

# Components installed with Spend and Savings Management

Several types of components are installed with activation of the Spend and Savings Management \(sn\_spend\_mgmt\) plugin, including user roles and tables.

## Roles installed

|Role title \[name\]|Description|Contains roles|
|-------------------|-----------|--------------|
|sn\_spend\_mgmt.category\_manager\_admin|Can import the category taxonomy, update the Spend Category and Spend Category Stage tables and update the Spend category to Product category mappings.|None|
|sn\_spend\_mgmt.sourcing\_category\_manager|Can view and access the Category management tab and the Savings dashboard in Spend and Savings Management.|sn\_shop.procurement\_specialist|

## Tables installed

<table id="table_y4x_m1n_3hc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Spend Category \(sn\_spend\_mgmt\_category\)

</td><td>

Stores data about spend categories.

</td></tr><tr><td>

Spend Category Stage \(sn\_spend\_mgmt\_category\_stage\)

</td><td>

Temporarily stores important data about spend categories before this data is sent to the Spend Category \(sn\_spend\_mgmt\_category\) primary table.Extends the Import Set Row \(sys\_import\_set\_row\) table.

</td></tr><tr><td>

Spend to Product Category Mapping\(sn\_spend\_mgmt\_m2m\_spend\_product\)

</td><td>

Stores the mapping of spend categories to product categories.

</td></tr></tbody>
</table>**Parent Topic:**[Spend and Savings Management](../concept/spo-spend-mgmt.md)

