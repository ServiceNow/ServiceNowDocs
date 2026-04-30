---
title: Components installed with Customer Engagement Sequences
description: Several types of components are installed with activation of the Customer Engagement Sequences plugin, including tables and user roles.
locale: en-US
release: xanadu
product: Sales and Order Management
classification: sales-and-order-management
topic_type: reference
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Sales Customer Relationship Management]
---

# Components installed with Customer Engagement Sequences

Several types of components are installed with activation of the Customer Engagement Sequences plugin, including tables and user roles.

## Roles installed

<table id="table_fhs_5x3_wfc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Sequence viewer

 \[sn\_crm\_sequence.viewer\]

</td><td>

Views sequence-related records.

</td><td>

sn\_crm\_sequence.sn\_crm\_sequence\_task\_read\_granular

</td></tr><tr><td>

Sequence task read granular

 \[sn\_crm\_sequence.sn\_crm\_sequence\_task\_read\_granular\]

</td><td>

Granular role to grant read access to the sequence task records.

</td><td>

None

</td></tr></tbody>
</table>## Tables installed

<table id="table_jhs_5x3_wfc"><thead><tr><th>

Table

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Customer Engagement Sequence Task

 \[sn\_crm\_sequence\_task\]

</td><td>

Stores the sequence task records that are generated when a sequence is triggered.

</td></tr></tbody>
</table>The Customer Engagement Sequence Task \[sn\_crm\_sequence\_task\] table extends the Task \[task\] table.

