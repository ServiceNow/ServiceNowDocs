---
title: Relationship registry new record form
description: Use the Relationship registry record form to create a relationship registry between objects.
locale: en-US
release: yokohama
product: GRC: Business Continuity Management Components
classification: grc-business-continuity-management-components
topic_type: reference
last_updated: "2025-01-30"
reading_time_minutes: 1
breadcrumb: [Create a relationship registry record, Data Relationships Framework, Reference, Business Continuity Management, Governance, Risk, and Compliance]
---

# Relationship registry new record form

Use the Relationship registry record form to create a relationship registry between objects.

## Relationship registry new record form

<table id="table_jjg_syg_rzb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Name

</td><td>

Name of the relationship registry record. For example, BIA analysis –&gt; Issue.

</td></tr><tr><td>

Table

</td><td>

Table used to set up the relationship registry record. For example, Impact analysis \[sn\_bia\_analysis\].

</td></tr><tr><td>

Relationship type

</td><td>

Relationship type for the relationship registry record. Available options are:-   **One-to-one**: One record has a relationship to one record in another table.
-   **One-to-many**: One record has a relationship to one or more records in another table.
-   **Many-to-many**: One or more records have a relationship to one or more records in another table.
-   **Scripted relationship**: Use scripts to define the relationship between the tables.

</td></tr><tr><td>

Active

</td><td>

Option to indicate that the relationship registry record is active.

</td></tr><tr><td>

Relationship

</td><td>

Table used to set up the relationship with the object that is defined in the **Table** field. For example, Issue \[sn\_grc\_issue\].

</td></tr><tr><td>

Relationship table

</td><td>

Read-only field. The table selected in the **Relationship** field is displayed as a relationship table by default. For example, Issue \[sn\_grc\_issue\].

</td></tr></tbody>
</table>**Parent Topic:**[Create a relationship registry record](../task/create-a-rela-registry-record.md)

