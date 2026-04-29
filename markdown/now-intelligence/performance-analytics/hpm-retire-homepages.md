---
title: Retire a homepage
description: Use the homepage migration status table to retire homepages. When you retire a homepage, you remove visibility and editing options from all but the admin.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 1
breadcrumb: [Homepage deprecation, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Retire a homepage

Use the homepage migration status table to retire homepages. When you retire a homepage, you remove visibility and editing options from all but the admin.

## Before you begin

Role required: admin or dashboard\_admin.

1.  Disable the creation of new homepages: Set the system property **com.glideapp.home.deprecate\_homepages** to true.

    **Important:** When set to true, this property disables the creation of new homepages and sets the default start page or landing page to Dashboards. Menu items and URLs that open homepages will continue to point to those homepages. Otherwise, homepages are unavailable and should be migrated using this tool.

2.  [Populate the homepage migration status table](hpm-populate-hp-status-table.md).

**Note:**

When you retire a homepage, users can no longer select the associated portal pages and only the admin has read and write permissions on the pages.

To configure the time limit to respond to a retirement request, edit the system property **sn\_home\_page\_depr.approval\_due\_date**.

## Procedure

1.  Navigate to **All** &gt; **Homepage deprecation help tool** &gt; **Homepage migration status**.

2.  Check the boxes next to the homepages that you want to retire.

3.  From the **Actions on selected rows** menu, select `Retire`.

    ![Homepage migration status table with three homepages selected and the Actions on selected rows menu open with Retire option highlighted](../image/hp-migration-status-retire.png)

    -   If the homepage is a Global homepage, meaning one with no specified owner, it is retired and the task state is set to **Closed complete** immediately.
    -   If there is no response from the owner of a personal homepage within the time limit, the homepage is retired and the task state is set to **Closed complete**.
    -   If the owner rejects the retirement request, the homepage is converted to a dashboard.

## Result

Changes are made on the homepage migration status table.

-   Entries in the State column for the converted homepages are changed to **Closed complete**.
-   Entries in the Decision column for retired homepages are changed to **Retired**.
-   Entries in the Decision column for homepages the owner rejects for retirement are changed to **Converted**.
-   Personal homepages of users who are inactive or locked out no longer appear on the **Personal homepages** tab of the Homepage deprecation dashboard.
-   Read and write permissions for retired homepages are limited to admin.

## What to do next

[Restore a homepage](hpm-restore-homepages.md)

