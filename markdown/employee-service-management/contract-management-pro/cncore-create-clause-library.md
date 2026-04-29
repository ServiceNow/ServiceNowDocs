---
title: Create or edit a contract clause
description: As a contract configurator, create or modify clauses that manage clause variations that are mapped to contract templates.
locale: en-US
release: australia
product: Contract Management Pro
classification: contract-management-pro
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Configure dynamic clauses for contract templates, Configure contract templates, Configure, Contract Management Pro, Legal and Contract Operations, Employee Service Management]
---

# Create or edit a contract clause

As a contract configurator, create or modify clauses that manage clause variations that are mapped to contract templates.

## Before you begin

Role required: sn\_cm\_core.contract\_config

## Procedure

1.  Navigate to **All** &gt; **Contracts Core** &gt; **Contracts Administration** &gt; **Clause Management**.

2.  Choose whether you are creating a new clause or modifying an existing clause.

    -   To create a clause, select **New**.
    -   To modify an existing clause, open a clause from the list.
3.  On the form, fill in the fields.

<table id="table_qfw_c4s_ypb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Number

</td><td>

This field is automatically populated with a unique number.

</td></tr><tr><td>

Name

</td><td>

Unique name for the clause.

</td></tr><tr><td>

Contract Type

</td><td>

Type of contract for which you want to associate the clause.**Note:** Only active contract types are displayed in the list.

</td></tr><tr><td>

Table

</td><td>

Table to which you want to associate the clause.**Note:** The Contract Request table \[sn\_cm\_core\_contract\_request\] is selected by default to centralize the configuration on a single table and improve reusability across product lines. You can choose to configure the clause library on a different table.

Example: If you select Legal Contract Request table, the clause will appear only for the templates associated to that table.

</td></tr><tr><td>

Description

</td><td>

Information about the clause.

</td></tr><tr><td>

Application

</td><td>

Application to which the clause belongs. This field is automatically set to the application scope in which you’re creating the clause.

</td></tr><tr><td>

Active

</td><td>

Option to make the clause active and available for use. **Note:** While editing an existing clause, you can’t set the clause as inactive if an active clause variation is present.

</td></tr></tbody>
</table>4.  Right-click in the form header and select **Save**.

    The clause is saved and the related lists for Clause variations and Templates appear.

5.  Save the clause.

    -   To save a new clause, select **Submit**.
    -   To save the changes to an existing clause, select **Update**.
    ![Create a clause and clause variations](../image/cmpro-cls-mgmt-new.png "Clause form")


## What to do next

Create clause variations to use them in the document template for a predefined condition. For more information, see [Create a clause variation](cncore-add-clauses-doc-tmplt.md).

**Parent Topic:**[Configure dynamic clauses for contract templates](../concept/cncore-clause-and-cv.md)

