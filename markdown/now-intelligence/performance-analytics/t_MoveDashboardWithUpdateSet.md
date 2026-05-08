---
title: Move a Core UI dashboard with an update set
description: Portal pages related to dashboard tabs aren’t automatically transferred in update sets. You can add portal pages to update sets from a dashboard record using the Unload Dashboard function. The Unload Dashboard function unloads the entire dashboard with all related tabs, including portal pages.
locale: en-US
release: australia
product: Performance Analytics
classification: performance-analytics
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
keywords: [move a dashboard, move a responsive dashboard]
breadcrumb: [Administering dashboards, Responsive dashboards in the Core UI, Reporting, dashboards, and Performance Analytics in the Core UI, Platform Analytics]
---

# Move a Core UI dashboard with an update set

Portal pages related to dashboard tabs aren’t automatically transferred in update sets. You can add portal pages to update sets from a dashboard record using the **Unload Dashboard** function. The **Unload Dashboard** function unloads the entire dashboard with all related tabs, including portal pages.

## Before you begin

Role required: admin.

## About this task

This procedure describes moving the dashboard structure to an update set. The dashboard structure includes the dashboard itself, tabs, the related security configuration, and dashboard-specific widget settings such as header color, and borders.

This procedure doesn’t move the content of the dashboard \(such as reports, PA widgets, content blocks, and other widgets\) to the update set. You can add dashboard content to the update set using default platform functionality.

**Important:** Make sure that the dashboard content is either in the same update set as the dashboard record or is already present in the target instance. Errors result if the moved dashboard points to content that doesn’t exist on the target instance.

Additional steps may be necessary if you are moving a dashboard on a scoped application. For more information, see [Update set id 'global' is different than update set scope id](../concept/troubleshooting-dashboard-update-set.md#).

**Tip:** If you have difficulty with this procedure, contact Customer Service and Support.

## Procedure

1.  In the source instance, navigate to the location of the dashboard you want to unload, for example, **Self-Service** &gt; **Dashboards**.

2.  Select the dashboard that you want to unload to an update set.

3.  Verify that there’s a portal page record associated with each tab.

    1.  Select the context menu icon \(![](../image/icon-context-p.png)\) and select **Launch Dependency Assessment**.

        ![Dependency assessment example highlighting dashboard and dashboard tab tiles](../image/move-dp-update-da-ex.png)

    2.  Point to the corner of each dashboard tab's tile and select the info icon \(![Admin console tree view info button](../../performance-analytics/image/admin-console-treeview-info.png)\) to see the associated portal page. ![Dependency assessment example with portal page highlighted](../image/dependency-assess-portal-page.png)

4.  Point to the corner of the dashboard's tile and select the info icon \(![Admin console tree view info button](../../performance-analytics/image/admin-console-treeview-info.png)\).

    Select **Open Record** to open the dashboard form.

    The dashboard's tile has the same name as the dashboard itself.

5.  Select the context menu icon \(![](../image/icon-context-p.png)\) and select **Unload Dashboard**.

    Only perform this step after the dashboard is ready to unload, meaning that you’ve added all content to the tabs.

6.  When you’re ready to move the update set, mark the update set as complete.

7.  On the target instance, move the update using standard update set functionality.

    For more information, see Retrieve an update set.

    On the Remote Instance page, the **Retrieved Update Sets** related list shows all retrieved update sets. Select the update set to see if there are errors. Errors are shown on the **Retrieved Update Set** form in a related list called **Update Set Preview Problems**. See [Solving errors on dashboards moved with update sets](../concept/troubleshooting-dashboard-update-set.md#).

8.  On the target instance, make sure that all the tabs of the dashboard have associated portal pages.

    Follow the procedure in [Validate that tabs are moved to a target dashboard](validate-dashboard-tabs-moved.md).

    If the portal page is missing in the Tab form, select the search icon \(![](../../../common/image/List_SearchIcon.png)\) next to the **Page** field to search for the associated portal page.

    **Note:** If you can’t find the associated portal page in the target instance, follow these steps to move each missing portal page through the update:

    1.  Navigate to **Homepage Admin** &gt; **Pages**.
    2.  Filter the list to show only the portal page with the sys\_id you copied when following the procedure in [Validate that tabs are moved to a target dashboard](validate-dashboard-tabs-moved.md).
    3.  Right-click the record and select **Unload Portal Page**.

        ![Portal page record context menu with the item Unload portal page selected.](../../performance-analytics/image/unload-portal-page.png)

        The portal page for the current tab is added to the current update set.

    4.  Move the update set to another instance using standard update set functionality. For more information, see Retrieve an update set.

## Result

The dashboard and its tabs are moved to the target instance.

