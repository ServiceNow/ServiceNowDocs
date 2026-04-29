---
title: Table rotation
description: Optimize performance and manage data lifecycle by rotating tables, allowing older data to be systematically archived while maintaining system efficiency.
locale: en-US
release: australia
topic_type: concept
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Applying database rotation techniques, Data Management, Tables and data, Configure core features, Administer the ServiceNow AI Platform]
---

# Table rotation

Optimize performance and manage data lifecycle by rotating tables, allowing older data to be systematically archived while maintaining system efficiency.

Table rotation preserves instance performance and averts risk associated with querying growing data sets. This feature uses the sys\_created\_on field to separate data sets into multiple tables based on date.

-   **Functionality**

    The administrator specifies the time parameter \(duration\) of the process and the number of tables \(rotations\) within. After the rotation writes the last table in a rotation, the rotation overwrites the first table in the rotation.

    Examples:

    -   The query `Records created between 2015/12/10 08:49 and 2015/12/09 07/34 where topic=SystemCommand` is translated to a SQL query on a single table, because the clause on **sys\_created\_on** targets a single shard.
    -   The query `Records updated between 2015/12/10 08:49 and 2015/12/09 07/34 where topic=SystemCommand`, or without a date range, needs to target all shards and therefore is translated as a union query on all shards.
-   **Advantages**
    -   Allows deletion of old data without affecting current data \(for example, to drop or truncate a table\).
    -   Ensures tables only grow to a reasonable size.
    -   Reduces working set of data when date is known for query.
-   **Disadvantages**
    -   Queries that do not use the table rotation date \(for example, by using the **sys\_created\_on** field\), force an inefficient union query to query time ranges that span multiple tables and can be extremely slow if the number of sub-tables is large.

        To improve performance, it is recommended that the query includes a window of created dates.

    -   Users can't dot-walk to a rotated table.

You can use table rotation for sequentially-written tables or for insert-only tables. You cannot use table rotation for sys\_import tables or tables that extend the Task \[task\] table.

-   **[Apply table rotation](../task/t_ApplyTableRotation.md)**  
Preserve instance performance by applying table rotation.

**Parent Topic:**[Applying database rotation techniques](../../database-rotation/concept/c_DatabaseRotation.md)

**Related topics**  


[Activate database rotation](../../database-rotation/task/t_ActivateDatabaseRotation.md)

[Table extension](../../managing-data/concept/table-extension.md)

