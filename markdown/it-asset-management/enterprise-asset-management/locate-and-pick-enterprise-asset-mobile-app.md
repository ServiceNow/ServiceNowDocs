---
title: Locate and pick the enterprise assets in your stockroom using the Mobile Agent application
description: Locate an enterprise asset placed in a specific aisle and space in the stockroom by using indoor maps. After locating the asset, pick and drop off the asset to another location within the stockroom using the Mobile Agent application.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 2
breadcrumb: [Manage enterprise asset pick tasks using the Mobile Agent application, Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Locate and pick the enterprise assets in your stockroom using the Mobile Agent application

Locate an enterprise asset placed in a specific aisle and space in the stockroom by using indoor maps. After locating the asset, pick and drop off the asset to another location within the stockroom using the Mobile Agent application.

## Before you begin

You should explicitly install Indoor Mapping for Assets \(com.sn\_ima\) application from the ServiceNow Store. When you install this application, Indoor Mapping \(sn\_map\_core\) and Indoor Mapping component \(sn\_map\_component\) are also installed.

Role required: inventory\_user

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **My Tasks** tab.

    The home screen of the My Tasks application opens displaying only the first few tasks in the list of tasks assigned to you.

3.  If the task you want to start isn't displayed, tap **See all**.

4.  Filter or sort the task view.

    -   To filter your tasks, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\) and enter the values to use as a filter in the **Due Date**, **Asset**, **Location**, or **Priority** fields.
    -   To sort your tasks, tap the Filter icon \(![Filter icon](../image/filter-mobile-task-eam.png)\), tap **Sort by**, and select the fields by which to sort your tasks.
5.  Tap the Asset pick task for which you have started work.

6.  To locate the enterprise asset in the stockroom, on the **Details** tab, tap **Locate**.

    -   The exact location of the enterprise asset in the stockroom is displayed on the map.
    -   The **Get directions** option is displayed.
7.  Get directions to the asset location in the stockroom.

    1.  Tap **Get directions**.

    2.  Choose the start location on the map.

    3.  Tap **Save**.

    -   The following details are displayed on the map:
        -   Path from the start location to the asset location
        -   Approximate time required for you to reach the asset location
    -   **View steps** and **Scan asset** options are displayed.
8.  To view the route to the asset location, tap **View steps**.

9.  After reaching the asset location, pick the asset.

10. Complete the Asset pick task.

    1.  Tap **Scan asset**.

    2.  Provide the asset tag information.

        -   To provide the information through a scan, scan the asset tag of the asset.
        -   To provide the information manually, enter a value in the **Asset tag** field.
    3.  In the **Drop off location** field, select the space within the stockroom where you want to drop off the asset that you picked.

    4.  Select **Close complete**.

    -   The state of the Asset pick task changes to Closed complete.
    -   The **Location** field of the asset is updated with the drop off location only if you have specified the drop off location.
    -   The Enterprise Asset request flow and Enterprise Refresh Request flow proceed to the next stage.

**Parent Topic:**[Manage enterprise asset pick tasks using the Mobile Agent application](../concept/manage-asset-pick-task-eam-mobile-app.md)

