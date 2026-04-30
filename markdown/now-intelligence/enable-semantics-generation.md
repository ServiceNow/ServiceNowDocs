---
title: Enable semantic generation for tables in the semantic layer
description: Tables can be included in the semantic table configuration but have semantic generation turned off. Enable semantic generation to include that table in Query Generation. Deactivate irrelevant data to improve results.
locale: en-US
release: yokohama
topic_type: task
last_updated: "2025-07-28"
reading_time_minutes: 3
breadcrumb: [Configure, Query Generation, Now Assist in Platform Analytics, Platform Analytics]
---

# Enable semantic generation for tables in the semantic layer

Tables can be included in the semantic table configuration but have semantic generation turned off. Enable semantic generation to include that table in Query Generation. Deactivate irrelevant data to improve results.

## Before you begin

Query Generation must be activated, and the desired table must have a Semantic Table Configuration record. For more information, see [Query Generation skills](enable-query-generation.md) and [Add a table to the semantic data layer](add-table-semantic-layer.md#).

Role required: admin, now\_assist\_explorer\_admin, sn\_query\_gen.admin

## About this task

When a query is generated, the system searches for tables and table columns by looking through the Entities \[sn\_query\_gen\_entity\] and Dimensions \[sn\_query\_gen\_dimension\] tables. It selects a limited set to provide as context for the language model that creates your query. By turning off unused Entities or Dimensions, you help the system focus on the most important data, which makes your queries more accurate and useful.

On the other hand, sometimes a table or table hierarchy is included in the Semantic Table Configuration \[sn\_query\_gen\_table\_config\] table, but semantic generation is deactivated. For example, some CMDB tables are supported by default but have semantic generation disabled. In this case, the performance impact of including these tables can be significant, and you have the option of turning semantic generation on for these tables only if you are sure that you want to. You could also turn semantic generation on and off for a table to test its performance impact, for example.

You can control semantic generation at different levels of granularity depending on whether you control it through the Semantic Table Configurations, Entities, or Dimensions tables, as follows:

-   Semantic Table Configuration: Changes to semantic generation enablement affect the Entities for the main table and all child tables, if included. Changes also affect all Dimensions for those tables.

    **Note:** After you disable semantic generation for a Semantic Table Configuration record, you can reactivate individual Entities in the affected table hierarchy. Doing so reactivates the Dimensions for that Entity and only that Entity.

-   Entity: If you activate or deactivate an Entity record, the change affects only that table but not its parent or sibling tables. However, all of its associated Dimensions are activated or deactivated.
-   Dimension: If you deactivate a Dimension record, only that record is affected.

## Procedure

1.  Navigate to **All** &gt; **Query Generation**.

    If you do not have this navigation path despite having the correct roles, you may be missing the entitlement.

2.  Open one of the following tables:

    -   To disable or enable semantic generation for an entire table hierarchy, navigate to **Administration** &gt; **Semantic Table Config**.
    -   To disable or enable semantic generation for a single table and all its columns, navigate to **Semantic Layer** &gt; **Entities**.
    -   To disable or enable semantic generation for individual columns of a table, navigate to **Semantic Layer** &gt; **Dimensions**.
3.  Locate the table or column of interest.

    **Tip:**

    -   If you are in the Semantic Table Configurations table and the table is not listed, consider adding it as described in [Add a table to the semantic data layer](add-table-semantic-layer.md#).
    -   If you are searching for a deactivated Entity or Dimension, ensure that you have removed the Active = true condition from the list filter.
    -   If you are searching for an Entity that represents a child table in a hierarchy, look for the Semantic Usage Instructions entries that begin with the parent table.
    -   If you are looking for a Dimension record that is associated with a particular Entity, consider searching for that Entity value.
4.  Open the table record.

5.  Toggle semantic generation.

    -   In a Semantic Table Configuration record, change to the correct application scope and select or deselect **Enable Semantic Generation**.

        ![Enable Semantic Generation option on a Semantic Table Generation record.](../image/qgen-disable-semantic-gen.png)

    -   In an Entity or Dimension record, select or deselect **Active**.

        ![Active option on an Entity record.](../image/qgen-entity-deactivate.png)

6.  Select **Update**.


**Parent Topic:**[Configuring Query Generation](../concept/configuring-query-generation.md)

