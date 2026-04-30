---
title: Put away enterprise assets using the ServiceNow Agent application
description: Scan available assets in the inventory and perform asset put away in the designated scanned drop-off location.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2025-05-09"
reading_time_minutes: 1
keywords: [asset put away task, put away asset]
breadcrumb: [Manage enterprise asset put away using the ServiceNow Agent application, Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Put away enterprise assets using the ServiceNow Agent application

Scan available assets in the inventory and perform asset put away in the designated scanned drop-off location.

## Before you begin

Role required: inventory\_user

## About this task

The inventory user can scan the available assets in the inventory and put them away in the scanned aisle-space in the stockroom. The Enterprise Asset Management application checks the existence of an active put away task for the asset and makes the required update in the Enterprise Asset Workspace.

-   If an active Asset put away task exists, the task is closed when the asset is placed in the designated stockroom location.
-   If an active Asset put away task doesn't exist for the asset, then a task is created and closed when the asset is placed in the designated stockroom location.

## Procedure

1.  From your mobile device, launch the Now Mobile Agent application.

2.  On the navigation bar, tap the **Asset put away** menu.

    ![Asset put away menu](../../hardware-asset-management/image/asset-put-away-task-ma.png)

    The Asset put away page is displayed.

3.  Enter or scan the asset serial number and tap **Next**.

    ![Scan asset serial number](../../hardware-asset-management/image/asset-putaway-scan.png)

    You can scan multiple assets at a time. All the scanned asset serial numbers are listed in the **Review** tab.

    ![Review scanned assets](../../hardware-asset-management/image/asset-putaway-review-tab.png)

4.  Enter or scan the drop-off location and tap **Submit**.

    ![Asset put away Drop-off location](../../hardware-asset-management/image/asset-putaway-dropoff-location.png)


## Result

A confirmation message appears on the mobile screen showing the number of put away tasks closed.

**Parent Topic:**[Manage enterprise asset put away using the ServiceNow Agent application](../concept/manage-asset-put-away-eam-mobile-agent.md)

