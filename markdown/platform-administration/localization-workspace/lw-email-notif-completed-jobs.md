---
title: Create email notifications for completed translation jobs
description: Configure email notifications so you can be informed when Localization Workspace translation jobs are completed.
locale: en-US
release: australia
product: Localization Workspace
classification: localization-workspace
topic_type: task
last_updated: "2026-03-12"
reading_time_minutes: 2
breadcrumb: [Creating email notifications for Localization Workspace, Configuring Localization Workspace, Localization Workspace, Translation and localization, Configure core features, Administer the ServiceNow AI Platform]
---

# Create email notifications for completed translation jobs

Configure email notifications so you can be informed when Localization Workspace translation jobs are completed.

## Before you begin

Create your own notification category to identify and group your notifications related to Localization Workspace translation projects. For instructions see [Create notification categories](../../notification/task/create-notification-categories.md).

Role required: admin.

## About this task

From Zurich Patch 1, along with tracking the progress of translation jobs in Localization Workspace, you can set up email notifications to be alerted upon completion of translation jobs.

For detailed information about configuring email notifications, see [Create an email notification](../../notification/task/t_CreateANotification.md). The following procedure is specific to notifications for Localization Workspace jobs.

## Procedure

1.  Navigate to **All** &gt; **System Notification** &gt; **Email** &gt; **Notifications**.

2.  Select **New**.

3.  Fill in the fields according to the following guidance.

    |Field|Description|
    |-----|-----------|
    |**Name**|Enter a unique, descriptive name for these notifications.|
    |**Table**|Select the Translation Request \[sn\_lw\_trans\_request\] table from the list of tables.|
    |**Category**|If you have already set up your own category for these notifications, you can select it from the drop-down list. For information see [Create notification categories](../../notification/task/create-notification-categories.md).|

4.  On the **When to send** tab, fill in the fields.

    |Field|Description|
    |-----|-----------|
    |**Send when**|Select `Record inserted or updated`.|
    |**Updated**|Select this check box.|
    |**Inserted**|Clear this check box.|
    |**Conditions**|Set one row to `State is Complete`.|

5.  On the **Who will receive** tab, fill in the fields according to your organizational requirements.

<table id="choicetable_xvd_hzb_lgc"><thead><tr><th align="left" id="d59631e245">

Field

</th><th align="left" id="d59631e248">

Description

</th></tr></thead><tbody><tr><td id="d59631e254">

**Users**

</td><td>

Select the lock icon ![](../../../use/using-forms/image/LockIconNE.png) to add an individual user from the User \[sys\_user\] table.

</td></tr><tr><td id="d59631e265">

**Users/Groups in Fields**

</td><td>

Select the lock icon to add recipients from fields in the Translation Request \[sn\_lw\_trans\_request\] table.

</td></tr><tr><td id="d59631e274">

**Groups**

</td><td>

Select the lock icon to add a group of users, such as Localization Requestor, from the Group \[sys\_user\_group\] table.

</td></tr><tr><td id="d59631e283">

**Subscribable**

</td><td>

Option to enable all users to subscribe to the notification.**Note:** Recipients can receive email about records that they can’t normally access from the user interface, so consider the sensitivity of the information before selecting this option.

</td></tr></tbody>
</table>    ![The Who will receive tab on a new email notification for Localization Workspace's Translation Request table.](../image/lw-email-notif-completed-jobs-who.png)

6.  On the **What it will contain** tab, fill in the fields according to your organizational requirements.

<table id="choicetable_l2h_f1c_lgc"><thead><tr><th align="left" id="d59631e317">

Field

</th><th align="left" id="d59631e320">

Description

</th></tr></thead><tbody><tr><td id="d59631e326">

**Email template**

</td><td>

You can search for an existing template.

</td></tr><tr><td id="d59631e335">

**Subject**

</td><td>

You can use variables from the Translation Request \[sn\_lw\_trans\_request\] table, available under **Select variables**.

</td></tr><tr><td id="d59631e347">

**Message HTML**

</td><td>

You can use variables from the Translation Request \[sn\_lw\_trans\_request\] table, available under **Select variables**. Example variables from this table:-   `${lf_project.number}` is the corresponding number from Localization Framework.
-   `${sys_created_by}` is the person who submitted the translation request.


</td></tr></tbody>
</table>7.  Select **Submit** \(or **Update** if you are editing\) to finish the record.


## What to do next

After creating a new notification, you can review its record in the Notifications \[sysevent\_email\_action\] table. From that finished record you can select **Preview Notification** to open an example of the email notification. Use this function to confirm how the notification appears to recipients.

![The Preview Notification button is highlighted on a submitted email notification record.](../image/lw-email-notif-completed-jobs-preview.png)

For more information, see [Preview email notifications](../../notification/task/t_PreviewingNotifications.md).

**Parent Topic:**[Creating email notifications for Localization Workspace](../concept/lw-email-notifications.md)

