---
title: Convert homepages to dashboard tabs
description: After you populate the Homepage migration status table, you can convert one or more homepages to tabs on new or existing dashboards.
locale: en-US
release: zurich
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2023-08-03"
reading_time_minutes: 1
breadcrumb: [Convert homepages to individual dashboards, Homepage deprecation, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Convert homepages to dashboard tabs

After you populate the Homepage migration status table, you can convert one or more homepages to tabs on new or existing dashboards.

## Before you begin

Role required: admin or dashboard\_admin.

**Note:** To convert one or more homepages to dashboard tabs, the homepages must have the same owner.

## Procedure

1.  Navigate to **All** &gt; **Homepage deprecation help tool** &gt; **Homepage migration status**.

    All unaddressed homepages have the state Open.

2.  Select the boxes next to the homepages that you want to convert.

3.  From the **Actions on selected rows** menu, select `Convert to tabs`.

    ![Homepage migration status table with two homepages selected and the Actions on selected rows menu open with Convert to tabs option highlighted](../image/hp-migration-status-convert-2.png)

4.  Select an existing dashboard or set the title for a new dashboard.

    If you select an existing dashboard, the homepages are added as tabs after the existing tabs. If you set a title for a new dashboard, the new dashboard includes tabs for each of the homepages that you added.

    The convert flow triggers the script to create a new separate dashboard and move the permissions canRead and canWrite to the dashboard's permission.


## Result

Users no longer have access to converted homepages. They can find the dashboard versions of their homepages on the Dashboards overview. Navigate to **All** &gt; **Self Service** &gt; **Dashboards**. Select the **All** tab to show all dashboards that you have permission to view.

-   The Dashboard column is populated with the names of the new dashboards and links to the dashboards' forms.
-   The Dashboard Tab column is populated with the names of the new dashboard tabs and links to the dashboard tabs' forms.
-   Entries in the State column for the converted dashboards are changed to Closed complete.
-   Entries in the Decision column are changed to Converted.

![Results of the conversion of two homepages to dashboards in the Homepage migration status table](../image/hp-migration-status-converted.png)

## What to do next

Update menus that point to the converted homepages to point to the new dashboards.

Navigate to **All** &gt; **Self Service** &gt; **Dashboards**. Open the **All** tab to see the tiles for the converted dashboards.

[Retire a homepage](hpm-retire-homepages.md).

