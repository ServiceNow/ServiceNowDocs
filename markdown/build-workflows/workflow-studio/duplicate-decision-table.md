---
title: Duplicate a decision table
description: Save time creating similar decision tables by duplicating existing tables in Workflow Studio.
locale: en-US
release: zurich
product: Workflow Studio
classification: workflow-studio
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 1
breadcrumb: [Using decision tables, Use, Workflow Studio, Build workflows]
---

# Duplicate a decision table

Save time creating similar decision tables by duplicating existing tables in Workflow Studio.

## Before you begin

Role required: admin, decision\_table\_admin, or delegated developer

## Procedure

1.  Navigate to **All** &gt; **Process Automation** &gt; **Workflow Studio**.

2.  On the homepage, select **Decision tables**.

3.  Open the decision table you want to duplicate.

4.  Select the Decision table menu options icon \(![](../image/dec-table-menu-options.png)\) and select **Duplicate Decision Table**.

5.  On the form, fill in the fields.

<table id="table_jg4_vzd_qqb"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

New decision table name

</td><td>

Name for the decision table. This field pre-fills with `Duplicate of <original table name>`.

</td></tr><tr><td>

Application

</td><td>

Application scope for the decision table.

</td></tr><tr><td>

Version to duplicate

</td><td>

Version of the table you want to duplicate. This field is only available when draft authoring is enabled on the original table and there is a draft and a published version. You can select **Draft** or **Published**.

</td></tr><tr><td>

Include decision rows

</td><td>

Option to include the decision rows as well as the structure of the original table.This option is limited to tables with 300 rows or fewer. If your table has more than 300 rows, this feature is not available, and you can only duplicate the structure, not the rows.

</td></tr></tbody>
</table>6.  Select **Duplicate**.


**Parent Topic:**[Using decision tables](../concept/using-decision-builder.md)

