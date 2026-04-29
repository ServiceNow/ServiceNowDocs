---
title: Accept or reject part requests from peer agents
description: Review the part requests that you receive from peer agents.
locale: en-US
release: australia
product: Work Order Management
classification: work-order-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Inventory, ServiceNow Agent mobile app, Completing work on mobile, Use, Field Service Management]
---

# Accept or reject part requests from peer agents

Review the part requests that you receive from peer agents.

## Before you begin

-   The Field Service Advanced Parts Sourcing \(com.snc.fsm\_advanced\_parts\_sourcing\) plugin must be activated. For more information, see [Additional plugins for Field Service Management](../reference/field-service-additional-plugins.md).
-   The **Use part request approvals** property must be enabled to be able to receive part requests from your peer agents. For more information, see [Properties installed with Field Service Management](../../planning-and-policy/reference/r_PropInstallWFieldServMgmnt.md).
-   **Notifications** in the mobile device and Now Mobile Agent app must be enabled to be able to receive mobile push notifications from your peer agents.

Role required: wm\_agent

## Procedure

1.  Open the ServiceNow Agent application.

    **Tip:**

    If you know your inventory and whether you want to reject or accept the request right away, you can do so directly from the notification that appears by selecting **Accept** or **Reject**.

2.  Tap the push notification.

    **Note:** If you cannot access the push notification, access the request by tapping **Inventory**, and then in the **Part requests** section, tapping **Requested from me**.

3.  Check the part availability in your personal stockroom and determine whether you want to accept or reject the part request.

<table id="choicetable_ar5_wkb_35b"><thead><tr><th align="left" id="d142936e147">

Part availability

</th><th align="left" id="d142936e150">

Action

</th></tr></thead><tbody><tr><td id="d142936e156">

**The part is not available**

</td><td>

Tap **Reject**.

</td></tr><tr><td id="d142936e168">

**You cannot transfer the part because you have an insufficient quantity or need the part yourself**

</td><td>

Tap **Reject**.

</td></tr><tr><td id="d142936e180">

**The part is available to fulfill the request**

</td><td>

Review the listed parts, quantities, and any selected hardware assets.-   If the hardware assets match the part request, tap **Accept**.

-   If you need to change the models for hardware assets:

    1.  Tap **Edit Assets**.
    2.  Select the assets that you want to transfer.
    3.  Tap **Submit**.
    4.  Navigate back to the **Part Details** screen.
    5.  Navigate back to the **Part request** screen.
    6.  Tap **Accept**.


</td></tr></tbody>
</table>
## Result

-   If you accept the request, the part request record state changes to Approved and a mobile notification is sent to the requested field service agent. The transfer order lines are created as follows:
    -   For consumable parts, only one transfer order line is created for all requested parts.
    -   For hardware, one transfer order line is created for each asset of the requested parts.
-   If you reject the request, the part request record state changes to Rejected and a mobile notification is sent to the requested field service agent. The rejected part requests can be requested again. For more information, see [Request rejected parts from other stockrooms](request-rejected-parts-from-other-stockrooms.md).

## What to do next

-   [View transfer order lines for requested parts](source-part-mobile.md)
-   [Request rejected parts from other stockrooms](request-rejected-parts-from-other-stockrooms.md)

