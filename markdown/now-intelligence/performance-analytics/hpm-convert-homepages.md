---
title: Convert homepages to individual dashboards
description: Populate the Homepage migration status table and then determine which homepages to convert to dashboards. You can convert homepages to individual dashboards or you can convert multiple homepages to tabs on the same dashboard.
locale: en-US
release: xanadu
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 1
breadcrumb: [Homepage deprecation help tool, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Convert homepages to individual dashboards

Populate the Homepage migration status table and then determine which homepages to convert to dashboards. You can convert homepages to individual dashboards or you can convert multiple homepages to tabs on the same dashboard.

## Before you begin

Role required: admin or dashboard\_admin.

## Procedure

1.  Navigate to **All** &gt; **Homepage deprecation help tool** &gt; **Homepage migration status**.

    All unaddressed homepages have the state **Open**.

2.  Select the boxes next to the homepages that you want to convert.

3.  From the **Actions on selected rows** menu, select `Convert`.

    ![Homepage migration status table with two homepages selected and the Actions on selected rows menu open with Convert option highlighted](../image/hp-migration-status-convert-1.png)

    The Convert flow triggers the script to create a separate dashboard and move the permissions canRead and canWrite to the dashboard's permission.

    The Retire flow automatically retires personal homepages, and sets the **Selectable** field to false and assigns the read/write permission to the admin user.

    The flow asks permission of owners of non-personal homepages to retire them. The permission flow includes a 14-day waiting period for permission.


## Result

Users no longer have access to converted homepages. They can find the dashboard versions of their homepages on the Dashboards overview. Navigate to **All** &gt; **Self Service** &gt; **Dashboards**. Select the **All** tab to show all dashboards that you have permission to view.

-   The Dashboard column is populated with the names of the new dashboards and links to the dashboards' forms.
-   Entries in the **State** column for the converted dashboards are changed to Closed complete.
-   Entries in the **Decision** column are changed to Converted.

![Results of the conversion of two homepages to dashboards in the Homepage migration status table](../image/hp-migration-status-converted.png)

## What to do next

Update menus that open converted homepages to open the new dashboards.

Navigate to **All** &gt; **Self Service** &gt; **Dashboards**. Open the **All** tab to see the tiles for the converted dashboards.

[Retire a homepage](hpm-retire-homepages.md).

