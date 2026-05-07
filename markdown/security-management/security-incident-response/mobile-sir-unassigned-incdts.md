---
title: View, edit and assign unassigned security incidents with the Security Incident Response Mobile app
description: From your mobile device, view, edit, and assign unassigned Security Incident Response \(SIR\) incidents. View related lists and the audit trail of work notes for more details about incidents.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 4
breadcrumb: [Mobile Experience for Security Incident Response, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View, edit and assign unassigned security incidents with the Security Incident Response Mobile app

From your mobile device, view, edit, and assign unassigned Security Incident Response \(SIR\) incidents. View related lists and the audit trail of work notes for more details about incidents.

## Before you begin

Role required: sn\_si.analyst

## About this task

From the list of records, assign an open, unassigned security incident to yourself or to another analyst in your group. Alternatively, view the details and related lists of the record or add a work note prior to assignment. Time to complete this task: 5-10 minutes.

## Procedure

1.  If you are not logged in to your ServiceNow AI Platform instance on your mobile device, for more information see [Log in to the Security Incident Response Mobile app](mobile-sir-get-started.md).

2.  With the Security Incidents landing screen displayed, tap **Unassigned Incidents**.

    If you navigate away from the Security Incident Response Mobile app after you have logged in, tap the Now Agent app at any time to return to the last screen you had displayed.

    ![Unassigned incidents applet highlighted.](../image/mobile_SIR_applet_callout_unassgnsi.jpg)

    The Unassigned Incidents screen is displayed with a list of unassigned security incident records.

    ![Unassigned security incidents list.](../image/mobile_SIR_unassgnsi-list.jpg)

3.  Refer to [Search for security incidents with the Security Incident Response Mobile app](mobile-sir-search.md) to search for security incidents that match specific criteria.

    Alternatively, with the filter icon \(![Filter icon.](../image/sir-filter-image.png)\) displayed, [Set filters to limit the number of records](mobile-sire-filters.md) on the list. Filtering records on screens in the mobile app works like filtering with a condition builder on the ServiceNow AI Platform.

4.  To assign or reassign an open security incident record directly from the list, with the list of open unassigned security incident records displayed, swipe left on a record to open the menu.

    ![Swipe action on unassigned security incident record.](../image/mobile-sir-unassgnsi-swipe.jpg)

5.  Choose one from the menu to continue.

<table id="choicetable_er2_4pf_thb"><thead><tr><th align="left" id="d223738e190">

Option

</th><th align="left" id="d223738e193">

Description

</th></tr></thead><tbody><tr><td id="d223738e199">

**Assign to Me**

</td><td>

Assign the security incident to yourself. If the security incident is already assigned to you, this option is not displayed.

</td></tr><tr><td id="d223738e208">

**Reassign**

</td><td>

To assign or reassign the assignment group:1.  Tap **Assignment group**.
2.  Tap a group from the list that is displayed, or enter text in the search field. The group must be a security-related assignment group.
 To assign or reassign the security incident to a member of the assignment group:

 1.  Tap **Assigned to**.
2.  Tap a name from the list that is displayed, or enter text in the search field.
 Tap the send icon \(![Send icon in Android.](../../vulnerability-response/image/mobile_instances_send_droid.png)\) or **Submit** to save and submit your changes.

</td></tr></tbody>
</table>6.  Alternatively, with the Unassigned Incidents screen displayed, tap a record on the list.

7.  On the open record that is displayed, choose one option from the following table to continue.

    ![Unassigned security incident with tabs highlighted.](../image/mobile-sir-unassgn-record.jpg)

<table id="choicetable_yfw_cgw_lhb"><thead><tr><th align="left" id="d223738e284">

Option

</th><th align="left" id="d223738e287">

Description

</th></tr></thead><tbody><tr><td id="d223738e293">

**Tap the menu icon \(![Menu icon.](../../vulnerability-response/image/mobile-top-menu.png)\) on the upper right of the screen.**

</td><td>

From the menu that is displayed, choose from the following options.-   Tap **Edit**. With the Edit Security Incident screen displayed, tap a field to expand it and choose one or more of the options that are displayed. Alternatively, tap the search icon and enter text.
-   To assign or reassign the incident, tap **Reassign** or **Assign to Me**. Follow the instructions described in the previous table.
 After you complete your edits, tap the send icon \(![Send icon in Android.](../../vulnerability-response/image/mobile_instances_send_droid.png)\) or **Submit** to save your changes and update the security incident.

</td></tr><tr><td id="d223738e338">

**Activity Stream tab**

</td><td>

With the Activity Stream tab selected, review the audit trail of work notes, activities, and additional comments of the record. Tap the plus icon \(![Plus icon.](../../vulnerability-response/image/mobile_instances_plus.png)\) to add a work note or attach a file.

</td></tr><tr><td id="d223738e356">

**Related List tab**

</td><td>

With the Related List tab selected, view the items on any of the Related Lists that are populated on the security incident.

 Tap an item on the list that is displayed to view the details for a related list. From the lists of items that are displayed, tap an item to continue to view the activity streams and related lists associated with the parent security incident.

</td></tr><tr><td id="d223738e371">

**Screen icons at the bottom of the screen.**

</td><td>

On the bottom of the screen, choose one to continue.-   Tap the Security Incidents icon to return to the landing screen.
-   If displayed, tap an icon to open another ServiceNow® mobile app.
-   Tap **Notification** to view notifications from the ServiceNow AI Platform and the Security Incident Response Mobile app.
-   Tap **Settings** and choose one to continue.
    -   View information about the ServiceNow AI Platform instance on your device.
    -   Log out of the current ServiceNow AI Platform instance.


</td></tr></tbody>
</table>
