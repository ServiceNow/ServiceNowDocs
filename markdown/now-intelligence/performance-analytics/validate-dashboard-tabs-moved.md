---
title: Validate that tabs are moved to a target dashboard
description: When you move a dashboard with an update set, validate that the tabs are moved to the target instance and are populated.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Move a Core UI dashboard with an update set, Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Validate that tabs are moved to a target dashboard

When you move a dashboard with an update set, validate that the tabs are moved to the target instance and are populated.

## Before you begin

Role required: admin.

## About this task

Moving dashboards from one instance to another requires associating the sys\_id values of dashboard tabs with the sys\_id values of the associated portal pages. This task explains how to find these values and map them to each other if there are problems with moving the dashboard. Perform this task after you [Move a Core UI dashboard with an update set](t_MoveDashboardWithUpdateSet.md).

## Procedure

1.  In the target instance, navigate to the dashboard you have just moved.

2.  Select the context menu icon \(![](../image/icon-context-p.png)\) and select **Dashboard Properties**.

3.  For each tab in the tab form, verify that the required field **Page** \(sys\_portal\_page reference\) is there.

    If every tab has an associated portal page, then the dashboard was successfully moved.

4.  If the portal page in the target instance is missing in any of the tab forms, perform these steps:

    1.  Select the context menu icon \(![](../image/icon-context-p.png)\) in the Tab form and select **Copy sys\_id**.

    2.  In the filter navigator of the source instance, enter `pa_tabs.list`.

    3.  Filter the list to show only the tab with the sys\_id you copied in substep a.

    4.  Select the name of the tab to open its form.

    5.  Select the information icon \(![](../image/IconInformation.png)\) of the Page value for that tab.

    6.  On the **Portal Page**, select the context menu icon \(![](../image/icon-context-p.png)\) and select **Copy sys\_id**.

        Paste this value into the text editor.![Copy sys_id](../../performance-analytics/image/copy-sys-id.png)

        This value is the sys\_id for the portal page. It is different than the sys\_id for the associated tab that you have already used. These values are used together to map the tab to the portal page.

    7.  Select the search icon \(![](../../../common/image/List_SearchIcon.png)\) associated with the **Page** field.

    8.  In the pop-up window, filter on the portal page sys\_id and select the returned query result.

    9.  Select **Update** in the Tab form to save your changes.

5.  Ensure that all of the objects used in the dashboard, such as widgets, data visualizations, and content blocks are migrated to the target instance.

    The associated portal page should be visible in the target instance.

6.  If you can't find the portal page in the target, perform the following:

    1.  Follow Step 4 a-f to obtain the sys\_id of the portal page on the source instance.

    2.  In the source instance, navigate to **Homepage Admin** &gt; **Pages**.

    3.  Filter the list to show only the portal page with the sys\_id you copied.

    4.  Right-click the record and select **Unload Portal Page**.![Portal page record context menu with the item Unload portal page selected.](../../performance-analytics/image/unload-portal-page.png)

    5.  Move the update set to another instance using standard update set functionality.

        For more information, see [Retrieve an update set](https://www.servicenow.com/docs/access?context=t_RetrieveAnUpdateSet&version=australia&pubname=australia-application-development&ft:locale=en-US).


