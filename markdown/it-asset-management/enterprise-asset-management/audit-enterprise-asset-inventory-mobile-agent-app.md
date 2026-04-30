---
title: Scan enterprise assets for stockroom inventory audits using the Mobile Agent application
description: Use the ServiceNow Mobile Agent application to scan the enterprise assets that you want to include in your stockroom inventory audits. After you scan all enterprise assets, you can complete the audit on your ServiceNow instance. Use your audit results to understand where your enterprise assets are located and what their current status is.
locale: en-US
release: xanadu
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2024-08-01"
reading_time_minutes: 4
breadcrumb: [Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Scan enterprise assets for stockroom inventory audits using the Mobile Agent application

Use the ServiceNow® Mobile Agent application to scan the enterprise assets that you want to include in your stockroom inventory audits. After you scan all enterprise assets, you can complete the audit on your ServiceNow instance. Use your audit results to understand where your enterprise assets are located and what their current status is.

## Before you begin

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **Enterprise Asset** tab.

    The navigation bar displays tabs for the ServiceNow applications and applets that you have access to through the Mobile Agent application. The navigation bar also displays tabs for your Mobile Agent application settings and notifications.

    The home screen for the Enterprise Asset Management application opens.

    ![Enterprise Asset Management home screen in the ServiceNow Mobile Agent application.](../image/eam-mobile-agent-app-home-screen.png)

3.  Tap **Stockroom audits**.

    The Stockroom audits screen opens, where you can view all open and completed audits.

4.  If the desired stockroom audit does not already exist, open a new stockroom audit.

    1.  Tap the more options menu at the top right corner of the screen.

    2.  When the menu opens, tap **New stockroom audit**.

        The New stockroom audit screen opens.

    3.  Select the stockroom that you want to audit.

    4.  In the **Aisle space** field, select the aisle and space within the stockroom where you want to perform the audit.

        This field is available with Enterprise Asset Management version 9.0 and later.

    5.  In the **Model category field**, select the model category that you want to audit.

        This field is available with Enterprise Asset Management version 9.0 and later.

    6.  Tap **Submit**.

        You automatically return to the Stockroom audits screen, which displays the new stockroom audit on the **Open** tab.

5.  On the **Open** tab, tap the stockroom audit that you want to complete.

    The stockroom audit record opens.

6.  On the **Details** tab of the stockroom audit record, tap **Scan**.

    The Asset scan screen opens.

7.  Use the camera on your mobile device to scan the asset tag of the enterprise asset that you want to include in the audit.

    You can also enter the asset tag value manually in the **Asset Tag** field.

8.  Tap the Enter key on the keyboard of your mobile device.

    The enterprise asset is automatically added to the **Review** tab of the Asset scan screen.

9.  Repeat steps 7 and 8 for every enterprise asset that you want to include in the audit.

10. After you scan or enter the asset tag value for all desired enterprise assets, go to the **Review** tab to verify the complete list.

    If you want to remove any enterprise assets from the list, tap the Delete icon \(![Delete icon.](../image/delete-icon-mobile-agent-app.png)\) for that enterprise asset.

11. Tap **Submit**.

    The Asset scan screen closes and you automatically return to the stockroom audit record. On the **Details** tab of the stockroom audit record, the **Expected**, **Not expected and location corrected**, **Missing**, and **New** fields update based on the enterprise assets that you just scanned or entered the asset tag value for.

12. Tap the more options menu at the top right corner of the screen.

13. When the menu opens, tap **Complete**.


## What to do next

Complete the inventory audit on your ServiceNow instance. See [Audit enterprise asset inventory](audit-eam-assetinventory.md) for detailed instructions.

**Parent Topic:**[Managing enterprise assets and tasks using the Mobile Agent application](../concept/manage-enterprise-assets-tasks-mobile-app.md)

**Related topics**  


[Create an enterprise asset in the Mobile Agent application](create-enterprise-asset-mobile-agent-app.md)

[Look up enterprise assets using the Mobile Agent application](lookup-enterprise-assets-mobile-agent-app.md)

[Scan enterprise assets for location inventory audits using the Mobile Agent application](audit-enterprise-asset-location-mobile-agent-app.md)

[Verify and depart your enterprise assets for disposal using the Mobile Agent application](dispose-enterprise-assets-mobile-agent-app.md)

[Manage an Enterprise Asset Management task using the Mobile Agent application](work-order-mobile-agent-eam.md)

[Manage enterprise asset repair tasks using the Mobile Agent application](../concept/repair-orders-mobile-agent-eam.md)

[Manage enterprise asset pick tasks using the Mobile Agent application](../concept/manage-asset-pick-task-eam-mobile-app.md)

[Manage enterprise asset put away using the ServiceNow Agent application](../concept/manage-asset-put-away-eam-mobile-agent.md)

[Manage Drop off tasks for enterprise assets using the Mobile Agent application](../concept/manage-dropoff-mobile-agent.md)

