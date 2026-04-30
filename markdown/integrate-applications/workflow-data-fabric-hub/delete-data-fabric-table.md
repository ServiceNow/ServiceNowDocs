---
title: Delete a data fabric table
description: Remove a data fabric table from your instance by deleting it.
locale: en-US
release: yokohama
product: Workflow Data Fabric Hub
classification: workflow-data-fabric-hub
topic_type: task
last_updated: "2025-03-25"
reading_time_minutes: 1
breadcrumb: [Managing data fabric tables in Workflow Data Fabric Hub, Workflow Data Fabric Hub, Data and Automation]
---

# Delete a data fabric table

Remove a data fabric table from your instance by deleting it.

## Before you begin

Role required: One of the following role combinations or admin.

-   delegated\_developer with sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms OR sn\_dd\_&lt;application\_scope\_name&gt;\_delegatedadmin, and a role containing the df\_data\_steward role
-   delegated\_developer with sn\_dd\_&lt;application\_scope\_name&gt;\_tablesforms OR sn\_dd\_&lt;application\_scope\_name&gt;\_delegatedadmin, and df\_connection\_admin

## Procedure

1.  Navigate to the **Data fabric tables** tab in Workflow Data Fabric Hub in one of the following ways:

    -   Navigate to **All** &gt; **Workflow Data Fabric Hub** &gt; **Data fabric tables**
    -   Navigate to **Admin** &gt; **Workflow Data Fabric Hub** &gt; **Data fabric tables**.
2.  Delete a data fabric table.

    1.  Find the data fabric table that you want to delete.

    2.  Select the More Actions icon \(![More actions icon](../../integrationhub/images/more-actions-menu-icon.png)\), and select **Delete**.

    3.  Confirm that you want to remove the table by selecting **Delete**.


## Result

The data fabric table is deleted and its data is no longer available on your instance.

**Parent Topic:**[Managing data fabric tables in Workflow Data Fabric Hub](../concept/managing-data-fabric-tables-wdf.md)

