---
title: View, edit, and reassign security incidents assigned to you with the Security Incident Response Mobile app
description: As a security incident analyst, view, edit, and reassign Security Incident Response \(SIR\) incidents that are assigned to you. View related lists and the audit trail of work notes for more details about incidents.
locale: en-US
release: zurich
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 4
breadcrumb: [Mobile Experience for Security Incident Response, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View, edit, and reassign security incidents assigned to you with the Security Incident Response Mobile app

As a security incident analyst, view, edit, and reassign Security Incident Response \(SIR\) incidents that are assigned to you. View related lists and the audit trail of work notes for more details about incidents.

## Before you begin

Role required: sn\_si.analyst

## About this task

Reassign an open security incident to another analyst in your group from the list of records. Alternatively, view the details and related lists of the record or add a work note prior to assignment. Time to complete this task: 5-10 minutes.

## Procedure

1.  If you are not logged in to your ServiceNow AI Platform instance on your mobile device, see [Log in to the Security Incident Response Mobile app](mobile-sir-get-started.md).

2.  With the Security Incidents landing screen displayed, tap **My Incidents**.

    If you navigate away from the Security Incident Response Mobile app after you have logged in, tap the Now Agent app at any time to return to the last screen you had displayed.

    ![My Incidents applet highlighted.](../image/mobile_SIR_applet_callout_mysi.jpg)

    The My Incidents screen is displayed with a list of open security incident records that are assigned to you.

    ![List of security incidents assigned to you.](../image/mobile-sir-my-si-list.jpg)

3.  Refer to [Search for security incidents with the Security Incident Response Mobile app](mobile-sir-search.md) to search for security incidents that match specific criteria.

    Alternatively, with the filter icon \(![Filter.](../image/sir-filter-image.png)\) displayed, [Set filters to limit the number of records](mobile-sire-filters.md) on the list. Filtering records on screens in the mobile app works like filtering with a condition builder on the ServiceNow AI Platform.

4.  To reassign an incident directly from the list, with the list of open security incident records displayed, swipe left on a record to open the menu.

    ![My Incidents list swipe menu.](../image/mobile-sir-my-si-swipe.jpg)

5.  Edit the Assignment group or the Assigned to fields from the menu that is displayed.

<table id="choicetable_er2_4pf_thb"><thead><tr><th align="left" id="d464308e186">

Option

</th><th align="left" id="d464308e189">

Description

</th></tr></thead><tbody><tr><td id="d464308e195">

**Reassign**

</td><td>

To reassign the assignment group:1.  Tap **Assignment group**.
2.  Tap a group from the list that is displayed, or enter text in the search field. The group must be a security-related assignment group.
 To assign or reassign the security incident to a member of the assignment group:

 1.  Tap **Assigned to**.
2.  Tap a name from the list that is displayed, or enter text in the search field.
 Tap the send icon \(![Send in Android.](../../vulnerability-response/image/mobile_instances_send_droid.png)\) or **Submit** to save and submit your changes.

</td></tr></tbody>
</table>6.  Alternatively, to view the details of the open security incident record, with the My Incidents screen displayed, tap a record on the list.

7.  On the open record that is displayed, choose one option from the following table to continue.

    ![My incidents open record with tabs highlighted.](../image/mobile-sir-my-si-record.jpg)

<table id="choicetable_yfw_cgw_lhb"><thead><tr><th align="left" id="d464308e271">

Option

</th><th align="left" id="d464308e274">

Description

</th></tr></thead><tbody><tr><td id="d464308e280">

**Tap the menu icon \(![Menu.](../../vulnerability-response/image/mobile-top-menu.png)\) on the upper right of the screen.**

</td><td>

From the menu that is displayed, choose from the following options.-   Tap **Edit**. With the Edit Security Incident screen displayed, tap a field to expand it and choose one or more of the options that are displayed. Alternatively, tap the search icon and enter text.
-   To reassign the incident, tap **Reassign**. Follow the instructions described in the previous table.
 After you complete your edits, tap the send icon \(![Send in Android.](../../vulnerability-response/image/mobile_instances_send_droid.png)\) or **Submit** to save your changes and update the security incident.

</td></tr><tr><td id="d464308e322">

**Activity Stream tab**

</td><td>

With the Activity Stream tab selected, review the audit trail of work notes, activities, and additional comments of the record. Tap the plus icon \(![Plus.](../../vulnerability-response/image/mobile_instances_plus.png)\) to add a work note or attach a file.

</td></tr><tr><td id="d464308e340">

**Related List tab**

</td><td>

With the Related List tab selected, view the items on any Related Lists that are populated on the security incident.

 Tap an item on the list that is displayed to view the details for a related list. From the lists of items that are displayed, tap an item to continue to view the activity streams and related lists associated with the parent security incident.

</td></tr><tr><td id="d464308e355">

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
