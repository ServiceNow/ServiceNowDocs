---
title: Set up table notifications for task tables
description: You can set up a table notification for a task table to enable automatic Live Feed messages.
locale: en-US
release: zurich
product: Live Feed
classification: live-feed
topic_type: task
last_updated: "2025-07-31"
reading_time_minutes: 3
breadcrumb: [Live Feed table notifications, Administering Live Feed, Live Feed Core UI, Manage people and work capabilities, Extend ServiceNow AI Platform capabilities]
---

# Set up table notifications for task tables

You can set up a table notification for a task table to enable automatic Live Feed messages.

## Before you begin

Role required: live\_feed\_admin or chat\_admin

## Procedure

1.  Navigate to **Live Feed** &gt; **Feed Administration** &gt; **Table Notifications**.

2.  Click **New** or select a notification to open it.

3.  Complete the form.

<table id="table_xjv_sl1_fr"><thead><tr><th>

Field

</th><th>

Description

</th></tr></thead><tbody><tr><td>

Table

</td><td>

Select the table for which notifications are generated.

 **Note:** The list shows only tables and database views that are in the same scope as the table notification.

</td></tr><tr><td>

Post to chat rooms

</td><td>

Select the check box to generate the notification in chat rooms that are associated with the record, This applies to task records only and requires that the Chat plugin is active.

</td></tr><tr><td>

Post to Live Feed

</td><td>

Select the check box to generate the notification on Live Feed. If record feeds are not set up and the **Feed group** field is blank, the notification is posted to the company feed.

</td></tr><tr><td>

Record Feeds

</td><td>

Select the fields to post for record feeds.This field is available only if **Post to live feed** is selected.

</td></tr><tr><td>

Application

</td><td>

Select the application that contains this record.

</td></tr><tr><td>

Active

</td><td>

Select the check box to enable the notification.

</td></tr><tr><td>

Insert

</td><td>

Select the check box to generate the notification when a record is inserted into the database.

</td></tr><tr><td>

Update

</td><td>

Select the check box to generate the notification when a record is updated.

</td></tr><tr><td>

Feed

</td><td>

Select the Live Feed team to which you want to post messages. This field is available only if **Post to Live Feed** is selected. Clear the field to post notifications on the company feed.

</td></tr><tr><td>

Conditions

</td><td>

Create the condition that must be met to generate the notification. If you add a condition statement, the system evaluates the condition first and parses the **Before script** field only if the condition is met. You may choose to leave this field blank and include conditions in the script.

</td></tr><tr><td>

Description

</td><td>

Enter a description of the table notification.

</td></tr><tr><td>

Message

</td><td>

Construct the automatic message you want to generate. You can include field values as variables and a link to the record. To add a variable, position the cursor in the text and then click the field name in the **Select variables** field. To add a link to the record, enter `${URI}` in the message text as shown in the following example.

 ```
High priority incident opened: ${URI}
 Short description: ${short_description}
```

 **Note:** For security reasons, any HTML code is automatically stripped out of a message before it is posted.

</td></tr><tr><td>

Before script

</td><td>

Create a script that runs before a notification is generated. The script runs only if the condition evaluates to true or is empty. The following variables are available in the script.-   *current*: the GlideRecord object that triggered the notification.
-   *changedFields*: an ArrayList of fields changed on submit. Use changedFields.contains\('fieldname'\) to check for change.
-   *answer*: set answer to false to cancel the notification.
-   *profileSource*: set to a valid GlideRecord object to define the profile that is posting the message.
-   *profileID*: set to a live\_profile sys\_id to define the profile that is posting the message; by default it is the current record. Overrides profileSource if both are specified.
 Any custom variable created in the script is also exposed to the message in the form of *$\{myVariableName\}*.

</td></tr></tbody>
</table>4.  Click **Submit** or **Update**.


**Parent Topic:**[Live Feed table notifications](../concept/c_SetUpLiveFeedTableNotifications.md)

**Related topics**  


[Set up table notifications for non-task tables](t_SetUpTableNotifNonTaskTables.md)

[Live Feed table notification examples](../concept/c_LFTableNotifiExamples.md)

