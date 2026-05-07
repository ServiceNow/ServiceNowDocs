---
title: Verify and depart your enterprise assets for disposal using the Mobile Agent application
description: Use the ServiceNow Mobile Agent application to complete the verification and departure of any enterprise assets that you want to dispose of.
locale: en-US
release: australia
product: Enterprise Asset Management
classification: enterprise-asset-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Managing enterprise assets and tasks using the Mobile Agent application, Enterprise Asset Management, IT Asset Management]
---

# Verify and depart your enterprise assets for disposal using the Mobile Agent application

Use the ServiceNow® Mobile Agent application to complete the verification and departure of any enterprise assets that you want to dispose of.

## Before you begin

Before you can complete the verification or departure of an enterprise asset, create a disposal order for that asset. See [Create a disposal order in the Enterprise Asset Workspace](create-eamdisposal-order.md) for detailed instructions.

Role required: sn\_eam.enterprise\_admin or sn\_eam.enterprise\_asset\_manager

## Procedure

1.  From your mobile device, launch the Mobile Agent application.

2.  On the navigation bar at the bottom of the screen, tap the **Enterprise Asset** tab.

    The navigation bar displays tabs for the ServiceNow applications and applets that you have access to through the Mobile Agent application. The navigation bar also displays tabs for your Mobile Agent application settings and notifications.

    The home screen for the Enterprise Asset Management application opens.

3.  Tap **Asset disposal**.

    The Asset disposal screen opens, where you can view all open verification and departure tasks for your enterprise asset disposal orders.

4.  If the enterprise assets that are associated with a disposal order require verification, complete the verification task for that disposal order.

    1.  On the **Verifications** tab, tap the verification task that you want to complete.

        The Verifications screen opens.

    2.  Tap the **Not verified** field to view the complete list of enterprise assets that require verification through this verification task.

    3.  Tap the back arrow at the top left corner of the screen to return to the Verifications screen.

    4.  Tap **Scan**.

        The Scan and verify assets screen opens.

    5.  Use the camera on your mobile device to scan the asset tag of the enterprise asset that you want to verify.

        You can also enter the asset tag value manually in the **Asset Tag** field.

    6.  Tap the Enter key on the keyboard of your mobile device.

        The enterprise asset is automatically added to the **Review** tab of the Scan and verify assets screen.

    7.  Repeat steps e and f for every enterprise asset that you want to verify.

    8.  After you scan or enter the asset tag value for all desired enterprise assets, go to the **Review** tab to verify the complete list.

        If you want to remove any enterprise assets from the list, tap the Delete icon ![](../image/delete-icon-mobile-agent-app.png) for that enterprise asset.

    9.  Tap **Submit**.

        The Scan and verify assets screen closes and you automatically return to the Verifications screen. On the Verifications screen, the **Expected**, **Verified**, and **Not verified** fields update based on the enterprise assets that you just scanned or entered the asset tag value for.

    10. Tap **Complete**.

        The Verifications screen closes and you automatically return to the Asset disposal screen.

5.  If the enterprise assets that are associated with a disposal order require departure, complete the departure task for that disposal order.

    1.  On the **Departures** tab, tap the departure task that you want to complete.

        The Departures screen opens.

    2.  Tap the **Not departed** field to view the complete list of enterprise assets that require departure through this departure task.

    3.  Tap the back arrow at the top left corner of the screen to return to the Departures screen.

    4.  Tap **Scan**.

        The Scan and depart assets screen opens.

    5.  Use the camera on your mobile device to scan the asset tag of the enterprise asset that you want departed.

        You can also enter the asset tag value manually in the **Asset Tag** field.

    6.  Tap the Enter key on the keyboard of your mobile device.

        The enterprise asset is automatically added to the **Review** tab of the Scan and depart assets screen.

    7.  Repeat steps e and f for every enterprise asset that you want departed.

    8.  After you scan or enter the asset tag value for all desired enterprise assets, go to the **Review** tab to verify the complete list.

        If you want to remove any enterprise assets from the list, tap the Delete icon ![](../image/delete-icon-mobile-agent-app.png) for that enterprise asset.

    9.  Tap **Submit**.

        The Scan and depart assets screen closes and you automatically return to the Departures screen. On the Departures screen, the **Expected**, **Departed**, and **Not departed** fields update based on the enterprise assets that you just scanned or entered the asset tag value for.

    10. Tap the **Pickup contact name** field.

        The Pickup contact name screen opens.

    11. In the **Pickup Contact Name** field, enter the name of the person who is picking up the enterprise assets for departure.

    12. Tap **Submit**.

        The Pickup contact name screen closes and you automatically return to the Departures screen. On the Departures screen, the **Pickup contact name** field updates with the name that you entered.

    13. Tap **Complete**.

        The Departures screen closes and you automatically return to the Asset disposal screen.


## What to do next

Complete the remaining disposal order tasks on your ServiceNow instance. See [Enterprise asset disposal order stages](../reference/eamasset-disposalorder-stages.md) for more information on enterprise asset disposal order tasks.

