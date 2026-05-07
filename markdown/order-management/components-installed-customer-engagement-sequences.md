---
title: Components installed with Customer Engagement Sequences
description: Several types of components are installed with activation of the Customer Engagement Sequences plugin, including tables and user roles.
locale: en-US
release: australia
topic_type: reference
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Customer Engagement Sequences reference, Lead and opportunity management, Reference, Sales Customer Relationship Management]
---

# Components installed with Customer Engagement Sequences

Several types of components are installed with activation of the Customer Engagement Sequences plugin, including tables and user roles.

## Roles installed

The following roles are installed if you're using Customer Engagement Sequences version 1.0.0.

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
</table>The following roles are installed if you're using Customer Engagement Sequences version 2.0.0:

<table id="table_pnh_fbp_ghc"><thead><tr><th>

Role title \[name\]

</th><th>

Description

</th><th>

Contains roles

</th></tr></thead><tbody><tr><td>

Sequence admin

 \[sn\_crm\_sequence.admin\]

</td><td>

Granular admin role grants full administrative access to all sequence records and their related data.

</td><td>

-   pd\_cancel
-   pd\_content\_author
-   sn\_crm\_sequence.writer

</td></tr><tr><td>

Sequence writer

 \[sn\_crm\_sequence.writer\]

</td><td>

Creates sequence records, and views related records such as sequence tasks and sequence steps.

</td><td>

-   playbook.write
-   sn\_crm\_sequence.executor

</td></tr><tr><td>

Sequence executor

 \[sn\_crm\_sequence.executor\]

</td><td>

Views sequence and sequence task records, and completes activities related to the sequence steps.

</td><td>

-   sn\_crm\_sequence.reader
-   sn\_crm\_sequence.sn\_crm\_sequence\_task\_read\_granular

</td></tr><tr><td>

Sequence reader

 \[sn\_crm\_sequence.reader\]

</td><td>

Views sequence records.

</td><td>

playbook.designer\_access

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

**Parent Topic:**[Customer Engagement Sequences reference](../concept/customer-engagement-sequences-reference.md)

**Related topics**  


[Install Customer Engagement Sequences](../task/install-customer-engagement-sequences.md)

[Using Customer Engagement Sequences](../concept/using-customer-engagement-sequences.md)

