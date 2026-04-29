---
title: View, edit, and reassign your response tasks with the Security Incident Response Mobile app
description: View, edit, and reassign response tasks that are assigned to you. Your changes are saved on the Security Incident Response Task of the parent security incident.
locale: en-US
release: australia
product: Security Incident Response
classification: security-incident-response
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 3
breadcrumb: [Mobile Experience for Security Incident Response, Security Incident Response, Enterprise security case management applications, Security Operations]
---

# View, edit, and reassign your response tasks with the Security Incident Response Mobile app

View, edit, and reassign response tasks that are assigned to you. Your changes are saved on the Security Incident Response Task of the parent security incident.

## Before you begin

Role required: sn\_si.analyst

## About this task

From the list of records, reassign an open response task that is assigned to you to another analyst in your group. Alternatively, view the details of the record or add a work note prior to reassignment. Time to complete this task: 5-10 minutes.

## Procedure

1.  If you are not logged in to your ServiceNow AI Platform instance on your mobile device, for more information see [Log in to the Security Incident Response Mobile app](mobile-sir-get-started.md).

2.  With the Security Incidents landing screen displayed, tap **My Response Tasks**.

    If you navigate away from the Security Incident Response Mobile app after you have logged in, tap the Now Agent \(Fulfiller\) app at any time to return to the last screen you had displayed.

    ![My Response Tasks applet highlighted.](../image/mobile_SIR_myrt.jpg)

    The My Response Tasks screen is displayed with a list of the response tasks that are assigned to you.

    ![My Response Tasks list.](../image/mobile-myresptsk-list.jpg)

3.  Refer to [Search for security incidents with the Security Incident Response Mobile app](mobile-sir-search.md) to search for tasks that match specific criteria.

    Alternatively, with the filter icon \(![Filter.](../image/sir-filter-image.png)\) displayed, [Set filters to limit the number of records](mobile-sire-filters.md) on the list. Filtering records on screens in the mobile app works like filtering with a condition builder on the ServiceNow AI Platform.

4.  To reassign a task directly from the list of task records that are assigned to you, swipe left on a record to open the menu.

    ![Swipe action displayed.](../image/mobile_sir_assign_task-crop.jpg)

5.  Tap **Reassign**.

6.  On the Assign Response Task to Another screen that is displayed, tap a field to expand it and select another group or user for the task.

7.  Tap the send icon \(![Send in Android.](../../vulnerability-response/image/mobile_instances_send_droid.png)\) or **Submit** to save your changes and update the response task.

    A message is displayed that confirms the record is updated. The task is assigned to a new user on the parent security incident and your ServiceNow AI Platform instance is updated.

8.  To view the details of an open response task and to see the work notes, with the My Response Tasks screen displayed, tap a record on the list.

9.  With the fields on the response task displayed, choose one in the following table to continue.

    ![My Response Task record.](../image/mobile-sir-my-tasks.jpg)

<table id="choicetable_yfw_cgw_lhb"><thead><tr><th align="left" id="d202215e239">

Option

</th><th align="left" id="d202215e242">

Description

</th></tr></thead><tbody><tr><td id="d202215e248">

**Details tab**

</td><td>

With the Details tab selected, review the fields on the response task. To edit fields or reassign the task, tap the menu icon \(![Menu.](../../vulnerability-response/image/mobile-top-menu.png)\). From the menu that is displayed, choose from the following options.-   Tap **Edit**. With the Edit Response Task screen displayed, tap a field to expand it and choose one or more of the options that is displayed. Alternatively, tap the search icon and enter text.
-   To reassign the task, tap **Assign to Another**.
 After you complete your edits, tap the send icon \(![Send in Android.](../../vulnerability-response/image/mobile_instances_send_droid.png)\) or **Submit** to save your changes and update the record. The Security Incident Response Task on the parent security incident in your ServiceNow AI Platform instance is updated.

</td></tr><tr><td id="d202215e293">

**Activity Stream tab**

</td><td>

With the Activity Stream tab selected, choose one to continue.

 -   View the audit trail created by the Work notes on the task record. To add a work note or attach a file, tap \(![Plus.](../../vulnerability-response/image/mobile_instances_plus.png)\).
-   Tap \(![Menu.](../../vulnerability-response/image/mobile-top-menu.png)\) to edit or reassign the task.


</td></tr><tr><td id="d202215e326">

**Tap a screen icon at the bottom of the screen.**

</td><td>

On the bottom of the screen, choose one to continue.-   If displayed, tap another icon to open another ServiceNow® core application to open it.
-   Tap **Notification** to view notifications for critical security incidents that are assigned to you or to your assignment group.
-   Tap **Settings** and choose one to continue.
    -   View information about the ServiceNow AI Platform instance.
    -   Log out of the current instance. To log out of a ServiceNow AI Platform instance on your device, with the details page displayed, tap **Logout**.


</td></tr></tbody>
</table>
