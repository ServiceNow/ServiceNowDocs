---
title: Create email notifications for translation request due dates
description: As an admin, you can create email notifications triggered by translation request due dates.
locale: en-US
release: zurich
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2025-12-05"
reading_time_minutes: 3
breadcrumb: [Creating email notifications for Localization Workspace, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer]
---

# Create email notifications for translation request due dates

As an admin, you can create email notifications triggered by translation request due dates.

## Before you begin

Create your own notification category to identify and group your notifications related to Localization Workspace translation projects. For instructions see [Create notification categories](../../notification/task/create-notification-categories.md).

Role required: admin

## About this task

From version 2.0.2, your users may set a due date when requesting translations in Localization Workspace. You can reference these due dates to send email notifications.

For more information see [Request translations in Localization Workspace: Estimate and Due Date](lw-estimate.md). For background information about configuring email notifications, see [Create an email notification](../../notification/task/t_CreateANotification.md).

The following procedure is specific to notifications for Localization Workspace translation request due dates. In the example scenario, a notification is sent when a translation request is past due \(the request is still in progress after its due date\).

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Select **New**.

3.  Fill in the fields according to the following guidance.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a unique, descriptive name for these notifications.|
    |**Table**|Select the Localization Project \[sn\_lf\_project\] table from the list of tables.|
    |**Category**|If you have already set up your own category for these notifications, you can select it from the drop-down list. For information see [Create notification categories](../../notification/task/create-notification-categories.md).|

    ![An email notification form with the Table field set to Localization Project. Includes a reminder to preconfigure the notification Category.](../image/lw-email-notif-due-dates-main.png)

4.  On the **When to send** tab, fill in the fields.

<table id="choicetable_fpy_zx4_nhc"><thead><tr><th align="left" id="d234428e191">

Field

</th><th align="left" id="d234428e194">

Description

</th></tr></thead><tbody><tr><td id="d234428e200">

**Send when**

</td><td>

Select `Record inserted or updated`.

</td></tr><tr><td id="d234428e212">

**Updated**

</td><td>

Select this check box.

</td></tr><tr><td id="d234428e221">

**Inserted**

</td><td>

Clear this check box.

</td></tr><tr><td id="d234428e230">

**Conditions**

</td><td>

In the example, two conditions are set:1.  `State is In Progress`
2.  `Due date before Today`


</td></tr></tbody>
</table>    ![The When to send tab of the email notification form. Two example conditions are highlighted.](../image/lw-email-notif-due-dates-when.png)

5.  On the **Who will receive** tab, fill in the fields according to your organizational requirements.

<table id="choicetable_kyt_4th_nhc"><thead><tr><th align="left" id="d234428e268">

Field

</th><th align="left" id="d234428e271">

Description

</th></tr></thead><tbody><tr><td id="d234428e277">

**Users**

</td><td>

Select the lock icon ![](../../../use/using-forms/image/LockIconNE.png) to add an individual user from the User \[sys\_user\] table.

</td></tr><tr><td id="d234428e288">

**Users/Groups in Fields**

</td><td>

Select the lock icon to add recipients from fields in the Localization Project \[sn\_lf\_project\] table.

</td></tr><tr><td id="d234428e297">

**Groups**

</td><td>

Select the lock icon to add a group of users, such as Localization Requestor, from the Group \[sys\_user\_group\] table.

</td></tr><tr><td id="d234428e306">

**Subscribable**

</td><td>

Option to enable all users to subscribe to the notification.**Note:** Recipients can receive email about records that they can’t normally access from the user interface, so consider the sensitivity of the information before selecting this option.

</td></tr></tbody>
</table>6.  On the **What it will contain** tab, fill in the fields according to your organizational requirements.

<table id="choicetable_bxw_f1p_nhc"><thead><tr><th align="left" id="d234428e330">

Field

</th><th align="left" id="d234428e333">

Description

</th></tr></thead><tbody><tr><td id="d234428e339">

**Email template**

</td><td>

You can search for an existing template.

</td></tr><tr><td id="d234428e348">

**Subject**

</td><td>

You can use variables from the Localization Project \[sn\_lf\_project\] table, available under **Select variables**.

</td></tr><tr><td id="d234428e360">

**Message HTML**

</td><td>

You can use variables from the Localization Project \[sn\_lf\_project\] table, available under **Select variables**. Example variables from this table:-   `${short_description}` for Short Description
-   `${due_date}` for due date
-   `${made_sla}` for Made SLA


</td></tr></tbody>
</table>7.  Select **Submit** \(or **Update** if you are editing\) to finish the record.


## What to do next

After creating or updating a notification, review its record in the Notifications \[sysevent\_email\_action\] table. You can select **Preview Notification** to open an example of the email notification. Use this function to confirm how the notification appears to recipients.

![In the top menu bar of the example's notification form, the Preview Notification button is highlighted.](../image/lw-email-notif-due-dates-preview.png)

For more information, see [Preview email notifications](../../notification/task/t_PreviewingNotifications.md).

**Parent Topic:**[Creating email notifications for Localization Workspace](../concept/lw-email-notifications.md)

