---
title: Delete a data fabric table
description: Remove a data fabric table from your instance by deleting it.
locale: en-US
release: australia
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Manage data fabric tables, Zero Copy Connectors, Workflow Data Fabric]
---

# Delete a data fabric table

Remove a data fabric table from your instance by deleting it.

## Before you begin

Role required: One of the following role combinations or admin.

-   delegated\_developer with sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms OR sn\_dd\_&lt;application\_scope\_name&gt;\_delegatedadmin, and a role containing the df\_data\_steward role
-   delegated\_developer with sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms OR sn\_dd\_&lt;application\_scope\_name&gt;\_delegatedadmin, and df\_connection\_admin

## Procedure

1.  Navigate to the **Data fabric tables** tab in the Zero Copy Connector Hub in one of the following ways:

    -   Navigate to **All** &gt; **Zero Copy Connector Hub** &gt; **Data fabric tables**
    -   Navigate to **Admin** &gt; **Zero Copy Connector Hub** &gt; **Data fabric tables**.
2.  Delete a data fabric table.

    1.  Find the data fabric table that you want to delete.

    2.  Select the More Actions icon \(![More actions icon](../../../administer/integrationhub/images/more-actions-menu-icon.png)\), and select **Delete**.

    3.  Confirm that you want to remove the table by selecting **Delete**.


## Result

The data fabric table is deleted and its data is no longer available on your instance.

**Parent Topic:**[Managing data fabric tables](../concept/managing-data-fabric-tables-zcc.md)

