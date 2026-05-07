---
title: Process pending approvals for Policy exceptions with the GRC Mobile application
description: Approve or reject pending policy exceptions and policy exception extension requests that are assigned to you.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 5
breadcrumb: [Managing mobile experience for GRC Policy and Compliance, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Process pending approvals for Policy exceptions with the GRC Mobile application

Approve or reject pending policy exceptions and policy exception extension requests that are assigned to you.

## Before you begin

Role required: Compliance manager \(sn\_compliance.manager\)

## About this task

With this applet, you can perform the following tasks on a list of policy exception records:

-   Edit
-   Request more information
-   Approve, or reject pending policy exceptions or extension requests
-   View the details of the record or add a work note prior to processing the request

Time to complete this task: 5-10 minutes.

## Procedure

1.  If you are not logged in to your ServiceNow AI Platform instance on your mobile device, for more information see [Log in to the GRC Mobile application](mobile-login-P-C-app.md).

2.  With the Policy and Compliance landing screen displayed, tap **Policy Exceptions**.

    If you navigate away from the GRC Mobile application after you have logged in, tap the Now Agent app at any time to return to the last screen you had displayed.

    ![Policy Exceptions applet highlighted.](../image/mobile_Policy_and_Compliance_overview-app_rd.png)

    The Policy Exceptions screen is displayed with a list of records.

    ![Policy Exceptions list.](../image/mobile-exception-list.jpg)

3.  If you want to reduce the number of records that are displayed on the screen, see [Filter records with the GRC Mobile application](mobile-pc-set-filters.md) to search for records that match specific search criteria.

    Filtering records on screens in the mobile app works like filtering with a condition builder on the ServiceNow AI Platform. Setting filters can reduce the number of records that are displayed on screens.

4.  To edit, approve or reject, or request more information about a policy exception directly from the list of records displayed on the screen, swipe left on a record to open the menu.

    ![Policy Exception swipe action.](../image/mobile-policy-exception-swip.png)

5.  On the menu that is displayed, choose one from the following table to continue.

<table id="choicetable_khx_51t_xhb"><thead><tr><th align="left" id="d278434e178">

Option

</th><th align="left" id="d278434e181">

Description

</th></tr></thead><tbody><tr><td id="d278434e187">

**Tap the menu icon \(![Swipe menu icon.](../../grc-common/image/mobile-top-menu-rotated.png)\)**

</td><td>

From the fields that are displayed, choose one to continue.-   Tap **Request more information**.

In the Additional comments field, enter a comment to the user who requested the policy exception request. Your request is sent to the originator of the exception request and the extension number is included with your comment. Tap the send icon \(![Send icon.](../../grc-common/image/mobile_instances_send_droid.png)\) or **Submit** to submit your request.

After your request is sent, the option to request more information is no longer available from the menu until the requester provides the information and requests approval once again. If available, tap the **Activity Stream** tab on the policy exception record and refer to the work notes for the audit trail.

-   Tap **Edit** and tap a field to edit the Valid from, Valid to, and Approver fields.

**Note:** Only users from your approval group are available for the Approver field.

Tap the Send icon \(![Send icon.](../../grc-common/image/mobile_instances_send_droid.png)\) or **Submit** to save and submit your changes.

-   Cancel the operation and return to the exception record list.


</td></tr><tr><td id="d278434e251">

**Approve**

</td><td>

In the Additional comments field, enter comments. Comments are optional for approvals. Tap the calendar icon to edit the Valid to date. Tap **OK** followed by the Send icon \(![Send icon.](../../grc-common/image/mobile_instances_send_droid.png)\) or **Submit** to save and submit your changes.

</td></tr><tr><td id="d278434e272">

**Reject**

</td><td>

In the Additional comments field, enter comments. Comments are required for rejections. Tap the Send icon \(![Send icon.](../../grc-common/image/mobile_instances_send_droid.png)\) or **Submit** to save and submit your changes.

</td></tr></tbody>
</table>6.  To approve or reject a policy exception extension request directly from the list of records displayed on the Policy Exceptions screen after you have requested more information, swipe left on a record to open the menu.

    ![Swipe menu on exception extension request.](../image/mobile-policy-ext-except-menu.png)

7.  On the menu for policy extension that is displayed, choose one to continue.

<table id="choicetable_rt2_ldt_xhb"><thead><tr><th align="left" id="d278434e318">

Option

</th><th align="left" id="d278434e321">

Description

</th></tr></thead><tbody><tr><td id="d278434e327">

**Approve the extension**

</td><td>

In the Additional comments field, enter comments. Comments are optional for approvals.In the Requested extension field, tap the calendar icon to edit the date. Tap **OK** followed by the Send icon \(![Send icon.](../../grc-common/image/mobile_instances_send_droid.png)\) or **Submit** to save and submit your changes.

</td></tr><tr><td id="d278434e351">

**Reject the extension**

</td><td>

In the Additional comments field, enter comments. Comments are required for rejections. Tap the Send icon \(![Send icon.](../../grc-common/image/mobile_instances_send_droid.png)\) or **Submit** to save and submit your changes.

</td></tr></tbody>
</table>8.  Alternatively, with the Policy Exceptions screen displayed, tap a record on the list to open it and review more details.

    With the fields on the record displayed, choose one in the following table to continue.

    ![Policy Exception record details.](../image/mobile-exception-record.png)

<table id="choicetable_zfb_gdt_xhb"><thead><tr><th align="left" id="d278434e393">

Option

</th><th align="left" id="d278434e396">

Description

</th></tr></thead><tbody><tr><td id="d278434e402">

**Details tab**

</td><td>

With details tab selected, choose one to continue.-   View the fields for details about the Policy Exception record.

If displayed, tap the **Policy** field to display a list of policies and tap an item to display the Policy record.

Tap the **Control Objective** field to display a list of control objectives. Tap an item on the list to open the record.

-   At the top right of the screen, tap the menu icon \(![Top menu icon.](../../grc-common/image/mobile-top-menu.png)\). Approve or reject the pending policy exception request, or edit it and request more information. Follow the steps described in the preceding table. If the extension request menu is displayed, follow the steps described in the preceding table to approve or reject the extension request.


</td></tr><tr><td id="d278434e437">

**Activity Stream tab**

</td><td>

With the Activity Stream tab selected, choose one to continue.-   View work notes and additional comments. Tap the plus icon ![Plus icon.](../../grc-common/image/mobile_instances_plus.png) to add a work note or attach a file.
-   At the top right of the screen, tap the menu icon \(![Top menu icon.](../../grc-common/image/mobile-top-menu.png)\). Approve or reject the pending policy exception request, or edit and request more information. Follow the steps described in the preceding table. If the extension request menu is displayed, follow the steps described in the preceding table to approve or reject the extension request.


</td></tr><tr><td id="d278434e467">

**Related Lists**

</td><td>

With the Related lists tab selected, follow these steps.

 1.  Tap **Impacted Controls** to view the items on the Impacted Controls related list.
2.  On the list that is displayed, tap an item to open the record and view more details.
 At the top right of the screen, tap the menu icon \(![Top menu icon.](../../grc-common/image/mobile-top-menu.png)\). Approve or reject the pending policy exception request, or edit and request more information. Follow the steps described in the preceding table. If the extension request menu is displayed, follow the steps described in the preceding table to approve or reject the extension request.

</td></tr><tr><td id="d278434e500">

**Screen icons at the bottom of the screen.**

</td><td>

On the bottom of the screen, choose one to continue.-   Tap the Policy and Compliance icon to return the landing screen.
-   If displayed, tap an icon to open another ServiceNow® mobile app.
-   Tap **More**:
    -   Tap **Notification** to view notifications from the ServiceNow AI Platform and the GRC Mobile application.
    -   Tap **Settings** followed by **Logout** to log out of the current instance.


</td></tr></tbody>
</table>
**Parent Topic:**[Managing mobile experience for GRC Policy and Compliance](../concept/mobile-policy_compliance-ovrvw.md)

