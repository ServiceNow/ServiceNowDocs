---
title: Assign Policy and Compliance Management issues with the GRC Mobile application
description: Assign unassigned Policy and Compliance Management issues to a member of your assignment group. Navigate through the record to view more details about the Control Objective, the Control record, and Remediation Tasks associated with an issue.
locale: en-US
release: australia
product: Policy and Compliance Management
classification: policy-and-compliance-management
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Managing mobile experience for GRC Policy and Compliance, Policy and Compliance Management, Governance, Risk, and Compliance]
---

# Assign Policy and Compliance Management issues with the GRC Mobile application

Assign unassigned Policy and Compliance Management issues to a member of your assignment group. Navigate through the record to view more details about the Control Objective, the Control record, and Remediation Tasks associated with an issue.

## Before you begin

Role required: GRC Compliance manager \(sn\_compliance.manager\)

## About this task

Time to complete this task: 5-10 minutes.

## Procedure

1.  If you are not logged in to your ServiceNow AI Platform instance on your mobile device, for more information see [Log in to the GRC Mobile application](mobile-login-P-C-app.md).

2.  With the Policy and Compliance landing screen displayed, under the section titled, `Team's Unassigned Work`, tap **Issues**.

    If you navigate away from the GRC Mobile application after you have logged in, tap the Now Agent app at any time to return to the last screen you had displayed.

    ![Issues applet highlighted.](../image/mobile_Policy_and_Compliance_overview-app_rd.png)

    The Issues screen is displayed with a list of records.

3.  If you want to reduce the number of records that are displayed on the screen, see [Filter records with the GRC Mobile application](mobile-pc-set-filters.md) to search for records that match specific search criteria.

    Filtering records on screens in the mobile app works like filtering with a condition builder on the ServiceNow AI Platform. Setting filters can reduce the number of records that are displayed on screens.

4.  To edit or assign an issue directly from the list of records displayed on the Issues screen, swipe left on a record to open the menu.

    ![Issue swipe menu.](../image/mobile-issue-swipe.png)

5.  In the menu that is displayed, choose one to continue.

    |Option|Description|
    |------|-----------|
    |**Edit**|In the Extend by days field on the Edit Issue screen that is displayed, enter a value. This value is added to the Duration field in your ServiceNow AI Platform instance. Tap the Send icon \(![Send icon.](../../grc-common/image/mobile_instances_send_droid.png)\) or **Submit** to save and submit your changes.|
    |**Assign**|On the Issue Assignment screen that is displayed, tap the **Assignment Group** and **Assigned to** fields to assign the issue.|

6.  Alternatively, with the Issues screen displayed, tap a record on the list to open it and view more details.

    With the fields on the issue record displayed, choose one in the following table to continue.

    ![Issue record.](../image/mobile-issue-record.jpg)

<table id="choicetable_sgf_5fd_xhb"><thead><tr><th align="left" id="d145905e236">

Option

</th><th align="left" id="d145905e239">

Description

</th></tr></thead><tbody><tr><td id="d145905e245">

**Details tab**

</td><td>

With the Details tab selected, choose one to continue.

 -   View the fields for details about the issue, especially the planned start and end dates.

Tap the **Control Objective/Risk Statement** field to expand it. A list of records is displayed. Tap an item to display a control objective record.

Tap the **Control/Risk** field to expand it. A list of records is displayed. Tap an item on the list to open the record. With the record displayed, select the **Details** or **Activity Stream** tabs for more information.

-   At the top right of the screen with the Issue screen displayed, tap the menu icon \( ![Menu icon.](../../grc-common/image/mobile-top-menu.png)\) to edit and assign the issue. Follow the steps described in the preceding table.


</td></tr><tr><td id="d145905e289">

**Activity Stream tab**

</td><td>

Choose one to continue.-   View work notes and additional comments. Tap the plus icon \(![Plus icon.](../../grc-common/image/mobile_instances_plus.png)\) to add a work note or attach a file.
-   At the top right of the screen, tap the menu icon \( ![Menu icon.](../../grc-common/image/mobile-top-menu.png)\) to edit and assign the issue. Follow the steps described in the preceding table.


</td></tr><tr><td id="d145905e319">

**Related List tab**

</td><td>

View the related lists.

 1.  Tap **Remediation Tasks** to expand the field. On the Remediation Task screen, view the items on the Remediation Tasks related list that are associated with the Issue record.
2.  On the list that is displayed, tap an item to open the record and view more details about the task.
3.  After your review, navigate back to the issue record and tap the menu \( ![Menu icon.](../../grc-common/image/mobile-top-menu.png)\) to edit and assign the issue. Follow the steps described in the preceding table.


</td></tr><tr><td id="d145905e352">

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

