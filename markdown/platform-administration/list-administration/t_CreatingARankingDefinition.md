---
title: Create a ranking definition
description: Enable context ranking for a related list by creating a ranking definition.
locale: en-US
release: zurich
product: List Administration
classification: list-administration
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 2
breadcrumb: [Context ranking, Administer, List administration, Forms, fields, and lists, Configure core features, Administer]
---

# Create a ranking definition

Enable context ranking for a related list by creating a ranking definition.

## Before you begin

Role required: admin

## Procedure

1.  Navigate to **All** &gt; **System Definition** &gt; **Ranking Definitions**.

2.  Click **New**.

3.  Enter a **Name** for the ranking definition.

4.  In the **Record table** field, select the table for which ranking is enabled.

    This is the table of the records in the ranked related list. For example, to enable ranking for a related list of incidents in the Problem form, select the Incident \[incident\] table.

5.  In the **Context column** field, select the reference column providing the context in which ranking is to be performed.

    The context in this case is the form in which the related list appears and not a table name. For example, a related list with a **Record table** of Incident \[incident\] can have several contexts, including the **Problem** form or a **Configuration item** form.

6.  Complete the relationship-based fields if the ranking is to be performed on a related list that is defined by a relationship.

    -   **Relationship table:** select the table forming the other side of the relationship. In the case of the ranking definition for Product stories in scrum, you might use the Product Model \[cmdb\_model\] table.
    -   **Relationship column:** select the column from the relationship table to compare with the context column. To avoid adding a related list of user stories to the Product Model \[cmdb\_model\] table, you might use the **Sys ID** column, which defines a subclass of the Product Model table \(cmdb\_model.sys\_id\).
7.  In the **Attributes** field, enter attributes to change and restrict the contents of the Rank dialog box, as appropriate.

    -   **visible\_columns:** a semi-colon separated list of columns to be displayed in the Rank dialog box. If not specified, the Rank dialog box uses the default view of the related list you selected in the **Record table** field.
    -   **extra\_conditions:** an encoded query to restrict the records shown in the Rank dialog box. For example, the query `extra_conditions=^state!=7` displays all incidents whose state is not **Closed**. If not specified, the Rank dialog box shows all records for the relationship.
8.  Click **Submit**.

    The index is generated automatically. The system completes these read-only fields:

    -   Index column
    -   Rank ui action
    -   Context menu item
    **Note:** After you submit a ranking definition, only the **Attributes** field can be edited. If additional changes are required, delete the record and create a new one with the revised settings.


## What to do next

The system does not generate indexes for ranking definitions inserted into the database by an update set. To use a ranking definition inserted by an update set, you must generate the indexes manually. To generate indexes, open the Ranking Definition form, and click **Generate Indexes**.

![Generate an index manually](../image/RankingDefinitionForm.png)

**Parent Topic:**[Context ranking](../reference/r_ContextRanking.md)

